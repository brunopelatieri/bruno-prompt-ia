## 👽 :20/06/2026


---

# Prompt principal (cole exatamente assim no Nano Banana / Gemini junto com a imagem)

```
Remove the background from this image completely. Keep the main subject 100% unchanged — same pose, same colors, same lighting, same proportions, same details, no retouching, no smoothing, no style changes.

Requirements:
- Output a PNG with a fully transparent background (alpha channel), not white or gray.
- Cut around the subject with clean, precise edges. Preserve fine details exactly as they are: hair strands, fur, fabric texture, jagged or thin edges, semi-transparent areas (like glass, smoke, or sheer fabric) — keep partial transparency where the original had it, do not hard-cut these areas.
- Do not leave any halo, fringing, color bleed, or leftover background pixels around the edges.
- Do not crop, resize, stretch, or reposition the subject. Keep the original resolution and aspect ratio.
- Do not add shadows, reflections, outlines, or any new background elements.
- Do not alter skin tone, color grading, exposure, or sharpness of the subject.
- Export at the highest possible resolution and quality, no compression artifacts.

The only change allowed is: background removed, everything else pixel-faithful to the original.
```

### Por que cada trecho existe (pra você poder calibrar):

- **"Keep the main subject 100% unchanged"** → o erro mais comum do Nano Banana é "melhorar" a imagem sem você pedir (suaviza pele, muda cor, recompõe luz). Essa linha bloqueia isso.
- **"fully transparent... not white or gray"** → modelos de imagem às vezes confundem "remover fundo" com "fundo branco". Isso especifica alpha channel de forma explícita.
- **"hair strands, fur... semi-transparent areas... keep partial transparency"** → é onde 90% das remoções de fundo falham (cabelo, pelo, vidro, tecido fino). Sem essa instrução, o modelo faz um corte "duro" tipo silhueta.
- **"no halo, fringing, color bleed"** → evita aquela bordinha esbranquiçada/acinzentada que sobra do fundo antigo.
- **"Do not crop, resize, stretch, reposition"** → trava enquadramento, porque alguns modelos "recompõem" a imagem ao editar.
- **"highest possible resolution... no compression artifacts"** → empurra pra melhor qualidade de export.

---

## Se você quiser, me manda a imagem (ou só descreve ela)

Eu adapto esse prompt pro caso específico — por exemplo:
- Se for **pessoa com cabelo solto** → eu reforço a parte de fios individuais.
- Se for **produto com reflexo/vidro/metal** → eu adiciono instrução pra preservar reflexos do próprio objeto sem fundo.
- Se for **animal com pelo** → ajusto a linguagem de "fur edges" com mais peso.
- Se a imagem já tiver fundo simples (estúdio, cor sólida) → posso simplificar o prompt, já que o risco de erro é menor.

Quer mandar a imagem pra eu calibrar, ou seguir com esse prompt genérico mesmo?

---

# Prompt Persona for Nano Banana Gemini -> Use on Claude ou GPT

Você é um prompt engineer AI especialista em nano banana Gemini. Você é capaz de escrever prompt que alcançam 99% de assertividade no resultado final de geração e ajustes de imagens no nano bananaGemini.