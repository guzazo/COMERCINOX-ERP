---
id: TELA-001
título: Cadastro de Clientes
módulo: Financeiro → A Receber → Clientes
sistema: ZUMA
status: em-revisão
versão: 1.0.0
criado-em: 2025-06-19
atualizado-em: 2025-06-19
relacionado-com: FEAT-001, RN-CLI-001 a RN-CLI-015, PROB-001
---

# Cadastro de Clientes

## 1. Identificação

| Campo | Valor |
|---|---|
| Sistema | ZUMA ERP 9.25.2.2 |
| Módulo | Financeiro → A Receber → Clientes |
| Caminho de acesso | Financeiro > A Receber > Clientes |
| Frequência de uso | Diário |
| Usuários | Comercial / Administrativo |
| Prioridade | **Crítica** — MVP: **Sim** |

---

## 2. Objetivo da Tela

Cadastrar e manter os dados de clientes (PF/PJ), contatos, endereços de entrega,
condições comerciais (vendedor, comissão, desconto, limite de crédito, bloqueios)
e a ficha financeira automática usada por todo o fluxo de vendas e cobrança.

---

## 3. Estrutura

- **46 campos mapeados** distribuídos em **3 abas** + tela de pesquisa.
- Abas: **Dados Cadastrais** / **Dados Complementares** / **Informações Adicionais**.
- Grid de **múltiplos contatos** (telefone, WhatsApp, e-mail).
- Grid de **múltiplos endereços de entrega** (um marcado como principal).
- **Ficha financeira automática:** primeira compra, última compra, maior compra,
  histórico de atrasos, limite de crédito.

---

## 4. Regras de Negócio (15)

RN-CLI-001 a RN-CLI-015 — ver [RN-MASTER-sprint01.md](../../regras-negocio/RN-MASTER-sprint01.md).
Destaques:

- **RN-CLI-007:** bloqueio para venda a prazo e para entrega são **independentes**.
- **RN-CLI-008:** campo "Observações" usado para flags como "ISENTO" (isenção fiscal).
- **RN-CLI-010:** sistema registra automaticamente histórico financeiro do cliente.
- **RN-CLI-015:** busca padrão usa **CNPJ/CPF**, não Nome (problema operacional).

---

## 5. Problemas de UX (10)

Ver [PROB-001-ux-sprint01.md](../../../research/problemas/PROB-001-ux-sprint01.md):
UX-005, UX-007, UX-008, UX-011, UX-012, UX-014, UX-017, UX-019, UX-023, UX-024.

Críticos (🔴):
- **UX-008:** título "[Contas à Receber] — Cadastro de clientes": cliente tratado como conceito financeiro.
- **UX-017:** busca padrão por CNPJ/CPF — vendedor busca por nome.
- **UX-019:** acesso enterrado em Financeiro → A Receber (problema de arquitetura de informação).

---

## 6. Melhorias Possíveis (12 → FEAT-001)

Acesso via menu CRM principal, busca por nome como padrão, validação de CNPJ/CPF com
ReceitaWS, auto-preenchimento por CEP, status do cliente como badge, segmento claro,
observações sempre visíveis, autocomplete nos campos de seleção. Ver
[FEAT-001-cadastro-clientes.md](../../../backlog/features/FEAT-001-cadastro-clientes.md).

---

## 7. Histórico de Versões

| Versão | Data | Mudanças |
|---|---|---|
| 1.0.0 | 2025-06-19 | Criação — 46 campos, 15 RN, 10 problemas UX, 12 melhorias |
