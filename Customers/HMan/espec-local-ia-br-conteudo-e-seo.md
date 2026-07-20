# local.ia.br — Conteúdo Completo + Instruções de SEO
### Documento de texto puro para implementação por Agente de IA (Fable 5) em React/Vite

---

## Nota do Editor (o que mudou nesta versão)

Esta versão substitui e expande o documento anterior (que era só CFTV para 2 cidades). Agora o site cresceu em 3 frentes, e reorganizei o conteúdo para acompanhar isso:

1. **Escopo de serviço** — de "só câmera" para "câmera + manutenção + alarme + informática/redes".
2. **Escopo geográfico** — de 2 cidades para 6, mantendo Águas de Lindóia e Monte Sião como foco principal e Lindóia, Serra Negra, Socorro e Itapira como cobertura secundária (ótimo para long-tail de SEO sem diluir a narrativa central).
3. **Escopo de site** — de "uma página" para "duas páginas": Home (`/`) e Computadores e Redes (`/pc`).

Troquei o nome fictício de "CFTV Protege" para **"Local"**, porque agora o negócio não é mais só CFTV — é segurança eletrônica + tecnologia, e "Local" conversa direto com o domínio `local.ia.br` (que, a propósito, segue o mesmo padrão do seu portfólio de domínios `.ia.br`). Uso "Local Segurança" como sub-marca da Home e "Local PC & Redes" como sub-marca da página de informática, mas ambas sob o mesmo guarda-chuva visual "Local". Troque livremente se já tiver um nome definido.

Este documento contém **apenas texto** — nenhum HTML, nenhum CSS, nenhum trecho de código. Tudo que parece "instrução técnica" abaixo é para o Agente de IA (Fable 5) interpretar e implementar com suas próprias ferramentas em React/Vite.

---

## 1. Instruções para o Agente de IA (Fable 5) — Arquitetura e SEO Técnico

Estas instruções não são código — são a especificação que você (Fable 5) deve traduzir para React/Vite ao construir o site.

**Domínio e rotas**
- Domínio: `https://www.local.ia.br`
- Rota 1 (Home): `/` — conteúdo de CFTV, alarmes e segurança eletrônica.
- Rota 2: `/pc` — conteúdo de informática, hardware e redes.
- Use React Router (ou equivalente) para as duas rotas. Mesmo header e footer nas duas páginas, com navegação cruzada clara entre elas.

**SEO técnico — requisitos**
- Cada rota precisa ter seus próprios metadados (título, descrição, Open Graph, canonical) gerenciados de forma independente — não um único `index.html` estático para as duas. Use uma solução de gerenciamento de head por rota compatível com React (ex: biblioteca de head management ou geração estática por rota).
- Priorize renderização estática ou pré-renderização por rota (SSG) em vez de SPA 100% client-side puro — motores de busca precisam ler o conteúdo sem depender de JavaScript pesado para indexar corretamente.
- Idioma do documento: português do Brasil.
- Gere `sitemap.xml` contendo as duas rotas e `robots.txt` permitindo indexação total.
- Use URLs amigáveis e estáveis — evite parâmetros de query nas rotas principais.
- Estrutura de headings: um único H1 por página, contendo a palavra-chave principal daquela página. H2 para cada section listada abaixo, H3 para subitens (ex: dentro de Aplicações e FAQ).
- Use marcação semântica de página (cabeçalho, navegação, conteúdo principal, rodapé, sections e artigos correspondentes a cada bloco de conteúdo) em vez de divs genéricas — isso importa tanto para SEO quanto para acessibilidade.
- O bloco de contato/endereço no rodapé deve usar semântica de "informação de contato", não um bloco de texto genérico.
- Todas as imagens precisam de texto alternativo descritivo e específico (ex: "instalação de câmera CFTV em fachada de pousada em Águas de Lindóia" — nunca "imagem1.jpg" ou texto vazio).
- Links internos entre Home e `/pc` devem usar texto âncora descritivo (ex: "conheça nossos serviços de redes para hotéis", nunca "clique aqui").
- Implemente breadcrumb semântico na página `/pc` (Home > Computadores e Redes).

**Dados estruturados (Schema.org) — implementar via JSON-LD**
- Tipo principal: negócio local de segurança eletrônica (categoria mais próxima disponível no vocabulário do Schema.org).
- Campos: nome, URL, telefone, endereço, área de atendimento (listar as 6 cidades: Águas de Lindóia, Monte Sião, Lindóia, Serra Negra, Socorro, Itapira), horário de funcionamento, perfis de redes sociais.
- Na página `/pc`, adicionar também um bloco de serviço para cada item listado (montagem de computador, cabeamento de rede, configuração de wifi, etc.).
- Nas duas páginas, implementar dados estruturados de Perguntas Frequentes correspondentes ao conteúdo do FAQ de cada página — isso costuma gerar destaque extra nos resultados de busca do Google.
- Se possível, implemente também dados estruturados de "trilha de navegação" (breadcrumb) na página `/pc`.

**Performance (afeta SEO via Core Web Vitals)**
- Carregamento preguiçoso (lazy loading) para imagens abaixo da dobra.
- Otimize e sirva imagens em formato moderno e responsivo.
- Evite bloqueio de renderização por fontes ou scripts de terceiros.

---

## 2. Mapa do Site

| Rota | Nome da página | Foco de conteúdo |
|---|---|---|
| `/` | Home — Local Segurança | CFTV, alarmes, manutenção, as 6 cidades |
| `/pc` | Computadores e Redes — Local PC & Redes | Hardware, software, redes, especialidade em hotéis |

---

# PÁGINA 1 — Home (`/`)

## SEO da Página Home

**Meta título** (até ~60 caracteres): CFTV e Alarmes em Águas de Lindóia e Monte Sião

**Meta descrição** (até ~160 caracteres): Instalação, manutenção e suporte de CFTV e alarmes em Águas de Lindóia, Monte Sião e região. Segurança para pousadas, lojas, fábricas e residências.

**Open Graph — título**: Local Segurança — CFTV e Alarmes em Águas de Lindóia e Monte Sião

**Open Graph — descrição**: Câmeras e alarmes com instalação, manutenção e suporte contínuo. Atendimento em Águas de Lindóia, Monte Sião, Lindóia, Serra Negra, Socorro e Itapira.

**Open Graph — imagem**: foto real (não banco de imagens) de uma instalação concluída — fachada de pousada ou loja com câmera visível. Dimensão recomendada 1200x630. Texto alternativo descritivo obrigatório.

**Palavras-chave principais desta página**: CFTV Águas de Lindóia, alarme Monte Sião, câmeras de segurança Águas de Lindóia, instalação de alarme residencial MG, manutenção de câmeras CFTV, segurança para pousada, segurança para loja de tricô.

**URL canônica**: `https://www.local.ia.br/`

---

## Sumário das Sections da Home

Mantive as 8 sections originais e adicionei 2 novas, totalizando **10 sections**, para acomodar o crescimento de escopo (manutenção, alarmes e a ponte para a página de informática):

| # | Section | Motivo |
|---|---|---|
| 1 | Hero | (mantida) |
| 2 | Números | (mantida) |
| 3 | Diferenciais + Manutenção | Expandida para incluir os serviços de manutenção pedidos |
| 4 | Aplicações | Expandida com bloco das 4 cidades secundárias |
| 5 | Tecnologias CFTV | (mantida) |
| 6 | **Alarmes Residenciais e Comerciais** | **Nova** — pesquisa de marcas que você trouxe |
| 7 | **Informática e Redes (teaser)** | **Nova** — resumo + chamada para `/pc` |
| 8 | FAQ | Expandida com perguntas sobre alarme e manutenção |
| 9 | Contato Final | (mantida) |
| 10 | Footer | Expandido com as 6 cidades |

---

### 1. Hero

**Título (H1):** CFTV e Alarmes em Águas de Lindóia e Monte Sião — Instalação, Manutenção e Suporte Real

**Subtítulo:** Câmeras e alarmes para pousada, loja, fábrica, condomínio ou residência — com instalação cuidadosa, manutenção periódica e um time que continua disponível depois que a câmera já está na parede.

**Selo de credibilidade:** Atendimento em Águas de Lindóia, Monte Sião, Lindóia, Serra Negra, Socorro e Itapira — sem taxa de deslocamento na região.

**Botões (CTA):**
- Falar agora no WhatsApp
- Pedir orçamento grátis em 2 minutos

---

### 2. Números

- **[X]+** câmeras e alarmes instalados na região
- **[X]** anos de experiência com segurança eletrônica
- Atendimento em até **[XX]h** após contato
- **[XX]%** dos orçamentos aprovados em até 1 visita técnica

*(lembrete: só publique número real — evite estatística inventada)*

---

### 3. Diferenciais + Manutenção

**Título (H2):** Por que escolher a Local Segurança

1. **Especialistas na região** — conhecemos a realidade de quem vive de temporada em Águas de Lindóia e de quem vive do tricô em Monte Sião, além de atender bem Lindóia, Serra Negra, Socorro e Itapira.
2. **Marcas líderes de mercado** — trabalhamos com as principais marcas de câmeras e alarmes do Brasil, escolhidas conforme seu orçamento e a exigência do local.
3. **Acesso remoto pelo celular** — veja sua casa, pousada, loja ou fábrica de qualquer lugar do mundo, em tempo real.
4. **Instalação limpa e rápida** — sem quebra-quebra, sem fio aparente.
5. **Conformidade com a LGPD** — orientamos a sinalização correta de área monitorada.
6. **Orçamento sem compromisso** — visita técnica, projeto e proposta sem custo.

**Subtítulo (H3):** Não é só instalar — é manter funcionando

A maior parte dos problemas de CFTV não aparece na instalação, aparece meses depois: cabo ressecado, conector oxidado, câmera desalinhada, fonte de alimentação queimada. Por isso, oferecemos:

- **Manutenção periódica** de câmeras e alarmes, com revisão de imagem, conexão e gravação.
- **Ajuste e troca de local de câmeras** quando o ambiente muda (nova estante em loja, novo quarto liberado para hóspede, novo layout de fábrica).
- **Passagem e substituição de cabos** que se desgastam com sol, chuva e tempo.
- **Troca de conectores e fontes de alimentação**, causa mais comum de câmera "fora do ar" sem ninguém perceber até o dia em que precisa da imagem e ela não existe.

---

### 4. Aplicações

**Título (H2):** Onde instalamos e por quê

#### 4.1 — Águas de Lindóia (SP): Segurança para quem vive de turismo

Águas de Lindóia recebe turistas o ano inteiro — e onde há fluxo de gente de fora, há risco. Hotéis, pousadas e principalmente imóveis de aluguel por temporada (Airbnb, VRBO, Booking.com e sistemas de gestão como o Stays) precisam de duas coisas ao mesmo tempo: hóspede protegido e proprietário protegido.

Câmeras nas áreas comuns, portarias, garagens e acessos externos:
- Inibem furto, roubo e atos de violência antes que aconteçam.
- Geram prova em vídeo para resolver disputas de check-in/check-out, dano ao imóvel ou conduta do hóspede.
- Reduzem o risco de avaliação negativa causada por incidentes que poderiam ter sido evitados ou documentados.
- Dão segurança jurídica ao anfitrião em caso de acionamento de seguro ou disputa com plataforma.

*Ideal para: pousadas, hotéis, casas e apartamentos de temporada, prédios com locação por curta duração.*

#### 4.2 — Monte Sião (MG): Segurança para o polo têxtil do Sul de Minas

Monte Sião é a Capital Nacional do Tricô, com mais de mil fábricas e 600 lojas recebendo compradores o ano inteiro. Onde há fluxo de dinheiro e mercadoria, há risco de furto, roubo e agressão a clientes e funcionários.

Câmeras internas e externas na loja, no estoque e na linha de produção:
- Inibem furto de mercadoria e reduzem perdas.
- Protegem clientes durante a compra e funcionários durante o expediente.
- Geram prova em vídeo para ocorrência policial, seguro e processos trabalhistas.
- Nas fábricas e malharias, monitoram acesso, controle de produção e segurança da linha.

*Ideal para: lojas de tricô, malharias, fábricas, estoques, centros de distribuição.*

#### 4.3 — Residências, condomínios e locais públicos

Casa, prédio, condomínio, academia — qualquer lugar com fluxo de pessoas precisa de tudo filmado. Em caso de furto, roubo, agressão ou disputa, quem tem imagem tem prova.

- **Residências:** monitoramento de portão, garagem e áreas externas.
- **Condomínios e prédios:** hall, portaria, elevador e áreas comuns.
- **Academias e locais com grande circulação:** segurança de patrimônio e de pessoas.

#### 4.4 — Também atendemos: Lindóia, Serra Negra, Socorro e Itapira

Além do foco principal em Águas de Lindóia e Monte Sião, atendemos toda a região do Circuito das Águas Paulista e o entorno da divisa SP/MG:

- **Lindóia e Serra Negra:** mesmo perfil turístico e de temporada de Águas de Lindóia — pousadas, hotéis e locação por plataforma.
- **Socorro:** turismo de aventura e temporada, com necessidade semelhante de segurança patrimonial em pousadas e comércio.
- **Itapira:** perfil mais comercial e residencial, com demanda por CFTV em lojas, condomínios e indústrias locais.

---

### 5. Tecnologias CFTV

**Título (H2):** Trabalhamos com as marcas mais confiáveis do mercado

| Marca | Perfil | Aplicação ideal |
|---|---|---|
| Intelbras | Custo-benefício | Residências e pequenos comércios |
| Hikvision | Custo-benefício avançado | Lojas e projetos médios/grandes |
| Dahua | Custo-benefício avançado | Lojas e projetos médios/grandes |
| Vivotek | Técnica intermediária | Comércio e projetos mais exigentes |
| Axis | Premium | Fábricas, malharias e projetos corporativos |
| Bosch | Premium | Ambientes críticos e corporativos |
| Hanwha Vision | Premium | Projetos corporativos robustos |
| Avigilon | Segurança avançada | Grandes instalações |
| Geovision | Custo-benefício | Comércio e integração de sistemas |
| TecVoz | Entrada | Residências e pequenos comércios |

**Recomendação rápida por perfil:**
- Residência / pousada pequena: Intelbras.
- Loja de tricô / comércio de médio porte: Hikvision ou Dahua.
- Fábrica / malharia / projeto corporativo: Axis, Bosch ou Hanwha Vision.

---

### 6. Alarmes Residenciais e Comerciais (NOVA)

**Título (H2):** Alarmes para todo perfil — do básico ao conectado

Assim como em câmeras, no alarme existe uma faixa que vai do sistema simples e sem fio até soluções com monitoramento 24h, aplicativo e automação. Ajudamos você a escolher o nível certo para o seu caso — sem vender mais tecnologia do que você precisa.

**Entrada e custo-benefício**
- **Intelbras** — a porta de entrada mais comum no Brasil, com boa disponibilidade e integração por aplicativo.
- **JFL** — tradição em segurança eletrônica, com foco em robustez e boa relação preço/funcionalidade.
- **Giga** — opção acessível para quem quer um sistema funcional sem partir para o premium.
- **Positivo Casa Segura** — para quem busca praticidade e um app simples de usar.

**Nível intermediário**
- **Intelbras (linhas IP e monitoradas)** — sensores sem fio, app e comunicação por Ethernet ou Wi-Fi.
- **JFL Active 32 Duo** — mais zonas e recursos que os kits mais simples.
- **Ajax** — sobe o nível em tecnologia, automação e confiabilidade.
- **Verisure** — entra aqui quando o foco é monitoramento contratado, não só equipamento.

**Sofisticado e IoT**
- **Verisure** — monitoramento 24h, sensores conectados, videomonitoramento e resposta profissional.
- **Ajax** — ecossistema inteligente, sensores sem fio e automação de ponta.
- **Intelbras IP/monitoradas** — acompanhamento em tempo real via app, ideal para projetos conectados.
- **Soluções corporativas premium** — arquiteturas com monitoramento profissional e múltiplos canais de comunicação.

**Leitura prática:**
- Prioridade em **custo-benefício**: Intelbras e JFL são os nomes mais seguros para começar.
- Prioridade em **tecnologia conectada e IoT**: Ajax e Verisure se destacam pelo ecossistema e automação.
- Prioridade em **facilidade de compra e suporte local**: Intelbras continua sendo a referência mais prática.
- Prioridade em **monitoramento profissional completo**: Verisure é a opção mais forte.

**Por segmento:**

| Segmento | Marcas mais indicadas |
|---|---|
| Residencial básico | Intelbras, JFL, Giga, Positivo Casa Segura |
| Residencial premium | Verisure, Ajax |
| Comércio pequeno e médio | Intelbras, JFL, Ajax |
| Comércio maior e corporativo | Verisure, Ajax, Intelbras IP/monitorada |

---

### 7. Informática e Redes — Teaser (NOVA)

**Título (H2):** Também cuidamos do resto da sua estrutura de tecnologia

Câmera e alarme dependem de rede, cabo e computador funcionando bem — por isso também oferecemos montagem e manutenção de computadores, redes cabeadas e wi-fi, formatação e instalação de sistemas, e uma especialidade em redes para hotéis e pousadas.

**Resumo dos serviços:**
- Montagem de computadores, troca de hardware e periféricos.
- Instalação de softwares, formatação e instalação de Windows e Linux.
- Crimpagem e teste de cabos de rede (LAN RJ45).
- Configuração de redes Windows e Linux, cabeadas e wi-fi.
- Consultoria e dimensionamento de computadores para cada uso: desktop, servidor, computador para CFTV e computador gamer.
- Especialidade em dimensionamento de rede wi-fi para hotéis e pousadas.

**CTA:** Conheça todos os serviços de Computadores e Redes → `https://www.local.ia.br/pc`

---

### 8. FAQ

**1. Quanto custa instalar CFTV ou alarme em Águas de Lindóia ou Monte Sião?**
O valor varia conforme número de câmeras/sensores, resolução e tipo de imóvel. Fazemos visita técnica gratuita e enviamos orçamento fechado.

**2. Consigo ver as câmeras e o status do alarme pelo celular?**
Sim. Trabalhamos com sistemas com acesso remoto por aplicativo.

**3. As câmeras funcionam à noite?**
Sim, com visão noturna infravermelho ou colorida de baixa luminosidade.

**4. É legal gravar minha loja, pousada ou condomínio?**
Sim, desde que a área monitorada esteja sinalizada e o uso das imagens respeite a LGPD. Orientamos a sinalização correta em toda instalação.

**5. Vocês fazem manutenção de câmera já instalada por outra empresa?**
Sim. Fazemos revisão, ajuste de posição, troca de cabo, conector e fonte de alimentação em sistemas já existentes.

**6. Qual a diferença entre um alarme básico e um alarme com monitoramento 24h?**
O básico dispara localmente (sirene/app); o monitorado aciona uma central que verifica e pode acionar apoio. Ajudamos a escolher o nível certo para o seu caso e orçamento.

**7. Atendem apenas Águas de Lindóia e Monte Sião?**
Nosso foco é essas duas cidades, mas atendemos também Lindóia, Serra Negra, Socorro e Itapira.

---

### 9. Contato Final

**Título (H2):** Proteja o que você construiu — hoje, não depois de um problema

Furto, roubo e prejuízo não avisam. Fale agora com quem entende a realidade de Águas de Lindóia, Monte Sião e região.

**Botões (CTA):**
- Chamar no WhatsApp: [SEU NÚMERO]
- E-mail: [SEU E-MAIL]
- Preencher formulário de orçamento gratuito

---

### 10. Footer

**Local Segurança — CFTV e Alarmes**
Instalação, manutenção e suporte de CFTV e alarmes em Águas de Lindóia, Monte Sião, Lindóia, Serra Negra, Socorro e Itapira.

Atendemos: Águas de Lindóia/SP · Monte Sião/MG · Lindóia/SP · Serra Negra/SP · Socorro/SP · Itapira/SP

[SEU TELEFONE] · [SEU E-MAIL] · CNPJ: [SEU CNPJ]

[Instagram] · [WhatsApp] · [Facebook]

Link interno: Computadores e Redes (`/pc`)

[Política de Privacidade] · [Termos de Uso]

© [ANO] Local Segurança. Todos os direitos reservados.

---

# PÁGINA 2 — Computadores e Redes (`/pc`)

## SEO da Página `/pc`

**Meta título:** Informática e Redes em Águas de Lindóia e Monte Sião

**Meta descrição:** Montagem de computadores, redes cabeadas e wi-fi, formatação Windows/Linux e suporte técnico. Especialistas em redes para hotéis. Atendimento local, orçamento grátis.

**Open Graph — título:** Local PC & Redes — Informática e Redes em Águas de Lindóia e Monte Sião

**Open Graph — descrição:** Montagem, formatação, cabeamento de rede e wi-fi para residências, comércio, hotéis e pousadas. Consultoria de dimensionamento para cada necessidade.

**Open Graph — imagem:** foto real de cabeamento de rede organizado ou instalação de rack/hub, 1200x630, com texto alternativo descritivo.

**Palavras-chave principais desta página:** manutenção de computadores Águas de Lindóia, montagem de computador Monte Sião, rede wi-fi para hotel, crimpagem de cabo de rede, formatação Windows e Linux, rede cabeada para comércio, computador para CFTV, computador gamer sob medida.

**URL canônica:** `https://www.local.ia.br/pc`

---

## Sumário das Sections de `/pc`

| # | Section |
|---|---|
| 1 | Hero |
| 2 | Serviços |
| 3 | Especialidade: Redes para Hotéis |
| 4 | Diferenciais |
| 5 | FAQ |
| 6 | Contato Final |
| 7 | Footer (compartilhado com a Home) |

---

### 1. Hero

**Título (H1):** Computadores e Redes em Águas de Lindóia e Monte Sião

**Subtítulo:** Montagem, manutenção, cabeamento, wi-fi e redes bem dimensionadas — para residência, comércio, indústria e hotelaria. O mesmo cuidado técnico que aplicamos em CFTV, agora para toda a sua estrutura de tecnologia.

**Botões (CTA):**
- Falar agora no WhatsApp
- Pedir orçamento grátis

---

### 2. Serviços

**Título (H2):** Tudo que sua estrutura de tecnologia precisa, em um só lugar

**Montagem e manutenção de computadores**
- Montagem de computadores novos ou sob medida.
- Troca de hardware e periféricos (memória, armazenamento, fonte, placas, mouse, teclado, monitor).

**Instalação e suporte de software**
- Instalação de softwares em geral.
- Formatação e instalação de Windows e Linux.

**Cabeamento e redes**
- Crimpagem (montagem) de cabo de rede LAN RJ45.
- Teste de cabos de rede para garantir conexão estável.
- Configuração de redes Windows e Linux.
- Configuração de hub/switch de rede e wi-fi.
- Dimensionamento de rede cabeada e sem fio para residência e comércio.

**Consultoria e dimensionamento sob medida**
- Escolha do computador certo para cada uso: desktop de trabalho, servidor, computador dedicado a gravação de CFTV, computador para jogos.
- Inclui também escolha e configuração de periféricos.

---

### 3. Especialidade: Redes para Hotéis

**Título (H2):** Especialistas em rede wi-fi para hotéis e pousadas

Rede de hóspede lenta ou instável gera reclamação, avaliação ruim e cancelamento. Dimensionamos a rede wi-fi e cabeada do seu hotel ou pousada para aguentar múltiplos hóspedes conectados ao mesmo tempo, com cobertura em todas as áreas — quartos, área comum e recepção — e prioridade correta entre rede de hóspede e rede administrativa/CFTV.

*Combina diretamente com nossos serviços de CFTV para hospedagem: câmera bem instalada precisa de rede bem dimensionada para gravar e transmitir sem falha.*

---

### 4. Diferenciais

1. **Atendimento local** — mesma equipe que já atende CFTV e alarme na região.
2. **Diagnóstico antes do orçamento** — identificamos o problema real antes de vender peça ou serviço.
3. **Suporte contínuo** — não paramos no dia da instalação.
4. **Dimensionamento sob medida** — nada de vender mais rede ou mais máquina do que você precisa.

---

### 5. FAQ

**1. Vocês fazem backup dos meus arquivos antes de formatar?**
Sim, orientamos e podemos realizar backup antes de qualquer formatação, para garantir que nada se perca.

**2. Atendem empresas e não só residências?**
Sim, atendemos residências, comércio, indústria e hotelaria.

**3. Fazem rede para hotel pequeno, com poucos quartos?**
Sim, dimensionamos a rede para o tamanho real do seu negócio, de pousadas pequenas a hotéis maiores.

**4. Trabalham com Windows e Linux?**
Sim, instalamos, formatamos e configuramos rede nos dois sistemas.

**5. Montam computador para gravação de CFTV?**
Sim, dimensionamos o computador certo conforme número de câmeras, resolução e tempo de gravação necessário.

**6. Qual o prazo de um serviço de rede ou formatação?**
Depende do porte — após diagnóstico, você recebe prazo exato antes de aprovar o orçamento.

---

### 6. Contato Final

**Título (H2):** Sua estrutura de tecnologia, resolvida de uma vez

Fale agora e receba um diagnóstico e orçamento sem compromisso.

**Botões (CTA):**
- Chamar no WhatsApp: [SEU NÚMERO]
- E-mail: [SEU E-MAIL]
- Preencher formulário de orçamento gratuito

---

### 7. Footer

(idêntico ao footer da Home, incluindo link interno de volta para `/` e para os serviços de CFTV e Alarmes)

---

## Observações Finais do Editor

1. **Prioridade de link interno:** a Home deve linkar para `/pc` na section 7 (teaser), e `/pc` deve linkar de volta para a Home no footer e, se fizer sentido, dentro do bloco "Especialidade: Redes para Hotéis" (cross-sell natural com CFTV para hospedagem).
2. **Naming:** revise o nome "Local" comigo antes de aprovar — é só uma sugestão para manter coerência com o domínio `local.ia.br`.
3. **Todo número de "força bruta"** (quantidade de instalações, % de aprovação) segue como placeholder — publique só dado real.
4. Posso, a partir daqui, seguir para uma versão em HTML/artifact navegável só para você visualizar o layout (não como entrega final de código, já que isso fica com o Fable 5), ou seguir direto para outro pedido.
