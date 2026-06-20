---
id: INS-001
título: Comissão de Vendedores Calculada 100% em Excel — Fora do ZUMA
origem: Engenharia reversa ZUMA ERP 9.25.2.2 (sessão 2025-06-19)
status: confirmado
versão: 1.0.0
criado-em: 2025-06-19
telas-fonte: TELA-007, TELA-008, TELA-009, TELA-010
relacionado-com: FEAT-002, RN-VND-001, RN-VND-002
---

# INS-001 — Comissão de Vendedores é Calculada 100% em Excel

> **Insight crítico.** Maior oportunidade de valor imediato do MVP do ERP Comercialinox.

---

## O Insight

A Comercinox **não calcula comissão de vendedores dentro do ZUMA**. Todo o cálculo
é feito manualmente em uma planilha Excel externa, sem auditoria, sem histórico
estruturado e sujeito a erro humano. A empresa não consegue saber quanto deve a
cada vendedor sem abrir e conferir a planilha.

---

## As 4 Evidências Simultâneas

| # | Evidência | Tela |
|---|---|---|
| 1 | Comissão zerada no Demonstrativo de Saldos para **ambos** os vendedores | TELA-007 |
| 2 | Comissão zerada em **todos** os 137 lançamentos do extrato da vendedora | TELA-008 |
| 3 | Campos de comissão (Vista / Prazo / Devolução) = **0,00%** no cadastro do funcionário | TELA-009 |
| 4 | Item **"Metas de vendas" desabilitado** no menu — metas também vivem no Excel | TELA-010 |

Quatro telas independentes confirmam o mesmo fato: o módulo comercial do ZUMA está
sendo usado apenas como registro de vendas, não como ferramenta de comissionamento.

---

## Dados de Referência (01–19/jun/2026)

| Vendedor | Venda Líquida | Devoluções |
|---|---|---|
| ANDERSON TARGINO (cód. 2) | R$ 102.298,76 | — |
| POLYANNE PIMENTEL (cód. 39) | R$ 94.973,25 | R$ 8.223,60 |
| **Total** | **R$ 197.272,01** | |

- 137 vendas de POLYANNE em 19 dias (~7/dia).
- Venda a prazo representa ~87% do volume.

---

## Por que é Crítico

- **Risco financeiro:** erro de planilha = pagamento errado de comissão.
- **Sem rastreabilidade:** não há histórico auditável de comissões pagas.
- **Trabalho manual recorrente:** alguém recompila a planilha todo período.
- **Desconfiança:** vendedor não tem visibilidade transparente do próprio ganho.

---

## Oportunidade para o MVP

Calcular comissão **nativamente** no ERP Comercialinox é a **killer feature** do MVP:
maior valor percebido com menor esforço relativo, pois os dados de venda já existem.

→ Materializado em **FEAT-002 — Gestão de Vendedores e Cálculo de Comissão**.

---

## Perguntas em Aberto (validar nas entrevistas)

- [ ] Qual a fórmula exata de comissão na planilha?
- [ ] A % é igual para à vista e a prazo?
- [ ] Devoluções são descontadas da base de comissão?
- [ ] Existe carência (comissão paga só após recebimento)?
- [ ] Como é comissionado o "Indicador Externo"?

---

## Histórico de Versões

| Versão | Data | Mudanças |
|---|---|---|
| 1.0.0 | 2025-06-19 | Criação — insight confirmado por 4 evidências |
