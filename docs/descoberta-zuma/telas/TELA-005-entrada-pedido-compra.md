---
id: TELA-005
título: Entrada de Pedido de Compra
módulo: Compras
sistema: ZUMA
status: em-revisão
versão: 1.0.0
criado-em: 2025-06-19
atualizado-em: 2025-06-19
relacionado-com: RN-CMP-001 a RN-CMP-007, TELA-006
---

# Entrada de Pedido de Compra

## 1. Identificação

| Campo | Valor |
|---|---|
| Sistema | ZUMA ERP 9.25.2.2 |
| Módulo | Compras |
| Frequência de uso | Diário |
| Usuários | Compras (BRENDO) |
| Prioridade | **Importante** — MVP: **Não (permanece no ZUMA)** |

---

## 2. Objetivo da Tela

Registrar a entrada de mercadoria a partir da nota fiscal do fornecedor, importando
o XML da NF-e para o pedido de compra.

---

## 3. Caso Observado

- **Pedido 355** — fornecedor **BLACK DECKER**, NF **2421365**, status **BAIXADO**.
- Criado por **BRENDO**, responsável **WANDERSON**.
- **Importação de XML de NF-e confirmada.**
- Frete **CIF** (por conta do remetente) como padrão.
- "Sem Recálculo de ST" como exceção fiscal aplicável por entrada.

---

## 4. Regras de Negócio

- **RN-CMP-001:** entrada exige nota fiscal do fornecedor (campo NF obrigatório).
- **RN-CMP-002:** XML da NF-e é importado para o pedido de compra.
- **RN-CMP-003:** frete CIF é o padrão.
- **RN-CMP-004:** BRENDO é o responsável por lançar compras.
- **RN-CMP-007:** "Sem Recálculo de ST" é exceção fiscal por entrada.

---

## 5. Decisão de Escopo

Processo de compras com forte componente fiscal (XML NF-e, ST) **permanece no ZUMA**.
Fora do MVP do ERP Comercialinox.

---

## 6. Histórico de Versões

| Versão | Data | Mudanças |
|---|---|---|
| 1.0.0 | 2025-06-19 | Criação — pedido 355, importação XML confirmada |
