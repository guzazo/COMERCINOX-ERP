---
id: SPEC-06
tela: Lista de Clientes
sprint: Sprint UX 1
status: pronto-para-figma
versão: 1.0.0
criado-em: 2026-06-20
deriva-de: TELA-001, print "pesquisa de cliente", RN-CLI, FEAT-001, REVISAO-ARQUITETURA-MVP
design-system: figma/design-system/UI-KIT-ERP-v1.md
---

# Especificação — Lista de Clientes (06)

## Objetivo
Encontrar qualquer cliente em segundos e enxergar seu **status comercial** sem abrir o cadastro.
Substitui a "Pesquisa de Cliente" do ZUMA (modal denso, busca padrão por CNPJ).

## Usuário principal
Comercial/Vendedor (uso o dia inteiro). Secundário: Proprietário, Administrativo.

## Fluxo principal
Sidebar → **Clientes** → busca por **nome** (padrão) → filtra (status/segmento/vendedor) →
abre ficha **ou** clica "Novo cliente". Ver Fluxo 1 e Fluxo 3 (page 03).

## Componentes utilizados (do DS)
Sidebar · Topbar · campo de busca grande · **filtros** (chips: Status, Segmento, Vendedor,
"Só inativos") · **tabela** densa · **status pills** · tag de segmento · avatar do vendedor ·
botão primário "Novo cliente" · empty/loading states · paginação.

## Estrutura da página
1. Header: H1 "Clientes" + contador ("248 clientes") + **botão primário "Novo cliente"** (dir).
2. Barra de busca: input largo "Buscar por nome, fantasia ou CNPJ" (foco automático, atalho `/`).
3. Linha de filtros (chips, básicos visíveis): Status ▾ · Segmento ▾ · Vendedor ▾ ·
   toggle "Mostrar inativos" (desligado por padrão = RN-CLI-002). "Mais filtros" colapsável.
4. **Tabela**: Cliente (nome + CNPJ + fantasia) · Segmento · Status · Última compra ·
   Vendedor · (ações: kebab → Ver ficha / Orçamento / WhatsApp).
5. Rodapé: paginação + densidade (compacta/confortável).

## Hierarquia visual
Nome do cliente (`Body Strong` branco) > CNPJ/fantasia (`Caption` muted). Status como pill
colorida (ação visual). Última compra antiga (>90d) em `state/warning`. Vendedor com avatar.

## Regras de negócio relacionadas
RN-CLI-015 (**busca por nome como padrão**, não CNPJ — corrige a dor central), RN-CLI-002
(ocultar inativos), RN-CLI-007 (status bloqueio prazo/entrega), RN-CLI-003 (vendedor),
RN-CLI-008 (observações/flags), RN-CLI-011 (segmento/grupo), RN-CLI-010 (última compra).

## Melhorias em relação ao ZUMA
- ZUMA busca por CNPJ por padrão (UX-017) → aqui **nome** por padrão.
- ZUMA = modal apertado com 10 radio-buttons → aqui página limpa, filtros como chips (UX-029).
- Status só visível abrindo o registro → aqui **pill na linha** (UX-027/RN-CLI-007).
- Acesso enterrado em Financeiro→A Receber (UX-019) → item de 1º nível "Clientes".
- Filtro por código numérico (UX-025) → autocomplete por nome.

## Especificação pronta para Figma
- Frame 1440×, sidebar 256 (Clientes ativo). Conteúdo pad 32.
- Busca: input 100% largura, altura 44, `surface/raised`, ícone lupa, placeholder muted.
- Chips de filtro: pill `surface/raised` borda hairline; ativo = borda/título laranja.
- Tabela 100% largura, header `Overline` em `surface/base`, linhas 56 confortável,
  zebra `surface/raised-alt`, hover `border/strong`. Status = pill (Ativo/Inativo/Bloqueado).
- Estado vazio (busca sem resultado): ícone + "Nenhum cliente encontrado" + CTA "Novo cliente".
- Estado loading: skeleton de 6 linhas.

## Checklist Nielsen
1. Visibilidade: status na linha, contador, última compra ✓
2. Mundo real: "Buscar por nome" ✓
3. Controle: filtros removíveis, densidade, paginação ✓
4. Consistência: tabela/pill do DS ✓
5. Prevenção de erro: inativos ocultos por padrão; >90d destacado ✓
6. Reconhecimento: filtros como chips visíveis, não memorizar radio ✓
7. Eficiência: busca por nome, `/`, ações rápidas (kebab) ✓
8. Minimalista: filtros básicos visíveis, avançados colapsados ✓
