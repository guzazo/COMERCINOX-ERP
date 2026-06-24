---
id: ENT-DOM-001
título: Entidades de Domínio — Comercinox ERP (ENTIDADES-DOMINIO)
status: em-revisão
versão: 1.0.0
criado-em: 2026-06-23
fontes: RN-MASTER, inventario-telas v2, MAPA-NAVEGACAO-ZUMA, prints jun/2026
objetivo: visão única das entidades reais antes da modelagem definitiva
---

# Entidades de Domínio — Comercinox ERP

> Catálogo das entidades observadas nas telas do ZUMA e nos processos manuais. Cada entidade
> traz: papel, MVP, origem (evidência) e confiança. **Não foram inventadas entidades sem evidência.**

**MVP:** 🔥 modelar no MVP · ⚡ Fase 3 · 💤 permanece no ZUMA · 🚫 fiscal/externo
**Confiança:** A=tela nítida · B=tela legível · C=foto/borrão · H=hipótese

---

## 1. Comercial

| Entidade | Papel | MVP | Origem | Conf. |
|---|---|---|---|---|
| **Cliente** | PF/PJ, status, segmento, funil, flags fiscais | 🔥 | TELA-001 | A |
| **Contato** (N por cliente) | telefone/WhatsApp/e-mail, principal | 🔥 | TELA-001 | A |
| **Endereço** (N; 1 principal MVP) | entrega/cobrança | 🔥 (1) / ⚡ (N) | TELA-001, romaneio | A |
| **Condições Comerciais** (do cliente) | bloqueio prazo/entrega, limite crédito, desconto máx, comissão override | 🔥 | RN-CLI-004..007 | A |
| **Pré-venda / Orçamento** | cabeçalho + itens + condição pgto + desconto + IPI/frete | 🔥 | TELA-011 | A |
| **Item de Pré-venda** | produto, qtd, valor, subtotal | 🔥 | TELA-011 | A |
| **Pedido** (pré-venda liberada→pedido) | conversão, separação | ⚡ | TELA-011 (travada/liberada) | A |
| **Devolução** | reduz base de venda/comissão | 🔥 (modelo) | TELA-017, TELA-008 | B |
| **Interação / Follow-up** (CRM) | data, responsável, lembrete | 🔥 | EPIC-001, personas | H |
| **Funil / Estágio** | Frio/Médio/Quente/Recorrente | 🔥 | EPIC-001 | H |
| **Meta de vendas** | por vendedor/período | 🔥 (lite) | TELA-010 (Excel) | B |

## 2. Comissão & Pessoas

| Entidade | Papel | MVP | Origem | Conf. |
|---|---|---|---|---|
| **Comissionado** (abstração) | vendedor \| **indicador externo** | 🔥 | RN-VND-009, TELA-009 | A |
| **Vendedor** | % à vista/prazo, desconto máx, liberação crédito % | 🔥 | TELA-009 | A |
| **Regra de Comissão** | base (líquido − devolução), %, override por cliente, carência? | 🔥 | INS-001, RN-VND | B |
| **Fechamento de Comissão** | período, por vendedor, **adiantamentos**, **despesas de viagem** | 🔥 | EXT-03 (manuscrito) | B |
| **Adiantamento** | valor antecipado a descontar | 🔥 | EXT-03 | B |
| **Despesa de viagem** (alimentação/pernoite) | reembolso vendedor/motorista | ⚡ | EXT-03, formulario_motorista | B |
| **Funcionário / Papel** | Vendedor/Indicador/Montador/Motorista/Conferente/Supervisor/Gerente | 🔥 (papéis usados) | RN-FNC-001 | A |
| **Motorista** | jornada, rotas | ⚡ | romaneio, EXT-02 | B |

## 3. Catálogo

| Entidade | Papel | MVP | Origem | Conf. |
|---|---|---|---|---|
| **Produto** | descrição, unidade (KG/MT/PC/UN), fiscal | 💤 (mantido no ZUMA) / 🔥 (consulta) | TELA-003/004 | A |
| **Tabela de Preço** | REVENDA / CONSUMIDOR (N tabelas) | 🔥 | RN-PRD-003 | A |
| **Preço** (produto×tabela) | à vista / a prazo (~+15%) | 🔥 | RN-PRD-004 | A |
| **Saldo de Estoque** (produto×local) | 4+ locais, negativo permitido | 🔥 (consulta) | TELA-003 | A |
| **Localização / Depósito** | 1,2,5,10 | 🔥 | RN-PRD-001 | A |
| **Categoria / Grupo de Produto** | classificação | ⚡ | TELA-004 (filtros) | B |
| **Formação de Preço** | precificação além da tabela (Ctrl+F6) | ⚡ | RN-PRD-010 | C |
| **Movimentação / Ajuste de Estoque** | entrada/saída/ajuste; divergência físico×sistema | ⚡ (PROC-007) | PERSONA-004 | B |
| **Inventário** | contagem física periódica | ⚡ (PROC-007) | PERSONA-004 | B |

## 4. Financeiro (permanece no ZUMA)

| Entidade | Papel | MVP | Origem | Conf. |
|---|---|---|---|---|
| **Conta a Receber / Título** | recebíveis | 💤 | TELA-013 | A |
| **Conta a Pagar** | pagáveis | 💤 | TELA-013 | A |
| **Caixa / Lançamento** | abertura, E/S, estorno | 💤 | TELA-014 | B |
| **Forma de Pagamento** | à vista/prazo/cheque/cartão/boleto | 🔥 (referência) | TELA-014, RN-CLI-014 | A |
| **Plano de Pagamento** | parcelamento padrão por cliente | 🔥 (referência) | RN-CLI-014 | A |
| **Previsão de Fluxo** | projeção 0–92 dias | 💤 (ler no futuro) | TELA-013 | A |

## 5. Logística (Fase 3)

| Entidade | Papel | MVP | Origem | Conf. |
|---|---|---|---|---|
| **Romaneio** | agrupador de entrega | ⚡ | TELA-016 | A |
| **Carga / Rota** | veículo + motorista + sequência | ⚡ | TELA-016 | A |
| **Veículo** | frota | ⚡ | TELA-016/011 | A |
| **Entrega** | status (aberto/baixado/devolvido) | ⚡ | TELA-016 | A |
| **Separação de mercadoria** | picking | ⚡ | TELA-011/016 | A |

## 6. Fiscal (permanece no ZUMA — 🚫)

| Entidade | Papel | Origem | Conf. |
|---|---|---|---|
| **Nota Fiscal (NF-e/NFC-e/NFS-e/MDF-e)** | documento fiscal | TELA-017 | B |
| **Operação fiscal** | venda/devolução/transferência/correção | TELA-017 | B |
| **Flags fiscais do cliente** | Consumidor Final, DIFAL, tipo contribuinte | RN-CLI-012/013 | A |

## 7. Sistema / Administrativo

| Entidade | Papel | MVP | Origem | Conf. |
|---|---|---|---|---|
| **Usuário** (login) ≠ Funcionário | autenticação, estação | 🔥 | RN-SIS-001, TELA-009 | A |
| **Papel / Permissão** | RBAC; **Proprietário** aprova desconto acima do teto | 🔥 | RN-FNC-005/006, RN-APR | A |
| **Aprovação de Desconto** | solicitação→aprovação→histórico (orçamento) | **Fase 2** | RN-APR (proprietário) | A |
| **Empresa / CNPJ** | 3 CNPJs; **2 dormentes (manobra fiscal), 1 operacional** | ❌ não-MVP (sem tenant) | cliente 2026-06-23 | A |
| **Segmento / Ramo de Atividade** | classificação de cliente (CMI…) | 🔥 | RN-CLI-011, TELA-008 | A |

## 8. RH / Benefícios (externo ao ERP)

| Entidade | Papel | MVP | Origem | Conf. |
|---|---|---|---|---|
| **Fechamento Administrativo** | consolidação mensal (Roberta) p/ contabilidade | Oportunidade futura | fechamentoMes | B |
| **Benefício / Vale-alimentação** | interno: R$10/dia, mín. 20 dias (~R$210); motorista: almoço R$30/dia | Oportunidade futura | folhaMotorista | B |
| **Pernoite + Jantar** (motorista) | R$38/pernoite + **R$30 jantar automático** = R$68 | Oportunidade futura | folhaMotorista | B |
| **Hora Extra** (somente motorista) | formulário→Excel→contadora (fórmula desconhecida) | Oportunidade futura | formularioMotorista | B |

---

## 9. Crédito, Carteira & Bloqueio (rev. B — PROC-002/003/004/005)

| Entidade | Papel | MVP | Origem | Conf. |
|---|---|---|---|---|
| **Bloqueio de Cliente** | motivo + data + responsável + histórico de liberações | 🔥 (motivo/data/resp.) / Fase 2 (histórico) | PROC-004 (gap do ZUMA) | A |
| **Análise de Crédito** | Serasa, 3 referências, maior compra, capital/contrato social, porte, IR | Fase 2 | PROC-003 | A |
| **Crédito do Cliente (devolução)** | saldo de crédito lançado após devolução validada | 🔥 (modelo) | PROC-005 | A |
| **Carteira / Região** | vínculo cliente↔vendedor; contato principal (ex.: Wanderson) | 🔥 (vínculo) / Fase 2 (regras) | PROC-002 | A |
| **Regra de Comissão por Cliente** | override (ex.: **Lucilene 0,5%** vs padrão **1%**) | 🔥 | PROC-001, RN-COM-006/007 | A |
| **Devolução** (atualiza) | exige **confirmação física** (Benini/Brendo); afeta comissão se antes do fechamento | 🔥 | PROC-001/005 | A |

### Atores reais identificados (ver personas)
Wanderson (proprietário/vendas) · Polyane, Targino (vendedores) · Roberta (admin/financeiro — comissão,
fechamento, crédito de devolução) · **mãe do proprietário** (análise de crédito) · Brendo (compras/conferência
de devolução) · Benini (estoque/validação física de devolução).

## Entidades NOVAS desta auditoria (não estavam no modelo anterior)
Pré-venda/Orçamento · Item de pré-venda · Devolução · Caixa/Lançamento · Previsão de fluxo ·
Romaneio/Carga/Rota/Veículo/Entrega · Separação · NF/Operação fiscal · **Empresa/Grupo Empresarial** ·
Adiantamento · Despesa de viagem · Fechamento de comissão.

## Decisões de modelagem que evitam retrabalho
1. **Comissionado** como abstração (vendedor/indicador) — não acoplar comissão a "vendedor".
2. **SEM tenant de empresa no MVP** — operação usa 1 CNPJ; os outros 2 são manobra fiscal dormente.
3. **Pré-venda** como entidade central do comercial (orçamento→pedido→separação→entrega→NF).
4. **Devolução** existe no modelo do Comercinox (afeta comissão/funil) mesmo sem emitir NF.
5. **Fechamento de comissão** = venda líquida − devoluções − **adiantamentos** × %. Benefícios/horas extras são externos.
6. **Aprovação de desconto**: MVP guarda só o *limite por vendedor*; o *workflow* de aprovação é Fase 2.

## Histórico
| 1.0.0 | 2026-06-23 | Criação — catálogo de entidades pós-auditoria |
| 1.1.0 | 2026-06-23 | Multi-empresa rebaixado (1 CNPJ); +Aprovação de Desconto, Benefícios, Hora Extra, Fechamento |
| 1.2.0 | 2026-06-23 | +Bloqueio, Análise de Crédito, Crédito do Cliente, Carteira/Região, Comissão por cliente; atores reais |
| 1.3.0 | 2026-06-23 | +Movimentação/Ajuste de Estoque e Inventário (PROCESSO-007 / Benini) |
