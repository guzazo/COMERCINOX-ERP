---
id: TELA-016
título: Romaneio de Entregas — Ordem de Entrega (ZumaRomaneio)
módulo: Logística / Entregas
sistema: ZUMA · ZumaRomaneio
status: em-revisão
versão: 1.0.0
criado-em: 2026-06-23
confiança-evidência: A
relacionado-com: TELA-011, RN-CMP, RN-CLI-009
---

# Romaneio de Entregas — Ordem de Entrega

## 1. Identificação
| Campo | Valor |
|---|---|
| Sistema | ZumaRomaneio (app separado) |
| Módulo | Logística / Entregas |
| Frequência | Diário |
| Usuários | Expedição / Logística / Motorista |
| Prioridade | **Fase 3** — MVP: **Não** (domínio logístico) |

## 2. Objetivo
Planejar e imprimir o romaneio de entregas: agrupar pré-vendas em **cargas/rotas**, definir
**veículo/motorista**, gerar **separação de carga** e acompanhar status de entrega.

## 3. Campos / Filtros
Carga · Data inicial/final · P.V. inicial/final · Cliente · Local · Estado · Município ·
Veículo · Motorista · Grupo · Local de Expedição · Período (Manhã/Tarde/Ambos) ·
status (Aberto/Cancelado/Devolvido/Baixado/Pendente/Recolhimento/Romaneio sem Carga).
Grid: Romaneio, Pré-venda, Cliente, Código, Descrição (produto), Unidade (KG/MT/PC/UN),
Município, Bairro.

## 4. Ações
Imprimir · Separação · Separação de Carga · Filtros · Rotas · opções de impressão
(peso bruto/líquido, endereço, valores, embalagens, assinatura, forma de pagamento).

## 5. Regras de negócio (novas)
- **RN-LOG-001:** entrega é gerada a partir da **pré-venda** (vínculo P.V. → romaneio → carga).
- **RN-LOG-002:** carga agrupa itens por **rota/veículo/motorista**.
- **RN-LOG-003:** unidades reais de venda: **KG, MT, PC, UN** (inox por peso e por barra).
- **RN-LOG-004:** status de entrega: Aberto/Baixado/Devolvido/Pendente/Recolhimento.
- **RN-LOG-005:** "Devolvido" no romaneio conecta-se à devolução fiscal (impacta comissão/estoque).

## 6. Dependências
Pré-venda (TELA-011) · Cliente/endereço (RN-CLI-009) · Motorista/Veículo · NF (devolução).

## 7. Problemas de UX / 8. Melhorias
Tela muito densa (muitos filtros e checkboxes de impressão). MVP não cobre logística; futura
gestão de entregas deve nascer ligada ao orçamento/pedido e ao status do cliente.

## 9. Histórico
| 1.0.0 | 2026-06-23 | Criação — domínio Logística/Entregas identificado |
