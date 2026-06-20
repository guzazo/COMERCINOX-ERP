---
id: PROB-001
título: Problemas de UX/UI Consolidados — Sprint 01
origem: Engenharia reversa ZUMA ERP 9.25.2.2
status: em-revisão
versão: 1.0.0
criado-em: 2025-06-19
telas-fonte: TELA-001 a TELA-010
---

# Problemas de UX/UI Consolidados — Sprint 01

> Identificados pela análise das 10 telas mapeadas do ZUMA ERP.
> Classificados por heurística de Nielsen violada e impacto operacional.

---

## Classificação de Impacto

| Impacto | Significado |
|---|---|
| 🔴 Alto | Causa erros, retrabalho ou perda de produtividade diária |
| 🟡 Médio | Causa fricção e lentidão mas não impede a tarefa |
| 🟢 Baixo | Incomoda mas não impacta resultado |

---

## CATEGORIA: Visibilidade e Feedback (Nielsen #1)

| ID | Problema | Tela | Impacto | Melhoria no ERP |
|---|---|---|---|---|
| UX-001 | Home sem nenhum indicador de negócio — tela de atalhos apenas | TELA-002 | 🔴 Alto | Dashboard com KPIs em tempo real |
| UX-002 | Estoque negativo sem destaque visual — número normal sem alerta | TELA-003 | 🔴 Alto | Badge vermelho quando saldo ≤ 0 |
| UX-003 | Comissão zerada sem aviso — usuário pensa que está correto | TELA-007/008 | 🔴 Alto | Remover campo ou mostrar "Calculado externamente" |
| UX-004 | Saldo total negativo (-17,64) sem contexto sobre se é crítico | TELA-003 | 🔴 Alto | Indicador visual com semáforo por localização |
| UX-005 | Campos obrigatórios não destacados — sem asterisco ou cor | TELA-001 | 🔴 Alto | Asterisco vermelho + validação em tempo real |
| UX-006 | "Aguarde... Preparando dados" sem barra de progresso | TELA-003 | 🟡 Médio | Skeleton loader com progresso estimado |
| UX-007 | Tela vazia por padrão sem placeholders ou exemplos | TELA-001 | 🟡 Médio | Estado vazio com instrução clara |

---

## CATEGORIA: Correspondência Sistema-Mundo Real (Nielsen #2)

| ID | Problema | Tela | Impacto | Melhoria no ERP |
|---|---|---|---|---|
| UX-008 | Título "[Contas à Receber] — Cadastro de clientes" — cliente não é conceito financeiro | TELA-001 | 🔴 Alto | Módulo "CRM / Clientes" com nome direto |
| UX-009 | "CST PIS", "CST COFINS", "MVA" misturados no grid de estoque — linguagem fiscal em tela operacional | TELA-003 | 🟡 Médio | Separar claramente abas: Operacional vs Fiscal |
| UX-010 | "Ocorr." no extrato de vendas — abreviação sem significado claro | TELA-008 | 🟢 Baixo | Usar rótulos completos |

---

## CATEGORIA: Controle e Liberdade do Usuário (Nielsen #3)

| ID | Problema | Tela | Impacto | Melhoria no ERP |
|---|---|---|---|---|
| UX-011 | Sem confirmação antes de excluir (não verificado — validar) | TELA-001 | 🔴 Alto | Confirmação explícita com preview do que será excluído |
| UX-012 | Não há "desfazer" visível para alterações de cadastro | TELA-001 | 🟡 Médio | Histórico de alterações rastreável por usuário |

---

## CATEGORIA: Consistência e Padrões (Nielsen #4)

| ID | Problema | Tela | Impacto | Melhoria no ERP |
|---|---|---|---|---|
| UX-013 | "Descrição" no extrato mistura código + nome do cliente em um campo só: "78613 LUCIANO RANGEL" | TELA-008 | 🟡 Médio | Colunas separadas: Código Cliente \| Nome Cliente |
| UX-014 | Campo "Graduação" (checkbox) sem rótulo explicativo suficiente | TELA-001 | 🟢 Baixo | Tooltip ou rótulo descritivo |
| UX-015 | Dois painéis sem diferença clara: "Painel Local" vs "Painel Web" | TELA-002 | 🟡 Médio | Unificar em um painel com toggle ou eliminar redundância |

---

## CATEGORIA: Prevenção de Erros (Nielsen #5)

| ID | Problema | Tela | Impacto | Melhoria no ERP |
|---|---|---|---|---|
| UX-016 | Produtos com estoque zero aparecem na lista sem destaque — vendedor pode orçar produto inexistente | TELA-004 | 🔴 Alto | Filtro "Somente com estoque" marcado por padrão + badge de disponibilidade |
| UX-017 | Busca de cliente com padrão CNPJ/CPF — vendedor precisa trocar filtro toda vez que quer buscar por nome | TELA-001 | 🔴 Alto | Padrão de busca = Nome |
| UX-018 | Tabela de preço precisa ser selecionada manualmente na pesquisa — erro se selecionar errada | TELA-004 | 🔴 Alto | Auto-selecionar tabela pelo perfil do cliente carregado |

---

## CATEGORIA: Reconhecimento vs Memorização (Nielsen #6)

| ID | Problema | Tela | Impacto | Melhoria no ERP |
|---|---|---|---|---|
| UX-019 | Acesso a Clientes requer memorizar caminho: Financeiro → A Receber → Clientes | TELA-001/002 | 🔴 Alto | Menu principal com "Clientes / CRM" em destaque |
| UX-020 | Atalhos F4/F5/F6/F10 visíveis apenas na pesquisa, não no cadastro principal | TELA-001 | 🟡 Médio | Botões visíveis com ícones no cadastro |
| UX-021 | 11 itens no menu principal — navegação por memória | TELA-002 | 🟡 Médio | Menu com ícones e agrupamento por área |
| UX-022 | "Ctrl+F6 — Formação de Preço" atalho não documentado visivelmente | TELA-004 | 🟡 Médio | Botão visível "Ver formação de preço" |

---

## CATEGORIA: Flexibilidade e Eficiência (Nielsen #7)

| ID | Problema | Tela | Impacto | Melhoria no ERP |
|---|---|---|---|---|
| UX-023 | Grid de contatos na aba 1 começa com linha azul vazia selecionada — confunde | TELA-001 | 🟡 Médio | Estado vazio com CTA "Adicionar contato" |
| UX-024 | Campos Vendedor, Grupo, Sub-grupo, etc. exigem dois cliques (número + lupa) para preencher | TELA-001 | 🟡 Médio | Autocomplete por digitação, busca inline |
| UX-025 | Filtro por cliente no extrato requer código numérico — não aceita nome | TELA-008 | 🔴 Alto | Busca por nome com autocomplete |
| UX-026 | 15+ filtros no extrato do vendedor, mas uso real = vendedor + período apenas | TELA-008 | 🟡 Médio | Filtros avançados colapsáveis; básicos visíveis por padrão |
| UX-027 | Relatórios exigem abertura manual, configuração e impressão — sem visão em tempo real | TELA-007/008 | 🔴 Alto | Dashboard em tempo real substitui relatórios manuais |

---

## CATEGORIA: Design Estético e Minimalista (Nielsen #8)

| ID | Problema | Tela | Impacto | Melhoria no ERP |
|---|---|---|---|---|
| UX-028 | Preview do produto selecionado tem muitos campos vazios (Prateleira, Setor, Cor, Embalagem) | TELA-004 | 🟡 Médio | Mostrar apenas campos com valor preenchido |
| UX-029 | 10 filtros de pesquisa em radio button — maioria nunca usada | TELA-004 | 🟡 Médio | Máximo 3 filtros visíveis; restantes em "avançado" |
| UX-030 | Tela de cadastro de funcionário mistura dados operacionais com dados trabalhistas | TELA-009 | 🟡 Médio | Separar: Vendedor (CRM) vs RH (fora do escopo do MVP) |

---

## Resumo por Heurística

| Heurística Nielsen | Problemas | Críticos (🔴) |
|---|---|---|
| #1 Visibilidade e Feedback | 7 | 5 |
| #2 Correspondência com o Mundo Real | 3 | 1 |
| #3 Controle e Liberdade | 2 | 1 |
| #4 Consistência e Padrões | 3 | 0 |
| #5 Prevenção de Erros | 3 | 3 |
| #6 Reconhecimento vs Memorização | 4 | 1 |
| #7 Flexibilidade e Eficiência | 5 | 3 |
| #8 Design Estético | 3 | 0 |
| **TOTAL** | **30** | **14** |

---

## Top 5 Problemas — Priorizar no MVP

| # | Problema | Por quê é urgente |
|---|---|---|
| 1 | Acesso a Clientes enterrado no módulo Financeiro | Todo vendedor perde tempo todo dia |
| 2 | Busca de cliente com padrão CNPJ/CPF | Vendedor busca por nome, não por CNPJ |
| 3 | Produtos sem estoque visíveis sem alerta | Leva a orçamentos com itens indisponíveis |
| 4 | Comissão zerada sem aviso | Gera desconfiança e trabalho manual |
| 5 | Relatórios manuais sem dashboard em tempo real | Proprietário não tem visibilidade imediata |

---

## Histórico de Versões

| Versão | Data | Mudanças |
|---|---|---|
| 1.0.0 | 2025-06-19 | Criação — 30 problemas de UX identificados em 10 telas |
