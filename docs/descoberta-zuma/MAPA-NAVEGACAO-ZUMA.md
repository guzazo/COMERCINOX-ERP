---
id: MAPA-NAV-ZUMA-001
título: Mapa de Navegação do ZUMA (suite) — MAPA-NAVEGACAO-ZUMA
status: em-revisão
versão: 1.0.0
criado-em: 2026-06-23
fontes: prints jun/2026 + 2026-06-23-novas + inventario-telas v2
---

# Mapa de Navegação do ZUMA (suite)

> Árvore reconstruída a partir das evidências. O ZUMA opera como **vários executáveis** que
> compartilham a mesma base. A Comercinox transita entre eles conforme a tarefa.

---

## Visão por aplicativo

```
ZUMA (suite, C:\ZMCS\PROGRAMAS)
│
├── ZUMA_ERP ............... núcleo: Físico | Financeiro | Fiscal | Módulos Aux. | Rotinas Aux. | Controles
├── ZumaPDV ................ pré-venda / orçamento / pedido (LOJA)
├── ZumaRomaneio ........... romaneio de entregas, rotas, separação
├── ZumaNF / NFC / NFS ..... emissão fiscal (NF-e / NFC-e / NFS-e)
├── ZumaMDFe / ZumaFiscal .. manifesto de carga / apurações
├── ZumaWMS ................ armazém (uso a validar)
├── ZumaPCP ................ produção (provável grupo JAPA Indústria)
└── ZumaSeletor ............ seletor de empresa/base  →  indício de MULTI-EMPRESA
```

---

## Árvore por domínio de negócio

### 🟦 COMERCIAL
```
ZUMA_ERP › Físico › Vendas
  ├── Demonstrativo de Saldos (vendedores) ........... TELA-007  [Relatório]
  ├── Extrato do Vendedor ............................ TELA-008  [Relatório]
  └── Metas de vendas (DESABILITADO — vive no Excel) . TELA-010
ZUMA_ERP › Financeiro › A Receber
  └── Clientes (cadastro/pesquisa) ................... TELA-001  [Cadastro]  ⚠ acesso fora de lugar
ZumaPDV [LOJA]
  ├── Pré-venda / Orçamento .......................... TELA-011  [Principal]  🔥
  │     └── Alt+P: e-mail PDF/HTML, lucratividade, clonar, separação, painel de entregas
  └── Pesquisa de Pré-venda .......................... TELA-012  [Consulta]  (conf. C)
Funcionários/Vendedores
  └── Cadastro de Funcionário ........................ TELA-009  [Cadastro]
```

### 🟩 CATÁLOGO
```
ZUMA_ERP › Físico › Produtos
  ├── Cadastro de Produtos (preços/estoque/fiscal) ... TELA-003  [Cadastro]  💤
  ├── Pesquisa de Produtos (2.335 itens) ............. TELA-004  [Consulta]  🔥
  └── Estoque por localização ........................ (print "estoque")  🔥
  Tabelas de preço: REVENDA / CONSUMIDOR (embutidas no produto)
```

### 🟧 COMPRAS
```
ZUMA_ERP › (Físico/Financeiro) › Compras
  ├── Entrada de Pedido de Compra (XML NF-e) ......... TELA-005  💤
  └── Pesquisa de Pedido de Compra (R$33M hist.) ..... TELA-006  💤
```

### 🟨 FINANCEIRO
```
ZUMA_ERP › Financeiro / Rotinas padrões / Caixa Geral
  ├── Fluxo Financeiro — Previsão (0–92 dias) ........ TELA-013  [Relatório]  💤
  ├── Manutenção do Caixa (abertura/E-S/estorno) ..... TELA-014  [Processo]   💤
  ├── Consistência Financeira ........................ TELA-015  [Consulta]   💤
  ├── Recebimentos / Emissão de Boleto / Grade pag. .. (atalhos home)         💤
  └── Pré-venda Financeiro (vincula PV ↔ caixa)
```

### 🟫 LOGÍSTICA / ENTREGAS
```
ZumaRomaneio
  └── Romaneio de Entregas — Ordem de Entrega ........ TELA-016  [Principal]  ⚡
        Cadastros | Movimentação | Relatórios | Rotinas Aux.
        (carga, rota, veículo, motorista, separação de carga)
```

### 🟥 FISCAL
```
ZumaNF / NFC / NFS / MDFe / Fiscal
  ├── Emissor de NF — Inclusão (tipos de operação) ... TELA-017  [Cadastro]  🚫
  └── NF — Emissão/Consulta .......................... TELA-018  (conf. C)   🚫
```

### ⬛ ADMINISTRATIVO / SISTEMA
```
ZUMA_ERP › Controles
  ├── Usuário logado / estação (rodapé) .............. (RN-SIS-002)
  ├── Senha/acesso por funcionário ................... TELA-009 (RN-FNC-003)
  └── ZumaSeletor → seleção de empresa/base .......... (multi-empresa? validar)
Ctrl+F: pesquisa de menus (qualquer tela)
```

### ⬜ RH / PESSOAL (FORA DO ZUMA)
```
Externo (contábil / papel / Excel)
  ├── Folha de pagamento (holerite — JAPA Indústria) . EXT-01  🚫
  ├── Controle de jornada do motorista (papel) ....... EXT-02  ⚡
  └── Fechamento de comissão do mês (papel + Excel) .. EXT-03  🔥  (INS-001)
```

---

## Observações de navegação (problemas)
- **Clientes** vive em *Financeiro › A Receber* — não no comercial (UX-019, RN-SIS-004).
- O usuário **alterna entre 3–5 executáveis** num dia (ERP, PDV, Romaneio, NF) — sem navegação única.
- Comissão e Metas **não estão no software** — vivem em Excel/papel.

## Hipóteses a validar (com nível de confiança)
| Hipótese | Confiança | Como validar |
|---|---|---|
| Operação multi-empresa (Comercinox/JAPA/Celinox) via ZumaSeletor | Média | Entrevista + ver ZumaSeletor |
| ZumaPCP/WMS usados pela Comercinox (vs só pela indústria do grupo) | Baixa | Entrevista |
| TELA-012/018 (pesquisas) — campos exatos | Baixa (borrão) | Nova captura |

## Histórico
| 1.0.0 | 2026-06-23 | Criação — árvore da suite ZUMA por app e por domínio |
