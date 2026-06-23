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
| **Papel / Permissão** | RBAC (ver comissão, editar condições/limites) | 🔥 | RN-FNC-005/006 | B |
| **Empresa** | entidade faturada | ⚡/H | holerite JAPA, "Grupo Empresarial" | B |
| **Grupo Empresarial** | Comercinox / JAPA / Celinox | H | ZumaSeletor, holerite | B/H |
| **Segmento / Ramo de Atividade** | classificação de cliente (CMI…) | 🔥 | RN-CLI-011, TELA-008 | A |

---

## Entidades NOVAS desta auditoria (não estavam no modelo anterior)
Pré-venda/Orçamento · Item de pré-venda · Devolução · Caixa/Lançamento · Previsão de fluxo ·
Romaneio/Carga/Rota/Veículo/Entrega · Separação · NF/Operação fiscal · **Empresa/Grupo Empresarial** ·
Adiantamento · Despesa de viagem · Fechamento de comissão.

## Decisões de modelagem que evitam retrabalho
1. **Comissionado** como abstração (vendedor/indicador) — não acoplar comissão a "vendedor".
2. **Empresa** como dimensão desde o início **se** multi-empresa confirmado (alto impacto — validar **antes** de modelar).
3. **Pré-venda** como entidade central do comercial (orçamento→pedido→separação→entrega→NF).
4. **Devolução** existe no modelo do Comercinox (afeta comissão/funil) mesmo sem emitir NF.
5. **Fechamento de comissão** inclui adiantamentos e despesas — não é só "venda × %".

## Histórico
| 1.0.0 | 2026-06-23 | Criação — catálogo de entidades pós-auditoria |
