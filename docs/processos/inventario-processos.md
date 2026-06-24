---
id: INV-PROC-001
título: Inventário de Processos Operacionais — Comercinox
origem: Engenharia reversa ZUMA ERP 9.25.2.2 (Sprint 01)
status: rascunho
versão: 1.0.0
criado-em: 2025-06-19
telas-fonte: TELA-001 a TELA-010
---

# Inventário de Processos Operacionais — Comercinox

> 42 processos operacionais identificados na Sprint 01, distribuídos em 8 áreas e
> priorizados por fase de substituição do ERP. Derivados das 10 telas mapeadas do ZUMA.
>
> ⚠️ O detalhamento AS-IS de cada processo (template `processo.md`) será produzido
> nas entrevistas da Sprint 01. Este inventário é o índice priorizado.

---

## Legenda

| Fase | Significado |
|---|---|
| 🔥 MVP | Substituir / nativar no MVP do ERP Comercialinox |
| ⚡ Fase 3 | Substituir em fase posterior |
| 💤 ZUMA | Permanece no ZUMA por mais tempo |
| 🚫 Fiscal | Obrigação fiscal — não substituir |

| Criticidade | 🔴 Alta · 🟡 Média · 🟢 Baixa |
|---|---|

---

## Área 1 — Comercial / CRM

| # | Processo | Fase | Criticidade | Tela-fonte |
|---|---|---|---|---|
| P-01 | Cadastrar novo cliente | 🔥 MVP | 🔴 | TELA-001 |
| P-02 | Atualizar dados / status de cliente | 🔥 MVP | 🔴 | TELA-001 |
| P-03 | Consultar histórico de compras do cliente | 🔥 MVP | 🔴 | TELA-001 |
| P-04 | Bloquear/desbloquear cliente (prazo/entrega) | 🔥 MVP | 🔴 | TELA-001 |
| P-05 | Classificar cliente no funil (frio→recorrente) | 🔥 MVP | 🟡 | TELA-001 |
| P-06 | Qualificar e acompanhar lead | ⚡ Fase 3 | 🟡 | — |

---

## Área 2 — Orçamentos / Pré-venda

| # | Processo | Fase | Criticidade | Tela-fonte |
|---|---|---|---|---|
| P-07 | Consultar produto e preço para orçar | 🔥 MVP | 🔴 | TELA-004 |
| P-08 | Selecionar tabela de preço pelo perfil do cliente | 🔥 MVP | 🔴 | TELA-003/004 |
| P-09 | Montar orçamento | 🔥 MVP | 🔴 | — |
| P-10 | Enviar orçamento (WhatsApp / e-mail) | 🔥 MVP | 🔴 | — |
| P-11 | Acompanhar status do orçamento | 🔥 MVP | 🟡 | — |
| P-12 | Converter orçamento em venda | ⚡ Fase 3 | 🔴 | — |

---

## Área 3 — Vendas

| # | Processo | Fase | Criticidade | Tela-fonte |
|---|---|---|---|---|
| P-13 | Registrar venda | 💤 ZUMA | 🔴 | TELA-008 |
| P-14 | Registrar venda a prazo (fluxo padrão, ~87%) | 💤 ZUMA | 🔴 | TELA-007 |
| P-15 | Registrar devolução | 💤 ZUMA | 🟡 | TELA-007/008 |
| P-16 | Aplicar desconto dentro do teto do vendedor | 🔥 MVP | 🟡 | TELA-009 |
| P-17 | Consultar extrato de vendas por vendedor | 🔥 MVP | 🔴 | TELA-008 |
| P-18 | Acompanhar metas de vendas | 🔥 MVP | 🔴 | TELA-010 |

---

## Área 4 — Comissão

| # | Processo | Fase | Criticidade | Tela-fonte |
|---|---|---|---|---|
| P-19 | Apurar venda líquida do período por vendedor | 🔥 MVP | 🔴 | TELA-007 |
| P-20 | Descontar devoluções da base de comissão | 🔥 MVP | 🔴 | TELA-007 |
| P-21 | Calcular comissão (hoje em Excel) | 🔥 MVP | 🔴 | INS-001 |
| P-22 | Gerar relatório de comissão mensal | 🔥 MVP | 🔴 | INS-001 |
| P-23 | Comissionar "Indicador Externo" | ⚡ Fase 3 | 🟡 | TELA-010 |

---

## Área 5 — Estoque / Produtos

| # | Processo | Fase | Criticidade | Tela-fonte |
|---|---|---|---|---|
| P-24 | Cadastrar produto | 💤 ZUMA | 🟡 | TELA-003 |
| P-25 | Manter preço por tabela (REVENDA/CONSUMIDOR) | 💤 ZUMA | 🔴 | TELA-003 |
| P-26 | Consultar saldo por localização | 🔥 MVP | 🔴 | TELA-003/004 |
| P-27 | Sincronizar/importar catálogo para o ERP | 🔥 MVP | 🔴 | TELA-004 |
| P-28 | Alertar estoque ≤ 0 | 🔥 MVP | 🔴 | TELA-003 |
| P-29 | Analisar giro / ranking de produtos | ⚡ Fase 3 | 🟡 | — |

---

## Área 6 — Compras

| # | Processo | Fase | Criticidade | Tela-fonte |
|---|---|---|---|---|
| P-30 | Lançar pedido de compra | 💤 ZUMA | 🔴 | TELA-005 |
| P-31 | Importar XML da NF-e do fornecedor | 💤 ZUMA | 🔴 | TELA-005 |
| P-32 | Dar entrada / baixa no pedido | 💤 ZUMA | 🔴 | TELA-005 |
| P-33 | Consultar histórico de compras por fornecedor | 💤 ZUMA | 🟡 | TELA-006 |
| P-34 | Analisar fornecedores (curva ABC) | ⚡ Fase 3 | 🟡 | TELA-006 |

---

## Área 7 — Financeiro

| # | Processo | Fase | Criticidade | Tela-fonte |
|---|---|---|---|---|
| P-35 | Gerir ficha financeira do cliente | 💤 ZUMA | 🔴 | TELA-001 |
| P-36 | Emitir boleto | 💤 ZUMA | 🔴 | TELA-002 |
| P-37 | Controlar recebimentos / grade de pagamentos | 💤 ZUMA | 🔴 | TELA-002 |
| P-38 | Acompanhar limite de crédito do cliente | ⚡ Fase 3 | 🔴 | TELA-001 |
| P-39 | Analisar inadimplência | ⚡ Fase 3 | 🟡 | — |

---

## Área 8 — Sistema / Administração

| # | Processo | Fase | Criticidade | Tela-fonte |
|---|---|---|---|---|
| P-40 | Cadastrar vendedor / funcionário | 🔥 MVP | 🔴 | TELA-009 |
| P-41 | Gerir acesso (senha, permissões, crédito) | 🔥 MVP | 🔴 | TELA-009 |
| P-42 | Acompanhar indicadores do negócio (dashboard) | 🔥 MVP | 🔴 | TELA-002 |

---

## Área 9 — Logística / Entregas (NOVO — ZumaRomaneio)

| # | Processo | Fase | Criticidade | Tela-fonte |
|---|---|---|---|---|
| P-43 | Gerar romaneio a partir das pré-vendas | ⚡ Fase 3 | 🔴 | TELA-016 |
| P-44 | Montar carga / rota (veículo + motorista) | ⚡ Fase 3 | 🟡 | TELA-016 |
| P-45 | Separação de mercadoria (picking) | ⚡ Fase 3 | 🟡 | TELA-011/016 |
| P-46 | Acompanhar status de entrega / devolução | ⚡ Fase 3 | 🔴 | TELA-016 |

## Área 10 — Caixa / Financeiro operacional (NOVO)

| # | Processo | Fase | Criticidade | Tela-fonte |
|---|---|---|---|---|
| P-47 | Abertura e lançamentos do caixa (E/S) | 💤 ZUMA | 🔴 | TELA-014 |
| P-48 | Consistência / conciliação do caixa | 💤 ZUMA | 🔴 | TELA-015 |
| P-49 | Previsão de fluxo financeiro (0–92 dias) | 💤 ZUMA | 🟡 | TELA-013 |
| P-50 | Vincular recebimento à pré-venda (Pré-venda Financeiro) | 💤 ZUMA | 🟡 | TELA-014 |

## Área 11 — Fechamento de comissão & RH (NOVO — manual/externo)

| # | Processo | Fase | Criticidade | Tela-fonte |
|---|---|---|---|---|
| P-51 | **Fechar comissão do mês (papel + Excel)** | 🔥 MVP | 🔴 | EXT-03 |
| P-52 | Descontar adiantamentos no acerto | 🔥 MVP | 🔴 | EXT-03 |
| P-53 | Apurar despesas de viagem (alimentação/pernoite) | ⚡ Fase 3 | 🟡 | EXT-03 |
| P-54 | Controle de jornada do motorista (papel) | ⚡ Fase 3 | 🟡 | EXT-02 |
| P-55 | Folha de pagamento (sistema contábil externo) | 🚫 Externo | 🟡 | EXT-01 |

## Área 12 — Fiscal (NOVO — ZumaNF, permanece no ZUMA)

| # | Processo | Fase | Criticidade | Tela-fonte |
|---|---|---|---|---|
| P-56 | Emitir NF por operação (venda/transferência) | 🚫 Fiscal | 🔴 | TELA-017 |
| P-57 | Registrar devolução de cliente (NF entrada) | 🚫 Fiscal | 🔴 | TELA-017 |

## Área 13 — Aprovação Comercial (NOVO — proprietário)

| # | Processo | Fase | Criticidade | Origem |
|---|---|---|---|---|
| P-58 | Aplicar desconto dentro do teto do vendedor | 🔥 MVP | 🔴 | RN-APR-001 |
| P-59 | **Solicitar aprovação de desconto ao proprietário** | ⚡ Fase 2 | 🔴 | RN-APR-002 |
| P-60 | Aprovar/recusar com registro (histórico) | ⚡ Fase 2 | 🟡 | RN-APR-004 |

---

## Detalhamento AS-IS dos processos manuais (esclarecido 2026-06-23)

### P-51/P-58..60 — Fechamento administrativo & aprovação
- **P-51 Fechamento mensal** — responsável **Roberta**; papel; 1ª semana do mês seguinte; fora do
  ZUMA. Insumos: vendas/vendedor (ZUMA) + adiantamentos + horas extras + alimentação + dados do
  motorista. Saída: valores para a **contabilidade**. *(crítico, externo, automação futura)*
- **P-58→60 Aprovação de desconto** — vendedor monta orçamento (ZumaPDV) → ZUMA calcula preço →
  **proprietário** avalia preço/margem/perfil → libera (ou não) desconto extra. Hoje **informal**,
  sem histórico. Mais comum em cliente novo/negociação.

### P-54 — Horas extras do motorista (somente motorista faz)
Formulário físico impresso → motorista preenche chegada/almoço/retorno/término → entrega ao
administrativo → lançamento manual em Excel → Excel calcula horas extras → envia à **contadora** →
contadora faz o cálculo final. *(manual, externo, dependente de planilha e de contador; fórmula
trabalhista não é dominada pela empresa)*

### Benefícios (regra operacional — externo)
- Interno: **R$10/dia**, mín. 20 dias (~R$210), PIX mensal · 4 internos.
- Motorista: **almoço R$30/dia**; **pernoite R$38 + jantar automático R$30 = R$68**.

> Estes processos **não entram no MVP** — são trabalhistas/contábeis externos. O ERP pode, no
> futuro, **exportar** a comissão comercial para reduzir o trabalho manual da Roberta.

## Área 14 — Crédito, Carteira & Bloqueio (NOVO — PROC-002/003/004/005)

| # | Processo | Fase | Criticidade | Origem |
|---|---|---|---|---|
| P-61 | Gestão de carteira por vendedor/região (transferência, ausência) | ⚡ Fase 2 | 🟡 | PROC-002 |
| P-62 | Concessão de crédito (análise manual — mãe do proprietário) | ⚡ Fase 2/3 | 🔴 | PROC-003 |
| P-63 | Bloqueio de cliente (motivo/data/responsável) | 🔥 MVP* | 🔴 | PROC-004 |
| P-64 | Devolução com geração de crédito (vendedor→Benini→Roberta) | 🔥 MVP (modelo) | 🔴 | PROC-005 |

\* *Registrar motivo/data/responsável do bloqueio é recomendado para o MVP (3 campos, baixo custo,
fecha lacuna do ZUMA — a tela de Cliente já mostra status). Histórico de liberações = Fase 2.*

---

## Detalhamento AS-IS (rev. B — 2026-06-23)

### PROC-001 — Fechamento mensal de comissão (Roberta)
Ferramentas: Zuma + **papel + calculadora**. Fonte: relatório "Vendas por Vendedor".
Fórmula: **1% da venda líquida** (Lucilene **0,5%**). Devolução só reduz a base **se antes do
fechamento** e **confirmada fisicamente** (Brendo: material voltou ao estoque?). Fluxo: consulta
relatório → verifica devoluções → confirma com Brendo → remove itens → calcula à mão → registra em
papel → paga junto ao salário (1º dia útil da 1ª semana).
**Problemas:** 100% manual, sem histórico, sem rastreabilidade, dependente de pessoas.

### PROC-003 — Concessão de crédito (mãe do proprietário)
Critérios: Serasa · 1ª forma de pagamento/relacionamento · **3 comprovantes de fornecedores
semelhantes** · maior compra · pontualidade · capital social · contrato social · porte · IR.
Crédito só após análise completa. **Problemas:** sem workflow, critérios não documentados, decisão
concentrada em 1 pessoa.

### PROC-004 — Bloqueio de clientes
~15% dos inadimplentes bloqueados no ZUMA. ZUMA **não tem campo de motivo**. Exceção: bloqueado
**compra à vista** mantendo débito antigo. Futuro: motivo/data/responsável/histórico de liberações.

### PROC-005 — Devolução com geração de crédito
Vendedor preenche formulário → **Benini** valida retorno físico ao estoque → **Roberta** confirma →
**crédito lançado manualmente no cadastro do cliente**. **Problemas:** papel, conferência manual,
sem rastreabilidade digital.

## Área 15 — Gestão Operacional de Estoque (NOVO — PROCESSO-007, dono: Benini)

> **Prioridade ALTA.** Benini participa de vários processos críticos **ainda não documentados**;
> risco de conhecimento concentrado (bus factor). Subprocessos a mapear em entrevista dedicada.

| # | Subprocesso | Fase | Criticidade | Origem |
|---|---|---|---|---|
| P-65 | Entrada de material (recebimento + conferência) | 💤 ZUMA / ⚡ | 🔴 | PERSONA-004 |
| P-66 | Cadastro de produto no ZUMA | 💤 ZUMA | 🟡 | PERSONA-004 |
| P-67 | Separação para entrega (picking) | ⚡ Fase 3 | 🔴 | PERSONA-004, TELA-016 |
| P-68 | Conferência de devolução (validação física) | 🔥 MVP (liga PROC-005) | 🔴 | PERSONA-004 |
| P-69 | Ajustes de estoque / divergências | ⚡ Fase 3 | 🔴 | PERSONA-004, RN-PRD-002 |
| P-70 | Inventário | ⚡ Fase 3 | 🟡 | PERSONA-004 |

> **Status:** AS-IS detalhado **pendente de entrevista com Benini** (ver ROTEIRO-ENTREVISTA).
> Hipótese a investigar: regras práticas (estoque negativo, divergências) são informais/tácitas.

---

## Resumo

| Área | Processos | MVP 🔥 |
|---|---|---|
| 1. Comercial / CRM | 6 | 5 |
| 2. Orçamentos / Pré-venda | 6 | 5 |
| 3. Vendas | 6 | 3 |
| 4. Comissão | 5 | 4 |
| 5. Estoque / Produtos | 6 | 4 |
| 6. Compras | 5 | 0 |
| 7. Financeiro | 5 | 0 |
| 8. Sistema / Administração | 3 | 3 |
| 9. Logística / Entregas | 4 | 0 |
| 10. Caixa / Financeiro op. | 4 | 0 |
| 11. Comissão & RH (manual) | 5 | 2 |
| 12. Fiscal | 2 | 0 |
| 13. Aprovação Comercial | 3 | 1 |
| 14. Crédito, Carteira & Bloqueio | 4 | 2 |
| 15. Gestão Operacional de Estoque (PROC-007) | 6 | 1 |
| **TOTAL** | **70** | **30** |

---

## Histórico de Versões

| Versão | Data | Mudanças |
|---|---|---|
| 1.0.0 | 2025-06-19 | Criação — 42 processos em 8 áreas, priorizados por fase |
| 2.0.0 | 2026-06-23 | +15 processos (Logística, Caixa, Comissão/RH manual, Fiscal) = 57 |
| 2.1.0 | 2026-06-23 | +Aprovação comercial (P-58..60) e AS-IS dos manuais (Roberta, motorista) = 60 |
| 2.2.0 | 2026-06-23 | +Crédito/Carteira/Bloqueio/Devolução (P-61..64) e AS-IS PROC-001..005 = 64 |
| 2.3.0 | 2026-06-23 | +PROCESSO-007 Gestão Operacional de Estoque (P-65..70, Benini) = 70 |
