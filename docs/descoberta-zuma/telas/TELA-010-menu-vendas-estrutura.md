---
id: TELA-010
título: Estrutura do Menu Físico → Vendas
módulo: Vendas / Comercial
sistema: ZUMA
status: em-revisão
versão: 1.0.0
criado-em: 2025-06-19
atualizado-em: 2025-06-19
relacionado-com: RN-VND-008, RN-VND-009, INS-001
---

# Estrutura do Menu Físico → Vendas

## 1. Identificação

| Campo | Valor |
|---|---|
| Sistema | ZUMA ERP 9.25.2.2 |
| Módulo | Físico → Vendas |
| Frequência de uso | Diário |
| Usuários | Comercial / Administrativo |
| Prioridade | **Importante** — MVP: **Referência de arquitetura** |

---

## 2. Objetivo da Tela

Mapear a estrutura completa do menu de Vendas do ZUMA para entender quais funções
existem, quais são usadas e quais estão desabilitadas.

---

## 3. Achados

- Estrutura completa do menu **Físico → Vendas** mapeada.
- **"Metas de vendas" desabilitado** — confirma que metas vivem no **Excel**.
- Relatórios efetivamente usados: **Demonstrativo de Saldos** (TELA-007) e
  **Extrato por Vendedor** (TELA-008).
- Existe tipo **"Indicador Externo"** de comissionado além do vendedor padrão.

---

## 4. Regras de Negócio

- **RN-VND-008:** "Metas de vendas" desabilitado — metas gerenciadas em Excel.
- **RN-VND-009:** existe tipo "Indicador Externo" de comissionado.

---

## 5. Relação com INS-001

Reforça a 4ª evidência de [INS-001](../../../research/insights/INS-001-comissao-excel-processo-critico.md):
tanto comissão quanto metas estão fora do ZUMA, em planilhas.

---

## 6. Uso como Referência

Serve de referência de arquitetura para o módulo comercial do ERP Comercialinox:
quais relatórios manter, quais funções nativar (metas, comissão) e quais papéis de
comissionamento contemplar.

---

## 7. Histórico de Versões

| Versão | Data | Mudanças |
|---|---|---|
| 1.0.0 | 2025-06-19 | Criação — metas desabilitadas, estrutura mapeada |
