---
id: UI-KIT-ERP-v1
título: Comercinox ERP — Product UI Design System (camada de produto)
status: em-revisão
versão: 1.0.0
criado-em: 2026-06-20
deriva-de: figma/design-system/DESIGN_SYSTEM.md (Brand v2)
aplica-se-a: telas do ERP Comercialinox (Figma page "04 - Design System")
---

# Comercinox ERP — Product UI Design System (v1)

> **Relação com a marca.** O [`DESIGN_SYSTEM.md`](./DESIGN_SYSTEM.md) (Brand v2) é a
> **fonte única da verdade visual** e governa peças de marca/social (stories, posts,
> banners). Ele define o DNA inegociável: **navy profundo + laranja de ação + Inter**,
> com profundidade de luz. Porém **não** define primitivos de produto (tabelas, campos,
> navegação, estados de validação, densidade de lista). Este documento **estende** a
> marca para a camada de produto **sem violá-la** — todo token aqui deriva da paleta de
> marca. Onde foi necessário criar algo novo para ERP, está marcado com
> **🟧 Extensão justificada** (conforme a regra "nunca criar componentes fora do DS sem
> justificativa").
>
> Esta é a especificação que materializa a página **`04 - Design System`** no Figma.

---

## 0. Princípios de produto (regem toda decisão)

Derivados das personas, dos problemas de UX (PROB-001) e das heurísticas de Nielsen:

1. **Velocidade operacional** — usuário administrativo usa o dia inteiro. Menos cliques,
   atalhos de teclado, busca por nome como padrão.
2. **Reconhecimento > memorização** — navegação lateral persistente e rotulada; nada
   enterrado em menus (corrige UX-019).
3. **Prevenção de erros** — validação inline, estados claros, confirmação destrutiva.
4. **Clareza com densidade** — ERP é denso por natureza; densidade organizada, não
   poluição. Hierarquia visível sempre.
5. **Autoridade técnica premium** — herda o acabamento dimensional da marca (luz no
   fundo, glow no destaque), mas dosado para uso prolongado.

---

## 1. Cores — tokens semânticos de produto

A marca proíbe fundo branco e mantém navy+laranja. Para o ERP adotamos um **tema dark
navy** (coerente com a marca e confortável para uso prolongado), com uma escala de
**superfícies** derivada dos navies de marca.

### 1.1 Superfícies (elevação)

| Token de produto | Valor (deriva de) | Uso |
|---|---|---|
| `surface/app` | `#0A1426` (`--bg-deep`) | Fundo da aplicação (body) |
| `surface/sidebar` | `#0B1D3A` (`--bg-edge`) | Navegação lateral / topbar |
| `surface/base` | `#0D2347` (`--bg-mid`) | Área de conteúdo |
| `surface/raised` | `#162F52` (`--card`) | Cards, painéis, linhas de tabela |
| `surface/raised-alt`| `#1A3860` (`--card-2`) | Zebra de tabela, hover sutil |
| `surface/spotlight` | `radial-gradient(120% 80% at 50% 0%, #16345F, #0D2347 55%, #0B1D3A)` | Headers de página/login (luz da marca) |

### 1.2 Conteúdo (texto/ícones)

| Token | Valor | Uso |
|---|---|---|
| `text/primary` | `#FFFFFF` (`--white`) | Títulos, números-chave |
| `text/body` | `#BCD0E8` (`--text-soft`) | Corpo, labels de dado |
| `text/muted` | `#8BA3C1` (`--muted`) | Secundário, placeholders, captions |
| `text/on-accent` | `#0D2347` (`--bg-mid`) | Texto sobre laranja (CTA) |

### 1.3 Marca / ação

| Token | Valor | Uso |
|---|---|---|
| `accent/primary` | `#F5A623` (`--orange`) | **Ação primária** (1 por contexto), seleção, foco-âncora |
| `accent/primary-press`| `#E8961E` (`--amber`) | Hover/pressed do primário |
| `accent/glow` | `rgba(245,166,35,0.32)` | Glow de CTA/destaque |
| `border/hairline` | `rgba(120,165,225,0.22)` | Bordas/divisores (deriva de `--blue-accent`) |
| `border/strong` | `rgba(120,165,225,0.5)` | Borda de input focado / card ativo |
| `focus/ring` | `#78A5E1` (`--blue-accent`) | Anel de foco de acessibilidade |

### 1.4 Estados semânticos (funcionais)

A marca reserva **verde `#25D366` (WhatsApp)** e **amarelo `#FFE600` (Mercado Livre)**
para canais — **não** podem virar cor de status genérico. Por isso:

| Token | Valor | Uso | Observação |
|---|---|---|---|
| `state/success` | `#2BB673` | Confirmações, "Ativo", estoque OK | 🟧 Extensão justificada (verde de marca é reservado a WhatsApp) |
| `state/warning` | `#F5A623` | Atenção, estoque baixo | = laranja de marca |
| `state/danger` | `#E5484D` | Erro, bloqueio, estoque ≤ 0, destrutivo | 🟧 Extensão justificada (ERP exige estado de erro; marca não define vermelho) |
| `state/info` | `#78A5E1` | Informativo, dicas | = azul de acento |
| `channel/whatsapp`| `#25D366` | Botão "Falar no WhatsApp" | Uso funcional de marca |
| `channel/mercadolivre`| `#FFE600` | Selo Mercado Livre | Uso funcional de marca |

> **Acessibilidade:** todos os pares texto/superfície miram **WCAG AA** (≥ 4.5:1 corpo,
> ≥ 3:1 títulos grandes). `text/body #BCD0E8` sobre `surface/raised #162F52` passa AA.
> Status nunca é comunicado só por cor — sempre cor + ícone + rótulo (prevenção de erro).

---

## 2. Tipografia — escala de produto

**Família: Inter** (fallback Arial), conforme marca. A escala de marca (96px headline) é
para social; o produto usa uma escala compacta de aplicação, mantendo os pesos da marca
(400/500/700/800) e tracking apertado nos títulos.

| Token | Tamanho / LH | Peso | Tracking | Uso |
|---|---|---|---|---|
| `display` | 32 / 40 | 800 | -0.5 | Número-herói do dashboard (KPI) |
| `h1` | 24 / 32 | 800 | -0.3 | Título de página |
| `h2` | 20 / 28 | 700 | -0.2 | Título de seção / card |
| `h3` | 16 / 24 | 700 | 0 | Subtítulo, header de tabela |
| `body` | 14 / 20 | 400 | 0 | Texto e dados padrão |
| `body-strong` | 14 / 20 | 600 | 0 | Ênfase, valores |
| `label` | 13 / 16 | 500 | 0.2 | Labels de campo |
| `caption` | 12 / 16 | 500 | 0.2 | Metadados, ajuda |
| `overline` | 11 / 16 | 700 | 1.0 | CAIXA ALTA — tags, headers de coluna |
| `mono` | 13 / 20 | 500 | 0 | Valores monetários/numéricos (tabular nums) |

> Números monetários e de tabela usam `font-variant-numeric: tabular-nums` para
> alinhamento de colunas — crítico em telas financeiras (extrato, comissão).

---

## 3. Espaçamento, grid e raio

- **Base 8px** (escala de marca): `4 · 8 · 12 · 16 · 24 · 32 · 48 · 64`.
- **Grid de app:** sidebar fixa `256px` + área de conteúdo fluida; container de conteúdo
  máx `1280px`, gutter `24px`, 12 colunas.
- **Densidade de tabela:** linha confortável `48px`, compacta `40px` (toggle).
- **Raio:** `sm 8px` (inputs, botões) · `md 12px` (cards) · `lg 16–22px` (painéis, modais,
  herda `border-radius:22px` da marca) · `pill 999px` (badges/status).
- **Elevação:** `e1` cards `0 8px 24px rgba(0,0,0,0.35)` · `e2` modais/menus
  `0 16px 40px rgba(0,0,0,0.5)` · `glow` destaque `0 10px 34px rgba(245,166,35,0.32)`
  (sombras suaves e escuras, nunca preto sólido — regra de marca §5).

---

## 4. Biblioteca de componentes (página 04)

Cada componente lista variantes e estados. Todos em Inter, superfícies e cores acima.

### 4.1 Navegação
- **Sidebar** (`surface/sidebar`, 256px): logo "Ci" no topo; itens com ícone+label;
  item ativo com barra laranja `4px` à esquerda + `surface/raised`; agrupado por área
  (Comercial / Catálogo / Relatórios). Colapsável para 72px (só ícones).
- **Topbar** (64px): busca global (atalho `/`), seletor de período, perfil do usuário,
  sino de follow-ups. Resolve UX-019/UX-021 (navegação por reconhecimento).
- **Breadcrumb** + **Tabs** (sublinhado laranja no ativo) — para detalhe de cliente.

### 4.2 Ações
- **Button**: `primary` (laranja, texto navy, glow sutil), `secondary` (outline
  `border/strong`), `ghost` (texto), `danger` (vermelho). Tamanhos `sm 32` / `md 40` /
  `lg 48`. Estados: default / hover / pressed / focus(ring azul) / disabled / loading.
  **Um primário por contexto** (regra de marca: um CTA por peça).
- **Icon button** e **Dropdown / menu de ações** (kebab).

### 4.3 Formulário (corrige UX-005, UX-024)
- **Input / Textarea**: label acima, `surface/raised`, borda hairline → `border/strong`
  no foco + ring azul; **obrigatório = asterisco laranja**; helper/erro abaixo
  (`state/danger` + ícone + mensagem). Validação inline em tempo real.
- **Select / Combobox com autocomplete** (substitui o "número + lupa" do ZUMA — UX-024).
- **Masked input** (CNPJ/CPF, CEP, telefone, moeda).
- **Checkbox / Radio / Toggle / Date picker / Segmented control**.
- **Field group / Fieldset** com título de seção (substitui as abas densas do ZUMA).

### 4.4 Dados
- **Table**: header `overline`; zebra `surface/raised-alt`; row hover; seleção; colunas
  numéricas à direita (`mono`); ordenação; densidade compacta/confortável; **column
  config** colapsável (corrige UX-026/UX-029 — filtros básicos visíveis, avançados
  escondidos). Estados: loading (skeleton), vazio, erro.
- **DataCard / KPI card**: rótulo `overline`, número `display`, delta (▲/▼ com
  `success`/`danger`), sparkline opcional. Base do Dashboard.
- **Badge / Status pill** (pill da marca): `Ativo` (success), `Inativo` (muted),
  `Bloqueado prazo` / `Bloqueado entrega` (danger), `Em estoque/Baixo/Sem` —
  sempre cor + ícone + texto.
- **Tag / Chip** (segmento do cliente, filtros aplicados).
- **Funnel stage chip**: Frio / Médio / Quente / Recorrente (escala de calor).
- **Avatar** (iniciais do vendedor/cliente).

### 4.5 Feedback
- **Toast / Snackbar**, **Inline alert** (info/warning/danger/success),
- **Modal / Drawer** (raio lg, elevação e2, overlay navy translúcido),
- **Confirm dialog** destrutivo (corrige UX-011 — preview do que será afetado),
- **Empty state** (ícone + título + CTA — corrige UX-007),
- **Skeleton loader** (corrige UX-006).

### 4.6 Branding interno
- **Logo "Ci"** pequeno (badge da marca §4) no topo da sidebar.
- **Login / splash** usa `surface/spotlight` (gradiente hero da marca) — único ponto
  onde o produto exibe o acabamento dimensional pleno da marca.

---

## 5. Mapa de tokens → Figma Variables

Coleção **`Comercinox/ERP`** com modos `Dark` (default). Grupos: `surface/*`,
`text/*`, `accent/*`, `border/*`, `state/*`, `channel/*`, `radius/*`, `space/*`.
Text styles publicados a partir da §2. Effect styles a partir da §3 (`e1`, `e2`, `glow`).

---

## 6. Checklist de aprovação de produto (estende o §10 da marca)

Para qualquer tela do ERP:

1. Fundo navy (escala de superfícies), **sem branco/cinza claro**? (marca)
2. Par navy + laranja presente; laranja só como **ação/destaque**, nunca plano dominante?
3. Fonte **Inter**, hierarquia clara (h > body `#BCD0E8` > muted `#8BA3C1`)?
4. **Um** primário por contexto?
5. Campos obrigatórios com asterisco laranja + validação inline?
6. Status comunicado por **cor + ícone + rótulo** (nunca só cor)?
7. Navegação por **reconhecimento** (sidebar rotulada), nada enterrado?
8. Estados de tabela: loading / vazio / erro previstos?
9. Números com `tabular-nums` e alinhados à direita?
10. Efeitos **dosados** (luz no header, glow no CTA, sombra suave)?
11. Extensões fora da marca estão **justificadas** (§1.4)?
12. AA de contraste verificado nos textos sobre superfícies?

---

## Histórico de Versões

| Versão | Data | Mudanças |
|---|---|---|
| 1.0.0 | 2026-06-20 | Criação — camada de produto derivada do Brand DS v2 |
