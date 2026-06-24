---
id: PERG-ABERTAS-001
título: Perguntas em Aberto para Validação + Classificação de Regras
status: aberto
versão: 1.0.0
criado-em: 2026-06-23
origem: PROC-001..006, RN-MASTER (rev. B), MODELO-CONCEITUAL
objetivo: reduzir incerteza antes de requisitos/wireframe (etapa Validação do processo do projeto)
---

# Perguntas em Aberto — Validação com Usuários

> Etapa **Validação** do fluxo Descoberta→Processo→RN→Problemas→**Validação**→Requisitos→Wireframe.
> Cada resposta destrava uma decisão de modelagem/escopo.

---

## 0. Respostas recebidas (descoberta organizacional 2026-06-23)

| Pergunta | Resposta | Classificação | Ação |
|---|---|---|---|
| Outros clientes com % especial além da Lucilene? | Só Lucilene (0,5%) identificada até agora | 🟡 **Parcialmente validada** | **Não** virar campo de cadastro ainda; confirmar com Roberta se é exceção única ou padrão |
| Quem recebe comissão quando um vendedor atende cliente do outro? | Sem regra formal; Polyana/Targino se cobrem; alguns clientes só falam com Wanderson | 🔴 **Lacuna crítica (RN-CAR-002)** | Validar com Roberta, Wanderson, Targino, Polyana |
| Limite de crédito bloqueia a venda ou é informativo? | Não validado; só há análise manual (Serasa, comprovantes, capital social, aprovação da direção) | 🔴 **Lacuna crítica** | Validar — impacta cadastro, orçamento, pedido, bloqueio |

> **Hipótese de processo (Polyana):** confirmação de pedido por WhatsApp ("ok" do cliente) é tratada
> como venda confirmada e depois gera devolução/divergência. **Não é erro individual** — investigar se
> o processo induz. (liga a PROC-005 e ao funil do orçamento). Classificação: 🔴 **Hipótese de processo**.

---

## 1. Classificação das regras descobertas (PROC-001..006)

| Regra | Conteúdo | Classificação |
|---|---|---|
| RN-COM-006 | Comissão padrão = 1% da venda líquida | ✅ **Confirmada** |
| RN-COM-007 | Lucilene = 0,5% (override por cliente) | 🟡 **Parcialmente** — confirmada p/ Lucilene; **há outros?** |
| RN-COM-008 | Devolução só reduz comissão antes do fechamento | ✅ **Confirmada** |
| RN-COM-009 | Comissão paga junto ao salário (1ª semana) | ✅ **Confirmada** |
| RN-COM-010 | Devolução exige confirmação física | ✅ **Confirmada** |
| RN-CLI-016 | Bloqueado compra à vista mantendo débito | ✅ **Confirmada** |
| RN-CLI-017 | ZUMA sem campo de motivo de bloqueio | ✅ **Confirmada** |
| RN-CLI-018 | ~15% dos inadimplentes bloqueados | 🟡 **Parcialmente** — número aproximado |
| RN-CRE-001 | Critérios de concessão de crédito | 🟡 **Parcialmente** — lista pode não ser exaustiva |
| RN-CRE-002 | Crédito só após análise completa | ✅ **Confirmada** |
| RN-DEV-001 | Devolução gera crédito no cadastro após validação física | ✅ **Confirmada** |
| RN-CAR-001 | Carteira por vendedor/região | 🟡 **Parcialmente** — comportamento informal |
| RN-CAR-002 | Sem regra formal de transferência / impacto na comissão | 🔴 **Hipótese / Lacuna** |
| RN-CAR-003 | Clientes exclusivos do Wanderson | ✅ **Confirmada** |
| RN-CRE/limite | Limite de crédito **bloqueia** a venda ou é informativo? | 🔴 **Hipótese** |
| RN-SIS-005 | Opera-se 1 CNPJ (2 dormentes) | ✅ **Confirmada** (cliente) |

Resumo: **Confirmadas 9 · Parcialmente 4 · Hipótese/Lacuna 3.**

---

## 2. Perguntas por entrevistado

### 👤 Roberta (Administrativo/Financeiro)
1. **Quais clientes têm % de comissão diferente do 1%?** Só a Lucilene? (destrava RN-COM-007 → override por cliente)
2. Como você calcula a "venda líquida" hoje — o relatório já traz líquido ou você abate algo?
3. Os **adiantamentos** dos vendedores: como são lançados e de onde vêm os valores?
4. Quando a devolução chega **depois** do fechamento, o que acontece com a comissão no mês seguinte?
5. Quanto tempo leva o fechamento hoje? Onde mais erra/retrabalha?
6. O crédito de devolução lançado no cliente é **usado como abatimento** na próxima compra? Como?

### 👤 Wanderson (Proprietário)
7. **Aprovação de desconto:** existe um % de teto por vendedor hoje? Acima de quanto exige você?
8. Quando **outro vendedor atende** cliente da carteira alheia, **quem fica com a comissão?** (destrava RN-CAR-002)
9. Os clientes "exclusivos seus" — quantos são e por quê? Isso afeta comissão de alguém?
10. **Metas de vendas** existem hoje? Como são definidas (já que o ZUMA tem o item desabilitado)?
11. Confirma que os outros 2 CNPJs estão dormentes e não voltarão a operar no horizonte do projeto?

### 👤 Benini (Estoque)
12. Como você confere se o material devolvido **voltou ao estoque**? Há prazo?
13. O que acontece quando o material **não** retorna (cliente ainda está com ele)?
14. A devolução afeta o **saldo de estoque** no ZUMA automaticamente ou é manual?

### 👤 Brendo (Compras/Conferência)
15. Seu papel na devolução vs. o do Benini — onde começa e termina cada um?
16. Você participa do fechamento de comissão (confirmação de devolução)? Com que frequência?

### 👤 Vendedores (Polyane / Targino)
17. Como vocês sabem qual cliente é "de quem"? Existe lista/carteira formal?
18. Com que frequência um atende cliente do outro? Isso gera atrito de comissão?
19. No orçamento, vocês já aplicam desconto sozinhos ou sempre pedem ao Wanderson?
20. Que informação do cliente vocês mais consultam antes de orçar (status, crédito, histórico)?

### 👤 Mãe do proprietário (Crédito)
21. A lista de critérios está completa? Há um valor a partir do qual a análise é obrigatória?
22. O **limite de crédito** definido **bloqueia** vendas acima dele no ZUMA, ou é só referência? (RN-CLI-006)
23. Com que frequência um crédito é revisado/revogado?

---

## 3. O que cada resposta destrava

| Pergunta | Destrava |
|---|---|
| 1 | Modelar (ou não) **override de % por cliente** |
| 8, 17, 18 | Regra de **carteira/comissão** (RN-CAR-002) — hoje bloqueia modelagem |
| 22 | Comportamento do **limite de crédito** (bloqueia vs informa) |
| 12, 13 | Estados da **Devolução** e do **CréditoCliente** |
| 7 | Parâmetro **desconto máx/vendedor** e gatilho de aprovação (Fase 2) |

---

## Histórico de Versões
| 1.0.0 | 2026-06-23 | Criação — 23 perguntas por entrevistado + classificação de 16 regras |
| 1.1.0 | 2026-06-23 | +Seção 0 (respostas recebidas): comissão especial parcial, RN-CAR-002 e limite = lacunas críticas; hipótese WhatsApp |
