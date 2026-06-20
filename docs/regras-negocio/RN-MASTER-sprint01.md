---
id: RN-MASTER-001
título: Regras de Negócio Consolidadas — Sprint 01
origem: Engenharia reversa ZUMA ERP 9.25.2.2 (sessão 2025-06-19)
status: em-revisão
versão: 1.0.0
criado-em: 2025-06-19
telas-fonte: TELA-001 a TELA-010
---

# Regras de Negócio Consolidadas — Sprint 01

> Extraídas da engenharia reversa do ZUMA ERP durante a SPRINT-01.
> Marcadas como "inferidas" até validação com usuários nas entrevistas planejadas.

---

## MÓDULO: CLIENTES

| ID | Regra | Tela | Status | Criticidade |
|---|---|---|---|---|
| RN-CLI-001 | Cliente pode ser Pessoa Física ou Jurídica — tipo altera campos exibidos | TELA-001 | Inferida | Alta |
| RN-CLI-002 | Cliente inativado é ocultável na pesquisa via flag "Desconsiderar Clientes Inativos" | TELA-001 | Confirmada | Alta |
| RN-CLI-003 | Cada cliente tem um vendedor responsável vinculado — alimenta comissão e relatórios | TELA-001 | Confirmada | Alta |
| RN-CLI-004 | Comissão do vendedor pode ser sobrescrita por cliente (% específica por cliente) | TELA-001 | Confirmada | Alta |
| RN-CLI-005 | Desconto máximo configurado por cliente — teto de desconto para o vendedor | TELA-001 | Confirmada | Alta |
| RN-CLI-006 | Limite de crédito por compra bloqueia (ou deveria bloquear) vendas acima do limite | TELA-001 | Inferida ❓ | Alta |
| RN-CLI-007 | Cliente pode ser bloqueado para venda a prazo E para entrega de forma independente | TELA-001 | Confirmada | Alta |
| RN-CLI-008 | Campo "Observações" visível na pesquisa — usado para flags como "ISENTO" (isenção fiscal) | TELA-001 | Confirmada | Alta |
| RN-CLI-009 | Cliente pode ter múltiplos endereços de entrega com um marcado como principal | TELA-001 | Confirmada | Média |
| RN-CLI-010 | Sistema registra automaticamente: primeira compra, última compra, maior compra, histórico de atrasos | TELA-001 | Confirmada | Alta |
| RN-CLI-011 | Clientes segmentados por Grupo e Sub-grupo (ex: grupo "CMI" identificado) | TELA-001 | Confirmada | Média |
| RN-CLI-012 | "Consumidor Final" + "Calcula DIFAL" têm impacto fiscal direto na NF-e | TELA-001 | Confirmada | Alta |
| RN-CLI-013 | Tipo contribuinte impacta tributação nas NF-e emitidas | TELA-001 | Confirmada | Alta |
| RN-CLI-014 | Forma e plano de pagamento padrão configurados por cliente | TELA-001 | Confirmada | Média |
| RN-CLI-015 | Busca padrão usa CNPJ/CPF — não Nome (problema: vendedores buscam por nome) | TELA-001 | Confirmada | Alta |

---

## MÓDULO: PRODUTOS / ESTOQUE

| ID | Regra | Tela | Status | Criticidade |
|---|---|---|---|---|
| RN-PRD-001 | Produto tem saldo por localização — mínimo 4 locais identificados (1, 2, 5, 10) | TELA-003 | Confirmada | Alta |
| RN-PRD-002 | **Estoque negativo PERMITIDO** — sistema não bloqueia venda com saldo negativo | TELA-003 | Confirmada ⚠️ | Alta |
| RN-PRD-003 | Duas tabelas de preço distintas: REVENDA e CONSUMIDOR | TELA-003 | Confirmada | Alta |
| RN-PRD-004 | Preço a prazo (REVENDA) ~15% maior que à vista: R$37,62 vs R$32,71 | TELA-003 | Confirmada | Alta |
| RN-PRD-005 | CST PIS/COFINS varia por localização — impacto fiscal diferente por depósito | TELA-003 | Confirmada | Alta |
| RN-PRD-006 | Estoque mínimo = zero em todos os produtos identificados — sem alertas de reposição | TELA-003 | Confirmada | Média |
| RN-PRD-007 | Catálogo com 2.335 produtos cadastrados | TELA-004 | Confirmada | Informativa |
| RN-PRD-008 | Busca usa modo "Contendo" como padrão — adequado para inox (ex: "304 1x1/8") | TELA-004 | Confirmada | Média |
| RN-PRD-009 | Tabela de preço deve ser selecionada na pesquisa — define preço exibido | TELA-004 | Confirmada | Alta |
| RN-PRD-010 | Ctrl+F6 "Formação de Preço" existe — precificação além da tabela fixa | TELA-004 | Confirmada ❓ | Alta |

---

## MÓDULO: COMPRAS

| ID | Regra | Tela | Status | Criticidade |
|---|---|---|---|---|
| RN-CMP-001 | Entrada exige nota fiscal do fornecedor — campo NF obrigatório | TELA-005 | Confirmada | Alta |
| RN-CMP-002 | XML da NF-e é importado para o pedido de compra | TELA-005 | Confirmada | Alta |
| RN-CMP-003 | Frete CIF (por conta do remetente) é o padrão nas compras | TELA-005 | Confirmada | Média |
| RN-CMP-004 | BRENDO é o usuário responsável por lançar compras | TELA-005/006 | Confirmada | Alta |
| RN-CMP-005 | APERAM INOX SERVICOS BRASIL é o fornecedor dominante | TELA-006 | Confirmada | Informativa |
| RN-CMP-006 | Volume histórico total de compras: R$ 33.009.033,06 | TELA-006 | Confirmada | Informativa |
| RN-CMP-007 | "Sem Recálculo de ST" é exceção fiscal aplicável por entrada | TELA-005 | Confirmada | Alta |

---

## MÓDULO: VENDAS / COMERCIAL

| ID | Regra | Tela | Status | Criticidade |
|---|---|---|---|---|
| RN-VND-001 | **COMISSÃO NÃO É GERENCIADA PELO ZUMA** — todos os campos zerados | TELA-007/008/009 | Confirmada ⚠️ | Alta |
| RN-VND-002 | Cálculo de comissão feito em Excel externo ao ZUMA | INS-001 | Confirmada ⚠️ | Alta |
| RN-VND-003 | Vendedores ativos: ANDERSON TARGINO (cód.2) e POLYANNE RODRIGUES PIMENTEL (cód.39) | TELA-007 | Confirmada | Alta |
| RN-VND-004 | Venda a prazo é dominante: ~87% do volume vs ~13% à vista | TELA-007 | Confirmada | Alta |
| RN-VND-005 | Volume de vendas líquidas estimado: ~R$ 300K/mês | TELA-007/008 | Estimada | Informativa |
| RN-VND-006 | Devoluções devem ser descontadas da venda líquida para comissão | TELA-007 | Confirmada | Alta |
| RN-VND-007 | Hora exata de cada venda é registrada pelo sistema | TELA-008 | Confirmada | Média |
| RN-VND-008 | "Metas de vendas" no menu está desabilitado — metas gerenciadas em Excel | TELA-010 | Confirmada | Alta |
| RN-VND-009 | Existe tipo "Indicador Externo" de comissionado além do vendedor padrão | TELA-009/010 | Confirmada | Média |

---

## MÓDULO: FUNCIONÁRIOS / VENDEDORES

| ID | Regra | Tela | Status | Criticidade |
|---|---|---|---|---|
| RN-FNC-001 | Múltiplos papéis: Vendedor, Indicador, Montador, Motorista, Conferente, Supervisor, Gerente | TELA-009 | Confirmada | Média |
| RN-FNC-002 | "Vendedor Palm" indica uso/histórico de dispositivo mobile para vendas | TELA-009 | Confirmada ❓ | Média |
| RN-FNC-003 | Senha do vendedor configurada no cadastro — controle de acesso centralizado aqui | TELA-009 | Confirmada | Alta |
| RN-FNC-004 | Salário zerado — módulo de RH não é usado operacionalmente | TELA-009 | Confirmada | Média |
| RN-FNC-005 | Desconto máximo configurável por vendedor (além do desconto por cliente) | TELA-009 | Confirmada | Alta |
| RN-FNC-006 | "Liber. Máx. Crédito (%)" é permissão específica por vendedor | TELA-009 | Confirmada | Alta |

---

## MÓDULO: SISTEMA / GERAL

| ID | Regra | Tela | Status | Criticidade |
|---|---|---|---|---|
| RN-SIS-001 | Sistema multiestação: 6 estações simultâneas, rede local 192.168.15.x | TELA-002 | Confirmada | Alta |
| RN-SIS-002 | Usuário logado visível no rodapé em toda sessão | TELA-002 | Confirmada | Média |
| RN-SIS-003 | Ctrl+F abre pesquisa de menus em qualquer tela | TELA-002 | Confirmada | Baixa |
| RN-SIS-004 | Acesso a Clientes em Financeiro → A Receber (não módulo comercial) — problema de IA | TELA-001/002 | Confirmada ⚠️ | Alta |

---

## Resumo

| Módulo | Total | Confirmadas | Inferidas/Estimadas |
|---|---|---|---|
| Clientes | 15 | 12 | 3 |
| Produtos/Estoque | 10 | 10 | 0 |
| Compras | 7 | 7 | 0 |
| Vendas/Comercial | 9 | 8 | 1 |
| Funcionários | 6 | 6 | 0 |
| Sistema/Geral | 4 | 4 | 0 |
| **TOTAL** | **51** | **47** | **4** |

---

## 6 Regras Críticas para Arquitetura do ERP Comercialinox

| # | Regra | Decisão Arquitetural |
|---|---|---|
| 1 | Comissão fora do ZUMA (RN-VND-001/002) | Calcular comissão nativamente — killer feature do MVP |
| 2 | Estoque negativo sem bloqueio (RN-PRD-002) | Alerta visual obrigatório em consulta de produto com saldo ≤ 0 |
| 3 | Duas tabelas de preço (RN-PRD-003) | Orçamento seleciona tabela automaticamente pelo perfil do cliente |
| 4 | 87% das vendas a prazo (RN-VND-004) | Prazo é o fluxo principal — não exceção — no módulo de orçamentos |
| 5 | Status de bloqueio do cliente (RN-CLI-007) | Status visível imediatamente ao abrir cliente em qualquer tela |
| 6 | 6 estações simultâneas (RN-SIS-001) | ERP deve ser web-first — sem instalação de client |

---

## Perguntas em Aberto — Validar nas Entrevistas SPRINT-01

- [ ] RN-CLI-006: Limite de crédito bloqueia a venda ou é apenas informativo?
- [ ] RN-PRD-002: Estoque negativo é intencional (venda antecipada) ou problema operacional?
- [ ] RN-VND-002: Como é a fórmula de comissão no Excel? Quem calcula? Quando?
- [ ] RN-PRD-010: "Formação de Preço" (Ctrl+F6) — como funciona? Quem usa?
- [ ] RN-CLI-011: O que significa o grupo "CMI"? Quais outros grupos existem?
- [ ] RN-FNC-002: "Vendedor Palm" — app mobile em uso ou descontinuado?
- [ ] RN-VND-009: "Indicador Externo" — quem são? Como são comissionados?

---

## Histórico de Versões

| Versão | Data | Mudanças |
|---|---|---|
| 1.0.0 | 2025-06-19 | Criação — 51 regras extraídas de 10 telas mapeadas na Sprint 01 |
