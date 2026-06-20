---
id: SPEC-07
tela: Cadastro de Cliente
sprint: Sprint UX 1
status: pronto-para-figma
versão: 1.0.0
criado-em: 2026-06-20
deriva-de: TELA-001, prints "cadastro de clientes"/"dados complementares", RN-CLI, FEAT-001, REVISAO-ARQUITETURA-MVP
design-system: figma/design-system/UI-KIT-ERP-v1.md
---

# Especificação — Cadastro de Cliente (07)

## Objetivo
Cadastrar/editar um cliente de forma rápida e sem erro, com as **condições comerciais** que
alimentam orçamento, venda e comissão. Substitui a TELA-001 (3 abas densas em Financeiro→A Receber).

## Usuário principal
Comercial/Vendedor (cria no atendimento). Secundário: Administrativo (dados fiscais/financeiros).

## Fluxo principal
Lista de Clientes → "Novo cliente" → preenche **Identificação** (CNPJ → auto-preenche via
ReceitaWS) → Contatos → Condições comerciais → Salvar → volta à ficha. Ver Fluxo 1 (page 03).

## Componentes utilizados (do DS)
Sidebar · breadcrumb · **fieldsets** por seção (em vez de abas) · inputs com **validação inline**
(asterisco laranja, máscara, erro `state/danger`) · combobox autocomplete (vendedor, segmento) ·
toggle (bloqueios) · status pills · botões (primário "Salvar", secundário "Cancelar", WhatsApp).

## Estrutura da página (layout de 1 coluna com seções ancoradas; navegação lateral de seções)
1. Breadcrumb "Clientes / Novo cliente" + H1 + **status pill** (ao editar) + botões (topo, sticky).
2. **Seção Identificação**: Tipo (PF/PJ segmented), CNPJ/CPF (máscara + botão "Buscar ReceitaWS"),
   Razão social*, Nome fantasia, Inscrição estadual / "Isento" (RN-CLI-008), Segmento* (combobox).
3. **Seção Contatos** (RN-CLI-009): grid de contatos (tipo, valor, principal) + "Adicionar contato".
4. **Seção Endereço**: CEP (auto-preenche), logradouro, número, bairro, município/UF.
   (1 endereço no MVP; múltiplos = futuro.)
5. **Seção Condições comerciais** (bloco crítico — RN-CLI-004/005/006/007):
   Vendedor responsável* (combobox), Comissão override (%), Desconto máximo (%),
   Limite de crédito (R$), Forma/plano de pagamento padrão, **toggles** Bloquear venda a prazo /
   Bloquear entrega (independentes), Estágio no funil (Frio/Médio/Quente/Recorrente).
6. **Seção Fiscal** (capturada, read-mostly no MVP — RN-CLI-012/013): Consumidor final,
   Calcula DIFAL, Tipo de contribuinte. Recolhida por padrão ("Avançado").
7. Barra de ação sticky no rodapé: Cancelar · Salvar cliente (primário).

## Hierarquia visual
Título de seção (`H2`) > label (`Label` muted) > valor (`Body` branco). Obrigatórios com
asterisco laranja. Erros em `state/danger` com ícone. Condições comerciais com leve destaque
(card `surface/raised` com borda) por serem regra de negócio.

## Regras de negócio relacionadas
RN-CLI-001 (PF/PJ muda campos), 004 (comissão por cliente), 005 (desconto máx), 006 (limite
crédito — validar se bloqueia), 007 (bloqueios independentes), 008 (observações/ISENTO),
009 (contatos/endereços), 010 (ficha financeira — read-only no cadastro), 011 (segmento),
012/013 (flags fiscais), 014 (pagamento padrão).

## Melhorias em relação ao ZUMA
- 3 abas densas → **seções ancoradas** numa página rolável (UX-007).
- Sem asterisco/validação (UX-005) → obrigatórios + validação inline em tempo real.
- "Vendedor/Grupo" exigem nº + lupa (UX-024) → **combobox autocomplete**.
- Título "[Contas à Receber]" (UX-008) → "Clientes / Novo cliente" no CRM.
- Bloqueios e limite escondidos → **bloco Condições comerciais** explícito.
- CNPJ digitado à mão → **busca ReceitaWS** + CEP automático.

## Especificação pronta para Figma
- Frame 1440×, conteúdo centrado máx 880 (formulário) + coluna de navegação de seções (esq, sticky).
- Inputs: altura 40, `surface/raised`, borda hairline → `border/strong` no foco + ring `focus/ring`.
- Required: label + "*" `accent/primary`. Erro: borda `state/danger` + mensagem `Caption` danger.
- Segmented PF/PJ; toggles para bloqueios; combobox com lista.
- Seção Condições comerciais: card destacado radius 12 borda `border/strong`.
- Barra de ações sticky: fundo `surface/sidebar`, botão primário laranja com glow.

## Checklist Nielsen
1. Visibilidade: validação inline, status do cliente no topo ✓
2. Mundo real: rótulos diretos, seções nomeadas ✓
3. Controle: Cancelar sempre visível; sem perda de dados ✓
4. Consistência: campos/botões do DS ✓
5. **Prevenção de erro**: obrigatórios, máscaras, ReceitaWS, confirmação ao sair sem salvar ✓
6. Reconhecimento: combobox em vez de códigos memorizados ✓
7. Eficiência: auto-preenchimento CNPJ/CEP, navegação por seções ✓
8. Minimalista: fiscal avançado recolhido por padrão ✓
