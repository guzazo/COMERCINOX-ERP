---
id: TELA-006
título: Pesquisa de Pedido de Compra
módulo: Compras
sistema: ZUMA
status: em-revisão
versão: 1.0.0
criado-em: 2025-06-19
atualizado-em: 2025-06-19
relacionado-com: RN-CMP-004 a RN-CMP-006, TELA-005
---

# Pesquisa de Pedido de Compra

## 1. Identificação

| Campo | Valor |
|---|---|
| Sistema | ZUMA ERP 9.25.2.2 |
| Módulo | Compras |
| Frequência de uso | Diário / Semanal |
| Usuários | Compras / Administrativo |
| Prioridade | **Importante** — MVP: **Não (permanece no ZUMA)** |

---

## 2. Objetivo da Tela

Consultar o histórico de pedidos de compra por fornecedor, situação, data e produto.

---

## 3. Dados Observados

- **Volume histórico total de compras: R$ 33.009.033,06.**
- Fornecedor dominante: **APERAM INOX SERVICOS BRASIL**.
- **Filtros:** Fornecedor · Situação (Aberto / Baixado / Cancelado) · Data · Produto.

---

## 4. Regras de Negócio

- **RN-CMP-004:** BRENDO é o usuário responsável por lançar compras.
- **RN-CMP-005:** APERAM INOX SERVICOS BRASIL é o fornecedor dominante.
- **RN-CMP-006:** volume histórico total de compras: R$ 33.009.033,06.

---

## 5. Decisão de Escopo

Permanece no ZUMA. Relevante como **fonte de dados** para futura análise de
fornecedores e curva ABC de compras (fora do MVP).

---

## 6. Histórico de Versões

| Versão | Data | Mudanças |
|---|---|---|
| 1.0.0 | 2025-06-19 | Criação — R$ 33M histórico, APERAM dominante |
