---
id: INV-TELAS-001
título: Inventário de Telas — ZUMA ERP
status: em-revisão
versão: 1.1.0
criado-em: 2025
atualizado-em: 2025-06-19
---

# Inventário de Telas — ZUMA ERP

> **Objetivo:** Registrar todas as telas do ZUMA utilizadas pela Comercinox, seu status de mapeamento e prioridade para substituição.

---

## Legenda de Status

| Status | Significado |
|---|---|
| 🔴 Não mapeado | Tela identificada mas ainda não documentada |
| 🟡 Em mapeamento | Documentação em progresso |
| 🟢 Mapeado | Documentação completa e aprovada |
| ⚫ Não utilizado | Tela do ZUMA não usada pela Comercinox |

## Legenda de Prioridade de Substituição

| Prioridade | Significado |
|---|---|
| 🔥 Alta | Substituir no MVP |
| ⚡ Média | Substituir na Fase 3 |
| 💤 Baixa | Manter no ZUMA por mais tempo |
| 🚫 Nunca | Não substituir (ex: obrigações fiscais) |

---

## ✅ Telas Mapeadas na Sprint 01 (10 de ~24)

| ID | Tela | Módulo no ZUMA | Prioridade | MVP | Arquivo |
|---|---|---|---|---|---|
| TELA-001 | Cadastro de Clientes | Financeiro → A Receber | 🔥 Crítica | Sim | [TELA-001](telas/TELA-001-cadastro-clientes.md) |
| TELA-002 | Tela Inicial (Home) | Sistema | ⚡ Importante | Sim (dashboard) | [TELA-002](telas/TELA-002-tela-inicial.md) |
| TELA-003 | Cadastro de Produtos | Estoque | ⚡ Importante | Não (ZUMA) | [TELA-003](telas/TELA-003-cadastro-produtos.md) |
| TELA-004 | Pesquisa de Produtos | Estoque | 🔥 Crítica | Sim (consulta) | [TELA-004](telas/TELA-004-pesquisa-produtos.md) |
| TELA-005 | Entrada de Pedido de Compra | Compras | ⚡ Importante | Não (ZUMA) | [TELA-005](telas/TELA-005-entrada-pedido-compra.md) |
| TELA-006 | Pesquisa de Pedido de Compra | Compras | ⚡ Importante | Não (ZUMA) | [TELA-006](telas/TELA-006-pesquisa-pedido-compra.md) |
| TELA-007 | Demonstrativo de Saldos | Vendas | 🔥 Crítica | Sim (dashboard) | [TELA-007](telas/TELA-007-demonstrativo-saldos-vendedores.md) |
| TELA-008 | Extrato por Vendedor | Vendas | 🔥 Crítica | Sim (histórico) | [TELA-008](telas/TELA-008-extrato-vendedor.md) |
| TELA-009 | Cadastro de Funcionários | Funcionários | ⚡ Importante | Sim (simplificado) | [TELA-009](telas/TELA-009-cadastro-funcionarios.md) |
| TELA-010 | Estrutura Menu Vendas | Vendas | ⚡ Importante | Referência | [TELA-010](telas/TELA-010-menu-vendas-estrutura.md) |

---

## Módulo: Comercial / CRM

| # | Tela | Frequência de Uso | Status | Prioridade | Arquivo |
|---|---|---|---|---|---|
| 1 | Cadastro de Clientes | Diário | 🔴 | 🔥 | [TELA-001](../docs/descoberta-zuma/) |
| 2 | Histórico de Compras por Cliente | Diário | 🔴 | 🔥 | — |
| 3 | Controle de Vendas / Comissão | Diário | 🔴 | 🔥 | — |
| 4 | Orçamentos | Diário | 🔴 | 🔥 | — |
| 5 | Pré-Venda (ZUMA-PDV) | ? | 🔴 | ? | — |

---

## Módulo: Estoque

| # | Tela | Frequência de Uso | Status | Prioridade | Arquivo |
|---|---|---|---|---|---|
| 6 | Controle de Estoque | Diário | 🔴 | 💤 | — |
| 7 | Entrada de Produtos | Diário | 🔴 | 💤 | — |
| 8 | Saída de Produtos | Diário | 🔴 | 💤 | — |
| 9 | Análise de Giro de Produtos | Semanal | 🔴 | ⚡ | — |
| 10 | Ranking de Produtos | Mensal | 🔴 | ⚡ | — |

---

## Módulo: Financeiro

| # | Tela | Frequência de Uso | Status | Prioridade | Arquivo |
|---|---|---|---|---|---|
| 11 | Contas a Receber | Diário | 🔴 | 💤 | — |
| 12 | Contas a Pagar | Diário | 🔴 | 💤 | — |
| 13 | Controle Bancário | Semanal | 🔴 | 💤 | — |
| 14 | Ficha Financeira do Cliente | Semanal | 🔴 | ⚡ | — |
| 15 | Análise de Inadimplência | Mensal | 🔴 | ⚡ | — |
| 16 | Previsão Financeira | Mensal | 🔴 | 💤 | — |

---

## Módulo: Fiscal

| # | Tela | Frequência de Uso | Status | Prioridade | Arquivo |
|---|---|---|---|---|---|
| 17 | Emissão de NF-e | Diário | 🔴 | 🚫 | — |
| 18 | Emissão de NFC-e | ? | 🔴 | 🚫 | — |
| 19 | Livros Fiscais | Mensal | 🔴 | 🚫 | — |
| 20 | SPED Fiscal | Mensal | 🔴 | 🚫 | — |

---

## Módulo: Relatórios Gerenciais

| # | Tela | Frequência de Uso | Status | Prioridade | Arquivo |
|---|---|---|---|---|---|
| 21 | Desempenho de Vendas | Semanal | 🔴 | ⚡ | — |
| 22 | Meta de Vendas | Mensal | 🔴 | ⚡ | — |
| 23 | Margem de Contribuição | Mensal | 🔴 | ⚡ | — |
| 24 | Análise de Venda por Cliente | Mensal | 🔴 | ⚡ | — |

---

## Telas Não Utilizadas (confirmadas após entrevistas)

| # | Tela | Motivo de Não Uso |
|---|---|---|
| — | [Preencher após entrevistas] | |

---

## Resumo

| Categoria | Quantidade |
|---|---|
| Total de telas identificadas | 24 (estimativa inicial) |
| Telas mapeadas | 10 |
| Telas em mapeamento | 0 |
| Telas não utilizadas | ? |
| Telas com prioridade Crítica (MVP) | 4 (TELA-001, 004, 007, 008) |

---

> ⚠️ Este inventário é uma **estimativa inicial** baseada nos módulos do ZUMA.
> A frequência de uso real e as telas não utilizadas serão validadas nas entrevistas da SPRINT-01.

---

## Histórico de Versões

| Versão | Data | Mudanças |
|---|---|---|
| 1.0.0 | 2025 | Criação do inventário inicial (pré-entrevistas) |
| 1.1.0 | 2025-06-19 | Sprint 01 — 10 telas mapeadas (TELA-001 a TELA-010) |
