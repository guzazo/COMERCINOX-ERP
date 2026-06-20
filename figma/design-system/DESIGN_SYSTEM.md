# Comercinox — Design System v2

> Fonte da verdade visual da marca @comercinox. Use este arquivo como instrução de sistema em qualquer criação de conteúdo (posts, stories, carrosséis, banners).
>
> **v2 — atualização "story premium":** a identidade evoluiu de um navy chapado + Arial para um **navy com profundidade (gradiente radial) + Inter + camada de efeitos (glow, vidro, vinheta) + movimento**. O par navy + laranja continua sendo o coração da marca; o que mudou é a execução, que ficou mais dimensional e cara. A referência máxima agora é o **Story Comercinox** (lockup de logo + revelação animada) somado à série **Aço Inox** e aos posts fixados.

---

## 1. Identidade da marca

**Distribuidora industrial séria que parece grande, premium e confiável — autoridade técnica em aço inox e abrasivos, comunicada em navy profundo com profundidade de luz e laranja de ação.**

A marca não vende com firula, vende com clareza e domínio técnico — mas agora com acabamento dimensional: fundo que tem luz no centro, logo com brilho de metal, fotos integradas ao fundo, e um laranja que aparece como energia (glow), não como bloco. Cada peça deve passar "essa empresa é grande, sabe o que faz e resolve meu problema rápido".

---

## 2. Paleta de cores

O eixo é **navy (família de azuis profundos) + laranja `#F5A623` + branco**. A v2 troca o navy chapado por uma **família de azuis em gradiente** e adiciona acentos de azul e âmbar para dar dimensão.

### Navy — fundo (família de gradiente)

| Token | Hex | Papel |
|---|---|---|
| `--bg-deep` | `#0A1426` | Base mais escura (body/borda externa, vinheta) |
| `--bg-edge` | `#0B1D3A` | Stop externo do gradiente; navy chapado de fallback |
| `--bg-mid` | `#0D2347` | Stop intermediário do gradiente |
| `--bg-core` | `#16345F` | Centro do gradiente (mais claro, "luz" da peça) |

**Gradiente hero (fundo padrão de story/post):**
```css
background: radial-gradient(120% 80% at 50% 30%, #16345F 0%, #0D2347 45%, #0B1D3A 100%);
```
Body/outermost: `#0A1426`. Use o gradiente como look principal; navy chapado `#0B1D3A` é aceitável em peças simples de produto.

### Laranja / âmbar — ação e destaque

| Token | Hex | Uso |
|---|---|---|
| `--orange` | `#F5A623` | CTA, badge, divider, caret, barra do logo, glow de destaque |
| `--amber` | `#E8961E` | Palavra "COMERC" do wordmark; parceiro do laranja em gradientes |

### Azuis de acento — dimensão e brilho

| Token | Hex | Uso |
|---|---|---|
| `--blue-accent` | `#78A5E1` | Bordas, strokes finos, brilho sutil (`rgba(120,165,225,…)`) |
| `--badge-1` | `#3B6DB3` | Topo do gradiente do badge "Ci" |
| `--badge-2` | `#1C4682` | Meio do gradiente do badge "Ci" |
| `--badge-3` | `#0D2A55` | Base do gradiente do badge "Ci" |

### Texto

| Token | Hex | Uso |
|---|---|---|
| `--white` | `#FFFFFF` | Títulos, "INOX", texto principal |
| `--text-soft` | `#BCD0E8` | Corpo / subtexto (tom suave, novo na v2) |
| `--muted` | `#8BA3C1` | Tagline, labels secundários, URLs |

### Funcionais (uso exclusivo de plataforma)

| Token | Hex | Uso |
|---|---|---|
| `--yellow` | `#FFE600` | **Exclusivo** botão/selo Mercado Livre |
| `--green` | `#25D366` | **Exclusivo** botão/selo WhatsApp |

### Cards (mantidos da v1, para posts com painéis)

| Token | Hex | Uso |
|---|---|---|
| `--card` | `#162F52` | Cards e pills de spec |
| `--card-2` | `#1A3860` | Cards alternados |

### Regras de cor

- Navy + laranja é inegociável. O gradiente é o novo "default"; chapado só em peça simples.
- Laranja é **energia e ação**: pontos, glow, divider, CTA — nunca plano dominante.
- `--amber #E8961E` aparece basicamente no wordmark ("COMERC") e em gradientes com o laranja. Não use como cor de texto de corpo.
- Azuis de acento (`#78A5E1` e os do badge) são **estruturais/decorativos sutis** — bordas, brilhos, o badge "Ci". Nunca viram cor de texto.
- Amarelo e verde são **funcionais**: só quando o CTA é literalmente Mercado Livre ou WhatsApp.
- Proibido fundo branco, cinza claro ou qualquer paleta fora do navy + laranja.

---

## 3. Tipografia

**Família primária: Inter.** Fallback de sistema: Arial. Stack oficial:
```css
font-family: 'Inter', Arial, sans-serif;
```
> Migração: a v1 usava Arial. Inter é o novo padrão da marca; Arial continua como fallback fiel (métricas próximas). Peças/HTML carregam Inter via web font; geradores em Pillow precisam do arquivo Inter (`.ttf`) instalado — sem ele, caem em Arial.

**Pesos em uso:** 400 (corpo), 500 (tagline), 700 (CTA/labels fortes), 800 (títulos, wordmark, pill, badge), 900 (reservado para impacto máximo).

**Escala canônica** (base 1080px de largura) — valores do story são a referência:

| Nível | Tamanho | Peso | Tracking | Line-height | Cor |
|---|---|---|---|---|---|
| Headline / título | `96px` (88–110) | 800 | `-1.5px` | `1.05` | `#FFFFFF` |
| Wordmark | `52px` | 800 | `0.5px` | `1` | COMERC `#E8961E` + INOX `#FFFFFF` |
| Subtexto / corpo | `33px` (30–40) | 400 | `0.5px` | `1.5` | `#BCD0E8` |
| Pill badge | `25px` (24–28) | 800 | `1.5px` | — | `#0D2347` sobre laranja |
| CTA hint | `24px` | 700 | `2.5px` | — | `#FFFFFF` |
| Tagline | `19px` | 500 | `4px` | `1` | `#8BA3C1` |

**Regras de aplicação**

- Título **sempre** branco, com leve glow de profundidade (ver §5). Subtítulo/corpo em `#BCD0E8`. Tagline e apoio em `#8BA3C1`.
- Caixa alta apenas em pill, CTA hint e labels de spec — nunca em frases longas.
- Headline com tracking negativo (`-1.5px`) — característica da v2, dá ar premium. Máx. 2–3 linhas.
- Hierarquia visível: headline > subtexto > apoio. Tudo com o mesmo peso = refazer.

---

## 4. Componentes

### Logo lockup (assinatura da marca — v2)
Empilhado e centralizado: badge "Ci" → wordmark → tagline.

- **Badge "Ci":** `104×104px`, `border-radius:18px`, gradiente `linear-gradient(165deg, #3B6DB3 0%, #1C4682 42%, #0D2A55 100%)`, borda `1px solid rgba(120,165,225,0.5)`.
  - Brilho de vidro: realce superior (faixa branca translúcida) + `box-shadow: 0 10px 30px rgba(0,0,0,0.45), inset 0 2px 1px rgba(255,255,255,0.45), inset 0 -3px 6px rgba(0,0,0,0.4)`.
  - "Ci" em branco, `58px`, peso 800, tracking `-1px`.
  - Barra laranja `#F5A623` na base do badge (`~4px`, cantos arredondados).
- **Wordmark:** `COMERC` em `#E8961E` + `INOX` em `#FFFFFF` com glow `text-shadow:0 0 12px rgba(170,200,245,0.55)`. `52px`, peso 800.
- **Tagline:** "Aço Inoxidável & Abrasivos", `19px`, peso 500, tracking `4px`, `#8BA3C1`.

### Badge / pill (selo de status)
- Pill total (`border-radius:999px`), fundo `#F5A623`, texto `#0D2347`, `25px`, peso 800, tracking `1.5px`, **CAIXA ALTA**, padding `17px 36px`.
- **Glow laranja:** `box-shadow:0 10px 34px rgba(245,166,35,0.32)`.
- Pode levar 1 emoji funcional ao lado (ex.: 📦). Posição: topo do bloco central (story) ou topo esquerdo (post de produto, label "NOVIDADE").

### Divider
- Barra laranja `#F5A623`, `120px × 5px`, `border-radius:4px`, centrada. Separa headline do subtexto.

### CTA
- **Story (link sticker):** *hint* em caixa alta — `24px`, peso 700, tracking `2.5px`, branco — + **seta animada** para baixo (`stroke:#F5A623`, ~`46×58px`), logo acima do gap reservado do sticker. Texto-modelo: "Toque no link abaixo para comprar ⚡".
- **Post de produto:** banner laranja de rodapé "FAÇA SEU PEDIDO / MERCADO LIVRE" + URL, largura cheia.
- Plataforma: Mercado Livre `#FFE600`, WhatsApp `#25D366` — só nesses casos. **Um CTA por peça.**

### Pill de spec
- Fundo escuro `#162F52`, pill arredondada, texto Inter peso 700–800, caixa alta, branco. Agrupadas em linha/grade abaixo do subtítulo (ex.: `304` · `316` · `Ø 1/2"`).

### Card / painel
- Fundo `#162F52` (ou `#1A3860` alternado), `border-radius:22px`, padding `40–48px`. Para agrupar specs, comparações, blocos.

### Logo pequeno (posts de produto)
- "Ci" reduzido no canto superior direito. Transparente, sem fundo branco.

---

## 5. Efeitos e profundidade (novo na v2)

A "cara premium" vem desta camada. Aplique com parcimônia — efeito é tempero, não prato.

- **Fundo com luz:** gradiente radial com centro mais claro (`#16345F`) que escurece nas bordas (`#0B1D3A`/`#0A1426`). Dá a sensação de spotlight no conteúdo.
- **Glow de profundidade em texto branco:** títulos `text-shadow:0 3px 18px rgba(7,20,42,0.65)`; "INOX" com brilho azul `0 0 12px rgba(170,200,245,0.55)`.
- **Glow laranja:** pills e CTAs com `0 10px 34px rgba(245,166,35,0.32)`.
- **Vidro/metal no badge:** gradiente + realce branco no topo + insets (ver §4).
- **Foto integrada por vinheta (não retângulo):** a foto entra mascarada e fundida ao navy, como prova social, nunca como bloco recortado.
  - Máscara: `mask-image:radial-gradient(ellipse 74% 60% at 50% 44%, #000 0%, #000 44%, rgba(0,0,0,0.55) 66%, transparent 84%)`.
  - Tratamento: `filter:brightness(0.96) contrast(1.22) saturate(1.06)`, opacidade `~0.95`.
  - Overlay navy por cima para fundir nas bordas (`rgba(11,29,58,…)` crescente até `0.97`).
- **Sombras suaves e escuras** (`rgba(0,0,0,0.4–0.55)`) para dar relevo — nunca sombra dura/preta sólida.

---

## 6. Movimento (stories animados)

Linguagem de revelação sequenciada — para stories em vídeo/animados. Em export estático, use o **estado final** (tudo visível).

Ordem do reveal:
1. **Pill** entra (fade + leve descida).
2. **Headline** em **efeito máquina de escrever**, com caret laranja piscando (`#F5A623`).
3. **Divider** cresce do centro (`scaleX 0 → 1`).
4. **Subtexto** em máquina de escrever, caret `#8BA3C1`.
5. **CTA hint + seta** entram (fade + subida) e a seta fica em **bounce** contínuo (`1.4s`).

Tempos de referência: caret pisca `0.9s` (step-end); velocidade de digitação ~`52ms`/char (headline) e ~`26ms`/char (subtexto); loop com pausa de ~`4s` no final.

---

## 7. Grid e espaçamento

Princípio: **respiro generoso, conteúdo centrado, luz no meio.**

### Story — 1080×1920 (referência: Story Comercinox)
- Fundo: gradiente hero. Margens laterais do bloco central: `~90px`.
- **Topo (~300px):** logo lockup centralizado (badge → wordmark → tagline).
- **Centro (~720px):** pill → headline → divider → subtexto, centralizados.
- **CTA (~1430px):** hint + seta animada.
- **Gap reservado (~1560–1780px):** **deixar em branco** — é onde o sticker de link nativo do Instagram fica. Nada crítico aqui.
- **Foto de prova social (terço inferior, opcional):** banda mascarada por vinheta, fundida ao navy.
- Zona de UI do Instagram: evite elementos críticos nos primeiros/últimos `~220px`.

### Post de produto — 1080×1080
- Margem de segurança `64px` em todos os lados.
- **Topo (~0–15%):** badge "NOVIDADE" (esq) + logo "Ci" pequeno (dir).
- **Centro (~20–70%):** foto do produto sobre o gradiente — limpa ou com vinheta suave.
- **Inferior (~70–100%):** headline branca → subtítulo/âmbar → pills de spec → banner laranja com URL.
- Espaçamento entre blocos: `32–48px`.

### Espaçamento geral
- Múltiplos de `8px` (8/16/24/32/48/64/90).
- Mais vazio = mais premium. Na dúvida, tire elemento.

---

## 8. Regras de layout

**Sempre deve aparecer**
- Fundo navy — gradiente hero (preferencial) ou chapado `#0B1D3A`.
- Par navy + laranja na peça.
- Tipografia Inter (fallback Arial), com hierarquia clara.
- Logo: lockup completo (story) ou "Ci" pequeno (post de produto).
- Um CTA claro (hint + seta no story; banner no post).
- Profundidade controlada: luz no fundo, glow no destaque, sombra suave.

**Nunca deve aparecer**
- Fundo branco, cinza claro ou paleta fora do navy + laranja.
- Laranja como fundo dominante (ex.: post "OPORTUNIDADE VENDEDOR" — descartado).
- Tipografia display/editorial fora da marca (ex.: "mo.to. / 25 DE JULHO" — descartado).
- Repost de terceiros (ex.: fundo roxo/neon — descartado).
- Excesso de glow/sombra ("arte poluída"), foto recortada em retângulo duro, excesso de texto.
- Frases motivacionais, posts genéricos, Instagram como catálogo.
- Conteúdo crítico dentro do gap do link sticker. Mais de um CTA competindo.

---

## 9. Tom visual

**O que a identidade comunica**
- Autoridade técnica e porte — distribuidora grande, premium, organizada.
- Confiança industrial com acabamento moderno (luz, profundidade, metal).
- Clareza e ação — sempre há um próximo passo óbvio (comprar, pedir, falar no WhatsApp).

**O que a identidade rejeita**
- "Promoção de varejo barato" (fundos saturados, selos gritando desconto).
- Lifestyle, motivacional, abstrato ou decorativo sem função.
- Flat sem profundidade **e** excesso de efeito — o ponto é equilíbrio dimensional.
- Catálogo despejado / poluição de texto.

Teste-síntese: parece um **fornecedor industrial sério e moderno** ou uma **loja de promoção**? Só o primeiro passa.

---

## 10. Checklist de aprovação

Se qualquer resposta for "não", a peça volta.

1. O fundo é navy — gradiente hero (ou chapado `#0B1D3A`)?
2. O par navy + laranja está presente?
3. A fonte é **Inter** (fallback Arial), com pesos corretos?
4. O título é branco, com tracking apertado e leve glow de profundidade?
5. Há hierarquia clara (headline > subtexto `#BCD0E8` > apoio `#8BA3C1`)?
6. O logo está correto (lockup no story / "Ci" pequeno no post)?
7. Há **um** CTA claro (hint + seta no story; banner no post)?
8. No story, o **gap do link sticker (~1560–1780px)** está livre?
9. Os efeitos estão **dosados** (luz no fundo, glow no destaque, sombra suave — sem poluir)?
10. Fotos entram **fundidas por vinheta**, não em retângulo duro?
11. Amarelo/verde aparecem **só** se o CTA for Mercado Livre / WhatsApp?
12. A peça responde "o cliente se importa com isso?" e está livre de fundo claro, laranja dominante, motivacional e excesso de texto?

---

## 11. Regras de legenda e caption

**Tom de voz**
- Direto, técnico-acessível, de fornecedor que entende do assunto. Fala de igual para igual com serralheiro e comprador de indústria.
- Sem enrolação, sem motivacional, no máximo 1–2 emojis funcionais.
- Foco em utilidade e no próximo passo: o que o cliente ganha e como pedir.

**Estrutura padrão**
1. **Gancho** (1 linha) — dor, dúvida ou benefício concreto. Sem "Você sabia que...".
2. **Desenvolvimento** (2–4 linhas) — informação útil, especificação ou diferencial real.
3. **CTA** (1 linha) — ação clara: Mercado Livre, WhatsApp (27) 98100-2605 ou loja física.
4. **Hashtags** (3–6) — segmentadas. Ex.: `#acoinox #serralheria #vilavelha #metalurgia #inox304`.

**Evitar no texto**
- Frases motivacionais e clichês ("qualidade que você merece").
- Caixa alta em frases inteiras.
- Promessas vagas sem dado ou spec.
- Mais de um CTA / links concorrentes.
- Legenda como catálogo (lista crua de produtos).

**Templates prontos**

*Post de produto / novidade*
```
[Produto] em [especificação] — [benefício direto p/ a aplicação].

✓ [spec 1]   ✓ [spec 2]   ✓ [spec 3]
Pronta entrega para [serralheria / indústria].

Peça pelo Mercado Livre (link na bio) ou chame no WhatsApp (27) 98100-2605.

#acoinox #[segmento] #vilavelha #[produto]
```

*Post técnico / autoridade (ex.: 304 vs 316)*
```
[Pergunta técnica que o cliente realmente faz].

[Resposta objetiva em 2–3 linhas com a diferença prática na hora de comprar.]

Dúvida na escolha? A gente te orienta antes do pedido. Chama no WhatsApp (27) 98100-2605.

#inox304 #inox316 #serralheria #metalurgia
```

*Story / CTA rápido*
```
[Benefício ou novidade em 1 frase].
Toque no link abaixo para comprar ⚡
```

---

### Referências de identidade (máxima fidelidade)
**Story Comercinox** (lockup + reveal animado) + posts fixados + série **Aço Inox** (`stories/acoinox/`). Em qualquer dúvida visual, compare com essas peças — elas definem o padrão v2.

### Tokens (resumo para colar em ferramentas)
```css
--bg-deep:#0A1426; --bg-edge:#0B1D3A; --bg-mid:#0D2347; --bg-core:#16345F;
--orange:#F5A623; --amber:#E8961E;
--blue-accent:#78A5E1; --badge-1:#3B6DB3; --badge-2:#1C4682; --badge-3:#0D2A55;
--white:#FFFFFF; --text-soft:#BCD0E8; --muted:#8BA3C1;
--card:#162F52; --card-2:#1A3860; --yellow:#FFE600; --green:#25D366;
--hero:radial-gradient(120% 80% at 50% 30%, #16345F 0%, #0D2347 45%, #0B1D3A 100%);
--font: 'Inter', Arial, sans-serif;
```
