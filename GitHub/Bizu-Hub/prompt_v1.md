## 👽 :21/06/2026

# Icon

<context>
  Você está operando sob as regras de governança e automação do Bizu Hub Bruno Goulart.
  LEIA OBRIGATORIAMENTE antes de começar: @AI_CONTEXT.md, @CLAUDE.md e @PROJECT_TECHNICAL_SPEC.md.
  Você tem total visibilidade do projeto através do Agent Mode / Composer 2.5.
</context>

<task>
  Sua tarefa é auditar e corrigir todos os links de redes sociais e contatos no frontend público que estejam sem ícones representantes ou com ícones quebrados/incorretos.

  Faça uma varredura minuciosa nos componentes de interface (especificamente Footer/Rodapé, Navbar/Sidebar, Página Sobre e Página de Contato) e garanta que CADA LINK possua um ícone visual correspondente e elegante importado do 'lucide-react'.

  MAPEAMENTO ESTRETO DE ÍCONES POR PLATAFORMA:
  - YouTube (https://www.youtube.com/@devgalactico) -> Use o ícone 'Youtube'
  - TikTok (https://www.tiktok.com/@brunopelatieri) -> Use um SVG nativo polido ou o ícone correspondente (caso o Lucide não tenha uma alternativa limpa, monte um SVG do TikTok com as classes do Tailwind v4)
  - GitHub -> Use o ícone 'Github'
  - GitLab -> Use um SVG nativo do GitLab ou ícone correspondente
  - Docker Hub -> Use um SVG nativo do Docker ou ícone correspondente
  - LinkedIn -> Use o ícone 'Linkedin'
  - X (Twitter) -> Use o ícone 'Twitter' ou um SVG moderno do 'X'
  - Instagram -> Use o ícone 'Instagram'
  - Facebook -> Use o ícone 'Facebook'
  - WhatsApp -> Use o ícone 'MessageCircle' ou o 'Phone' (ou um SVG nativo do WhatsApp bem estilizado)
  - E-mail -> Use o ícone 'Mail'
  - Localização -> Use o ícone 'MapPin'

  DIRETRIZES DE AJUSTE:
  1. Identifique strings de texto de links que ficaram "soltas" e envolva-as ou substitua-as pelo layout padrão de ícone + texto (ou apenas o ícone com a propriedade 'aria-label' correta para acessibilidade, caso seja um grid de rodapé).
  2. Alinhe visualmente os ícones usando flexbox ('flex items-center gap-2') para garantir que fiquem perfeitamente centralizados e proporcionais ao tamanho do texto ao redor.
  3. Aplique estados de hover suaves ('transition-colors duration-200 hover:text-primary') nos ícones de link para manter a experiência premium e tecnológica da plataforma.

  Certifique-se de que nenhum import quebre e que a aplicação continue compilando perfeitamente com o SSR do React Router v7.
</task>


---

# Form page Login - Sing In

<context>
  Você está operando sob as regras de governança e automação do Bizu Hub Bruno Goulart.
  LEIA OBRIGATORIAMENTE antes de começar: @AI_CONTEXT.md, @CLAUDE.md e @PROJECT_TECHNICAL_SPEC.md.
  Você tem acesso visual às imagens image_1458e2.png e {873BFF05-8A68-4790-AE74-D0E14D09B35D}.png para entender o estado atual quebrado da interface de login.
</context>

<task>
  Refatore completamente o layout e os formulários da página de login/cadastro (atualmente exibindo um comportamento de grid lateral espremido e incorreto). Transforme-a em uma interface ultra-moderna de alta tecnologia (Engineering AI Design).

  Siga rigorosamente as diretrizes abaixo:

  1. INSTALAÇÃO DE DEPENDÊNCIAS SE NECESSÁRIO:
     - Garanta que o componente Tabs do shadcn/ui esteja disponível (se necessário, execute 'npx shadcn@latest add tabs' ou implemente-o usando a sintaxe nativa compatível com nosso Tailwind v4).
     - Para os ícones, utilize o pacote nativo 'lucide-react' já configurado no projeto para manter a consistência e leveza da stack.

  2. RECONSTRUÇÃO DO DESIGN E ESTRUTURA VISUAL:
     - Elimine o layout de divisão em duas colunas verticais exibido em image_1458e2.png.
     - Crie um card central únicoizado, fluido e responsivo (max-w-md ou max-w-lg) com background premium translúcido (ex: glassmorphism suave usando backdrop-blur, bordas sutis com opacidade baixa e um leve efeito de glow linear/gradiente característico de interfaces de IA).
     - Centralize o título "Bizu" e o subtítulo acima do card de forma limpa.

  3. ABAS ELEGANTES (TABS HORIZONTAIS):
     - Posicione o componente de Tabs na parte SUPERIOR interna do card, ocupando 100% da largura útil disponível (w-full).
     - Use duas abas de acionamento horizontal: "Entrar" (Login) e "Criar Conta" (Cadastro).
     - Dê um acabamento moderno com animações suaves de transição via Tailwind v4 ao alternar os estados.

  4. FORMULÁRIOS COM LARGURA MÁXIMA (WIDTH 100%):
     - Todos os inputs (E-mail, Senha, Nome, Telefone celular) e os botões de submissão (Submit) devem ocupar obrigatoriamente 100% da largura do contêiner ('w-full' ou 'grid grid-cols-1 gap-4').
     - Remova qualquer espremimento lateral. Dê espaçamento interno (padding) adequado para que os textos e placeholders fiquem perfeitamente legíveis sobre o fundo escuro.
     - Certifique-se de que o formulário de Cadastro continue exigindo Nome, E-mail e Telefone celular como campos obrigatórios integrados ao Zod / React Hook Form.

  Mantenha o ecossistema de SSR do React Router v7 intacto e valide o build após a alteração dos componentes.
</task>

---

# Add Links

<context>
  Você está operando sob as regras de governança e automação do Bizu Hub Bruno Goulart.
  LEIA OBRIGATORIAMENTE antes de começar: @AI_CONTEXT.md, @CLAUDE.md e @PROJECT_TECHNICAL_SPEC.md.
  Você tem total visibilidade do projeto através do Agent Mode / Composer 2.5.
</context>

<task>
  Sua tarefa é fazer uma auditoria e atualização cirúrgica dos dados de contato e redes sociais no frontend público do projeto (especificamente no Rodapé/Footer, na página Sobre e na página de Contato). 

  Adicione e garanta a presença dos novos canais de produção de conteúdo (YouTube e TikTok) que foram integrados à identidade da plataforma.

  Utilize estritamente a tabela oficial de dados abaixo para validar e atualizar as informações:

  | Campo | Valor |
  |---|---|
  | **Nome completo** | Bruno Pelatieri Goulart |
  | **Nome de exibição** | Bruno Pelatieri |
  | **Site pessoal** | https://brunogoulart.com.br/ |
  | **YouTube** | https://www.youtube.com/@devgalactico |
  | **TikTok** | https://www.tiktok.com/@brunopelatieri |
  | **GitHub** | https://github.com/brunopelatieri |
  | **GitLab** | https://gitlab.com/brunopelatieri |
  | **Docker Hub** | https://hub.docker.com/u/brunopelatieri |
  | **LinkedIn** | https://www.linkedin.com/in/bruno-pelatieri-goulart/ |
  | **X (Twitter)** | https://x.com/brunopelatieri |
  | **Instagram** | https://www.instagram.com/brunopelatieri/ |
  | **Facebook** | https://www.facebook.com/bruno.pelatierigoulart |
  | **WhatsApp** | https://wa.me/5519992496598 (+55 (19) 9 9249-6598) |
  | **E-mail** | brunopelatieri@gmail.com |
  | **Localização** | Campinas, São Paulo, Brasil |
  | **Anos de experiência** | 18+ (Início em 2006) |

  DIRETRIZES DE IMPLEMENTAÇÃO:
  1. No Rodapé (Footer/Layout público): Inclua os ícones do YouTube e TikTok (use Lucide React ou SVG nativo polido) ao lado das redes profissionais existentes. Certifique-se de que todos os links apontem exatamente para os endereços da tabela.
  2. Na Página Sobre (`src/pages/about-page.tsx` ou equivalente): Valide se a menção aos anos de experiência reflete "18+ anos de experiência" e se os novos canais são mencionados como parte da sua presença e produção de conteúdo técnica.
  3. Na Página de Contato (`src/pages/contact-page.tsx` ou equivalente): Além do formulário que envia os dados para a API Hono, certifique-se de que os canais diretos (E-mail com `mailto:`, WhatsApp linkado corretamente e Localização) estejam visíveis e formatados de maneira limpa.
  4. Centralização de Constantes (Altamente Recomendado): Se o projeto usar um arquivo de constantes (como `src/lib/constants/meta.ts` ou similar), atualize os links lá primeiro para que a interface herde os dados de forma limpa e centralizada.

  Mantenha o estilo atual do Tailwind v4 e shadcn/ui intacto e garanta que nenhuma alteração cause quebras na compilação ou no SSR.
</task>

---

Implemente header público responsivo no Bizu Hub Bruno Goulart.

Problema: SiteHeader (src/components/layout/site-header.tsx) estoura layout em mobile — 5 nav links sempre visíveis em linha.

Solução: Padrão dashboard — mobile (<md) hamburger + Sheet com navItems de navigation.ts + auth (Entrar ou Dashboard/Sair); desktop (≥md) layout atual inline.

Criar site-nav-links.tsx reutilizável com NavLink ativo e onNavigate para fechar sheet.

Anti-overflow: min-w-0, overflow-hidden, shrink-0, px responsivo.

Não alterar src/pages/. Atualizar AI_CONTEXT.md e PROJECT_TECHNICAL_SPEC.md.

Validar: npm run typecheck && npm run build.

---

<context>
  Você está atuando sob as regras de governança e automação do Bizu Hub Bruno Goulart.
  LEIA OBRIGATORIAMENTE antes de começar: @AI_CONTEXT.md, @CLAUDE.md, @PROJECT_TECHNICAL_SPEC.md e @.specify/config.toml.
  Você tem total visibilidade do projeto através do Agent Mode / Composer 2.5 e deve seguir os padrões do SpecifyX descritos nos arquivos de configuração.
</context>

<task>
  Execute a implementação da infraestrutura client-side (TanStack Query) e o redesign responsivo e ultra-moderno da Autenticação e do Menu do Dashboard. Siga os passos abaixo alterando os arquivos necessários:

  1. INSTALAÇÃO E INFRAESTRUTURA:
     - Adicione/garanta os componentes shadcn/ui necessários para o fluxo: dialog, dropdown-menu, sheet, table, form, select, skeleton, tooltip, avatar, tabs.
     - Configure o TanStack Query Provider (`QueryClientProvider`) em `src/root.tsx`. Como o projeto usa `ssr: true` global, certifique-se de instanciar o `QueryClient` de forma segura (usando `useState` dentro do componente ou uma factory function) para evitar vazamento de cache entre requisições no servidor Node.

  2. REDESIGN DA PÁGINA DE LOGIN (`src/routes/login.tsx` ou equivalente no seu routes.ts):
     - Crie uma interface premium que remeta a "Engineering AI Design": use dark mode dominante, grids cibernéticos sutis, texturas de linhas de código em background ou efeitos de glow/border-beam lineares usando as capacidades do Tailwind v4 e os tokens de design do projeto.
     - Use o componente `Tabs` do shadcn para alternar de forma limpa entre as telas de "Login" e "Cadastro" na mesma página.
     - O formulário de Cadastro deve usar `react-hook-form` + `zod` e conter os seguintes campos OBRIGATÓRIOS: Nome, E-mail e Telefone Celular.
     - Forneça feedback visual em tempo real nos inputs e notificações de sucesso/erro via `sonner`.

  3. NOVO MENU/SIDEBAR RESPONSIVO DO DASHBOARD (`src/components/layout/dashboard-layout.tsx`):
     - Refatore o layout e componentes de navegação para um padrão totalmente responsivo inspirado no `shadcn-admin`.
     - Desktop: Sidebar lateral fixa, colapsável, com estados ativos polidos e exibição do Avatar do usuário na base.
     - Mobile: Topbar fixa com botão hambúrguer que dispara um `Sheet` (gaveta lateral) contendo os links de navegação.
     - Mantenha a convenção do projeto: a renderização inicial do shell do dashboard não deve vazar dados sensíveis no HTML via SSR; o gate de autenticação continua client-side no `ProtectedRoute`.

  4. ATUALIZAÇÃO DE CONTEXTO E METODOLOGIA SPECIFYX:
     - Ao finalizar as alterações, lembre-se de seguir a Regra de Contexto Vivo do projeto: atualize as seções correspondentes em `AI_CONTEXT.md` e `PROJECT_TECHNICAL_SPEC.md` refletindo as novas dependências e a nova estrutura visual aplicada.
</task>