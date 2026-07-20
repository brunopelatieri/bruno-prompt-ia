# local.ia.br — Páginas 3 e 4: Elétrica e Marido de Aluguel
### + Header/Footer padrão do site + instruções atualizadas para o Agente de IA (Fable 5)

Este documento **complementa** o anterior (`local-ia-br-conteudo-e-seo.md`, que já cobre Home/CFTV e a página `/pc`). Aqui não repito o conteúdo das páginas 1 e 2 — só adiciono as páginas 3 e 4, formalizo o Header e Footer únicos (pedido explícito desta rodada) e atualizo o mapa do site para 4 páginas. Texto puro, sem HTML/CSS — tudo abaixo é conteúdo e instrução para o Fable 5 implementar.

---

## Nota do Editor

Duas decisões de conteúdo que tomei aqui, para você validar:

1. **Região ampliada para essas 2 páginas novas.** Elétrica e Marido de Aluguel são serviços de raio de atendimento mais amplo que instalação especializada de CFTV — por isso usei como foco **Conchal e região de Campinas (Circuito das Águas Paulista: Águas de Lindóia, Lindóia, Serra Negra, Socorro)**, mantendo Monte Sião/MG e Itapira como atendimento também coberto, mas em segundo plano nessas duas páginas específicas. Os preços que você mandou já são os que estou publicando como oferta real (não usei placeholder de preço, só nos números de "prova social" tipo "+X atendimentos").
2. **A marca "Local" faz ainda mais sentido agora.** Com CFTV, Alarme, PC/Redes, Elétrica e Marido de Aluguel no mesmo site, "Local" deixou de ser só um nome e virou literalmente o conceito: **"Local — serviços para sua casa e seu negócio"**. Usei esse tagline no header padrão abaixo.

---

## Instruções Atualizadas para o Agente de IA (Fable 5)

**O site agora tem 4 rotas.** Header e footer devem ser **componentes únicos e compartilhados**, renderizados em todas as rotas — não duplique o markup por página. Só o conteúdo central (`main`) muda entre rotas.

- `/` — Home (CFTV e Alarmes)
- `/pc` — Computadores e Redes
- `/eletrica` — Elétrica Residencial e Comercial
- `/marido-de-aluguel` — Marido de Aluguel / Reparos Gerais

Mantêm-se todas as instruções técnicas de SEO já passadas no documento anterior (metadados por rota, dados estruturados, semântica de heading única por página, sitemap.xml com todas as rotas, performance). Reforçando o que passa a valer com 4 páginas:

- O **header** deve ter navegação para as 4 rotas, com o item da rota atual marcado como ativo (estado visual e semântico, ex: atributo de página atual em navegação — sem eu especificar código, você decide a implementação).
- O **footer** deve repetir os links das 4 rotas, mais a área de atendimento consolidada (todas as cidades citadas nas 4 páginas).
- Cada uma das 4 páginas deve ter link interno para pelo menos uma outra página relevante dentro do corpo do texto (não só no header/footer) — ex: a página de Elétrica pode linkar para Marido de Aluguel quando fizer sentido ("para reparos que não são elétricos, veja nossos serviços de Marido de Aluguel"), e vice-versa.
- Adicione as 2 novas rotas ao `sitemap.xml` e aos dados estruturados de área de atendimento.
- Nas páginas de Elétrica e Marido de Aluguel, cada tabela de preços deve ser implementada de forma responsiva (em card empilhado no mobile, não tabela horizontal com scroll forçado) — isso é requisito de usabilidade que afeta SEO mobile-first.

---

## Mapa do Site (atualizado — 4 páginas)

| Rota | Página | Foco |
|---|---|---|
| `/` | Home — Local Segurança | CFTV, alarmes, 6 cidades do Circuito das Águas + Monte Sião |
| `/pc` | Computadores e Redes | Hardware, software, redes, especialidade em hotéis |
| `/eletrica` | Elétrica | Serviços elétricos residenciais/comerciais de pequeno porte, região de Campinas |
| `/marido-de-aluguel` | Marido de Aluguel | Reparos gerais, fixações, hidráulica leve, região de Campinas |

---

## Header Padrão do Site (todas as páginas)

**Marca:** Local
**Tagline (usar em telas menores/rodapé, se não couber no header):** Serviços para sua casa e seu negócio

**Navegação:**
- Início
- Computadores e Redes
- Elétrica
- Marido de Aluguel

**Botão de ação fixo no header:** Falar no WhatsApp

---

## Footer Padrão do Site (todas as páginas)

**Local — Serviços para sua casa e seu negócio**
CFTV e alarmes, computadores e redes, elétrica e reparos gerais — instalação, manutenção e suporte contínuo.

**Navegação (repetida):** Início · Computadores e Redes · Elétrica · Marido de Aluguel

**Área de atendimento:**
Águas de Lindóia/SP · Monte Sião/MG · Lindóia/SP · Serra Negra/SP · Socorro/SP · Itapira/SP · Conchal/SP · Região de Campinas/SP

**Contato:** [SEU TELEFONE] · [SEU E-MAIL] · CNPJ: [SEU CNPJ]

**Redes sociais:** [Instagram] · [WhatsApp] · [Facebook]

**Legal:** [Política de Privacidade] · [Termos de Uso]

© [ANO] Local. Todos os direitos reservados.

---

# PÁGINA 3 — Elétrica (`/eletrica`)

## SEO da Página Elétrica

**Meta título:** Eletricista Residencial e Comercial em Campinas e Região

**Meta descrição:** Serviços de elétrica residencial e comercial de pequeno porte: tomadas, disjuntores, chuveiro, iluminação e mais. Atendimento em Conchal, Campinas e Circuito das Águas Paulista. Orçamento rápido.

**Open Graph — título:** Local Elétrica — Serviços Elétricos em Conchal, Campinas e Região

**Open Graph — descrição:** Do reparo pontual à instalação completa. Elétrica residencial e comercial com segurança, normas técnicas e preço claro por serviço.

**Open Graph — imagem:** foto real de um quadro de disjuntores organizado ou de uma instalação elétrica concluída, 1200x630, com texto alternativo descritivo.

**Palavras-chave principais:** eletricista Conchal, eletricista Campinas, eletricista Águas de Lindóia, troca de disjuntor, instalação de tomada, quadro de disjuntores, instalação de chuveiro elétrico, eletricista comercial pequeno porte.

**URL canônica:** `https://www.local.ia.br/eletrica`

---

## Sumário das Sections de Elétrica

| # | Section |
|---|---|
| 1 | Hero |
| 2 | Confiança e Segurança (normas, EPI, ART) |
| 3 | Iluminação |
| 4 | Tomadas, Interruptores e Pontos de Rede |
| 5 | Quadro de Disjuntores, Proteção e Laudos |
| 6 | Chuveiro, Torneira Elétrica e Aquecimento |
| 7 | Ventiladores e Exaustores |
| 8 | Diagnóstico e Reparo |
| 9 | Infraestrutura Nova e Organização |
| 10 | Formas de Cobrança |
| 11 | FAQ |
| 12 | Contato Final |

---

### 1. Hero

**Título (H1):** Eletricista Residencial e Comercial em Conchal, Campinas e Região

**Subtítulo:** De uma lâmpada trocada a um quadro de disjuntores novo — serviço elétrico com preço claro, segurança e atendimento rápido em Conchal, Campinas e todo o Circuito das Águas Paulista.

**Selo de credibilidade:** Preço por serviço, sem letra miúda — você sabe o que vai pagar antes de fecharmos.

**Botões (CTA):**
- Falar agora no WhatsApp
- Ver tabela de serviços e preços

---

### 2. Confiança e Segurança

**Título (H2):** Trabalho elétrico não é lugar para economizar em segurança

Todo atendimento é feito com uso de EPI (equipamento de proteção individual), seguindo as normas técnicas da ABNT (NBR 5410 para instalações elétricas de baixa tensão) e, quando o serviço exige, com emissão de ART (Anotação de Responsabilidade Técnica) por profissional habilitado. Instalação elétrica malfeita não é só risco de defeito — é risco de incêndio e choque. Fazemos direito da primeira vez.

---

### 3. Iluminação

**Título (H2):** Iluminação para casa, loja e comércio

| Serviço | O que está incluso | Valor (mão de obra) |
|---|---|---|
| Troca de lâmpada comum | Substituição da lâmpada queimada, teste de soquete e tensão, limpeza leve da luminária | R$ 30–40 por ponto |
| Troca de lâmpada fluorescente | Retirada da tubular antiga, checagem de reator/soquete, instalação e teste | R$ 40–50 por ponto |
| Conversão para LED | Remoção do reator, adaptação da fiação conforme fabricante, instalação e teste | R$ 40–80 por ponto |
| Instalação de luminária simples | Fixação da base, ligação na caixa de passagem, acabamento e teste | R$ 70–120 por peça |
| Instalação de lustre/pendente | Montagem, reforço de fixação no teto, ligação, ajuste de altura | R$ 120–250 por peça |
| Instalação de plafon/spot embutido | Furação ou aproveitamento de recorte existente, fixação, ligação e teste | R$ 80–180 por ponto |
| Instalação de refletor externo | Fixação em parede/mastro, passagem de cabo, ligação com sensor/comando | R$ 150–300 por ponto |
| Iluminação de jardim | Montagem de luminárias baixas, cabos protegidos, ligação a circuito ou temporizador | R$ 200–600 por área |
| Instalação de sensor de presença | Fixação, ajuste de tempo/alcance, ligação na iluminação, teste | R$ 90–180 por unidade |

---

### 4. Tomadas, Interruptores e Pontos de Rede

**Título (H2):** Tomadas e interruptores, feitos com segurança e testados na hora

| Serviço | O que está incluso | Valor (mão de obra) |
|---|---|---|
| Troca/instalação de interruptor simples | Desenergizar o circuito, remoção do antigo, ligação correta, teste | R$ 40–60 por unidade |
| Interruptor paralelo/three-way | Adequação de fiação entre caixas, instalação e teste em múltiplos pontos | R$ 80–150 por circuito |
| Troca/instalação de tomada 110/220V | Checagem de bitola, aterramento e tensão, ligação correta, teste com carga | R$ 40–70 por unidade |
| Tomada dupla/múltipla | Troca de suporte/espelho, adequação de fiação, teste de todos os encaixes | R$ 60–90 por unidade |
| Tomada de rede (RJ45) — ponto físico | Crimpagem de cabo, montagem da tomada, teste de conexão | R$ 60–100 por ponto |
| Ponto de rede completo (passagem de cabo) | Passagem por conduíte/aparente, fixação, terminação nas duas pontas, teste | R$ 90–180 por ponto |

*Este é o ponto físico/infraestrutura do cabo de rede. Para configuração de rede, wi-fi e testes avançados de conexão, veja nossa página de [Computadores e Redes](/pc).*

---

### 5. Quadro de Disjuntores, Proteção e Laudos

**Título (H2):** O coração da sua instalação elétrica

| Serviço | O que está incluso | Valor (mão de obra) |
|---|---|---|
| Troca de disjuntor | Desenergizar o quadro, remoção do antigo, instalação, aperto de conexões, teste | R$ 60–100 por unidade |
| Instalação de novo disjuntor no quadro | Adequação do barramento, ligação do novo circuito, identificação em legenda | R$ 75–150 por unidade |
| Montagem/troca de quadro completo | Avaliação de carga, montagem do quadro novo, transferência de circuitos, teste geral | R$ 400–900 (ou sob orçamento) |
| Instalação de DR/DPS | Instalação de proteção diferencial/contra surtos, ajuste de ligações, teste | R$ 250–600 por quadro |
| Mini quadro para área externa | Montagem de quadro com disjuntores/DR para quintal ou área gourmet | R$ 350–800 por quadro |
| Laudo simples de verificação | Visita, inspeção visual, relatório com recomendações (sem ART) | R$ 200–450 por imóvel |

---

### 6. Chuveiro, Torneira Elétrica e Aquecimento

**Título (H2):** Água quente com segurança elétrica de verdade

| Serviço | O que está incluso | Valor (mão de obra) |
|---|---|---|
| Instalação de chuveiro elétrico | Checagem de bitola, disjuntor exclusivo, aterramento, fixação, teste de aquecimento | R$ 90–180 por unidade |
| Troca de resistência de chuveiro | Desligar chave geral, abertura, troca conforme modelo, remontagem e teste | R$ 70–120 por unidade |
| Instalação de torneira elétrica | Fixação, ligação elétrica segura, teste de aquecimento | R$ 100–200 por unidade |
| Instalação de aquecedor elétrico pequeno | Fixação, ligação conforme manual, teste de aquecimento e segurança | R$ 200–400 por unidade |

---

### 7. Ventiladores e Exaustores

**Título (H2):** Circulação de ar bem instalada

| Serviço | O que está incluso | Valor (mão de obra) |
|---|---|---|
| Instalação de ventilador de teto | Fixação da base, montagem de pás/motor, ligação, teste de rotação e ruído | R$ 150–300 por unidade |
| Troca de ventilador de teto | Remoção do antigo, aproveitamento do ponto, instalação e teste | R$ 120–250 por unidade |
| Instalação de exaustor (banheiro/cozinha) | Fixação, ligação elétrica, duto se necessário, teste de fluxo de ar | R$ 150–300 por unidade |

---

### 8. Diagnóstico e Reparo

**Título (H2):** Quando algo já deu problema

| Serviço | O que está incluso | Valor (mão de obra) |
|---|---|---|
| Reparo de curto em tomada/ponto de luz | Diagnóstico, identificação do curto/fio solto, substituição do componente, teste | R$ 120–250 por chamado |
| Revisão de fiação em ambiente | Abertura de caixas, verificação de emendas, troca pontual de fios danificados | R$ 250–600 por ambiente |
| Adequação de tensão 110/220V | Verificação da rede, reconfiguração de ligações, troca de tomadas/disjuntores se necessário | R$ 180–450 por circuito |

---

### 9. Infraestrutura Nova e Organização

**Título (H2):** Ponto novo ou estrutura organizada

| Serviço | O que está incluso | Valor (mão de obra) |
|---|---|---|
| Nova tomada/ponto de luz (infraestrutura) | Rasgo/furação, caixa de embutir ou sobrepor, fiação, ligação no quadro | R$ 250–600 por ponto (sem material) |
| Instalação de nobreak em estação de trabalho | Checagem de potência, ligação entre tomada e equipamentos, organização de cabos | R$ 80–180 por ponto |
| Filtro de linha / organização de cabos | Instalação, etiquetagem, organização com abraçadeiras, orientação de carga máxima | R$ 60–120 por ponto |

---

### 10. Formas de Cobrança

- **Visita técnica com pequeno reparo:** ideal para 1–2 itens simples (ex: trocar lâmpada, trocar tomada). Faixa: R$ 80–200.
- **Hora técnica:** para diagnóstico ou lista de pequenos reparos na casa/comércio todo. Faixa: R$ 50–120/hora.

*Materiais (fios, disjuntores, luminárias, etc.) são cobrados à parte, sempre informados no orçamento antes de iniciar.*

---

### 11. FAQ

**1. Vocês emitem ART?**
Sim, quando o serviço exige — informamos antes se o seu caso precisa.

**2. O material está incluso no preço?**
Não, os valores são de mão de obra. Material é orçado à parte e você aprova antes de comprarmos.

**3. Atendem urgência (sem luz, curto-circuito)?**
Sim, priorizamos chamados de risco (curto, cheiro de queimado, sem energia total).

**4. Fazem serviço em comércio, não só residência?**
Sim, atendemos lojas, pequenos comércios e escritórios.

**5. Qual a região de atendimento?**
Conchal, Campinas e região, incluindo o Circuito das Águas Paulista (Águas de Lindóia, Lindóia, Serra Negra, Socorro), além de Monte Sião/MG e Itapira/SP.

---

### 12. Contato Final

**Título (H2):** Elétrica bem feita não é gasto, é prevenção

Fio solto, tomada quente e disjuntor que desarma sozinho são avisos — não espere virar problema maior.

**Botões (CTA):**
- Chamar no WhatsApp: [SEU NÚMERO]
- Pedir orçamento pela tabela de serviços

---

## Sugestões de Imagens — Elétrica

Buscar manualmente no Google Imagens com estes termos:
- "quadro de disjuntores residencial organizado"
- "eletricista instalando tomada"
- "instalação de chuveiro elétrico fiação"
- "instalação de ventilador de teto"
- "instalação de spot embutido gesso"
- "disjuntor DR DPS quadro elétrico"
- "eletricista com EPI trabalhando"

---

# PÁGINA 4 — Marido de Aluguel (`/marido-de-aluguel`)

## SEO da Página Marido de Aluguel

**Meta título:** Marido de Aluguel em Campinas e Região — Reparos Gerais

**Meta descrição:** Montagem de móveis, fixações, hidráulica leve, pintura e pequenos reparos. Marido de aluguel em Conchal, Campinas e Circuito das Águas Paulista. Peça seu orçamento.

**Open Graph — título:** Local Reparos — Marido de Aluguel em Conchal, Campinas e Região

**Open Graph — descrição:** Aquela lista de pequenos reparos que fica sempre para depois? Resolvemos tudo numa visita só — fixações, hidráulica leve, móveis, pintura e mais.

**Open Graph — imagem:** foto real de instalação de suporte de TV ou montagem de móvel concluída, 1200x630, com texto alternativo descritivo.

**Palavras-chave principais:** marido de aluguel Campinas, marido de aluguel Conchal, montagem de móveis, instalação de suporte de TV, troca de torneira, reparos residenciais, marido de aluguel Águas de Lindóia.

**URL canônica:** `https://www.local.ia.br/marido-de-aluguel`

---

## Sumário das Sections de Marido de Aluguel

| # | Section |
|---|---|
| 1 | Hero |
| 2 | O Pacote Marido de Aluguel |
| 3 | Fixações e Montagens |
| 4 | Portas e Fechaduras |
| 5 | Pintura e Acabamento |
| 6 | Hidráulica Leve |
| 7 | Instalação de Eletrodomésticos |
| 8 | Formas de Cobrança |
| 9 | FAQ |
| 10 | Contato Final |

---

### 1. Hero

**Título (H1):** Marido de Aluguel em Conchal, Campinas e Região

**Subtítulo:** Aquela lista de pequenos reparos que vive adiada — prateleira, suporte de TV, torneira pingando, porta que emperra. Resolvemos tudo numa visita só, com preço claro por serviço.

**Botões (CTA):**
- Falar agora no WhatsApp
- Ver pacote de reparos

---

### 2. O Pacote Marido de Aluguel

**Título (H2):** Não precisa chamar um profissional diferente para cada coisa

**Pacote de divulgação:** até 2 horas de serviços diversos (elétrica leve, hidráulica leve, instalações na parede), cobrindo até 5 tarefas pequenas — a partir de **R$ 180 + materiais**.

Ideal para quem tem aquela listinha: 1 prateleira, 1 torneira, 1 quadro na parede, 1 dobradiça ajustada — tudo numa visita só, sem pagar deslocamento e diagnóstico separado para cada item.

---

### 3. Fixações e Montagens

**Título (H2):** Na parede, com firmeza de verdade

| Serviço | O que está incluso | Valor (mão de obra) |
|---|---|---|
| Instalação de suporte de TV | Marcação, furação, buchas, fixação do suporte, montagem da TV, organização de cabos | R$ 80–250 por suporte |
| Instalação de prateleiras | Nivelamento, marcação, furação, buchas/parafusos, fixação e conferência de alinhamento | R$ 60–150 por peça |
| Instalação de nichos/armários pequenos | Fixação em parede sólida ou drywall com buchas adequadas, prumo e nível | R$ 120–300 por peça |
| Instalação de varão de cortina | Medição, marcação, furação, buchas, instalação de suportes e varão | R$ 60–150 por janela |
| Instalação de quadros/decorativos | Definição de posição, furação se necessário, buchas/ganchos, pendurar | R$ 15–40 por unidade (pacote a partir de 4) |
| Redes de proteção em janelas/sacadas | Medição, fixação de perfis/ganchos, tensionamento da rede, acabamento | R$ 50–90 por m² |
| Tela mosquiteiro fixa | Medição do vão, fixação de perfil/moldura, instalação da tela, acabamento | R$ 80–180 por abertura |
| Montagem de móveis (pequeno porte) | Montagem conforme manual, fixação em parede quando necessário, ajuste de portas/gavetas | R$ 100–300 por móvel |
| Ajuste de dobradiças | Regulagem contra atrito/folga, substituição se necessário | R$ 60–150 por conjunto |
| Suportes de banheiro (toalheiro, saboneteira) | Marcação, furação, buchas, fixação e teste de firmeza | R$ 40–120 por conjunto |
| Ajustes gerais em móveis (puxadores, corrediças) | Substituição de peças quebradas, ajuste de encaixe e funcionamento | R$ 80–200 por conjunto |

---

### 4. Portas e Fechaduras

**Título (H2):** Porta que fecha direito, fechadura que funciona

| Serviço | O que está incluso | Valor (mão de obra) |
|---|---|---|
| Troca de fechadura simples | Remoção da antiga, instalação da nova, ajuste de encaixe e chave | R$ 70–150 por porta |
| Instalação de olho mágico | Furação no ponto correto, encaixe da peça, teste de visão | R$ 60–120 por porta |
| Alinhamento de porta que pega no piso | Ajuste de dobradiças, aplainamento quando autorizado, regulagem do batente | R$ 100–220 por porta |
| Instalação de porta de madeira simples | Ajuste no vão, dobradiças, fixação, fechadura e batente | R$ 250–450 por porta |

---

### 5. Pintura e Acabamento

**Título (H2):** Retoque ou parede inteira, sem sujeira desnecessária

| Serviço | O que está incluso | Valor (mão de obra) |
|---|---|---|
| Retoques de pintura | Lixamento do ponto, massa, novo lixamento, pintura só na área afetada | R$ 20–30/m² ou R$ 150–350 por cômodo |
| Pintura de parede única (sem grande preparo) | Proteção do piso, aplicação em demãos necessárias, limpeza final | R$ 20–30/m² (mão de obra) |
| Vedação de rejuntes (banheiro/cozinha) | Remoção parcial do rejunte antigo, limpeza, novo rejunte ou silicone, acabamento | R$ 150–300 por ambiente |
| Calafetação com silicone (box/janelas) | Limpeza da área, remoção de silicone antigo, aplicação de novo selante | R$ 150–300 por ambiente |
| Pequenos reparos em drywall | Corte da área danificada, remendo, massa, lixamento, pintura local | R$ 150–350 por ponto |

---

### 6. Hidráulica Leve

**Título (H2):** Vazamento resolvido antes de virar conta de água alta

| Serviço | O que está incluso | Valor (mão de obra) |
|---|---|---|
| Troca de torneira simples | Fechamento do registro, remoção, instalação da nova, teste de vazamento | R$ 55–120 por unidade |
| Troca de torneira com misturador | Retirada cuidadosa, instalação do conjunto quente/frio, ajustes e testes | R$ 75–180 por unidade |
| Troca de sifão de pia/tanque | Remoção do antigo, limpeza, instalação do novo, vedação e teste | R$ 60–120 por unidade |
| Reparo de pequenos vazamentos | Troca de vedantes, reaperto de conexões, veda-rosca/silicone | R$ 60–150 por ponto |
| Instalação de ducha higiênica | Fixação do suporte, conexão na saída de água, teste de vedação | R$ 70–180 por conjunto |
| Instalação/substituição de vaso sanitário | Retirada do antigo, limpeza da base, instalação, vedação, teste de descarga | R$ 190–400 por unidade |
| Troca de assento/tampa de vaso | Remoção da tampa antiga, instalação da nova, ajuste dos fixadores | R$ 60–120 por unidade |
| Reparo de descarga/caixa acoplada | Troca do conjunto interno, regulagem, teste de vazamento | R$ 90–200 por unidade |
| Desentupimento leve (vaso/pia) | Uso de cabo/ferramenta simples, produto adequado, teste de escoamento | R$ 180–250 por ponto |
| Limpeza de caixa de gordura | Abertura, remoção de resíduos, limpeza interna, descarte adequado | R$ 130–250 por unidade |
| Troca de boia de caixa d'água | Substituição da boia, ajuste de nível, teste | R$ 100–200 por unidade |
| Limpeza de caixa d'água | Esvaziamento, escovação, remoção de resíduos, enxágue e reenchimento | R$ 250–400 (até 1.000 L) |
| Ponto de água aparente | Derivação externa, abraçadeiras/suportes, instalação de registro/torneira | R$ 90–200 por ponto |
| Ponto de água embutido | Quebra de parede, passagem de tubulação, caixa/saída, reboco simples | R$ 130–350 por ponto |

---

### 7. Instalação de Eletrodomésticos

**Título (H2):** Da caixa até funcionando

| Serviço | O que está incluso | Valor (mão de obra) |
|---|---|---|
| Instalação de máquina de lavar roupa | Entrada de água, dreno, ponto elétrico, nivelamento, teste de ciclo | R$ 80–180 por unidade |
| Instalação de máquina de lavar louça | Água e esgoto, ponto elétrico, nivelamento, teste de funcionamento | R$ 80–250 por unidade |
| Instalação de tanque de lavar roupa | Fixação em base/suporte, conexão de entrada/saída, teste de vazamento | R$ 180–350 por unidade |
| Instalação de filtro/purificador de água | Furação se necessário, fixação, ligação na rede de água, teste | R$ 120–250 por unidade |

---

### 8. Formas de Cobrança

- **Visita + pequeno reparo:** deslocamento, identificação e resolução rápida (ex: 1 prateleira, 1 torneira). Faixa: R$ 80–200.
- **Hora técnica:** para diagnóstico ou lista de reparos variados na casa toda. Faixa: R$ 50–120/hora.
- **Diária:** "faxina de manutenção" geral (elétrica leve, hidráulica leve, fixações, pintura pequena). Faixa: R$ 200–450/dia.
- **Pacote de divulgação:** até 2h, até 5 tarefas pequenas, a partir de R$ 180 + materiais.

---

### 9. FAQ

**1. Preciso saber exatamente o que quero, ou vocês ajudam a decidir?**
Você pode chegar só com a lista de "problemas" — a gente avalia o que dá para resolver na mesma visita.

**2. O material está incluso?**
Não, é orçado à parte e sempre aprovado por você antes da compra.

**3. Fazem serviço elétrico e hidráulico na mesma visita?**
Sim, o pacote marido de aluguel é justamente para resolver tarefas de áreas diferentes numa visita só.

**4. Atendem comércio, não só residência?**
Sim, atendemos pequenos comércios e escritórios também.

**5. Qual a região de atendimento?**
Conchal, Campinas e região, incluindo o Circuito das Águas Paulista (Águas de Lindóia, Lindóia, Serra Negra, Socorro), além de Monte Sião/MG e Itapira/SP.

---

### 10. Contato Final

**Título (H2):** Aquela lista de pequenos reparos? Resolve numa visita só

Chame agora e conte o que precisa ajustar, montar, trocar ou consertar.

**Botões (CTA):**
- Chamar no WhatsApp: [SEU NÚMERO]
- Pedir orçamento do pacote de reparos

---

## Sugestões de Imagens — Marido de Aluguel

Buscar manualmente no Google Imagens com estes termos:
- "instalação de suporte de tv na parede"
- "montagem de prateleira com nível"
- "troca de torneira banheiro"
- "montagem de móvel planejado"
- "instalação de varão de cortina"
- "conserto de fechadura de porta"
- "instalação de vaso sanitário"

---

## Observações Finais do Editor

1. **Cross-link estratégico:** já deixei uma chamada de Elétrica para Marido de Aluguel (ponto de rede vs. configuração de rede aponta para `/pc`) — vale replicar esse tipo de link contextual dentro do corpo das outras páginas, não só no menu.
2. **Preços:** usei os valores exatamente como você definiu, sem placeholder — se quiser revisar algum antes de publicar, me avise que eu atualizo a tabela específica.
3. **Próximo passo natural:** com as 4 páginas com conteúdo fechado, posso montar um checklist único de SEO técnico consolidado (títulos, descrições, URLs, todas numa tabela só) para facilitar a implementação do Fable 5, se for útil.
