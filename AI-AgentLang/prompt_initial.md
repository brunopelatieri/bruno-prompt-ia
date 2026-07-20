## 👽 :25/06/2026

Analise @langgraph-diretoria-agents.
O objetivo seria criar uma estrutura semelhante (já que essa estrutura executa perfeitamente no docker swarm com portainer em https://dlang.bru.ia.br/ deverá ser adotada como modelo para montar langchain langgraph que será executado no mesmo docker swarm portainer porem no link: https://lang.bru.ia.br/) em uma pasta diferente e isolada de nome: sugira um nome para pasta - mas lembre-se essa pasta será retirada do repositório do projeto "Diretoria-APP" e será iniciado em outro projeto repositório. Aqui só será usada para inicial esse projeto baseado no modelo em @langgraph-diretoria-agents.

Nesse novo projeto terá como objetivo postar conteúdo em um blog e nas redes sociais seguindo abaixo:
 - Dois agentes é a escolha certa. A variação entre redes (limite de caracteres, tom, hashtags, aspect ratio) é melhor tratada como input/contexto passado ao agente, não como agentes separados. Cinco agentes com lógica 90% igual é duplicação sem ganho.
 - Arquitetura limpa:
     - content_agent redes sociais — recebe brief + rede-alvo + voz da marca → devolve copy otimizado para aquela rede (sabe os limites: X=280 chars, LinkedIn formal, TikTok coloquial, etc.)
     - content_agent blog seguir a risca à regra: 
        "Boa pergunta — e a resposta certa não é um número único, é uma faixa com lógica por trás. Deixa eu te dar a visão real de editor, não só "regra de mercado":
            ## A faixa que funciona
            **1.200 a 2.000 palavras** é o ponto ótimo para esse público específico que você descreveu.
            Aqui está o porquê:
            | Faixa | O que acontece |
            |---|---|
            | < 800 palavras | Parece superficial para CEO/investidor — eles sentem que "faltou profundidade" |
            | 1.200–2.000 | Tempo de leitura de 5–8 min. Cabe em uma pausa de café, mas tem substância |
            | 2.000–3.000 | Funciona só se for pilar/cornerstone content (guia definitivo, comparativo) |
            | > 3.000 | Você perde 70% dos leitores na rolagem — só sobrevive se for ferramenta de referência, não leitura linear |
            ## Por que essa faixa e não outra
            **Seu público é "scanner", não "leitor linear".** CEO, investidor e dev sênior não leem de cima a baixo — eles escaneiam o H2/H3, decidem se vale parar, e leem só os trechos que importam pra eles. Isso muda completamente a lógica: o texto não precisa ser curto, precisa ser **escaneável em qualquer tamanho**.
            Isso é diferente de "número de palavras importa". O que importa de verdade é:
            1. **Densidade de informação por parágrafo** — 2 a 4 linhas, nunca blocos de 8+ linhas
            2. **Um H2 a cada 150-300 palavras** — se a pessoa só ler os títulos, ela já entende a estrutura do argumento
            3. **Uma ideia por parágrafo** — zero "e além disso, também, complementarmente"
            ## O ajuste fino por tipo de público dentro do seu grupo
            - **CEO/Investidor**: querem ver a conclusão e o número/dado logo no início (pirâmide invertida) — não economize palavras, mas não enrole pra chegar ao ponto
            - **Dev/Tech**: aceitam textos mais longos *se* tiverem código, tabela comparativa ou diagrama quebrando o texto a cada 300-400 palavras
            - **Recrutador/Curioso** (não prioritário): vão ler só a intro e a conclusão — então **essas duas partes precisam ser autossuficientes**, como se fossem um resumo do artigo inteiro
            ## Minha recomendação prática pra você
            Dado o seu estilo (Markdown Enterprise, tabelas, badges, bilíngue): **1.000 a 1.500 palavras** é o seu sweet spot. Dá espaço pra estrutura completa (Objetivo → Arquitetura → Exemplos → Boas Práticas) sem cansar quem só quer escanear, e ainda parece "denso o suficiente" pra quem está decidindo se te contrata ou investe.
     - image_agent — recebe brief + rede-alvo (blog imagem ratio 4:5, aspect ratio: 4:5 e/ou 1:1 Instagram/Facebook, 16:9 LinkedIn, 9:16 TikTok) → gera prompt para modelo de imagem estritamente (escolha por switch): Midjourney, ChatGPT/GPT Image e Nano Banana do Gemini → chama a API e devolve a imagem. Importante: teria um switch que acionaria a criação de imagem ou não. No caso, seria informado a url da imagem que seria utilizada. No caso da imagem teria-mos 3 situações: 
         - Criar a imagem através do prompt e LLM (será usando um desses: Midjourney, ChatGPT/GPT Image e Nano Banana do Gemini - qual estiver configurado em settings);
         - "Ler" a imagem enviada pela url através do LLM (será usando um desses: Midjourney, ChatGPT/GPT Image e Nano Banana do Gemini - qual estiver configurado em settings) e acrescentar contexto no brief que será enviado para o content_agent blog e redes sociais para criação de content text.
         - Apenas receber a imagem  da url e não faz nada. Apenas vincula anexo ao content-agent text para aprovação.
     - ponto de atenção: se o fluxo for "gerar texto → usar o texto para informar a imagem", você quer um grafo com os dois agentes em sequência + nó de aprovação humana no meio, não dois agentes independentes. LangGraph é exatamente para isso.
     - Esse agente irá será executado em uma VPS docker portainer (como no modelo em @langgraph-diretoria-agents) e irá trabalhar em um ecosistema com n8n, supabase e ficara no em uma pasta (que você LLM Fable 5 dará o nome) no repositório do projeto com essa arquitetura (trabalhará com esse sistema também - o principal do ecosistema):"## Arquitetura atual
            - React Router v7 Framework Mode com `ssr: true`.
            - Hono API em `src/api/app.ts`, montado por `src/server.ts`.
            - Processo único em dev/prod (`react-router dev`, `node build/server/index.js`).
            - Drizzle/Postgres como fonte de dados.
            - Supabase apenas auxiliar (Auth, Storage, Functions, Realtime).
            - Dashboard client-only por convenção: sem loaders server-side com dados sensíveis.

            ## Regra de contexto vivo

            Se alterar arquitetura, rotas, stack, deploy, banco, auth, billing, dashboard,
            rules ou SpecifyX, atualize também:

            - `.context/onboarding/AI_CONTEXT.md`
            - `.context/spec/TECHNICAL_SPEC_COMPACT.md`
            - `README.md` se afetar onboarding
            - `.cursor/rules/*.mdc` se afetar decisões futuras de agentes".


Importante questionar:
 - Dois agentes será o suficiente: um agente para content text: blog + redes sociais ou um agente para montar o content blog e outro para montar o text de redes sociais?
 - Ficar restrito a gerar content para: blog, facebook, instagram, X, linkedin e tiktok
 - Gerar Imagem restrito a esses: Midjourney, ChatGPT/GPT Image e Nano Banana do Gemini
 - Como esse projeto seria utilizado por vários segmento comerciais diferentes: Restaurantes, hotéis, agências etc...como faria-mos com o prompt? Teria-mos um prompt mestre (que nunca muda) e depois prompts de agent persona que muda para cada segmento? Prompt no format MD ou XML? Qual seria melhor? Eu prefiro XML. E você Fable 5 o que me fala?
 - Os prompt ficariam em tabela no supabase (gere migration com os prompts compatíveis com o supabase).
 - Os telas via HTML para mostrar os resultados para serem avaliados seria feito pela sistema react do ecosistema ou n8n?
 - As publicações nas redes sociais seria feita pelo sistema react ou n8n? 
 - Me ajude com essas questões. Como o blog vai ficar no sistema react eu faria tudo no sistema react usando o n8n talvez para questões que você fable 5 decidir, ok?
 - lembre-se você começará no projeto Diretoria-App depois vamos migrar para o projeto react:
 "## Arquitetura atual

- React Router v7 Framework Mode com `ssr: true`.
- Hono API em `src/api/app.ts`, montado por `src/server.ts`.
- Processo único em dev/prod (`react-router dev`, `node build/server/index.js`).
- Drizzle/Postgres como fonte de dados.
- Supabase apenas auxiliar (Auth, Storage, Functions, Realtime).
- Dashboard client-only por convenção: sem loaders server-side com dados sensíveis.

## Regra de contexto vivo

Se alterar arquitetura, rotas, stack, deploy, banco, auth, billing, dashboard,
rules ou SpecifyX, atualize também:

- `.context/onboarding/AI_CONTEXT.md`
- `.context/spec/TECHNICAL_SPEC_COMPACT.md`
- `README.md` se afetar onboarding
- `.cursor/rules/*.mdc` se afetar decisões futuras de agentes" em uma pasta que você dirá o nome. ok? ou prefere diferente e já criar no diretório onde tudo vai ficar e você, fable5 crie o prompt para executar o PRD ou SPEC (no outro repositório tem o SpecifyX - quer fazer por lá?). Você crie o prompt aqui no Diretoria-APP, com as informações relevantes e importantes e eu executo no repositório original do projeto que é o "bixu-hub" já descriminado aqui no claude desktop" - só me faça o prompt de migração com tudo que precisa + instruções que migramos, ok?
 - Melhor criar o PRD ou já vamos para SPEC ou utilizar o SpecifyX do repositório original "bizu-hub"?
 - Como é um projeto paralelo ao Diretori-APP, não quero utilizar a SKILL PRD ou SPEC (green field do projeto Diretoria-APP - ou menos se você, Fable 5 falar que devo fazer isso).
 - Se tiver dúvida me fale que complemento com todas as informações que você precisar, ok?  






