## 1. Paleta de cores (extraída por análise de pixels do PNG)

| Cor | Hex | Uso na imagem original | Papel sugerido no site |
|---|---|---|---|
| 🟨 **Âmbar/Dourado** | `#FFC400` | Janela, fundo dos dois módulos de ícone | **Cor primária/CTA** — botões, links, ícones de destaque, hover |
| ⬛ **Preto Grafite** | `#141514` | Telhado, paredes, chaminé (contorno da casa) | **Cor secundária/estrutura** — header, footer, textos principais, fundo escuro de seções |
| ⬜ **Cinza Ardósia** | `#787978` | Porta | **Cor neutra** — textos secundários, bordas, ícones inativos |
| 🟡 **Creme Dourado (glow)** | `#FFEBAB` | Luz saindo da porta | **Cor de apoio/fundo claro** — seções alternadas, backgrounds suaves, degradês a partir do âmbar |
| ⬜ **Branco** | `#FFFFFF` | Ícones da câmera e das ferramentas | **Fundo principal** — texto sobre fundo escuro, espaços em branco (whitespace) |

**Gradiente de destaque (brilho da porta):** transição de `#FFFFFF` → `#FFC400`, útil para hero sections, glows e botões com leve gradiente radial.
 
**Sugestão de uso (regra 60-30-10):**
- 60% Branco `#FFFFFF` (fundos, respiro visual)
- 30% Preto Grafite `#141514` (textos, header/footer, contraste)
- 10% Âmbar `#FFC400` (CTAs, ícones, destaques) — com `#FFEBAB` como tom de apoio em degradês/hover


### Variáveis prontas (CSS)
```css
:root {
  --color-primary: #FFC400;   /* amarelo - CTA e destaque */
  --color-dark: #141514;      /* preto - base/estrutura */
  --color-light: #FFFFFF;     /* branco - fundo */
  --color-neutral: #787978;   /* cinza - textos de apoio */
}
```

---

## 2. Leitura do logo

O ícone representa uma **casa** (silhueta preta, telhado em destaque) com três elementos internos:
- 📷 **Câmera de segurança** (bloco amarelo, esquerda) → segurança/monitoramento residencial
- 🚪 **Porta com brilho quente** (cinza + glow) → acesso, entrada, "portas abertas", atendimento
- 🔧 **Ferramentas (chave de fenda + chave inglesa)** (bloco amarelo, direita) → manutenção, instalação, serviços técnicos

O ícone representa uma **casa em corte transversal**, revelando três elementos internos:
 
- **Câmera de segurança** (módulo esquerdo) → serviço de **monitoramento/segurança residencial**
- **Porta aberta e iluminada** (módulo central) → sensação de **acolhimento, confiança e "portas abertas"**
- **Chave de fenda + chave inglesa cruzadas** (módulo direito) → serviço de **manutenção/reparos elétricos e gerais**
- **Janela em grade 2×2** no telhado → reforça o formato "casa" e serve como elemento decorativo repetível (padrão de marca)
- **Chaminé** → detalhe que reforça a silhueta residencial


IDENTIDADE VISUAL (usar exatamente estas cores):
- Primária (CTA/destaques): #FFC400
- Secundária (estrutura/texto): #141514
- Neutra (textos secundários/bordas): #787978
- Apoio (fundos claros/degradês): #FFEBAB
- Base (fundo principal): #FFFFFF

PALETA:
- Cor primária (destaque/CTA): #FFC400 (amarelo dourado)
- Cor de base (fundo escuro/header/footer): #141514 (preto grafite)
- Fundo claro: #FFFFFF
- Cor neutra secundária (textos de apoio, bordas): #787978

ESTILO:
- Visual moderno, confiável e técnico, com contraste forte entre preto e amarelo
- Ícones sólidos e geométricos (flat design), sem gradientes pesados
- CTAs em amarelo (#FFC400) sobre fundo escuro (#141514) ou branco
- **Direto e confiável** — fala de segurança e manutenção da casa das pessoas, exige clareza e credibilidade
- **Próximo, não corporativo-frio** — o "glow" da porta sugere acolhimento, não apenas tecnicidade
- Palavras-chave de tom: *proteção, confiança, resposta rápida, especialista, tranquilidade, 24h*
  
## 4. Tipografia sugerida (opcional)
Fonte da logo Russo_One
Font path em: public/font/RussoOne-Regular.ttf

Combinações que funcionam bem com a paleta preto/amarelo/cinza:
- **Títulos:** uma fonte geométrica e robusta, transmitindo solidez (ex.: *Poppins*, *Montserrat* ou *Sora*, peso 600–700)
- **Corpo de texto:** fonte de alta legibilidade (ex.: *Inter*, *Work Sans* ou *Roboto*, peso 400–500)
- Evitar serifadas clássicas — o ícone tem apelo técnico/moderno, não tradicional

- Tom de voz: direto, técnico e confiável — foco em segurança e tranquilidade para o cliente e serviços realizados com confiança e qualidade
- Favicon/logo: casa estilizada em preto com detalhe em amarelo (ver favicon.svg em anexo)

local do favicon.ico na raiz do site

local das images:
public/images/

Logo HMan:
 - retangular - principal para o site header: hman_logo_rectangular.webp
 - quadrada - caso precise utilizar: hman_logo_square.webp
 - og-image: og-image.web

Images Banners página CFTV:
hman_cftv_servicos_instalacao_banner.webp
hman_cftv_servicos_instalacao_banner_1.webp

Images Banners página Marido de Aluguel:
hman_marido_aluguel_servicos_instalacao_banner.webp
hman_marido_aluguel_servicos_instalacao_banner_1.webp

Images Banners página Elétrica:
hman_eletrica_servicos_instalacao_banner.webp
hman_eletrica_servicos_instalacao_banner_1.webp

Images Banners página Computadores/PC:
hman_computadores_redes_servicos_instalacao_banner.webp
hman_computadores_redes_servicos_instalacao_banner_1.webp