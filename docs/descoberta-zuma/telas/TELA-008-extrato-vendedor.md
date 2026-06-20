---
id: TELA-008
título: Extrato por Vendedor
módulo: Vendas / Comercial
sistema: ZUMA
status: em-revisão
versão: 1.0.0
criado-em: 2025-06-19
atualizado-em: 2025-06-19
relacionado-com: RN-VND-001 a RN-VND-007, INS-001, FEAT-002, PROB-001
---

# Extrato por Vendedor

## 1. Identificação

| Campo | Valor |
|---|---|
| Sistema | ZUMA ERP 9.25.2.2 |
| Módulo | Físico → Vendas → Extrato por Vendedor |
| Frequência de uso | Semanal / Mensal |
| Usuários | Proprietário / Administrativo |
| Prioridade | **Crítica** — MVP: **Sim (histórico de vendas com comissão)** |

---

## 2. Objetivo da Tela

Listar venda a venda os lançamentos de um vendedor no período, com data, hora,
cliente e valores.

---

## 3. Dados Observados (POLYANNE, 01–19/jun/2026)

| Métrica | Valor |
|---|---|
| Vendas no período | **137** (19 dias, ~7/dia) |
| Total bruto | R$ 205.495,61 |
| Devoluções | R$ 8.223,60 |
| **Líquido** | **R$ 197.272,01** |
| Comissão | **Zerada em todos os lançamentos** |

- Campo "Descrição" mistura código + nome do cliente: "78613 LUCIANO RANGEL".
- Hora exata de cada venda é registrada.
- 15+ filtros disponíveis; uso real = vendedor + período.

---

## 4. Regras de Negócio

- **RN-VND-002 (⚠️):** cálculo de comissão feito em Excel externo.
- **RN-VND-007:** hora exata de cada venda é registrada.

---

## 5. Problemas de UX

- **UX-003 (🔴):** comissão zerada sem aviso.
- **UX-013 (🟡):** código + nome do cliente num só campo.
- **UX-025 (🔴):** filtro por cliente exige código numérico, não aceita nome.
- **UX-026 (🟡):** 15+ filtros, uso real = vendedor + período.

---

## 6. Melhorias Possíveis (→ FEAT-002)

Histórico de vendas por vendedor com comissão calculada por lançamento, colunas
separadas (código / nome), busca de cliente por nome, filtros avançados colapsáveis.

---

## 7. Histórico de Versões

| Versão | Data | Mudanças |
|---|---|---|
| 1.0.0 | 2025-06-19 | Criação — 137 vendas, comissão zerada em todos |
