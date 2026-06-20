---
id: FEAT-002
épico: EPIC-001
título: Gestão de Vendedores e Cálculo de Comissão
módulo: CRM / Comercial
prioridade: Alta
status: rascunho
versão: 1.0.0
criado-em: 2025-06-19
origem: TELA-007, TELA-008, TELA-009, INS-001 — engenharia reversa ZUMA
---

# FEAT-002 — Gestão de Vendedores e Cálculo de Comissão

## Origem
Derivada da descoberta crítica INS-001: comissão calculada 100% em Excel externo ao ZUMA.
Confirmada pelas TELA-007, TELA-008 e TELA-009 onde campos de comissão estão zerados.

## Problema Real
A empresa não sabe quanto deve a cada vendedor sem abrir uma planilha Excel manualmente.
Sem auditoria, sem histórico, sujeito a erro humano.

## O que o ERP Comercialinox deve fazer

### Escopo do MVP
- [ ] Cadastro de vendedores com: nome, função, comissão à vista (%), comissão a prazo (%), desconto máximo
- [ ] Cálculo automático de comissão por período: (venda líquida × % comissão) por tipo de venda
- [ ] Desconto de devoluções na base de cálculo de comissão
- [ ] Relatório de comissão mensal por vendedor (substituindo o Excel)
- [ ] Dashboard: ranking de vendedores com venda líquida e comissão do período
- [ ] Histórico de comissões pagas por vendedor

### Regras de comissão a validar nas entrevistas
- [ ] A % é igual para à vista e a prazo ou diferente?
- [ ] Devoluções são descontadas da comissão?
- [ ] Existe comissão sobre Indicador Externo? Com qual fórmula?
- [ ] Existe período de carência (ex: comissão paga só após recebimento)?

### Fora do MVP
- Integração com folha de pagamento
- Múltiplas faixas de comissão (escalonamento por meta)
- Comissão por produto ou categoria

## Descoberta Crítica
Ver INS-001-comissao-excel-processo-critico.md

## Dependências
- FEAT-001 (Cadastro de Clientes) — vendedor vinculado ao cliente
- Histórico de vendas do ZUMA (leitura via exportação ou integração futura)
