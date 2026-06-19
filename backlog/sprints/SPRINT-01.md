---
id: SPRINT-01
título: Descoberta — Mapeamento do ZUMA e Usuários
fase: Fase 0 — Descoberta
status: planejado
início: YYYY-MM-DD
fim: YYYY-MM-DD
duração: 2 semanas
---

# SPRINT-01: Descoberta — Mapeamento do ZUMA e Usuários

## Objetivo da Sprint

Mapear as telas e processos do ZUMA mais utilizados diariamente pela Comercinox, entrevistar os usuários e gerar o primeiro inventário de telas e processos.

---

## Foco da Sprint

> **Regra:** Uma sprint, um foco. Nada de código.

Esta sprint é exclusivamente de **descoberta e documentação**.

---

## Tarefas

### Bloco 1 — Preparação

- [ ] Criar repositório no GitHub
- [ ] Fazer push da estrutura inicial
- [ ] Criar branch `discovery/zuma-mapeamento-inicial`
- [ ] Revisar templates com a equipe

### Bloco 2 — Entrevistas com Usuários

- [ ] Agendar entrevista com Proprietário 1
- [ ] Agendar entrevista com Proprietário 2 (se houver)
- [ ] Agendar entrevista com responsável comercial
- [ ] Agendar entrevista com responsável administrativo
- [ ] Conduzir entrevistas e documentar em `/research/entrevistas/`

**Roteiro básico de entrevista:**
1. Quais telas você usa todos os dias no ZUMA?
2. Para cada tela: o que você faz nela? O que não funciona bem?
3. Quais processos são feitos fora do ZUMA (Excel, WhatsApp, papel)?
4. O que te faz perder mais tempo no dia a dia?
5. O que você mais precisaria que um sistema novo tivesse?

### Bloco 3 — Mapeamento de Telas (ZUMA)

Para cada tela identificada nas entrevistas, usar o template `/templates/tela.md`:

- [ ] Tela: Cadastro de Clientes
- [ ] Tela: Controle de Vendas
- [ ] Tela: Emissão de NF-e
- [ ] Tela: Contas a Receber
- [ ] Tela: Contas a Pagar
- [ ] Tela: Controle de Estoque
- [ ] Tela: Relatórios Gerenciais (mais usados)
- [ ] [Outras identificadas nas entrevistas]

### Bloco 4 — Mapeamento de Processos

Para cada processo identificado, usar o template `/templates/processo.md`:

- [ ] Processo: Recebimento de lead / orçamento
- [ ] Processo: Emissão de NF-e
- [ ] Processo: Controle de estoque (entrada/saída)
- [ ] Processo: Contas a receber
- [ ] [Outros identificados nas entrevistas]

### Bloco 5 — Consolidação

- [ ] Criar inventário de telas em `/docs/descoberta-zuma/inventario-telas.md`
- [ ] Criar inventário de regras de negócio em `/docs/regras-negocio/`
- [ ] Criar relatório de problemas em `/research/problemas/`
- [ ] Atualizar backlog com épicos e features descobertos
- [ ] Fazer merge da branch em `develop`

---

## Entregáveis da Sprint

| Entregável | Status |
|---|---|
| Repositório criado e estruturado no GitHub | ⬜ |
| Mínimo 3 entrevistas realizadas e documentadas | ⬜ |
| Mínimo 5 telas do ZUMA mapeadas | ⬜ |
| Mínimo 3 processos mapeados | ⬜ |
| Inventário inicial de telas | ⬜ |
| Inventário inicial de regras de negócio | ⬜ |
| Relatório de problemas identificados | ⬜ |

---

## Critério de Conclusão da Sprint

A sprint só está concluída quando:
1. Todos os entregáveis acima estão com status ✅
2. Documentos estão com status `em-revisão` ou `aprovado`
3. Branch mergeada em `develop`

---

## Notas da Sprint

> [Espaço para anotações durante a sprint]

---

## Retrospectiva (preencher ao final)

### O que funcionou bem?
-

### O que não funcionou?
-

### O que fazer diferente na próxima sprint?
-
