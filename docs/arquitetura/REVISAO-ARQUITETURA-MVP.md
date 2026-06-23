---
id: ARQ-REV-001
título: Revisão Crítica de Arquitetura — antes das telas do Sprint UX 1
status: em-revisão
versão: 1.0.0
criado-em: 2026-06-20
origem: revisão sobre RN-MASTER-sprint01, TELAs 001–010, EPIC-001, FEAT-001/002/003, INS-001, personas
objetivo: garantir que nenhuma entidade/fluxo importante da Comercinox foi omitido antes de desenhar Dashboard, Lista de Clientes e Cadastro de Cliente
---

# Revisão Crítica de Arquitetura — MVP

> Conferência das entidades e fluxos documentados (51 regras de negócio, 10 telas, EPIC-001,
> personas) contra a Information Architecture inicial. Cada lacuna cita a regra de origem.

---

## 1. O que estava FALTANDO na IA inicial

A IA inicial (8 módulos: Dashboard, Clientes, Produtos, Orçamentos, Pedidos, CRM,
Relatórios, Vendedores/Admin) **omitia entidades reais** já documentadas:

| # | Lacuna | Origem documentada | Impacto |
|---|---|---|---|
| L1 | **Usuários ≠ Vendedores ≠ Clientes** — não havia entidade de *usuário de login* separada | RN-FNC-003 (senha no cadastro), RN-SIS-001 (6 estações) | Sem isso, login/permissão vira refatoração |
| L2 | **Permissões / papéis** | RN-FNC-001 (7 papéis), RN-FNC-005/006 (desconto e crédito por vendedor) | Comissão é dado sensível; acesso precisa de regra |
| L3 | **Comissão como domínio próprio** (não só relatório) | INS-001, RN-VND-001/002/006, RN-CLI-004 | Killer feature — precisa de modelo, não só tela |
| L4 | **Indicador Externo** (comissionado que não é vendedor) | RN-VND-009, RN-FNC-001 | Se o modelo de comissão só conhece "vendedor", quebra depois |
| L5 | **Tabela de preço como entidade** (REVENDA / CONSUMIDOR) | RN-PRD-003/004/009 | Hardcodar 2 tabelas impede adicionar uma 3ª |
| L6 | **Segmentos / Grupos de cliente** (grupo "CMI", sub-grupo) | RN-CLI-011 | Filtro, auto-seleção de preço e relatórios dependem disso |
| L7 | **Condições comerciais do cliente** (bloqueio prazo/entrega, limite crédito, desconto máx, comissão override) | RN-CLI-004/005/006/007 | Regra de orçamento/venda depende — capturar já |
| L8 | **Contatos e endereços múltiplos** como sub-entidades | RN-CLI-009, TELA-001 | EPIC-001 lista "Cadastro de Contatos" como feature |
| L9 | **CRM operacional**: interação/atividade, follow-up com data+responsável | EPIC-001 (FEAT-005), personas Comercial | É metade do valor do MVP CRM |
| L10 | **Devoluções** como entidade que reduz base de comissão | RN-VND-006, TELA-008 | Sem isso a comissão fica errada |
| L11 | **Metas de vendas** (hoje no Excel) | RN-VND-008 | Par natural de comissão/dashboard |
| L12 | **Fornecedores** | RN-CMP-004/005, TELA-006 | Mesmo ficando no ZUMA, produto referencia fornecedor |
| L13 | **Flags fiscais do cliente** (Consumidor Final, DIFAL, tipo contribuinte) | RN-CLI-012/013 | Capturar campo agora evita migração dolorosa |
| L14 | **Formas/planos de pagamento** | RN-CLI-014 | "A prazo" é 87% das vendas (RN-VND-004) |

---

## 2. O que pode gerar RETRABALHO (riscos de modelagem)

> Decisões a tomar **agora** no modelo conceitual, mesmo que a UI venha depois.

| R | Risco | Mitigação desde já |
|---|---|---|
| R1 | Auth acoplado a "vendedor" | Modelar **Usuário** (login/papel) separado de **Pessoa-Vendedor** e **Cliente** |
| R2 | Comissão só para vendedor | Abstração **Comissionado** (vendedor \| indicador externo) + **camada de regras** de comissão (%, base, devolução, override por cliente) |
| R3 | Tabela de preço hardcoded | **Entidade Tabela de Preço** (N tabelas) + regra de auto-seleção por perfil do cliente |
| R4 | Segmento como texto livre | **Entidade Segmento/Grupo** (lista gerenciada) |
| R5 | Condições comerciais soltas | Bloco **Condições Comerciais** no Cliente (bloqueios, limite, desconto, comissão override) desde o cadastro |
| R6 | Catálogo sem metadado de origem | Guardar **fonte + timestamp de sincronização** por produto (ZUMA é a fonte no MVP) |
| R7 | Status do cliente como booleano | **Enum de status** (Ativo / Inativo / Bloqueado-prazo / Bloqueado-entrega) — combináveis |
| R8 | Ignorar flags fiscais agora | Persistir campos fiscais (mesmo read-only) para não remigrar no Fase 4 |

---

## 3. O que DEVE entrar no MVP (Sprint UX 1–4)

| Entra no MVP | Por quê |
|---|---|
| **Usuários & Permissões** (RBAC básico: Proprietário/Admin, Comercial, Administrativo) | Dado de comissão é sensível; 6 estações; limites por vendedor |
| **Vendedor** com parâmetros de comissão (à vista %, prazo %, devolução, desconto máx, liberação crédito %) | Núcleo da killer feature |
| **Cliente** completo: dados + **condições comerciais** + status + segmento + funil + flags fiscais (capturados) | É o EPIC-001 |
| **Contatos** (N) + **endereço** (1 principal no MVP) | EPIC-001 FEAT |
| **Segmentos/Categorias de cliente** (lista gerenciada) | Filtro, preço, relatórios |
| **Tabela de preço** (REVENDA/CONSUMIDOR) + auto-seleção | Orçamento correto |
| **Catálogo de produtos** (leitura/sincronizado) + disponibilidade | FEAT-003 |
| **Comissão**: cálculo (líquido − devoluções) × % + relatório mensal | INS-001 — maior valor |
| **CRM**: funil + follow-ups + interações | Metade do valor do MVP |
| **Orçamentos** (básico, a prazo como padrão) | EPIC-001 / FEAT-003 |
| **Dashboard** comercial (KPIs + ranking + alertas) | Substitui home vazia do ZUMA |
| **Metas (lite)**: meta manual por vendedor vs realizado | Par de comissão/dashboard; tira do Excel |

---

## 4. O que fica para VERSÕES FUTURAS (Fase 3+)

| Futuro | Motivo |
|---|---|
| **Fornecedores / Compras** (gestão) | Permanece no ZUMA no MVP (RN-CMP, TELA-005/006) |
| **Pedidos de venda** (conversão de orçamento) | EPIC-001 Fase 3 |
| **Indicador Externo** (comissionamento) | Modelar a abstração agora; UI/regra depois (RN-VND-009 — pergunta em aberto) |
| **Múltiplos endereços de entrega** | RN-CLI-009 — Fase 3 |
| **Lógica fiscal** (DIFAL, tipo contribuinte, NF-e) | Fase 4 — fica no ZUMA; campos só capturados |
| **Gestão do catálogo** (cadastro de produto) | Produto é mantido no ZUMA (TELA-003) |
| **Comissão avançada** (escalonamento por meta, carência) | RN-VND — perguntas em aberto nas entrevistas |
| **Integrações** (ZUMA API, Mercado Livre, WhatsApp) | Fase 3/4 |

---

## 5. Navegação corrigida (4 grupos)

```
COMERCIAL          CATÁLOGO            RELATÓRIOS              CONFIGURAÇÕES
• Dashboard        • Produtos (consulta) • Comissão            • Vendedores
• Clientes         • [Fornecedores]ᶠ     • Vendas / Extrato    • Usuários & Permissões
• CRM (Pipeline,                          • Clientes inativos   • Segmentos / Categorias
  Follow-ups)                             • Metas               • Tabelas de preço
• Orçamentos                                                    • Formas de pagamento
• [Pedidos]ᶠ
```
ᶠ = Fase futura (visível na IA, fora do MVP).

---

## 6. Decisões para validar nas entrevistas (herdadas + novas)

- Limite de crédito bloqueia venda ou é informativo? (RN-CLI-006)
- Fórmula exata da comissão no Excel? Carência? (RN-VND-002)
- "Indicador Externo": quem são e como comissionam? (RN-VND-009)
- Quais segmentos/grupos existem além de "CMI"? (RN-CLI-011)
- Quantos papéis de usuário realmente precisam de login no MVP?

---

---

# ADENDO v2 — Auditoria de evidências (2026-06-23)

> Reanálise após novas capturas (suite ZUMA, Pré-venda, Caixa, Fluxo, Romaneio, NF, folha/fechamento
> manuais). Ver [ENTIDADES-DOMINIO](ENTIDADES-DOMINIO.md) e [MAPA-NAVEGACAO-ZUMA](../descoberta-zuma/MAPA-NAVEGACAO-ZUMA.md).

## A. Entidades ainda não modeladas (novas)
Pré-venda/Orçamento + Item · Devolução · Caixa/Lançamento · Previsão de fluxo · Romaneio/Carga/
Rota/Veículo/Entrega · Separação · NF/Operação fiscal · **Empresa / Grupo Empresarial** ·
Adiantamento · Despesa de viagem · Fechamento de comissão.

## B. Regras de negócio não mapeadas antes
27 novas (RN-PRV, RN-LOG, RN-FIN, RN-FIS, RN-COM, RN-SIS-005/006). Destaques: pré-venda À Prazo
padrão; pré-venda alimenta separação/entrega; pedido a prazo é compromisso financeiro; devolução
reduz comissão; fechamento manual com adiantamentos e despesas.

## C. Fluxos ausentes identificados
1. **Orçamento → Pedido → Separação → Entrega → NF** (cadeia comercial-logística real).
2. **Pré-venda → Recebimento no caixa** (Pré-venda Financeiro).
3. **Fechamento de comissão** (venda líquida − devolução − adiantamento + despesas).

## D. Dependências críticas
- Orçamento depende de: Cliente, Tabela de preço, Estoque, Vendedor.
- Comissão depende de: Venda, **Devolução**, Adiantamento, Regra de comissão.
- **Multi-empresa** (se confirmado) é dependência transversal de TODAS as entidades.

## E. Riscos de retrabalho (novos)
| R | Risco | Mitigação |
|---|---|---|
| R9 | Ignorar **multi-empresa** | **Decidir antes de modelar.** Se confirmado, `empresa_id` em tudo desde o schema |
| R10 | Orçamento sem ligação a pedido/entrega | Modelar pré-venda como raiz do ciclo comercial |
| R11 | Comissão sem devolução/adiantamento | Incluir esses fatores na regra desde o MVP |
| R12 | Tratar "Orçamentos" como tela nova ignorando o ZumaPDV | Espelhar o que já funciona na pré-venda |

## F. Entra no MVP (com justificativa por evidência)
| Item | Justificativa |
|---|---|
| **Orçamento (pré-venda)** com À Prazo padrão | É a operação diária real (TELA-011, RN-PRV-001) |
| **Devolução** no modelo de comissão | Reduz base — sem ela a comissão erra (RN-FIS-002, RN-COM) |
| **Adiantamento** no fechamento | Aparece no fechamento manual (EXT-03) |
| **Segmento/Grupo, Tabela de preço, Condições comerciais** | Já confirmados (mantidos do v1) |

## G. Fica FORA do MVP (com justificativa)
| Item | Justificativa |
|---|---|
| Caixa, Fluxo/Previsão, Recebimentos | Financeiro permanece no ZUMA (Fase 4) |
| Romaneio/Entregas, Separação, Veículo, Rota | Logística — Fase 3 (não bloqueia o valor inicial) |
| NF/NFC/NFS/MDFe e operações fiscais | Obrigação fiscal — permanece no ZUMA |
| Folha/RH, jornada motorista | Externo ao ZUMA (contador); não é dor do CRM |
| Despesas de viagem no acerto | Fase 3 (refinamento da comissão) |
| Produção (PCP/WMS) | Provavelmente do grupo industrial, não da Comercinox |

## H. Decisão que BLOQUEIA a modelagem (validar já)
**Multi-empresa (Comercinox / JAPA Indústria / Celinox).** Confiança média (ZumaSeletor + holerite +
"Grupo Empresarial"). Se confirmado, muda o data model inteiro (tenant por empresa). **Não modelar
entidades definitivas antes desta resposta.** — registrar como pergunta nº1 das entrevistas.

---

## Histórico de Versões

| Versão | Data | Mudanças |
|---|---|---|
| 1.0.0 | 2026-06-20 | Revisão crítica — 14 lacunas, 8 riscos de retrabalho, escopo MVP/futuro |
| 2.0.0 | 2026-06-23 | Adendo pós-auditoria: 12 entidades novas, 4 fluxos, R9–R12, multi-empresa como bloqueador |
