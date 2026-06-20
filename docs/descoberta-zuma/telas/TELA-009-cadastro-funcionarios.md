---
id: TELA-009
título: Cadastro de Funcionários
módulo: Funcionários / Vendedores
sistema: ZUMA
status: em-revisão
versão: 1.0.0
criado-em: 2025-06-19
atualizado-em: 2025-06-19
relacionado-com: RN-FNC-001 a RN-FNC-006, INS-001, FEAT-002, PROB-001
---

# Cadastro de Funcionários

## 1. Identificação

| Campo | Valor |
|---|---|
| Sistema | ZUMA ERP 9.25.2.2 |
| Módulo | Funcionários / Vendedores |
| Frequência de uso | Raramente |
| Usuários | Administrativo |
| Prioridade | **Importante** — MVP: **Sim (simplificado: apenas dados de vendedor)** |

---

## 2. Objetivo da Tela

Cadastrar funcionários e seus papéis, configurações de comissão, desconto máximo,
permissões de crédito e senha de acesso.

---

## 3. Caso Observado

- Funcionária: **POLYANNE RODRIGUES PIMENTEL**, cód. **39**, admissão **06/02/2023**.
- Comissão **Vista / Prazo / Devolução: 0,00%** (todos zerados).
- **"Vendedor Palm"** marcado — uso/histórico de dispositivo mobile.
- **Salário: R$ 0,00** — RH não é gerenciado pelo ZUMA.
- Papéis disponíveis: Vendedor, Indicador, Montador, Motorista, Conferente,
  Supervisor, Gerente.

---

## 4. Regras de Negócio

- **RN-FNC-001:** múltiplos papéis por funcionário.
- **RN-FNC-002 (❓):** "Vendedor Palm" indica uso de mobile.
- **RN-FNC-003:** senha do vendedor configurada aqui (controle de acesso centralizado).
- **RN-FNC-004:** salário zerado — módulo de RH não usado operacionalmente.
- **RN-FNC-005:** desconto máximo configurável por vendedor.
- **RN-FNC-006:** "Liber. Máx. Crédito (%)" é permissão por vendedor.

---

## 5. Problemas de UX

- **UX-003 (🔴):** campos de comissão zerados sem aviso.
- **UX-030 (🟡):** mistura dados operacionais (vendedor) com dados trabalhistas (RH).

---

## 6. Melhorias Possíveis (→ FEAT-002)

Cadastro de vendedor **simplificado** no MVP: nome, função, comissão à vista/prazo,
desconto máximo, liberação de crédito — **sem** campos trabalhistas/RH (fora do escopo).

---

## 7. Histórico de Versões

| Versão | Data | Mudanças |
|---|---|---|
| 1.0.0 | 2025-06-19 | Criação — comissão 0%, dados trabalhistas não usados |
