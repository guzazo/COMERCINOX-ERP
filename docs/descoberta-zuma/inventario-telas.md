---
id: INV-TELAS-001
título: Inventário de Telas — ZUMA ERP
status: rascunho
versão: 1.0.0
criado-em: 2025
atualizado-em: 2025
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
| Telas mapeadas | 0 |
| Telas em mapeamento | 0 |
| Telas não utilizadas | ? |
| Telas com prioridade Alta | ? |

---

> ⚠️ Este inventário é uma **estimativa inicial** baseada nos módulos do ZUMA.
> A frequência de uso real e as telas não utilizadas serão validadas nas entrevistas da SPRINT-01.

---

## Histórico de Versões

| Versão | Data | Mudanças |
|---|---|---|
| 1.0.0 | 2025 | Criação do inventário inicial (pré-entrevistas) |
