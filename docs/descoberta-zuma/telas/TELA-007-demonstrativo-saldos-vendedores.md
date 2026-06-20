---
id: TELA-007
título: Demonstrativo de Saldos de Vendedores
módulo: Vendas / Comercial
sistema: ZUMA
status: em-revisão
versão: 1.0.0
criado-em: 2025-06-19
atualizado-em: 2025-06-19
relacionado-com: RN-VND-001 a RN-VND-006, INS-001, FEAT-002, PROB-001
---

# Demonstrativo de Saldos de Vendedores

## 1. Identificação

| Campo | Valor |
|---|---|
| Sistema | ZUMA ERP 9.25.2.2 |
| Módulo | Físico → Vendas → Demonstrativo de Saldos |
| Frequência de uso | Semanal / Mensal |
| Usuários | Proprietário / Administrativo |
| Prioridade | **Crítica** — MVP: **Sim (dashboard com comissão calculada)** |

---

## 2. Objetivo da Tela

Relatório consolidado de vendas líquidas por vendedor no período. Deveria mostrar
comissão — mas a comissão aparece **zerada**.

---

## 3. ⚠️ Descoberta Crítica

**Comissão zerada para ambos os vendedores.** Confirma que a comissão é calculada
fora do ZUMA, em Excel (ver [INS-001](../../../research/insights/INS-001-comissao-excel-processo-critico.md)).

---

## 4. Dados Observados (01–19/jun/2026)

| Vendedor | Venda Líquida | Devoluções |
|---|---|---|
| ANDERSON TARGINO (cód. 2) | R$ 102.298,76 | — |
| POLYANNE PIMENTEL (cód. 39) | R$ 94.973,25 | R$ 8.223,60 |
| **Total líquido** | **R$ 197.272,01** | |

- **Venda a prazo: ~87% do volume.**

---

## 5. Regras de Negócio

- **RN-VND-001 (⚠️):** comissão NÃO é gerenciada pelo ZUMA — campos zerados.
- **RN-VND-003:** vendedores ativos = ANDERSON TARGINO e POLYANNE PIMENTEL.
- **RN-VND-004:** venda a prazo dominante (~87%).
- **RN-VND-006:** devoluções descontadas da venda líquida para comissão.

---

## 6. Problemas de UX

- **UX-003 (🔴):** comissão zerada sem aviso — parece correto.
- **UX-027 (🔴):** relatórios manuais sem visão em tempo real.

---

## 7. Melhorias Possíveis (→ FEAT-002)

Dashboard em tempo real com ranking de vendedores, venda líquida e **comissão
calculada automaticamente** (descontando devoluções), substituindo o relatório manual.

---

## 8. Histórico de Versões

| Versão | Data | Mudanças |
|---|---|---|
| 1.0.0 | 2025-06-19 | Criação — comissão zerada confirmada, R$ 197K líquido |
