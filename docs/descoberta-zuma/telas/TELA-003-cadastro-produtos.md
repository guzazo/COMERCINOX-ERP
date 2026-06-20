---
id: TELA-003
título: Cadastro de Produtos
módulo: Estoque / Produtos
sistema: ZUMA
status: em-revisão
versão: 1.0.0
criado-em: 2025-06-19
atualizado-em: 2025-06-19
relacionado-com: RN-PRD-001 a RN-PRD-006, FEAT-003, PROB-001
---

# Cadastro de Produtos

## 1. Identificação

| Campo | Valor |
|---|---|
| Sistema | ZUMA ERP 9.25.2.2 |
| Módulo | Estoque / Produtos |
| Frequência de uso | Diário |
| Usuários | Estoque / Administrativo |
| Prioridade | **Importante** — MVP: **Não (permanece no ZUMA)** |

---

## 2. Objetivo da Tela

Cadastrar produtos e gerir preços/estoque por localização. A aba **Preços/Estoque**
mostra saldo por depósito e as duas tabelas de preço (REVENDA e CONSUMIDOR).

---

## 3. Estrutura

- Aba **Preços/Estoque** com **4 localizações** (depósitos 1, 2, 5, 10).
- Tabelas de preço: **REVENDA** e **CONSUMIDOR**.
- Preço a prazo (REVENDA) ~15% maior que à vista: **R$ 37,62 vs R$ 32,71**.
- CST PIS/COFINS e MVA por localização (linguagem fiscal no grid operacional).
- "Aguarde... Preparando dados" sem barra de progresso.

---

## 4. ⚠️ Descoberta Crítica

**Estoque negativo permitido sem bloqueio.** Produto observado com **-116,52 KG**
em uma localização e **saldo total de -17,64 KG**, sem qualquer alerta visual. O
sistema não impede venda com saldo negativo.

---

## 5. Regras de Negócio

- **RN-PRD-001:** saldo por localização — mínimo 4 locais.
- **RN-PRD-002 (⚠️):** estoque negativo PERMITIDO — sem bloqueio.
- **RN-PRD-003:** duas tabelas de preço — REVENDA e CONSUMIDOR.
- **RN-PRD-004:** prazo ~15% mais caro que à vista.
- **RN-PRD-005:** CST PIS/COFINS varia por localização.
- **RN-PRD-006:** estoque mínimo = zero — sem alertas de reposição.

---

## 6. Problemas de UX

- **UX-002 (🔴):** estoque negativo sem destaque visual.
- **UX-004 (🔴):** saldo total negativo sem contexto de criticidade.
- **UX-006 (🟡):** "Aguarde..." sem barra de progresso.
- **UX-009 (🟡):** linguagem fiscal (CST/MVA) misturada na tela operacional.

---

## 7. Decisão de Escopo

Cadastro de produto **permanece no ZUMA** no MVP. O ERP Comercialinox apenas
**consulta** o catálogo para orçamentos (ver
[FEAT-003](../../../backlog/features/FEAT-003-consulta-catalogo-produtos.md)),
exibindo alerta visual obrigatório quando saldo ≤ 0.

---

## 8. Histórico de Versões

| Versão | Data | Mudanças |
|---|---|---|
| 1.0.0 | 2025-06-19 | Criação — estoque negativo sem bloqueio documentado |
