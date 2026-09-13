---
name: Conecta Saber Digital
description: Plataforma de letramento digital para idosos, extensão do IFNMG
colors:
  forest: "#0d351c"
  forest-deep: "#082413"
  forest-soft: "#315f37"
  leaf: "#76a064"
  mint: "#d9e8cf"
  cream: "#fff8e9"
  paper: "#fffcf3"
  ink: "#163221"
  muted: "#61705e"
typography:
  display:
    fontFamily: "Trebuchet MS, Segoe UI, Arial, sans-serif"
    fontSize: "clamp(2.4rem, 6vw, 5.7rem)"
    fontWeight: 700
    lineHeight: 0.98
    letterSpacing: "normal"
  headline:
    fontFamily: "Trebuchet MS, Segoe UI, Arial, sans-serif"
    fontSize: "clamp(2rem, 4vw, 3.5rem)"
    fontWeight: 700
    lineHeight: 1.05
    letterSpacing: "normal"
  title:
    fontFamily: "Trebuchet MS, Segoe UI, Arial, sans-serif"
    fontSize: "1.45rem"
    fontWeight: 800
    lineHeight: 1.15
    letterSpacing: "normal"
  body:
    fontFamily: "Trebuchet MS, Segoe UI, Arial, sans-serif"
    fontSize: "1.04rem"
    fontWeight: 400
    lineHeight: 1.6
    letterSpacing: "normal"
  label:
    fontFamily: "Trebuchet MS, Segoe UI, Arial, sans-serif"
    fontSize: "0.78rem"
    fontWeight: 900
    lineHeight: 1.2
    letterSpacing: "0.08em"
rounded:
  sm: "0.4rem"
  md: "0.5rem"
  pill: "999px"
spacing:
  xs: "0.35rem"
  sm: "0.8rem"
  md: "1.25rem"
  lg: "2rem"
  xl: "clamp(2.5rem, 6vw, 5rem)"
components:
  button-primary:
    backgroundColor: "{colors.cream}"
    textColor: "{colors.forest}"
    rounded: "{rounded.md}"
    padding: "0.72rem 1rem"
  button-ghost:
    backgroundColor: "transparent"
    textColor: "{colors.cream}"
    rounded: "{rounded.md}"
    padding: "0.72rem 1rem"
  card-module:
    backgroundColor: "#ffffff"
    textColor: "{colors.forest}"
    rounded: "{rounded.md}"
    padding: "1.3rem"
---

# Design System: Conecta Saber Digital

## Overview

**Creative North Star: "O Reflório Acolhedor"**

O sistema visual é um verde-floresta profundo e institucional (`--forest`) suavizado por creme quente (`--cream`, `--paper`), como uma estufa que acolhe quem está entrando pela primeira vez. É sério o suficiente para carregar credibilidade de um projeto de extensão do IFNMG, mas nunca frio: cantos sempre arredondados, sombras esfumaçadas em vez de bordas duras, tipografia grande e confiante.

A restrição mais importante do sistema é o público: idosos com pouca familiaridade digital. Isso empurra toda decisão visual para "simples e direto" — mas simples nunca pode significar infantilizado. O sistema rejeita explicitamente qualquer traço de UI condescendente (mascotes, ícones fofos, linguagem visual de "área infantil"): a seriedade institucional do verde-mata profundo é o que garante isso. É respeito, não decoração.

Densidade é baixa: espaçamentos generosos (`clamp` em quase todo padding relevante), poucos elementos por tela, hierarquia tipográfica exagerada (títulos de até `5.7rem` na hero) para que a primeira leitura nunca exija esforço.

**Key Characteristics:**
- Verde-mata profundo como base institucional, nunca como decoração isolada
- Creme/paper como respiro — o sistema não é escuro, é *aconchegante*
- Cantos sempre arredondados (nunca cortes retos), sombras suaves em vez de bordas duras
- Tipografia grande por padrão; hierarquia faz o trabalho, não o peso de cor
- Zero elementos que soem "para crianças" ou "para quem não entende" — simples é uma forma de respeito, não de simplificação condescendente

## Colors

A paleta é monocromática-verde com dois neutros quentes fazendo o contraponto — não há uma segunda cor de destaque competindo com o verde.

### Primary
- **Verde-Mata Profunda** (`#0d351c` / `--forest`): cor institucional base. Headers (`site-header`, `course-header`), fundo da hero, texto de títulos sobre fundo claro (`--forest` em h2, h3, module-card).
- **Verde-Mata Escura** (`#082413` / `--forest-deep`): tom mais fechado, usado no footer e no hover de botões ghost/nav — sempre um degrau abaixo do primary, nunca ao lado dele.

### Secondary
- **Broto-Verde** (`#76a064` / `--leaf`): único acento vivo do sistema. Usado com moderação — borda de blockquote, tag pill "Inscrições abertas". É o único lugar onde o sistema "sorri"; não deve virar cor de fundo de área grande.

### Neutral
- **Creme** (`#fff8e9` / `--cream`): fundo de botões primary/light, texto sobre fundo escuro, cor "de respiro" do sistema.
- **Paper** (`#fffcf3` / `--paper`): fundo de página (gradient com cream), superfície mais clara que existe.
- **Verde-Suave** (`#315f37` / `--forest-soft`): eyebrows sobre fundo claro, h3 dentro de conteúdo de aula — um meio-termo entre o forest institucional e o muted de apoio.
- **Menta** (`#d9e8cf` / `--mint`): eyebrow sobre fundo escuro (hero) — a única variação clara de verde usada como texto, não como superfície.
- **Tinta** (`#163221` / `--ink`): cor de texto base do body, quase preto mas ainda verde.
- **Verde-Neutro** (`#61705e` / `--muted`): texto secundário/descrição (`section-heading p`, `module-card p`, `course-note span`).

### Named Rules
**A Regra do Sorriso Único.** `--leaf` (Broto-Verde) é o único verde vivo do sistema e aparece em no máximo um elemento de destaque por tela (uma tag, uma borda). Se ele virar fundo de área grande ou se repetir em múltiplos elementos da mesma view, deixou de ser destaque.

## Typography

**Display/Body Font:** Trebuchet MS, com fallback Segoe UI, Arial, sans-serif (fonte única do sistema — não há uma segunda família para títulos vs. corpo).

**Character:** Uma única família sans-serif humanista carrega todo o sistema — a hierarquia vem inteiramente de tamanho e peso, não de troca de fonte. Isso é deliberado: menos variação tipográfica = menos chance de confundir o leitor iniciante.

### Hierarchy
- **Display** (peso 700, `clamp(2.4rem, 6vw, 5.7rem)`, altura de linha 0.98): título da hero da homepage. Só existe uma vez por página.
- **Headline** (peso 700, `clamp(2rem, 4vw, 3.5rem)`, altura de linha 1.05): títulos de seção (`section-heading h2`, `cabecalho-aula h1`, `sobre-hero h1`).
- **Title** (peso 800, `1.45rem`, altura de linha 1.15): títulos de card (`module-card h3`).
- **Body** (peso 400, `1.04rem`–`1.28rem`, altura de linha 1.6): parágrafos de conteúdo. Nas aulas (`corpo-aula p`), o texto é justificado com recuo de primeira linha (`text-indent: 2rem`) — um tratamento editorial deliberado, não padrão de blog.
- **Label** (peso 900, `0.78rem`, letter-spacing `0.08em`, uppercase): eyebrows e kickers (`eyebrow`, `module-kicker`) — sempre a etiqueta pequena acima de um título maior.

### Named Rules
**A Regra da Fonte Única.** Nenhuma segunda família tipográfica entra no sistema. Toda diferenciação visual vem de tamanho, peso e cor — nunca de trocar a fonte, o que adicionaria uma variável a mais para o leitor decodificar.

## Layout

Container-based, sem grid rígido de 12 colunas: cada seção define seu próprio `padding` em `clamp()` (tipicamente `clamp(1rem, 6vw, 6rem)` horizontal), deixando o conteúdo respirar em telas grandes e comprimir suavemente em mobile sem breakpoints abruptos. A hero da homepage usa CSS Grid de duas colunas (`minmax(0, 1.05fr) minmax(18rem, 0.8fr)`) que colapsa para uma coluna única abaixo de `860px`. Páginas de conteúdo (aulas, Sobre) usam uma coluna central com largura máxima (`56rem`), sem grid lateral — exceto as aulas, que somam uma sidebar fixa de navegação (`16rem`–`19rem`) que também colapsa em telas pequenas.

Densidade é baixa por toda parte: gaps generosos (`0.8rem`–`2rem`), nunca elementos colados uns nos outros. Essa folga é a principal ferramenta de acessibilidade do sistema hoje — grandes áreas de toque e respiro visual compensam a ausência de um padrão formal de acessibilidade ainda não definido (ver `PRODUCT.md`).

## Elevation & Depth

O sistema usa sombras suaves e esfumaçadas em verde (nunca cinza neutro) com dois papéis simultâneos: **ambiental em repouso**, **estrutural no hover**. Um card em repouso já tem uma sombra discreta (`0 12px 32px rgba(13, 53, 28, 0.08)` em `module-card`) que dá profundidade sem parecer flutuante; ao passar o mouse, a sombra se intensifica para a variante "alta" do sistema (`--shadow: 0 18px 55px rgba(8, 36, 19, 0.14)`), sinalizando interatividade sem precisar mudar a cor de fundo.

### Shadow Vocabulary
- **Sombra Baixa** (`box-shadow: 0 12px 32px rgba(13, 53, 28, 0.08)`): estado de repouso de cards (`module-card`).
- **Sombra Alta / `--shadow`** (`box-shadow: 0 18px 55px rgba(8, 36, 19, 0.14)`): hero-panel em repouso; hover de `module-card`. É a sombra "de destaque" do sistema.
- **Sombra de Conteúdo** (`box-shadow: 0 16px 45px rgba(13, 53, 28, 0.08)`): usada em superfícies de leitura longa (`corpo-aula`), mais discreta que a Sombra Alta porque não deve competir com o texto.

### Named Rules
**A Regra do Sobe-e-Desce.** Toda sombra que existe em repouso tem uma variante mais intensa reservada para hover/interação. Uma superfície nunca ganha sombra nova do nada ao ser tocada — ela intensifica a sombra que já tinha.

## Shapes

Cantos são sempre arredondados, nunca retos — é a assinatura de forma do sistema. Dois raios cobrem praticamente todos os componentes: `0.5rem` (botões, cards, painéis, blocos de conteúdo) e `0.4rem` (imagens dentro de painéis, blockquotes, ícone de toggle da sidebar). A única exceção é a forma pílula (`border-radius: 999px`), reservada exclusivamente para a tag de destaque `enrollment-tag` — pílula significa "chamada de atenção pontual", nunca um componente estrutural.

Bordas são finas e translúcidas (`--line: rgba(13, 53, 28, 0.14)`), usadas para dividir seções de conteúdo sem criar blocos isolados — divisórias, não caixas.

## Components

### Buttons
- **Shape:** cantos arredondados (`border-radius: 0.5rem`), altura mínima generosa (`min-height: 2.75rem`) para área de toque confortável.
- **Primary/Light:** fundo Creme (`--cream`), texto Verde-Mata Profunda (`--forest`), peso 800 — o botão "sólido" usado para a ação principal (`Começar agora`, `Inscrever-se`).
- **Ghost:** transparente com borda translúcida creme (`rgba(255, 248, 233, 0.5)`) e texto creme — usado sobre fundo escuro quando a ação é secundária (`Ver módulos`).
- **Hover / Focus:** o sistema ainda não define um tratamento de hover explícito para botões (lacuna a resolver em trabalho de design futuro; não inventar um valor aqui).

### Cards / Containers
- **Corner Style:** `0.5rem`.
- **Background:** branco puro (`#fff`) para `module-card`; Creme semi-opaco (`rgba(255, 248, 233, 0.96)`) para `hero-panel` — o branco puro é reservado a cards sobre fundo `--paper`, o creme translúcido a painéis sobre fundo escuro.
- **Shadow Strategy:** ver Elevation & Depth — Sombra Baixa em repouso, Sombra Alta no hover.
- **Border:** `1px solid var(--line)` em `module-card`; ausente em `hero-panel`.
- **Internal Padding:** `1.3rem` (module-card) a `clamp(1.4rem, 4vw, 2.4rem)` (corpo-aula).

### Tags / Pills
- **Style:** fundo Broto-Verde (`--leaf`), texto Verde-Mata Escura (`--forest-deep`), `border-radius: 999px`, uppercase, peso 900, letter-spacing `0.06em`.
- **Uso:** exclusivo para chamadas pontuais de urgência/novidade (ex: "Inscrições abertas"). Não é um componente de categorização geral.

### Navigation
- **Header:** fundo Verde-Mata Profunda de ponta a ponta, logo à esquerda, ações à direita como botões `btn-light`. Mesma estrutura em `site-header` (home) e `course-header` (aulas/Sobre), com o logo em versão compacta (`brand-link.compact`) nas páginas internas.
- **Sidebar de aulas:** fundo verde muito claro (`#f1f7ea`), itens de módulo em `<details>`/`<summary>` colapsáveis, item ativo/hover ganha fundo `rgba(255, 248, 233, 0.95)` e texto `--forest`.
- **Footer:** fundo Verde-Mata Escura, texto creme translúcido (`rgba(255, 248, 233, 0.82)`), layout flex com wrap — usado de forma idêntica na homepage e na página Sobre (título, subtítulo, linha de links legais).

## Do's and Don'ts

### Do:
- **Do** manter o verde-mata profundo como cor de header/footer em toda página nova — é a assinatura institucional do site.
- **Do** usar cantos arredondados (`0.5rem` ou `0.4rem`) em qualquer superfície nova; retas quebram a linguagem de forma do sistema.
- **Do** intensificar a sombra existente no hover em vez de introduzir uma sombra nova (A Regra do Sobe-e-Desce).
- **Do** manter espaçamento generoso — a folga visual é hoje a principal defesa de acessibilidade do site para o público idoso.

### Don't:
- **Don't** introduzir uma segunda cor de destaque além de Broto-Verde (`--leaf`); vira ruído e quebra A Regra do Sorriso Único.
- **Don't** usar `--leaf` como fundo de área grande (seção, card inteiro) — ele é reservado a toques pontuais.
- **Don't** trocar a família tipográfica para diferenciar hierarquia; use tamanho e peso.
- **Don't** adicionar qualquer elemento com tom infantilizado ou condescendente (mascotes, ícones "fofos", linguagem visual de app infantil) — confirmado como anti-referência explícita dado o público idoso.
