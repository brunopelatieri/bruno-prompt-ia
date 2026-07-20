# local.ia.br — Checklist Mobile-First
### Com 98% dos leads vindo do celular, mobile deixa de ser "também precisa funcionar" e vira a versão principal do site — desktop é o caso secundário, não o contrário.

Este documento complementa os 2 anteriores (conteúdo das 4 páginas + header/footer padrão). Aqui não repito copy — é checklist de execução para o Fable 5 seguir antes de considerar o site pronto para publicar.

**Legenda de prioridade:**
- **P0** — crítico. Sem isso, o site perde lead todo dia.
- **P1** — importante. Afeta conversão e SEO de forma direta.
- **P2** — recomendado. Melhora incremental.

---

## 1. Performance Mobile (Core Web Vitals)

- [ ] **P0** — Maior elemento visível de cada página (geralmente a imagem ou título do Hero) carregando em até 2,5s em conexão 4G mediana, não só em wi-fi rápido de escritório.
- [ ] **P0** — Todas as imagens em formato moderno (WebP ou AVIF), comprimidas, servidas no tamanho certo para tela de celular — não a mesma imagem gigante do desktop redimensionada por CSS.
- [ ] **P0** — Lazy loading em toda imagem abaixo da primeira tela visível.
- [ ] **P1** — Resposta ao toque abaixo de 200ms — evitar JavaScript pesado travando a rolagem ou o clique em botão.
- [ ] **P1** — Sem "pulos" de layout enquanto a página carrega — reservar o espaço da imagem e dos botões antes deles carregarem, para o botão de WhatsApp não "pular" bem na hora que o usuário ia tocar nele.
- [ ] **P1** — Fontes carregando sem troca visível de tipografia no meio da leitura.
- [ ] **P2** — Pré-carregamento da imagem principal do Hero de cada página.

---

## 2. Usabilidade Mobile-First (Design e Navegação)

- [ ] **P0** — Nenhuma rolagem horizontal forçada em nenhuma tela — inclusive as tabelas de preço de Elétrica e Marido de Aluguel, que precisam virar cards empilhados no celular, nunca tabela espremida com scroll lateral.
- [ ] **P0** — Botões e links grandes o bastante para tocar com o polegar sem errar o vizinho — nada de dois links colados que forçam zoom para acertar o certo.
- [ ] **P0** — Texto do corpo legível sem precisar dar zoom.
- [ ] **P0** — Menu de navegação funcionando 100% por toque — sem depender de "passar o mouse" (hover não existe em celular).
- [ ] **P1** — CTA principal de cada página alcançável com o polegar sem precisar esticar a mão até o topo da tela — considerar botão fixo na parte inferior, não só um botão lá em cima que some quando o usuário rola.
- [ ] **P1** — FAQ em acordeão que abre e fecha por toque, uma pergunta de cada vez — evita uma rolagem infinita de texto.
- [ ] **P1** — Nenhum pop-up ou banner que cubra o conteúdo assim que a página abre no celular — o Google penaliza isso especificamente em busca mobile.
- [ ] **P2** — Campos de formulário com o teclado certo para cada tipo de dado (teclado numérico para telefone, por exemplo), para o usuário não precisar trocar de teclado manualmente.

---

## 3. Conversão e Captura de Leads no Mobile

Esta é a parte que mais importa dado o seu número: 98% do lead entra e decide tudo pela tela do celular, com o polegar.

- [ ] **P0** — Botão flutuante de WhatsApp fixo na tela, visível em qualquer ponto de rolagem, em todas as 4 páginas — não escondido dentro do menu.
- [ ] **P0** — Link de WhatsApp abrindo direto o aplicativo (não uma página de contato genérica), com mensagem pré-preenchida.
- [ ] **P0** — Telefone tocável — um toque liga direto, sem precisar copiar o número.
- [ ] **P1** — Mensagem pré-preenchida do WhatsApp diferente por página, para o atendimento já saber de onde o lead veio:
  - Home: "Vim do site, quero orçamento de CFTV/Alarme"
  - PC: "Vim do site, quero orçamento de Informática/Redes"
  - Elétrica: "Vim do site, quero orçamento de Elétrica"
  - Marido de Aluguel: "Vim do site, quero orçamento de reparos"
- [ ] **P1** — Formulário de orçamento curto: nome, telefone, serviço de interesse, cidade — nada além disso. Cada campo a mais é lead que desiste no celular.
- [ ] **P2** — Rastreamento de clique no botão de WhatsApp e no telefone como evento de conversão, para saber quantos leads reais o site está gerando (não só visitas).

---

## 4. SEO Mobile e Local

- [ ] **P0** — Assumir indexação mobile-first como padrão: o Google usa a versão mobile do site como referência principal, então nada de conteúdo que só aparece na versão desktop.
- [ ] **P0** — Perfil da Empresa no Google criado, com nome, endereço e telefone idênticos aos do site (essa consistência de dado é o que mais pesa em busca "perto de mim" no celular).
- [ ] **P1** — Dados estruturados (negócio local, serviço, perguntas frequentes) implementados conforme já especificado nos documentos anteriores — no celular, isso pode aparecer direto no resultado de busca sem o usuário nem entrar no site.
- [ ] **P1** — Palavra-chave da cidade no título e no primeiro parágrafo de cada página (Conchal, Campinas, Águas de Lindóia, Monte Sião, conforme a página).
- [ ] **P2** — Sitemap.xml e robots.txt atualizados com as 4 rotas.

---

## 5. Checklist de Metadados por Página (consolidado)

| Página | URL | Meta título | Meta descrição (resumo) |
|---|---|---|---|
| Home | `/` | CFTV e Alarmes em Águas de Lindóia e Monte Sião | Instalação, manutenção e suporte de CFTV e alarmes na região. Segurança para pousadas, lojas, fábricas e residências. |
| Computadores e Redes | `/pc` | Informática e Redes em Águas de Lindóia e Monte Sião | Montagem de computadores, redes cabeadas e wi-fi, formatação Windows/Linux. Especialistas em redes para hotéis. |
| Elétrica | `/eletrica` | Eletricista Residencial e Comercial em Campinas e Região | Tomadas, disjuntores, chuveiro, iluminação e mais. Atendimento em Conchal, Campinas e Circuito das Águas Paulista. |
| Marido de Aluguel | `/marido-de-aluguel` | Marido de Aluguel em Campinas e Região — Reparos Gerais | Montagem de móveis, fixações, hidráulica leve, pintura e pequenos reparos, numa visita só. |

*(Descrições completas e Open Graph de cada página estão nos documentos anteriores — esta tabela é só para conferência rápida antes de publicar.)*

---

## 6. Testes Antes de Publicar

- [ ] Testar as 4 páginas em um celular real, não só redimensionando o navegador do computador.
- [ ] Rodar teste de velocidade mobile (ex: PageSpeed Insights, aba mobile) nas 4 páginas — não só na Home.
- [ ] Tocar no botão de WhatsApp e no telefone em um celular de verdade e confirmar que abre o app certo.
- [ ] Preencher o formulário de orçamento inteiro usando só o teclado do celular.
- [ ] Conferir se nenhuma tabela de preço quebra o layout em tela pequena (testar especificamente em torno de 360–390px de largura, a faixa mais comum de celular no Brasil).
- [ ] Rolar cada página inteira no celular e confirmar que o botão flutuante de WhatsApp nunca cobre um botão ou texto importante.

---

## Observações Finais

1. Se tiver que escolher entre "ficar bonito no desktop" e "funcionar perfeito no celular" em algum ponto do desenvolvimento, a prioridade é sempre o celular — é onde 98% do seu lead decide.
2. Depois de publicado, vale acompanhar por 2–3 semanas quantos cliques reais o botão de WhatsApp está gerando por página — isso mostra na prática qual dos 4 serviços está puxando mais gente, e ajuda a decidir onde investir em conteúdo ou anúncio depois.
