---
id: SPEC-05
tela: Dashboard
sprint: Sprint UX 1
status: pronto-para-figma
versão: 1.0.0
criado-em: 2026-06-20
deriva-de: TELA-002 (home ZUMA), INS-001, RN-VND, personas, REVISAO-ARQUITETURA-MVP
design-system: figma/design-system/UI-KIT-ERP-v1.md
---

# Especificação — Dashboard (05)

## Objetivo
Dar ao proprietário e ao comercial uma **visão imediata do negócio** ao abrir o sistema —
substituindo a home vazia do ZUMA (TELA-002, só atalhos). Responde em 5 segundos:
quanto vendi, quanto devo de comissão, o que precisa de ação.

## Usuário principal
Proprietário/Gestor (visão de resultado) e Comercial (ações do dia). Secundário: Administrativo.

## Fluxo principal
Login → **Dashboard** → (a) ler KPIs do período → (b) agir num alerta (cliente inativo,
follow-up, estoque) → navega para Clientes/CRM/Comissão. Ver Fluxo 1 e Fluxo 3 (page 03).

## Componentes utilizados (do DS)
Sidebar (Comercial ativo) · Topbar (busca `/`, seletor de período, perfil) · **KPI card** ×4 ·
gráfico de barras (vendas por dia) · **tabela** (ranking de vendedores) · **status pills** ·
inline alert · empty state.

## Estrutura da página (1440×, sidebar 256 + conteúdo)
1. **Topbar**: busca global, seletor de período (Mês corrente ▾), sino de follow-ups, avatar.
2. **Header**: H1 "Visão geral" + período + botão secundário "Exportar".
3. **Linha de KPIs (4)**: Vendas líquidas (mês) · Comissão a pagar · Clientes inativos ·
   Orçamentos abertos. Cada um com delta vs. mês anterior.
4. **2 colunas**:
   - Esq (60%): card "Vendas no período" (barras por dia) + toggle à vista/a prazo (prazo = 87%).
   - Dir (40%): card "Ranking de vendedores" (tabela: vendedor, líquido, **comissão calculada**, meta %).
5. **Faixa de alertas (cards acionáveis)**: "23 clientes inativos →", "14 orçamentos sem retorno →",
   "produtos com estoque ≤ 0 →".

## Hierarquia visual
Número-herói (KPI `Display` branco) > títulos de card (`H2`) > dados (`Body`/`Mono`) >
labels (`Overline`/`Caption` muted). Laranja só em: item de nav ativo, deltas de ação, CTAs.

## Regras de negócio relacionadas
RN-VND-001/002/006 (comissão nativa, líquido − devoluções), RN-VND-004 (prazo 87% → toggle),
RN-VND-008 (metas saem do Excel), RN-PRD-002 (alerta estoque ≤ 0), INS-001.

## Melhorias em relação ao ZUMA
- ZUMA: home sem nenhum indicador (UX-001). Aqui: KPIs em tempo real.
- Comissão **visível e calculada** (ZUMA mostra 0 — UX-003) → mata o Excel (INS-001).
- Relatórios manuais (UX-027) → dashboard ao vivo.
- Alertas acionáveis (inativos, follow-ups) que o ZUMA não tem.

## Especificação pronta para Figma
- Frame 1440×900, fill `surface/app`. Sidebar 256 `surface/sidebar`. Conteúdo pad 32, gap 24.
- KPI cards: 248×118, `surface/raised`, radius 12, sombra e1. Grid de 4 com gap 16.
- Cards de seção: radius 12, header `H2`, `surface/raised`.
- Tabela ranking: header `Overline` em `surface/base`, zebra `surface/raised-alt`,
  coluna comissão à direita em `Mono`, célula com delta ▲ `state/success`.
- Header de página usa faixa `surface/spotlight` (gradiente da marca) — toque premium.

## Checklist Nielsen
1. Visibilidade do estado: KPIs + alertas em tempo real ✓
2. Mundo real: rótulos diretos ("Comissão a pagar", não jargão) ✓
3. Controle: seletor de período, exportar ✓
4. Consistência: KPI/card/tabela do DS ✓
5. Prevenção de erro: alerta de estoque ≤ 0 e inativos ✓
6. Reconhecimento: sidebar rotulada, nada enterrado ✓
7. Eficiência: busca `/`, alertas que levam direto à ação ✓
8. Estético/minimalista: laranja só em ação, densidade organizada ✓
