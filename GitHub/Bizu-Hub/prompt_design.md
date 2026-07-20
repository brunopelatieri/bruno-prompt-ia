## 👽 :21/06/2026

---

# layout header & footer

<context>
  Você é o Claude Opus 4.8 atuando como Desenvolvedor Frontend Sênior especializado em Design Systems de vanguarda (Hype 2026).
  LEIA OBRIGATORIAMENTE os arquivos de governança: @AI_CONTEXT.md, @CLAUDE.md e @PROJECT_TECHNICAL_SPEC.md[cite: 1, 2].
  
  Os arquivos alvo diretos desta execução cirúrgica são:
  - @src/root.tsx (e os stores/providers de tema associados)
  - O componente de Header/Navbar (ex: 'src/components/layout/navbar.tsx' ou equivalente)
  - O componente de Footer (ex: 'src/components/layout/footer.tsx' ou equivalente)
  - O componente da Hero Section (ex: 'src/components/landing/hero-section.tsx')
</context>

<task>
  Sua missão é aplicar um refatoramento de elite focado no Cabeçalho (Header), no Rodapé (Footer) e na física de fundo da Hero Section, além de consolidar a plataforma em um modelo de TEMA ÚNICO (Dark Mode Only).

  EXECUTE ROTAÇÃO POR ROTAÇÃO OS 4 PASSOS ABAIXO:

  1. CONSOLIDAÇÃO DO TEMA ÚNICO (100% DARK MODE NATIVO):
     - A aplicação NÃO terá mais alternância entre temas. O conceito de "Light Mode" está oficialmente deprecado.
     - No arquivo de layout principal (como @src/root.tsx ou 'theme-provider.tsx'), fixe o atributo 'class="dark"' de forma definitiva e estática na tag <html>.
     - Remova completamente o componente ou botão de 'ThemeToggle' (ícone de sol/lua) do Header e de qualquer outro local do frontend público.
     - Limpe do código estados órfãos de persistência de tema (Zustand/localStorage), transformando o ThemeProvider em um mero pass-through ou travando-o estritamente no valor 'dark'.

  2. EFEITOS "HYPE TECNOLÓGICO" NO BACKGROUND DA HERO SECTION:
     - Na Hero Section ('src/components/landing/hero-section.tsx'), implemente um fundo de profundidade imersiva com pure CSS / Tailwind v4:
     - Injete um "Cybernetic Grid" no plano de fundo (ex: uma malha de linhas finas 'border-slate-800/40' combinada com uma máscara de desfoque/radial-gradient para que o grid desapareça suavemente nas bordas da tela).
     - Adicione "Auroras de IA" (Radial Glows) posicionadas assimetricamente atrás do texto: crie duas divs com 'position: absolute', 'filter: blur(120px)' e 'opacity: 25%'. Uma posicionada no topo-esquerdo usando o Azul Claro oficial da marca (#1096E6) e outra na central-direita usando o Verde-Teal (#00CDBA).

  3. HEADER FLOATING GLASSMORPHISM (NAVBAR):
     - Transforme o cabeçalho em uma barra flutuante fixada no topo ('sticky top-0 z-50 backdrop-blur-md bg-slate-950/80 border-b border-slate-800/50').
     - Lado Esquerdo: A marca "Bruno Goulart" com a tipografia Inter em bold e o ponto final ou subtítulo renderizado com o gradiente animado oficial da paleta.
     - Centro (Desktop): Navegação pública limpa ('Home', 'Sobre', 'Projetos', 'Contato') com microinteração de hover e traço sutil sob a rota ativa.
     - Lado Direito (Desktop): APENAS um botão principal de Call To Action de alta conversão (ex: "Fale com o Especialista" apontando para a rota '/contato' ou link do WhatsApp). Sem o botão de troca de tema.
     - Mobile: Mantenha o gatilho polido do 'Sheet' lateral contendo o menu.

  4. FOOTER DE AUTORIDADE MÁXIMA:
     - Reconstrua o Rodapé organizando a autoridade em um grid responsivo polido:
     - Coluna 1 (Brand Manifesto): Nome "Bruno Goulart — AI Automation Specialist", breve pitch de engenharia e a badge em JetBrains Mono: "Desde 2006 (18+ Anos de Código)".
     - Coluna 2 (Navegação): Links internos do site.
     - Coluna 3 (Canais e Conteúdo): Renderize a lista completa e exata de redes sociais com ícones do Lucide React (YouTube @devgalactico, TikTok @brunopelatieri, GitHub, GitLab, Docker Hub, LinkedIn, X, Instagram, Discord e WhatsApp direto).
     - Linha de Base: Copyright "© 2006-2026 Bruno Pelatieri Goulart. Construído com AI Software Engineering"[cite: 2] + um botão sutil e funcional de "Voltar ao topo" (Scroll to top).

  Valide a compilação do TypeScript. Nenhuma tag HTML deve quebrar a hidratação do React Router v7 no servidor Node.
</task>

---

# layout body content

<context>
  Você é o Claude Opus 4.8 atuando como um Desenvolvedor Frontend Sênior com 10+ anos de experiência na vanguarda da engenharia web.
  LEIA OBRIGATORIAMENTE os arquivos de governança da nossa arquitetura: @AI_CONTEXT.md, @CLAUDE.md, @PROJECT_TECHNICAL_SPEC.md e @.specify/config.toml.
  
  Você vai trabalhar estritamente nestes 4 arquivos principais (e nos subcomponentes de landing importados por eles):
  - @src/pages/home-page.tsx
  - @src/pages/about-page.tsx
  - @src/pages/projects-page.tsx
  - @src/pages/contact-page.tsx
</context>

<task>
  Sua missão é reformular o layout e preencher 100% do conteúdo das 4 páginas públicas listadas acima, adotando o posicionamento:
  "Bruno Goulart AI Automation Specialist & Full Stack Developer"

  REGRA DE ESCOPO INEGOCIÁVEL: Você está TERMINANTEMENTE PROIBIDO de alterar, refatorar ou tocar em qualquer arquivo da rota '/dashboard/**' ou na área logada. Seu escopo é 100% focado no site público.

  ====================================================================
  FONTE ÚNICA DE VERDADE (SINGLE SOURCE OF TRUTH):
  Utilize suas ferramentas de leitura de URL/Web Browsing para acessar, ler e absorver a totalidade do conteúdo real destes dois links do GitHub:
  1. https://github.com/brunopelatieri/brunopelatieri/blob/main/bruno_pelatieri_goulart-full-profile.md
  2. https://github.com/brunopelatieri/brunopelatieri/blob/main/README.md
  ====================================================================

  APLIQUE O "DESIGN SYSTEM 2026 (Hype Tecnológico)":
  - Paleta Fixa no @theme: Azul claro (#1096E6), Indigo (#3C51C4) e Verde-teal (#00CDBA).
  - Estilo: Dark mode dominante (slate-950 → slate-900), Glassmorphism com 'backdrop-blur-md', bordas sutis ('border-slate-800/50').
  - Tipografia: 'Inter' para os textos e 'JetBrains Mono' para acentos de código, números, stacks e badges.
  - Títulos: Use gradientes de texto animados combinando as 3 cores da logo.

  ====================================================================
  ROTEIRO DE PREENCHIMENTO EXAUSTIVO POR PÁGINA (Proibido atalhos):
  ====================================================================

  1. Em @src/pages/home-page.tsx (e todos os componentes da pasta 'src/components/landing/'):
     - Preencha TODAS as sections existentes. Não remova nenhuma.
     - HeroSection: Título magnético de Especialista em Automação de IA, badge de "18+ Anos de Engenharia", botões de CTA polidos.
     - AboutSection (Resumo): Pitch de autoridade retirado do README do GitHub.
     - Features/Services Section: Detalhe os pilares reais de atuação (SaaS Full Stack com Drizzle/Hono, Automações avançadas com n8n/Dify, AI Software Engineering).
     - HowItWorksSection: Explique a metodologia estruturada de desenvolvimento descrita no perfil.
     - StackSection: Liste as tecnologias reais do seu ecossistema (Vite, React, TypeScript, Hono, Postgres, Docker, Supabase, Tailwind, Python, n8n, etc.).
     - Audience / FAQ / CTA: Preencha com a copy persuasiva voltada para empresas, investidores e devs.

  2. Em @src/pages/about-page.tsx:
     - Transforme o arquivo 'bruno_pelatieri_goulart-full-profile.md' em uma página imersiva de storytelling e autoridade.
     - Destaque a linha do tempo da sua carreira: o início em 2006, os mais de 18 anos de evolução, a transição para AI Automation Specialist, e a sua filosofia rigorosa de código limpo e Spec-Driven Development.

  3. Em @src/pages/projects-page.tsx:
     - PROIBIDO usar placeholders genéricos. Extraia do GitHub os seus cases e projetos reais (ex: SaaS Diretoria, integrações Mercado Pago/Stripe, SpaceNet 24h, Bizu Hub, automações de infra).
     - Renderize cada projeto em um card de Glassmorphism com título, descrição real, links de repositório/demo e uma lista de badges horizontais com as tags da stack renderizadas em JetBrains Mono.

  4. Em @src/pages/contact-page.tsx:
     - Mantenha o formulário de contato funcional apontando para a API Hono ('/api/contact') com validação Zod e feedback visual via Sonner.
     - Na lateral ou topo do formulário, consolide todos os seus canais reais formatados de forma premium: WhatsApp (+55 19 99249-6598), E-mail, LinkedIn, YouTube (@devgalactico), TikTok (@brunopelatieri), GitHub, GitLab e Discord.

  ZERO DUMMY DATA: Nenhuma seção pode terminar com textos genéricos. Se um componente exigir um dado complementar que não esteja explícito no GitHub, utilize sua inteligência de Sênior para deduzir uma copy técnica condizente com a história do Bruno. Garanta que o SSR continue compilando sem erros de hidratação.
</task>


---

# logo - prompt nano banana

Minha sugestão: **"Bruno Goulart"** (com espaço e capitalização), não "brunogoulart" nem "BG".

Motivo prático: em layout horizontal, o símbolo (os elos entrelaçados) já vai ocupar espaço considerável à esquerda. Se o texto continuar em minúsculas coladas como está hoje, ele compete com o símbolo por "peso visual" sem ganhar legibilidade — minúsculas-coladas funcionam bem no formato vertical/empilhado (onde o texto é só uma legenda abaixo do símbolo, lido com calma), mas numa barra estreita de navbar, em tamanho pequeno, "brunogoulart" tudo junto fica mais difícil de escanear rápido que "Bruno Goulart". Capitalização correta com espaço dá ao olho dois blocos de leitura (nome + sobrenome), o que é mais rápido de processar numa faixa fina horizontal — exatamente o cenário de navbar que você quer cobrir.

"BG" eu não recomendo aqui: você está construindo marca pessoal (brunogoulart.com.br), e abreviar para iniciais faz sentido só quando o nome completo já está super consolidado/memorizado pelo público — não é ainda o seu caso, então perderia reconhecimento de marca por economia de espaço que você nem precisa (o formato horizontal já resolve o problema de espaço).

Vou montar o prompt agora com essas decisões: nome "Bruno Goulart", uso duplo (header E footer), mantendo as cores exatas, e com direção de fonte alinhada ao tema AI/automação/DevOps.Aqui está o prompt compilado para o Nano Banana:

```
Using the uploaded logo as the exact visual reference, create a new HORIZONTAL (landscape) version of this logo, optimized for use in both a website header/navbar and a footer.

DO NOT change any colors. Use these exact colors, pixel-faithful to the original:
- Light blue loop: #1096E6
- Indigo/blue loop (center, larger): #3C51C4
- Teal/green loop: #00CDBA
- Wordmark text color: #3C51C4 (same indigo as the center loop)

Layout — horizontal lockup:
- Place the interlocking-loops symbol on the LEFT side, vertically centered.
- Place the wordmark "Bruno Goulart" to the RIGHT of the symbol, on a single line, vertically centered and aligned with the symbol's optical center.
- The overall composition must read clearly and feel balanced in a wide, short aspect ratio (approximately 4:1 to 5:1 width-to-height), since it will sit in a thin horizontal navbar and footer strip.
- Keep generous, even negative space around the whole lockup so it can be placed on white or dark backgrounds without feeling cramped.
- Transparent background, true alpha transparency (not a drawn checkerboard pattern) — export as PNG with real transparency.

Symbol:
- Keep the exact same geometric concept: two interlocking rounded-rectangle/pill shapes forming an abstract link/connection, in the same 3-color arrangement and same interlock logic as the original. Do not redesign the shape concept — only adapt its proportions slightly if needed so it reads well at a smaller, wide format.

Wordmark — typography direction:
- Replace the current rounded, friendly, lowercase sans-serif with a more elegant, modern, futuristic, tech-forward typeface — the kind of font that visually communicates AI, automation, software engineering, and DevOps. 
- Think: geometric or semi-geometric sans-serif, clean and precise letterforms, slightly tightened letter-spacing, confident and technical character — avoid anything playful, rounded, or soft. Avoid anything that looks like a generic startup logo font; aim for something that feels engineered and intentional.
- Use proper capitalization: "Bruno Goulart" (capital B, capital G, with a space), not all-lowercase and not run together.
- Weight: medium-to-bold, strong enough to hold its own next to the bold, thick symbol strokes, but refined rather than heavy or chunky.

Output requirements:
- High resolution, crisp vector-like edges, no blur, no artifacts.
- Perfect vertical alignment between symbol and wordmark — they should sit on a shared optical center line, not just a shared baseline.
- The result should look like a single, intentional, professional brand lockup — not a symbol and text that were just placed side by side.

The only things allowed to change from the original: layout arrangement (horizontal instead of stacked), the wordmark's typeface and capitalization, and proportion refinement of the symbol if needed for horizontal balance. Colors, the interlocking-loops concept, and overall brand identity must remain recognizable and faithful to the original.
```

### Por que esse prompt deve funcionar bem

- **Hex exatos travados** → evita o risco real do Nano Banana "reinterpretar" suas cores ao redesenhar (acontece bastante quando se pede mudança de tipografia).
- **"true alpha transparency (not a drawn checkerboard pattern)"** → já aprendemos com a logo Bizu que sem essa instrução explícita ele desenha o xadrez como pixel. Mesmo assim, **eu recomendo fortemente** que você me mande o resultado depois — pelo padrão que já vimos duas vezes, é bem provável que ele ainda erre nisso, e eu finalizo a transparência real por código, como fiz antes.
- **"shared optical center line, not just a shared baseline"** → instrução técnica de design que evita o erro clássico de logos horizontais malfeitas (símbolo e texto alinhados pela base, parecendo "flutuar" desalinhados).
- **Direção tipográfica sem nomear uma fonte específica** → fontes específicas (Inter, Space Grotesk, etc.) muitas vezes confundem o modelo de imagem, que não tem acesso a fontes reais — é mais confiável descrever o *caráter* da tipografia.

Quando tiver o resultado do Nano Banana, me manda que eu confiro a transparência e os hex codes, e finalizo qualquer ajuste de centralização ou cor que tenha desviado.



