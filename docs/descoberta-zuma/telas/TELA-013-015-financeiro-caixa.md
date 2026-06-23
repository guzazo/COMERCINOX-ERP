---
id: TELA-013-015
título: Financeiro — Fluxo/Previsão, Manutenção e Consistência do Caixa
módulo: Financeiro
sistema: ZUMA_ERP (Caixa Geral / Rotinas padrões)
status: em-revisão
versão: 1.0.0
criado-em: 2026-06-23
confiança-evidência: A (fluxo) · B (caixa)
relacionado-com: TELA-011 (pré-venda financeiro), RN-VND-004
---

# Financeiro — Fluxo, Caixa e Consistência

> Três telas do domínio Financeiro descobertas na auditoria 2026-06-23. **Permanecem no ZUMA
> no MVP** (financeiro oficial é Fase 4). Documentadas para o modelo de domínio e dependências.

## TELA-013 — Fluxo Financeiro / Previsão  (Rotinas padrões)
- **Objetivo:** projeção de caixa por dia e por faixa (0–30 / 31–61 / 62–92 dias).
- **Período por:** Emissão ou **Vencimento**; Inicial/Final; Local.
- **Considera:** Contas a receber, Cheques pré-datados, Faturamento, Cartão de crédito,
  Contas a pagar, Cheques a pagar, **Pedidos a prazo**.
- **Grid:** Data · C. receber · Cheques · Faturam. · Cartão · C. pagar · Cheques p. · Pedidos ·
  Diferença · Saldo.
- **Valores observados:** Contas a receber R$ 325.730,19 · Cartão R$ 112.801,03 ·
  Contas a pagar R$ 546.211,70 · Cheques a receber R$ 1.833,34.
- **RN-FIN-001:** "Pedidos a prazo" entram na previsão → o **pedido a prazo é compromisso financeiro**.
- **RN-FIN-002:** previsão considera saldo de estoque (opcional) e meses anteriores/posteriores.

## TELA-014 — Manutenção do Caixa  (Caixa Geral)
- **Objetivo:** lançar/abrir/estornar movimentos de caixa (entrada/saída).
- **Campos:** Nº Documento · Ocor. · Local · Tipo · Data · **Movimento (E/S)** · Histórico ·
  Complemento · Forma de Pagamento · Valor · Funcionário.
- **Ações:** Incluir · Alterar · **Abertura** · Consist. · **Transf.** · **Estornar** · Opções.
- **Opções:** Forma de Pagamento, Detalhes, Controle Caixa, **Pré-venda Financeiro**,
  Excluir Lançamento, Cancelar Pré-venda Financeiro.
- **RN-FIN-003:** caixa tem **abertura** e movimentos E/S por forma de pagamento.
- **RN-FIN-004:** **Pré-venda Financeiro** vincula a pré-venda (TELA-011) ao caixa → recebimento.

## TELA-015 — Consistência Financeira  (Caixa Geral)
- **Objetivo:** conferir/auditar lançamentos do caixa por período, forma e movimento.
- **Filtros:** Nº Documento · Usuário (GUILHERME) · Funcionário · Data inicial/final ·
  Forma de Pagamento (À Vista/À Prazo/Todos) · Movimento (Entrada/Saída/Todos).
- **Totais:** Total de Entradas, Estorno (Entradas), Total de Saídas, Estorno (Saídas), Total Geral.
- **RN-FIN-005:** conciliação considera estornos separadamente (entradas e saídas).

## Dependências e MVP
Dependem de Pré-venda (recebimento) e Formas de pagamento. **Fora do MVP** (financeiro fica no
ZUMA — Fase 4). Relevância para o ERP Comercinox: **dashboard pode *ler* recebíveis/previsão**
no futuro (Fase 3), sem gerir o financeiro.

## Histórico
| 1.0.0 | 2026-06-23 | Criação — domínio Financeiro/Caixa documentado |
