## 👽 :21/06/2026

---

# SEO

<system_directives>
  MODELO ALVO: Gemini 3.1 Pro (Modo Compilador / Consciência de AST Ativa).
  ESTAMINA DE SAÍDA: 32k+ Tokens. Você tem a obrigação arquitetural de reescrever a totalidade de cada arquivo modificado da linha 1 até o fechamento da última tag. É estritamente proibido o uso de reticências ou comentários de encurtamento como "// ...".
</system_directives>

<context>
  Você é o Gemini 3.1 Pro atuando como Arquiteto Principal de SEO Técnico e Engenheiro Full Stack de Elite no projeto Bizu Hub.
  Você possui conhecimento nativo da infraestrutura de indexação do Googlebot / Google AI Overviews (SGE) e domina o contrato de SSR do React Router v7.
  LEIA OBRIGATORIAMENTE os nossos manifestos de arquitetura: @AI_CONTEXT.md[cite: 1], @CLAUDE.md[cite: 2] e @PROJECT_TECHNICAL_SPEC.md.
  
  Os arquivos alvo diretos desta mutação em lote são:
  - @src/root.tsx (para metadados globais e JSON-LD de Grafo de Entidade)
  - @src/routes/*.tsx (todas as rotas públicas declaradas no routes.ts: Home, Sobre, Projetos, Contato, Blog e BlogPost)
  - O arquivo 'public/robots.txt' (ou o endpoint gerador correspondente)
</context>

<task>
  Sua missão é compilar o frontend público da plataforma em uma "Máquina de Indexação Orgânica Definitiva", otimizando o DOM para dominar as SERPs sob os termos:
  "Bruno Goulart", "AI Automation Specialist", "Especialista em Automação com IA" e "Full Stack Developer Sênior".

  BARREIRA DE ISOLAMENTO INEGOCIÁVEL: Você está estritamente proibido de modificar qualquer linha de código sob as rotas '/dashboard/**'. O escopo é 100% público.

  Implemente a especificação dos 5 Pilares de SEO de Alta Performance:

  1. CONTRATO DE METADADOS POR ROTA (RRv7 'meta: MetaFunction'):
     Em cada página pública, implemente a tipagem estrita da função 'meta' respeitando a matemática exata de conversão:
     - 'title': Máximo de 55 a 60 caracteres (Ex na Home: "Bruno Goulart — AI Automation & Full Stack").
     - 'description': Entre 150 e 160 caracteres com alta densidade semântica ("18+ anos de experiência", "Automação IA", "n8n", "Dify", "Docker", "Campinas/SP").
     - 'canonical': Link absoluto '<link rel="canonical" href="https://brunogoulart.com.br/[rota]" />'.
     - 'robots': Diretiva 'index, follow, max-image-preview:large, max-snippet:-1, max-video-preview:-1'.

  2. GRAFO DE ENTIDADES PARA GOOGLE SGE / AI OVERVIEWS (JSON-LD @graph):
     No @src/root.tsx, injete no <head> (ou via componente <StructuredData />) a marcação Schema.org avançada unificando WebSite e Person:
     {
       "@context": "https://schema.org",
       "@graph": [
         {
           "@type": "WebSite",
           "@id": "https://brunogoulart.com.br/#website",
           "url": "https://brunogoulart.com.br",
           "name": "Bruno Goulart",
           "publisher": { "@id": "https://brunogoulart.com.br/#author" }
         },
         {
           "@type": "Person",
           "@id": "https://brunogoulart.com.br/#author",
           "name": "Bruno Pelatieri Goulart",
           "alternateName": "Bruno Pelatieri",
           "jobTitle": "AI Automation Specialist & Full Stack Developer",
           "url": "https://brunogoulart.com.br",
           "address": { "@type": "PostalAddress", "addressLocality": "Campinas", "addressRegion": "SP", "addressCountry": "BR" },
           "sameAs": [
             "https://github.com/brunopelatieri",
             "https://gitlab.com/brunopelatieri",
             "https://www.linkedin.com/in/bruno-pelatieri-goulart/",
             "https://www.youtube.com/@brunopelatieri",
             "https://www.tiktok.com/@brunopelatieri",
             "https://x.com/brunopelatieri",
             "https://www.instagram.com/brunopelatieri/",
             "https://www.facebook.com/bruno.pelatierigoulart"
           ],
           "knowsAbout": [ "AI Orchestration", "n8n", "Dify", "React Router v7", "Drizzle ORM", "Docker", "Supabase", "TypeScript", "Python" ]
         }
       ]
     }
     - Nas rotas dinâmicas do Blog ('/blog/:slug'), prepare o JSON-LD 'TechArticle' referenciando o autor através do ID "https://brunogoulart.com.br/#author".

  3. DOMÍNIO DO SOCIAL GRAPH (Open Graph & Twitter Cards):
     - Propriedades genéricas: 'og:site_name: "Bruno Goulart"', 'og:locale: "pt_BR"', 'og:type' ("website" ou "article").
     - Propriedades do X: 'twitter:card: "summary_large_image"', 'twitter:site: "@brunopelatieri"', 'twitter:creator: "@brunopelatieri"'.

  4. SANEAMENTO DE HIERARQUIA ON-PAGE:
     - Regra do H1 Solitário: CADA página pública terá exatamente UM elemento <h1>.
     - Garanta a descida semântica estrita de <h2> para <h3>.
     - Injete atributos 'alt' ricos em palavras-chave em todas as tags <img>.

  5. RASTREABILIDADE (Robots.txt & Sitemap):
     - Valide a sintaxe exata em public/robots.txt:
       User-agent: *
       Allow: /
       Disallow: /login
       Disallow: /auth/
       Disallow: /dashboard/
       Sitemap: https://brunogoulart.com.br/sitemap.xml

  VERIFICAÇÃO DE COMPILAÇÃO: O Gemini 3.1 Pro atua no nível do compilador. Valide se as tipagens do TypeScript estão perfeitas e se nenhuma injeção no HTML gera 'Hydration Mismatch' durante a renderização do React Router v7 no processo Node.
</task>
