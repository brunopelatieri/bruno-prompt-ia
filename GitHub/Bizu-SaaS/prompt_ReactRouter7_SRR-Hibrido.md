# Prompt para Cursor (Sonnet 4.6) — Migração para React Router v7 Framework Mode (SSR Híbrido)

---

## CONTEXTO DO PROJETO

Este é um boilerplate full-stack com a seguinte stack e arquitetura atual:

**Stack:**
- Vite + React + TypeScript + React Router v7 (atualmente em modo SPA/Data Mode, SEM SSR)
- shadcn/ui + Tailwind v4 + tw-animate-css
- Hono API + Drizzle ORM + postgres.js
- Supabase Auth + Storage
- Deploy planejado: VPS com Docker + Portainer

**Arquitetura atual (antes da migração):**
```
Browser (porta 5173 — Vite)
  │
  ├── /            React Router — páginas React (SPA, client-side only)
  ├── /dashboard   React Router — área autenticada (SPA)
  │
  └── /api/* ──→ proxy Vite ──→ Hono (porta 3001)
                                  │
                                  ├── GET  /api/health
                                  └── POST /api/contact ──→ Drizzle ──→ Postgres
```

- `vite.config.ts` tem proxy reverso: requests para `/api/*` são encaminhadas para `http://localhost:3001`.
- `server/main.ts` inicia o Hono via `@hono/node-server` na porta 3001.
- `server/index.ts` é o app Hono, com CORS configurado para aceitar apenas `localhost:5173`.
- `server/routes/contact.ts` contém a única rota de domínio até agora.
- `getDb()` está isolado no server — a conexão Drizzle não vaza para o frontend.

---

## OBJETIVO DA MIGRAÇÃO

Migrar o projeto para o **React Router v7 Framework Mode** (que incorpora as capacidades do antigo Remix), habilitando **SSR (Server-Side Rendering) apenas nas rotas públicas** (landing page e blog), enquanto a **área autenticada (`/dashboard` e demais rotas logadas) permanece como SPA client-side**, exatamente como está hoje.

### Por que isso é necessário
- O blog precisa de SEO funcional e de Open Graph correto (preview de link no WhatsApp, LinkedIn, Twitter/X), o que não funciona de forma confiável em SPA puro, pois esses crawlers não executam JavaScript.
- A área autenticada NÃO precisa de SSR — não há benefício de SEO em páginas logadas, e queremos manter a simplicidade de SPA ali.

### O que NÃO deve mudar
- A API Hono continua sendo a fonte de verdade para toda lógica de negócio, queries ao Postgres via Drizzle, e autenticação.
- A área autenticada (`/dashboard/**`) deve continuar funcionando como SPA client-side, SEM SSR — não renderize essas rotas no servidor.
- Drizzle, Supabase Auth/Storage, shadcn/ui, Tailwind config — nada disso deve ser alterado em sua configuração interna, apenas integrado ao novo modelo de build/serve.
- Não introduza Next.js. A migração é para o **Framework Mode nativo do React Router v7**, mantendo Vite como build tool por baixo dos panos.

---

## ESCOPO TÉCNICO DA TAREFA

### 1. Habilitar React Router v7 Framework Mode
- Instalar/configurar o que for necessário para sair do "Library Mode" (RR7 usado só como roteador em SPA) para o **Framework Mode** (com `@react-router/dev`, `react-router.config.ts`, suporte a `loader`/`action`/SSR nativo).
- Ajustar `vite.config.ts` para usar o plugin oficial do React Router v7 framework mode.

### 2. Configurar SSR seletivo por rota
- Rotas públicas com SSR habilitado:
  - `/` (landing page)
  - `/blog` (lista de posts)
  - `/blog/:slug` (post individual)
- Rotas da área autenticada SEM SSR (continuam client-side):
  - `/dashboard/**` e qualquer rota sob o grupo autenticado
- Pesquise e aplique a forma correta e atualizada do React Router v7 para fazer essa configuração por rota (pode ser via `ssr: true/false` no config de rota, route modules, ou outro mecanismo oficial da versão mais recente — não assuma, confirme na documentação atual antes de implementar).

### 3. Integração com o servidor Hono
- O objetivo final é ter **um único processo Node servindo tudo** em produção (mais simples para o deploy em VPS com Docker), com esta divisão lógica:
  - Hono continua respondendo `/api/*` (toda lógica de negócio, Drizzle, Supabase).
  - O servidor SSR do React Router responde as demais rotas (`/`, `/blog/*`, `/dashboard/*` — sendo que `/dashboard/*` apenas entrega o shell SPA, sem fazer SSR de fato).
- Pesquise a forma recomendada de montar o handler de SSR do React Router v7 **dentro de uma app Hono** (ou rodando lado a lado no mesmo processo, conforme a documentação oficial mais recente recomendar). Não invente uma solução — busque a abordagem documentada e estável para esta versão.
- Preserve a configuração de CORS existente, mas revise se ainda é necessária após a unificação dos servidores (se Hono e o frontend passarem a ser servidos pelo mesmo processo/origem, parte do CORS pode deixar de ser necessária — avalie e ajuste).

### 4. Build e Deploy (Docker + VPS)
- Ajustar os scripts de build (`package.json`) para gerar corretamente:
  - O bundle client (JS/CSS para hidratação no browser).
  - O bundle server (para SSR).
- Ajustar/criar o `Dockerfile` para refletir o novo processo de build e start, considerando que o destino é uma VPS com Docker + Portainer (não Vercel — não use otimizações específicas de Vercel).
- Garantir que o `docker-compose.yml` (se existir) ou as variáveis de ambiente continuem compatíveis com a nova estrutura de servidor único.

### 5. Meta tags e SEO
- Implementar a definição de `<title>`, `<meta description>`, e tags Open Graph (`og:title`, `og:description`, `og:image`) via o mecanismo nativo do React Router v7 (`meta` function nas route modules), e não mais via `react-helmet-async` — já que com SSR real, o framework já resolve isso nativamente e de forma mais robusta.
- Aplicar isso nas rotas: `/`, `/blog`, `/blog/:slug` (meta dinâmica por post, vinda dos dados carregados no `loader`).

### 6. Loaders para o Blog
- A listagem do blog (`/blog`) e o post individual (`/blog/:slug`) devem buscar os dados via `loader` do React Router v7, chamando diretamente a lógica de acesso ao Postgres via Drizzle (reaproveitando o schema e client Drizzle já existentes no `server/`), SEM passar por uma chamada HTTP para a API Hono nesse caso específico — já que o loader roda no mesmo servidor Node, podemos acessar o banco diretamente, evitando uma volta de rede desnecessária.
  - Se isso não for possível ou recomendado pela arquitetura final escolhida (por exemplo, se Hono e RR7 SSR ficarem em processos realmente separados), use a API Hono mesmo a partir do loader, mas deixe isso explícito e justificado no código.

---

## RESTRIÇÕES E BOAS PRÁTICAS

1. **Não quebre a área autenticada.** Antes de migrar, identifique todas as rotas sob `/dashboard` (ou equivalente) e garanta que elas continuem sendo client-side only depois da migração — sem loaders rodando SSR nelas, sem hidratação de dados sensíveis no HTML inicial.
2. **Não duplique lógica de autenticação.** Se houver necessidade de verificar sessão do Supabase Auth dentro de um loader SSR (por exemplo, se uma rota pública precisar saber se o usuário está logado para mudar algum CTA), implemente isso de forma explícita e comente o porquê.
3. **Mantenha TypeScript estrito.** Tipagem de loaders, actions e meta functions deve seguir os tipos gerados pelo React Router v7 (`Route.LoaderArgs`, `Route.MetaArgs`, etc., conforme a versão atual exigir).
4. **Não assuma sintaxe de versões antigas do Remix.** O React Router v7 mudou nomenclaturas e arquivos de configuração em relação ao Remix clássico — pesquise a documentação oficial atual antes de gerar qualquer arquivo de configuração (`react-router.config.ts`, estrutura de `routes.ts`, etc.).
5. **Documente as decisões.** Ao final da migração, gere um arquivo `MIGRATION_NOTES.md` explicando: o que mudou, por quê, quais arquivos foram criados/removidos, e quais passos manuais (se algum) o desenvolvedor precisa fazer (ex: variáveis de ambiente novas, comandos de build diferentes).

---

## ORDEM DE EXECUÇÃO SUGERIDA

1. Pesquisar a documentação oficial mais recente do React Router v7 sobre Framework Mode, SSR seletivo por rota, e integração com servidores customizados (Hono).
2. Propor o plano de migração resumido ANTES de tocar em qualquer arquivo, listando exatamente quais arquivos serão criados, modificados ou removidos.
3. Aguardar confirmação.
4. Executar a migração incrementalmente, validando que cada rota pública ganhou SSR e que a área autenticada continua intacta como SPA.
5. Ajustar Dockerfile/build scripts.
6. Gerar `MIGRATION_NOTES.md`.

---

## IMPORTANTE
Antes de implementar, **pesquise a documentação oficial atualizada do React Router v7** (não confie apenas em conhecimento prévio/treinamento, pois esta API mudou rapidamente entre versões). Se encontrar ambiguidade entre abordagens possíveis, pare e pergunte antes de prosseguir, em vez de assumir.