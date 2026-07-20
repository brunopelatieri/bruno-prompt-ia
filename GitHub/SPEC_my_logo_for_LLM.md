## 👽 :24/06/2026

---

# Especificação de Marca — Bruno Goulart
### Documento de referência técnica para geração e composição de layout (LLM-readable)

---

## ⚡ Resumo Pareto (80/20) — leia isto primeiro

As 5 regras abaixo resolvem ~80% das decisões de design com esta marca. O restante do documento é detalhamento de apoio — consulte-o só se a regra que você precisa não estiver aqui.

1. **Cores fixas, nunca substituir:**
   - Indigo (primária/dominante) `#3C50C4`
   - Azul Claro (secundária) `#1094E4`
   - Verde-Teal (secundária, menor área) `#00CCB8`

2. **Regra de contraste / dark mode:** o wordmark Indigo só é legível (WCAG AA) em **fundo claro**. Em fundo escuro, nunca usar o wordmark Indigo — usar só o símbolo isolado, ou recolorir o texto para branco/cinza claro.

3. **Forma:** símbolo = 2 elos em formato de pílula/cápsula entrelaçados, terminações sempre em semicírculo perfeito (nunca canto quadrado). Espessura do traço = ~13–14% da altura do símbolo (proporcional, não em px fixo).

4. **Tipografia:** "Bruno Goulart" (capitalizado, com espaço). Versão horizontal/web usa fonte geométrica moderna e técnica (estilo Space Grotesk/Sora/Inter bold) — nunca fonte arredondada, lúdica ou serifada. Símbolo e texto alinhados pelo centro óptico, não pela base.

5. **Nunca fazer:** distorcer/esticar o símbolo · usar as 3 cores em proporção igual · texto Indigo em fundo escuro · cantos vivos · recriar o terceiro elo (Verde-Teal) como forma completa (ele é parcialmente oculto, por design).

📋 **Prompt pronto para copiar:** ver Seção 8.

---

## 0. Propósito deste documento

Este documento existe para ser lido por um modelo de linguagem (LLM) como **fonte de verdade** sobre a identidade visual de Bruno Goulart, antes de qualquer tarefa de geração, edição ou composição de layout que envolva a logo (sites, apresentações, banners, redes sociais, materiais de marketing, etc.).

Qualquer LLM que receber este documento como contexto deve tratá-lo como **restrição de design**, não como sugestão. Os valores de cor (hex/RGB), proporções geométricas e regras de contraste aqui descritos foram medidos diretamente dos arquivos de origem oficiais — não são estimativas visuais.

---

## 1. Identidade da marca — visão geral

**Nome da marca:** Bruno Goulart
**Setor/posicionamento:** Desenvolvimento full stack, automação com IA (AI agents), engenharia de software, DevOps.
**Conceito central do símbolo:** Dois elos/correntes entrelaçados (formas de "pílula"/cápsula arredondada), representando **conexão, integração e engenharia de sistemas conectados** — uma metáfora visual direta para automação, integração de APIs, agentes de IA conectados, e arquitetura de sistemas.

A marca possui **3 versões oficiais do arquivo-fonte**, cada uma com finalidade distinta:

| Versão | Arquivo de referência | Proporção (W:H) | Uso recomendado |
|---|---|---|---|
| Empilhada (quadrada) | `bruno_goulart_logo.png` | 1:1 | Avatar, ícone de perfil social, posts quadrados, apresentações em capa |
| Horizontal (lockup completo) | `bruno_goulart_logo_horizontal.png` | ~4.18:1 | Header/navbar de site, footer, assinatura de e-mail, papelaria horizontal |
| Símbolo isolado (sem texto) | `bruno_goulart_logo_horizontal_icon.png` | ~1.18:1 | Favicon, ícone de app, marca de água, avatar pequeno, social icon |

---

## 2. Paleta de cores oficial

Todas as cores abaixo foram extraídas por amostragem de pixel direta do arquivo-fonte original (não estimadas visualmente). Os valores RGB representam o pixel mais frequente de cada elemento — ou seja, a cor "pura" de preenchimento, sem antialiasing de borda.

### 2.1 Cores primárias

| Nome interno | Hex | RGB | HSL | Elemento que representa |
|---|---|---|---|---|
| **Indigo Bruno Goulart** | `#3C50C4` | `60, 80, 196` | `233°, 54%, 50%` | Elo central (maior, em primeiro plano) + wordmark (texto "Bruno Goulart") |
| **Azul Claro Bruno Goulart** | `#1094E4` | `16, 148, 228` | `200°, 87%, 48%` | Elo da esquerda (atrás, mais claro) |
| **Verde-Teal Bruno Goulart** | `#00CCB8` | `0, 204, 184` | `172°, 100%, 40%` | Elo da direita (atrás, parcialmente oculto pelo elo indigo) |

**Observação de hierarquia visual:** o Indigo é a cor dominante da marca — ocupa a maior área do símbolo (o elo central, que está por cima dos outros dois na composição) e é também a cor do texto. Ao criar variações ou aplicações derivadas, **o Indigo deve ser tratado como a cor primária de marca**; Azul Claro e Verde-Teal são cores secundárias/de apoio que aparecem em proporção menor.

### 2.2 Regras de uso de cor

- **Nunca alterar os valores hex acima.** Se um layout exigir uma variação de cor (ex: estado hover, opacidade, tom mais escuro para texto secundário), aplicar transparência (alpha) ou `brightness`/`shade` sobre os hex originais — nunca substituir por uma cor "parecida" arbitrária.
- **Nunca usar as 3 cores em proporções iguais.** A hierarquia visual original é: Indigo (predominante) > Azul Claro > Verde-Teal (menor área visível, pois fica parcialmente atrás do elo indigo).
- **Não introduzir uma quarta cor de marca** sem necessidade explícita. Para textos neutros, UI, backgrounds, etc., usar escala de cinza/branco/preto padrão — não inventar uma cor "complementar" à paleta.

### 2.3 Contraste e acessibilidade (WCAG 2.1)

Razões de contraste calculadas (fórmula de luminância relativa WCAG) entre cada cor de marca e fundos comuns:

| Cor | Sobre branco `#FFFFFF` | Sobre preto `#000000` | Sobre cinza claro `#F5F5F5` | Sobre cinza escuro `#0A0A0A` |
|---|---|---|---|---|
| Indigo `#3C50C4` | 6.69:1 ✅ AA | 3.14:1 ❌ | 6.14:1 ✅ AA | 2.96:1 ❌ |
| Azul Claro `#1094E4` | 3.29:1 ❌ | 6.38:1 ✅ AA | 3.02:1 ❌ | 6.01:1 ✅ AA |
| Verde-Teal `#00CCB8` | 2.03:1 ❌ | 10.33:1 ✅ AA | 1.86:1 ❌ | 9.74:1 ✅ AA |

*(✅ AA = atende ao mínimo WCAG AA de 4.5:1 para texto normal)*

**Diretrizes derivadas, para qualquer LLM compondo layout:**

1. **A marca foi originalmente desenhada para fundos claros.** O Indigo (cor do texto/wordmark) só atinge contraste acessível (AA) sobre fundos claros (branco/cinza claro). Sobre fundos escuros/pretos, o Indigo **fica com contraste insuficiente para texto** (3.14:1 e 2.96:1 — abaixo do mínimo de 4.5:1).
2. **Em dark mode, não usar o Indigo como cor de texto/wordmark.** Se for necessário aplicar a logo sobre fundo escuro, usar a versão do símbolo isolado (ícone) ou recolorir o wordmark para branco/cinza claro — nunca deixar o wordmark indigo sobre fundo preto/escuro, pois fica com legibilidade comprometida.
3. **Azul Claro e Verde-Teal têm comportamento espelhado**: ótimos sobre fundo escuro, ruins sobre fundo claro. Isso já é resolvido naturalmente no símbolo porque o Indigo (elo central) é o elemento que fica por cima e mais perto da leitura — mas vale considerar se algum desses tons isolados (ex: usar só o Verde-Teal num botão) for cogitado: ele não deve ser usado como texto sobre fundo branco.

---

## 3. Geometria e proporções do símbolo

Medições feitas diretamente sobre o arquivo de origem em alta resolução (1563×1563px).

### 3.1 Conceito de forma

- O símbolo é composto por **2 formas de "pílula" (stadium/pill shape — retângulo com extremidades semicirculares)**, dispostas na diagonal e entrelaçadas (uma passa "por dentro" do espaço vazio da outra, criando um efeito de elo de corrente / link).
- Uma **terceira forma de pílula** (Verde-Teal) aparece parcialmente atrás do elo indigo — só sua extremidade superior direita é visível, sugerindo um terceiro elo da corrente que continua "por trás" da composição. Esse terceiro elemento é parcialmente oculto, não uma forma completa visível.
- O elo Indigo é o de maior dimensão e fica visualmente em primeiro plano, cruzando por cima do elo Azul Claro.

### 3.2 Proporções medidas

| Métrica | Valor medido | Proporção relativa |
|---|---|---|
| Espessura do traço (stroke) de cada elo | ~75–85px | ~13.5% da altura total do símbolo |
| Raio das extremidades arredondadas | ~40px | ~50% da espessura do traço (semicírculo perfeito — não é um *border-radius* parcial, é uma cápsula/stadium-shape completa) |
| Altura do símbolo (bbox) | 591px | referência-base |
| Largura do símbolo (bbox) | 702px | ~1.19 × altura |
| Altura do wordmark (texto) | 125px | ~21% da altura do símbolo |
| Espaço vertical entre símbolo e wordmark (versão empilhada) | 53px | ~9% da altura do símbolo |

**Regra de proporção para redimensionamento:** ao escalar o símbolo para qualquer tamanho, a espessura do traço deve sempre ser recalculada como **~13–14% da altura total do símbolo**, nunca um valor fixo em pixels. Isso garante que o símbolo continue legível tanto em favicon (16px) quanto em banner grande (>2000px).

### 3.3 Estilo de extremidade (terminação das formas)

As pontas de cada elo são **semicírculos perfeitos** (capsule/stadium shape), não cantos quadrados nem `border-radius` parcial. Esse é um elemento de identidade visual relevante: a marca usa exclusivamente formas com terminações totalmente arredondadas — nenhum elemento da marca (símbolo ou tipografia) deve introduzir cantos vivos/quadrados que contrastem com esse princípio.

---

## 4. Tipografia

### 4.1 Wordmark — versão original (empilhada/quadrada)

- Estilo: sans-serif geométrica, arredondada, amigável, capitalização própria: **"Bruno Goulart"** (nome e sobrenome com inicial maiúscula e espaço).
- Peso: bold/semibold.
- Cor: Indigo `#3C50C4` (mesma cor do elo central do símbolo).
- Contexto de uso: adequado para formatos verticais/empilhados onde o texto funciona como legenda abaixo do símbolo (ex: avatar, post quadrado, capa).

### 4.2 Wordmark — versão horizontal (lockup para web)

Para a versão horizontal (header/navbar/footer), a tipografia foi **intencionalmente evoluída** em relação à versão original, para refletir melhor o posicionamento técnico da marca (AI agents, automação, engenharia, DevOps):

- Estilo: sans-serif geométrica/semi-geométrica, moderna, mais técnica e "engenheirada" — sem o caráter lúdico/arredondado da versão original.
- Capitalização: **"Bruno Goulart"** (nome próprio com inicial maiúscula e espaço), mantendo a mesma convenção de capitalização da versão original — apenas o estilo da fonte muda entre as duas versões, não a capitalização.
- Cor: mantém o Indigo `#3C50C4`, sem alteração.
- Alinhamento: símbolo e wordmark compartilham uma **linha de centro óptico comum** (não apenas a mesma linha de base/baseline) — ou seja, o conjunto deve ser tratado como um lockup único e coeso, não como dois elementos posicionados lado a lado de forma independente.

**Diretriz para LLM:** ao gerar ou ajustar qualquer wordmark da marca, priorizar fontes geométricas sans-serif com caráter técnico/preciso (ex.: família de fontes do tipo Space Grotesk, Sora, General Sans, Inter com peso bold, ou equivalentes) — evitar fontes arredondadas, lúdicas, manuscritas, ou serifadas. A tipografia deve comunicar precisão e engenharia, alinhada ao posicionamento de IA/automação/DevOps.

---

## 5. Espaço de respiro (clear space) e área de proteção

- Manter sempre uma margem de respiro mínima ao redor do lockup completo (símbolo + texto) equivalente a, no mínimo, **a altura de um elo do símbolo** (ou ~15–20% da altura total do logotipo) — não posicionar outros elementos gráficos, textos ou bordas de container colados diretamente na logo.
- No símbolo isolado (versão ícone/favicon), manter respiro proporcional semelhante para evitar que as extremidades arredondadas dos elos pareçam "cortadas" pela borda do container, especialmente em contextos de ícone circular (ex: avatar redondo de redes sociais, ícone de app no iOS/Android).

---

## 6. Regras de fundo e aplicação

- **Fundo padrão/preferencial:** branco ou claro. É o contexto em que todas as 3 cores e o wordmark indigo atingem contraste adequado simultaneamente.
- **Fundo escuro:** aceitável **apenas para o símbolo isolado** (ícone), já que Azul Claro e Verde-Teal têm excelente contraste sobre fundo escuro/preto. Evitar o wordmark Indigo sobre fundo escuro (ver seção 2.3).
- **Nunca aplicar a logo sobre fundos fotográficos ou com ruído visual** sem uma camada de proteção (overlay, container sólido, ou drop shadow sutil) — as cores da marca, especialmente o Verde-Teal e o Azul Claro, podem se misturar visualmente com fundos complexos de tonalidade semelhante (azuis, verdes, ciano).
- **Transparência:** os arquivos de origem oficiais usam canal alpha real (true transparency) — qualquer arquivo derivado deve preservar transparência real (RGBA com alpha variável), nunca simular transparência com um padrão xadrez desenhado como pixel sólido.

---

## 7. O que NUNCA fazer com esta marca

1. Não alterar os valores hex/RGB das 3 cores oficiais.
2. Não mudar a proporção de área entre as 3 cores (Indigo deve permanecer dominante).
3. Não usar o wordmark Indigo sobre fundo escuro ou preto.
4. Não introduzir cantos quadrados/vivos em qualquer elemento do símbolo ou variações dele.
5. Não separar simbolo e wordmark sem alinhamento de centro óptico compartilhado, na versão horizontal.
6. Não usar fontes arredondadas/lúdicas/manuscritas na versão horizontal (web) — reservado apenas à versão original empilhada, se necessário.
7. Não comprimir, esticar ou distorcer desproporcionalmente o símbolo (manter proporção largura:altura de ~1.19:1 no símbolo isolado).
8. Não recriar a "terceira pílula" (Verde-Teal) como uma forma completa e totalmente visível — ela é, por design, parcialmente oculta atrás do elo indigo.

---

## 8. Resumo rápido para prompts de geração de imagem (IA generativa)

Bloco de referência compacto, para colar diretamente em prompts de geração/edição de imagem quando a logo precisar ser referenciada:

```
Brand colors (do not alter):
- Indigo (primary, dominant): #3C50C4
- Light blue (secondary): #1094E4
- Teal/green (secondary, smallest visible area): #00CCB8

Symbol: two interlocking capsule/stadium shapes (pill shapes with fully 
rounded semicircular ends) arranged diagonally, link/chain metaphor. 
A third teal capsule is partially hidden behind the indigo loop 
(only its top-right end is visible). Stroke thickness ≈ 13-14% of 
symbol height. No sharp corners anywhere.

Wordmark (horizontal/web version): "Bruno Goulart", proper capitalization, 
geometric modern sans-serif font with a technical/engineered character 
(AI/automation/DevOps positioning) — not rounded or playful. Color: 
same indigo #3C50C4. Aligned to shared optical center with the symbol, 
not just shared baseline.

Background rule: indigo wordmark requires light/white background for 
adequate contrast. Do not place indigo text on dark backgrounds.
```

---

## 9. Metadados do documento

| Campo | Valor |
|---|---|
| Marca | Bruno Goulart |
| Domínio | brunogoulart.com.br |
| Arquivos-fonte analisados | `bruno_goulart_logo.png` (1563×1563, RGBA), `bruno_goulart_logo_horizontal.png` (2015×482, RGBA), `bruno_goulart_logo_horizontal_icon.png` (714×604, RGBA) |
| Método de extração de cor | Amostragem direta de pixel + clustering de frequência sobre canal alpha >200 (pixels totalmente opacos) |
| Método de cálculo de contraste | Fórmula de luminância relativa WCAG 2.1 |
| Versão do documento | 1.0 |
