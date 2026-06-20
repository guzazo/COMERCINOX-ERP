---
id: INV-PROC-001
título: Inventário de Processos Operacionais — Comercinox
origem: Engenharia reversa ZUMA ERP 9.25.2.2 (Sprint 01)
status: rascunho
versão: 1.0.0
criado-em: 2025-06-19
telas-fonte: TELA-001 a TELA-010
---

# Inventário de Processos Operacionais — Comercinox

> 42 processos operacionais identificados na Sprint 01, distribuídos em 8 áreas e
> priorizados por fase de substituição do ERP. Derivados das 10 telas mapeadas do ZUMA.
>
> ⚠️ O detalhamento AS-IS de cada processo (template `processo.md`) será produzido
> nas entrevistas da Sprint 01. Este inventário é o índice priorizado.

---

## Legenda

| Fase | Significado |
|---|---|
| 🔥 MVP | Substituir / nativar no MVP do ERP Comercialinox |
| ⚡ Fase 3 | Substituir em fase posterior |
| 💤 ZUMA | Permanece no ZUMA por mais tempo |
| 🚫 Fiscal | Obrigação fiscal — não substituir |

| Criticidade | 🔴 Alta · 🟡 Média · 🟢 Baixa |
|---|---|

---

## Área 1 — Comercial / CRM

| # | Processo | Fase | Criticidade | Tela-fonte |
|---|---|---|---|---|
| P-01 | Cadastrar novo cliente | 🔥 MVP | 🔴 | TELA-001 |
| P-02 | Atualizar dados / status de cliente | 🔥 MVP | 🔴 | TELA-001 |
| P-03 | Consultar histórico de compras do cliente | 🔥 MVP | 🔴 | TELA-001 |
| P-04 | Bloquear/desbloquear cliente (prazo/entrega) | 🔥 MVP | 🔴 | TELA-001 |
| P-05 | Classificar cliente no funil (frio→recorrente) | 🔥 MVP | 🟡 | TELA-001 |
| P-06 | Qualificar e acompanhar lead | ⚡ Fase 3 | 🟡 | — |

---

## Área 2 — Orçamentos / Pré-venda

| # | Processo | Fase | Criticidade | Tela-fonte |
|---|---|---|---|---|
| P-07 | Consultar produto e preço para orçar | 🔥 MVP | 🔴 | TELA-004 |
| P-08 | Selecionar tabela de preço pelo perfil do cliente | 🔥 MVP | 🔴 | TELA-003/004 |
| P-09 | Montar orçamento | 🔥 MVP | 🔴 | — |
| P-10 | Enviar orçamento (WhatsApp / e-mail) | 🔥 MVP | 🔴 | — |
| P-11 | Acompanhar status do orçamento | 🔥 MVP | 🟡 | — |
| P-12 | Converter orçamento em venda | ⚡ Fase 3 | 🔴 | — |

---

## Área 3 — Vendas

| # | Processo | Fase | Criticidade | Tela-fonte |
|---|---|---|---|---|
| P-13 | Registrar venda | 💤 ZUMA | 🔴 | TELA-008 |
| P-14 | Registrar venda a prazo (fluxo padrão, ~87%) | 💤 ZUMA | 🔴 | TELA-007 |
| P-15 | Registrar devolução | 💤 ZUMA | 🟡 | TELA-007/008 |
| P-16 | Aplicar desconto dentro do teto do vendedor | 🔥 MVP | 🟡 | TELA-009 |
| P-17 | Consultar extrato de vendas por vendedor | 🔥 MVP | 🔴 | TELA-008 |
| P-18 | Acompanhar metas de vendas | 🔥 MVP | 🔴 | TELA-010 |

---

## Área 4 — Comissão

| # | Processo | Fase | Criticidade | Tela-fonte |
|---|---|---|---|---|
| P-19 | Apurar venda líquida do período por vendedor | 🔥 MVP | 🔴 | TELA-007 |
| P-20 | Descontar devoluções da base de comissão | 🔥 MVP | 🔴 | TELA-007 |
| P-21 | Calcular comissão (hoje em Excel) | 🔥 MVP | 🔴 | INS-001 |
| P-22 | Gerar relatório de comissão mensal | 🔥 MVP | 🔴 | INS-001 |
| P-23 | Comissionar "Indicador Externo" | ⚡ Fase 3 | 🟡 | TELA-010 |

---

## Área 5 — Estoque / Produtos

| # | Processo | Fase | Criticidade | Tela-fonte |
|---|---|---|---|---|
| P-24 | Cadastrar produto | 💤 ZUMA | 🟡 | TELA-003 |
| P-25 | Manter preço por tabela (REVENDA/CONSUMIDOR) | 💤 ZUMA | 🔴 | TELA-003 |
| P-26 | Consultar saldo por localização | 🔥 MVP | 🔴 | TELA-003/004 |
| P-27 | Sincronizar/importar catálogo para o ERP | 🔥 MVP | 🔴 | TELA-004 |
| P-28 | Alertar estoque ≤ 0 | 🔥 MVP | 🔴 | TELA-003 |
| P-29 | Analisar giro / ranking de produtos | ⚡ Fase 3 | 🟡 | — |

---

## Área 6 — Compras

| # | Processo | Fase | Criticidade | Tela-fonte |
|---|---|---|---|---|
| P-30 | Lançar pedido de compra | 💤 ZUMA | 🔴 | TELA-005 |
| P-31 | Importar XML da NF-e do fornecedor | 💤 ZUMA | 🔴 | TELA-005 |
| P-32 | Dar entrada / baixa no pedido | 💤 ZUMA | 🔴 | TELA-005 |
| P-33 | Consultar histórico de compras por fornecedor | 💤 ZUMA | 🟡 | TELA-006 |
| P-34 | Analisar fornecedores (curva ABC) | ⚡ Fase 3 | 🟡 | TELA-006 |

---

## Área 7 — Financeiro

| # | Processo | Fase | Criticidade | Tela-fonte |
|---|---|---|---|---|
| P-35 | Gerir ficha financeira do cliente | 💤 ZUMA | 🔴 | TELA-001 |
| P-36 | Emitir boleto | 💤 ZUMA | 🔴 | TELA-002 |
| P-37 | Controlar recebimentos / grade de pagamentos | 💤 ZUMA | 🔴 | TELA-002 |
| P-38 | Acompanhar limite de crédito do cliente | ⚡ Fase 3 | 🔴 | TELA-001 |
| P-39 | Analisar inadimplência | ⚡ Fase 3 | 🟡 | — |

---

## Área 8 — Sistema / Administração

| # | Processo | Fase | Criticidade | Tela-fonte |
|---|---|---|---|---|
| P-40 | Cadastrar vendedor / funcionário | 🔥 MVP | 🔴 | TELA-009 |
| P-41 | Gerir acesso (senha, permissões, crédito) | 🔥 MVP | 🔴 | TELA-009 |
| P-42 | Acompanhar indicadores do negócio (dashboard) | 🔥 MVP | 🔴 | TELA-002 |

---

## Resumo

| Área | Processos | MVP 🔥 |
|---|---|---|
| 1. Comercial / CRM | 6 | 5 |
| 2. Orçamentos / Pré-venda | 6 | 5 |
| 3. Vendas | 6 | 3 |
| 4. Comissão | 5 | 4 |
| 5. Estoque / Produtos | 6 | 4 |
| 6. Compras | 5 | 0 |
| 7. Financeiro | 5 | 0 |
| 8. Sistema / Administração | 3 | 3 |
| **TOTAL** | **42** | **24** |

---

## Histórico de Versões

| Versão | Data | Mudanças |
|---|---|---|
| 1.0.0 | 2025-06-19 | Criação — 42 processos em 8 áreas, priorizados por fase |
