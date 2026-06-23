---
id: TELA-017-018
título: Fiscal — Emissor de NF (tipos de operação) e Consulta de NF
módulo: Fiscal
sistema: ZUMA · ZumaNF
status: em-revisão
versão: 1.0.0
criado-em: 2026-06-23
confiança-evidência: B (emissor) · C (consulta — borrão, validar)
relacionado-com: TELA-005, TELA-016, RN-VND-006
---

# Fiscal — Emissor e Consulta de NF (ZumaNF)

> **Permanece no ZUMA (nunca migra no horizonte do MVP — obrigação fiscal).** Documentado pelo
> impacto em estoque, devolução e comissão.

## TELA-017 — Emissor de Nota Fiscal · Inclusão
- **Objetivo:** emitir NF-e escolhendo a **natureza/operação**.
- **Tipos de operação observados (dropdown):** Saída por Venda(+), Devolução de Cliente,
  Correção de Estoque, Transferência, Devolução a Fornecedor — *(leitura parcial, confiança B)*.
- **Campos:** Código · Operação · Cliente · Endereço · Itens/Produto · Data Emissão · Data Saída ·
  Validação automática. Abas: Resolução, Pré-Visualizar.
- **RN-FIS-001:** a operação da NF define o efeito em **estoque** (venda −, devolução +, correção, transferência).
- **RN-FIS-002:** **Devolução de Cliente** é uma NF de entrada → reduz a base de venda/comissão (liga RN-VND-006).
- **RN-FIS-003:** Transferência move estoque entre **locais** (confirma RN-PRD-001, multi-localização).

## TELA-018 — NF · Emissão/Consulta  *(confiança C — validar)*
- **Hipótese:** tela de busca/consulta de notas emitidas (grid + filtros + atalhos F). Evidência
  borrada — **necessita nova captura** para detalhar campos.

## Dependências e MVP
Depende de Pré-venda/Pedido, Cliente, Produtos/Estoque. **Fora do MVP** (fiscal permanece no ZUMA).
Impacto no ERP: o conceito de **Devolução** precisa existir no modelo de domínio do Comercinox
porque afeta comissão e funil — mesmo sem emitir NF.

## Histórico
| 1.0.0 | 2026-06-23 | Criação — emissor de NF e tipos de operação; consulta com baixa confiança |
