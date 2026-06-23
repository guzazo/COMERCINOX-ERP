---
id: INV-TELAS-001
título: Inventário de Telas — ZUMA (suite) · INVENTARIO-TELAS-ZUMA
status: em-revisão
versão: 2.0.0
criado-em: 2025
atualizado-em: 2026-06-23
fontes: docs/prints/ (sessões jun/2026) + docs/prints/2026-06-23-novas/ + TELA-001..010
---

# Inventário de Telas — ZUMA (suite)

> **v2.0 (Auditoria 2026-06-23):** incorpora novas evidências que mostram que o **ZUMA não é
> um único sistema, e sim uma SUITE de aplicativos** (pasta `C:\ZMCS\PROGRAMAS`). Reorganizado
> por aplicativo e domínio de negócio. Telas marcadas com nível de confiança quando a evidência
> é foto de monitor (baixa nitidez).

---

## 0. A suite ZUMA (evidência: print PROGRAMAS)

| Aplicativo | Função | Domínio | Usado pela Comercinox |
|---|---|---|---|
| `ZUMA_ERP` | ERP núcleo (vendas, clientes, produtos, financeiro) | Múltiplo | ✅ Confirmado |
| `ZumaPDV` | Pré-venda / orçamento / pedido (LOJA) | Comercial | ✅ Confirmado |
| `ZumaRomaneio` | Romaneio de entregas, rotas, separação | Logística | ✅ Confirmado |
| `ZumaNF` | Emissão NF-e | Fiscal | ✅ Confirmado |
| `ZUMANFC` | NFC-e (cupom) | Fiscal | ⚠️ Provável (hipótese) |
| `ZumaNFS` | NFS-e (serviço) | Fiscal | ⚠️ A validar |
| `ZumaMDFe` | Manifesto de carga (MDF-e) | Fiscal/Logística | ⚠️ Aba vista em Caixa |
| `ZumaFiscal` | Apurações/SPED | Fiscal | ⚠️ Aba vista em Caixa |
| `ZumaWMS` | Gestão de armazém | Estoque | ❓ Instalado; uso a validar |
| `ZumaPCP` | Planejamento de produção | Produção | ❓ Instalado; provavelmente p/ grupo (JAPA Indústria) |
| `ZumaSeletor` | Seletor de empresa/base | Sistema | ⚠️ Sugere **multi-empresa** |

> **Hipótese (confiança média):** `ZumaSeletor` + "Grupo Empresarial" no cadastro + holerite da
> **JAPA Indústria** indicam operação **multi-empresa** (Comercinox / JAPA / Celinox). Validar.

---

## Legenda
**Status:** 🟢 Mapeado · 🟡 Em mapeamento · 🔴 Não mapeado · ⚫ Não usado
**MVP:** 🔥 Substituir no MVP · ⚡ Fase 3 · 💤 Permanece no ZUMA · 🚫 Nunca (fiscal/obrigação)
**Classe:** Principal · Cadastro · Consulta · Modal · Relatório · Config · Processo
**Confiança da evidência:** A=screenshot nítido · B=foto legível · C=foto/borrão (validar)

---

## 1. COMERCIAL (ZUMA_ERP + ZumaPDV)

| ID | Tela | App | Classe | Status | MVP | Evid. | Arquivo |
|---|---|---|---|---|---|---|---|
| TELA-001 | Cadastro de Clientes | ERP | Cadastro | 🟢 | 🔥 | A | [TELA-001](telas/TELA-001-cadastro-clientes.md) |
| TELA-002 | Tela inicial (home) | ERP | Principal | 🟢 | 🔥 | A | [TELA-002](telas/TELA-002-tela-inicial.md) |
| TELA-007 | Demonstrativo de Saldos (vendedores) | ERP | Relatório | 🟢 | 🔥 | A | [TELA-007](telas/TELA-007-demonstrativo-saldos-vendedores.md) |
| TELA-008 | Extrato do Vendedor | ERP | Relatório | 🟢 | 🔥 | A | [TELA-008](telas/TELA-008-extrato-vendedor.md) |
| TELA-009 | Cadastro de Funcionários | ERP | Cadastro | 🟢 | 🔥 | A | [TELA-009](telas/TELA-009-cadastro-funcionarios.md) |
| TELA-010 | Estrutura menu Vendas | ERP | Config | 🟢 | ⚡ | A | [TELA-010](telas/TELA-010-menu-vendas-estrutura.md) |
| **TELA-011** | **Pré-venda / Orçamento (LOJA)** | **PDV** | **Principal** | 🟡 | 🔥 | A | *novo — ver §7* |
| **TELA-012** | **Pesquisa de Pré-venda** | **PDV** | **Consulta** | 🔴 | 🔥 | C | *novo (borrão — validar)* |

## 2. CATÁLOGO (ZUMA_ERP)

| ID | Tela | App | Classe | Status | MVP | Evid. | Arquivo |
|---|---|---|---|---|---|---|---|
| TELA-003 | Cadastro de Produtos | ERP | Cadastro | 🟢 | 💤 | A | [TELA-003](telas/TELA-003-cadastro-produtos.md) |
| TELA-004 | Pesquisa de Produtos | ERP | Consulta | 🟢 | 🔥 | A | [TELA-004](telas/TELA-004-pesquisa-produtos.md) |
| — | Estoque (saldo/localização) | ERP | Consulta | 🔴 | 🔥 | B | *print "estoque" — a detalhar* |

## 3. COMPRAS (ZUMA_ERP)

| ID | Tela | App | Classe | Status | MVP | Evid. | Arquivo |
|---|---|---|---|---|---|---|---|
| TELA-005 | Entrada de Pedido de Compra | ERP | Cadastro | 🟢 | 💤 | A | [TELA-005](telas/TELA-005-entrada-pedido-compra.md) |
| TELA-006 | Pesquisa de Pedido de Compra | ERP | Consulta | 🟢 | 💤 | A | [TELA-006](telas/TELA-006-pesquisa-pedido-compra.md) |

## 4. FINANCEIRO (ZUMA_ERP — Caixa & Fluxo)

| ID | Tela | App | Classe | Status | MVP | Evid. | Arquivo |
|---|---|---|---|---|---|---|---|
| **TELA-013** | **Fluxo Financeiro — Previsão** | ERP | Relatório | 🟡 | 💤 | A | *novo — ver §7* |
| **TELA-014** | **Manutenção do Caixa** | ERP | Cadastro/Processo | 🟡 | 💤 | B | *novo — ver §7* |
| **TELA-015** | **Consistência Financeira (Caixa)** | ERP | Consulta | 🟡 | 💤 | B | *novo — ver §7* |
| — | Contas a Receber / Boleto / Grade pagamentos | ERP | — | 🔴 | 💤 | B | atalhos vistos na home |

## 5. LOGÍSTICA / ENTREGAS (ZumaRomaneio)

| ID | Tela | App | Classe | Status | MVP | Evid. | Arquivo |
|---|---|---|---|---|---|---|---|
| **TELA-016** | **Romaneio de Entregas — Ordem de Entrega** | Romaneio | Principal/Processo | 🟡 | ⚡ | A | *novo — ver §7* |

## 6. FISCAL (ZumaNF / NFC / NFS / MDFe)

| ID | Tela | App | Classe | Status | MVP | Evid. | Arquivo |
|---|---|---|---|---|---|---|---|
| **TELA-017** | **Emissor de NF — Inclusão (tipos de operação)** | ZumaNF | Cadastro | 🟡 | 🚫 | B | *novo — ver §7* |
| **TELA-018** | **NF — Emissão/Consulta** | ZumaNF | Consulta | 🔴 | 🚫 | C | *novo (borrão)* |

## 7. RH / PESSOAL (fora do ZUMA — externo)

| ID | Item | Origem | Classe | MVP | Evid. | Observação |
|---|---|---|---|---|---|---|
| EXT-01 | Folha de pagamento (motorista) | Sistema contábil externo | Relatório | 🚫 | B | Holerite da **JAPA Indústria**; RH não está no ZUMA (RN-FNC-004) |
| EXT-02 | Controle de jornada do motorista | **Papel (manuscrito)** | Processo | ⚡ | B | Jornada/hora extra manual |
| EXT-03 | Fechamento de comissão do mês | **Papel + Excel (manuscrito)** | Processo | 🔥 | B | Adiantamentos + despesas de viagem (INS-001) |

---

## 8. Auditoria do material (Etapa 1) — classificação e conflitos

| Print | Classe | Domínio | Duplicada de | Relevância MVP |
|---|---|---|---|---|
| extrato vendas / controle de vendas / ex.vendedor | Relatório | Comercial | TELA-008 (mesma tela, 3 capturas) | 🔥 |
| zumaERP-01 | Principal | Sistema | TELA-002 | 🔥 |
| cadastro de clientes 01 / dados complementares / pesquisa de cliente | Cadastro/Consulta | Comercial | TELA-001 | 🔥 |
| cadastro produtos | Cadastro | Catálogo | TELA-003 | 💤 |
| estoque | Consulta | Catálogo | (complementa TELA-003/004) | 🔥 |
| orcamentos / dentro de orçamentos | Principal | Comercial | **= Pré-venda (TELA-011)** | 🔥 |
| funcionario | Cadastro | RH/Comercial | TELA-009 | 🔥 |
| **pre-venda-pesquisa** (novo) | Consulta | Comercial | TELA-012 | 🔥 (confiança C) |
| **caixa-manutencao / consistencia** (novo) | Cadastro/Consulta | Financeiro | TELA-014/015 | 💤 |
| **fluxo financeiro previsão** (inline) | Relatório | Financeiro | TELA-013 | 💤 |
| **romaneio** (inline) | Principal | Logística | TELA-016 | ⚡ |
| **PROGRAMAS** (inline) | Config/Sistema | Sistema | — (revela a suite) | referência |
| **nf-emissor-tipos / consulta** (novo) | Cadastro/Consulta | Fiscal | TELA-017/018 | 🚫 |
| **motorista-jornada / folha** (novo) | Processo/Relatório | RH | EXT-01/02 | 🚫/⚡ |
| **fechamento-mes** (novo, manuscrito) | Processo | Comercial/Comissão | EXT-03 | 🔥 |

**Conflitos/inconsistências resolvidos:**
- "orcamentos" (catalogado antes como módulo vago) **é a Pré-venda do ZumaPDV** → unificado em TELA-011.
- Versão do ZUMA mudou de **9.25.2.2 → 9.26.1.3** entre sessões (sem impacto funcional observado).
- TELA-008 tinha 3 capturas distintas → consolidadas (não são telas diferentes).

---

## 9. Resumo

| Categoria | Qtd |
|---|---|
| Aplicativos da suite ZUMA identificados | 11 |
| Telas mapeadas (com doc) | 10 |
| Telas novas identificadas (TELA-011..018) | 8 |
| Itens externos (RH/manual) | 3 |
| Domínios cobertos | Comercial, Catálogo, Compras, Financeiro, Logística, Fiscal, RH |
| Pendências de confiança C (validar) | TELA-012, TELA-018 |

> Detalhamento das telas novas (objetivo, campos, RN, dependências, UX) na seção complementar
> deste inventário e em [MAPA-NAVEGACAO-ZUMA](MAPA-NAVEGACAO-ZUMA.md).

---

## 10. Histórico de Versões

| Versão | Data | Mudanças |
|---|---|---|
| 1.0.0 | 2025 | Inventário inicial (pré-entrevistas) |
| 1.1.0 | 2025-06-19 | 10 telas mapeadas (TELA-001..010) |
| 2.0.0 | 2026-06-23 | Auditoria completa: suite ZUMA (11 apps), 8 telas novas, classificação e conflitos resolvidos |
