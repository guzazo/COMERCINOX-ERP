# GUIA DE CONTRIBUIÇÃO E CONVENÇÕES
> Fonte única de verdade para padrões do projeto COMERCINOX ERP

---

## 1. Convenção de Nomenclatura

### 1.1 Arquivos e Diretórios

| Tipo | Padrão | Exemplo |
|---|---|---|
| Documentação Markdown | `kebab-case.md` | `cadastro-clientes.md` |
| Diretórios | `kebab-case` | `historias-usuario/` |
| Wireframes (exportações) | `WF-[módulo]-[tela]-v[n].png` | `WF-crm-lista-clientes-v1.png` |
| Protótipos (links) | `PT-[módulo]-v[n].md` | `PT-crm-v1.md` |
| ADRs | `ADR-[número]-[título].md` | `ADR-001-escolha-banco-dados.md` |
| Fluxogramas | `FL-[processo].md` | `FL-processo-venda.md` |
| Entrevistas | `ENT-[data]-[usuário].md` | `ENT-2025-07-10-proprietario.md` |
| Sprints | `SPRINT-[número].md` | `SPRINT-01.md` |
| Épicos | `EPIC-[número]-[título].md` | `EPIC-001-crm-clientes.md` |
| Features | `FEAT-[número]-[título].md` | `FEAT-001-cadastro-cliente.md` |

### 1.2 IDs e Referências Cruzadas

Todo documento deve conter um ID único no cabeçalho:

```markdown
---
id: FEAT-001
título: Cadastro de Cliente
módulo: CRM
status: rascunho | em-revisão | aprovado | implementado
versão: 1.0.0
criado-em: YYYY-MM-DD
atualizado-em: YYYY-MM-DD
---
```

### 1.3 Status Permitidos

| Status | Significado |
|---|---|
| `rascunho` | Em criação, não revisado |
| `em-revisão` | Aguardando validação |
| `aprovado` | Validado e pronto para próxima fase |
| `implementado` | Código criado e em produção |
| `descartado` | Decidido por não implementar |
| `em-espera` | Aguardando decisão externa |

---

## 2. Estratégia de Branches Git

### 2.1 Branches Permanentes

```
main          → Documentação estável, aprovada e validada
develop       → Integração de trabalho em andamento
```

### 2.2 Branches Temporárias

| Tipo | Padrão | Exemplo |
|---|---|---|
| Descoberta | `discovery/[módulo]` | `discovery/zuma-estoque` |
| Documentação | `docs/[módulo]-[assunto]` | `docs/crm-regras-negocio` |
| Wireframe | `ux/wireframe-[tela]` | `ux/wireframe-lista-clientes` |
| Feature (código) | `feat/[módulo]-[funcionalidade]` | `feat/crm-cadastro-cliente` |
| Correção (código) | `fix/[módulo]-[problema]` | `fix/crm-validacao-cnpj` |
| Refactor | `refactor/[módulo]-[assunto]` | `refactor/crm-componentes` |

### 2.3 Fluxo de Trabalho

```
┌─────────────────────────────────────────────────────────┐
│                    FLUXO GIT                            │
│                                                         │
│  discovery/* ──┐                                        │
│  docs/*     ──►├── develop ──► (review) ──► main        │
│  ux/*       ──┘                                         │
│                                                         │
│  feat/*     ──┐                                         │
│  fix/*      ──►├── develop ──► (review) ──► main        │
│  refactor/* ──┘                                         │
└─────────────────────────────────────────────────────────┘
```

### 2.4 Regras de Branch

1. **Nunca commitar diretamente em `main`**
2. Todo merge em `main` requer que o documento esteja com status `aprovado`
3. Branches devem ser deletadas após merge
4. Nome de branch sempre em `kebab-case`, sem acentos

---

## 3. Padrão de Commit

Seguir o padrão **Conventional Commits**:

```
<tipo>(<escopo>): <descrição curta em português>

[corpo opcional]

[rodapé opcional]
```

### 3.1 Tipos de Commit

| Tipo | Quando usar |
|---|---|
| `docs` | Criação ou atualização de documentação |
| `discovery` | Descoberta de processo ou tela do ZUMA |
| `research` | Entrevistas, insights, problemas identificados |
| `ux` | Wireframes, protótipos, design system |
| `backlog` | Épicos, features, histórias de usuário |
| `feat` | Nova funcionalidade de código |
| `fix` | Correção de bug |
| `refactor` | Refatoração sem mudança de comportamento |
| `chore` | Tarefas de manutenção (configs, .gitignore, etc) |
| `adr` | Novo Architecture Decision Record |

### 3.2 Exemplos de Commits

```bash
docs(crm): adiciona regras de negócio do cadastro de clientes
discovery(zuma): mapeia tela de controle de estoque
research(entrevistas): adiciona entrevista com proprietário - 2025-07-10
ux(wireframes): adiciona wireframe da lista de clientes v1
backlog(epics): cria épico EPIC-001 CRM Clientes
adr(database): registra decisão de uso do PostgreSQL (ADR-001)
feat(crm): implementa cadastro de cliente básico
fix(crm): corrige validação de CNPJ duplicado
```

---

## 4. Estratégia de Versionamento

### 4.1 Versionamento de Documentos

Cada documento usa **Semantic Versioning simplificado**:

```
v[MAJOR].[MINOR].[PATCH]

MAJOR → Mudança estrutural (escopo, processo)
MINOR → Adição de conteúdo significativo
PATCH → Correções, ajustes menores, revisões de texto
```

| Situação | Exemplo |
|---|---|
| Documento criado | v1.0.0 |
| Nova seção adicionada | v1.1.0 |
| Correção de erro | v1.0.1 |
| Reestruturação completa | v2.0.0 |

### 4.2 Versionamento do Sistema (futuro)

Quando o código existir:

```
v[MAJOR].[MINOR].[PATCH]

MAJOR → Breaking change (incompatível com versão anterior)
MINOR → Nova feature retrocompatível
PATCH → Bug fix retrocompatível
```

### 4.3 Tags Git (futuro, para código)

```bash
git tag -a v1.0.0 -m "MVP CRM: primeira versão em produção"
git tag -a v1.1.0 -m "CRM: adição do módulo de orçamentos"
```

---

## 5. Processo de Revisão de Documentação

### 5.1 Para documentos na Fase 0 (Descoberta)

```
1. Criar branch discovery/* ou docs/*
2. Criar/atualizar documento com status: rascunho
3. Commitar e fazer push
4. Abrir Pull Request para develop
5. Revisar com usuários (validação informal)
6. Atualizar status para: aprovado
7. Merge em develop
8. Após acúmulo de documentos aprovados → merge em main
```

### 5.2 Checklist de Revisão de Documento

Antes de marcar um documento como `aprovado`:

- [ ] ID único definido no cabeçalho
- [ ] Status atualizado corretamente
- [ ] Data de criação e atualização preenchidas
- [ ] Conteúdo validado com pelo menos um usuário real
- [ ] Links para documentos relacionados presentes
- [ ] Sem erros ortográficos graves
- [ ] Nomenclatura de arquivo seguindo o padrão

---

## 6. Estrutura para Documentação Contínua

### 6.1 Cadência de Atualização

| Frequência | Atividade |
|---|---|
| A cada sessão de trabalho | Commitar progresso em branch ativa |
| Semanal | Revisar e mover documentos para `em-revisão` |
| Ao fim de cada sprint | Merge de documentos aprovados em `main` |
| Mensalmente | Atualizar ROADMAP e CHANGELOG |

### 6.2 CHANGELOG

O arquivo `CHANGELOG.md` deve registrar toda mudança significativa no projeto:

```markdown
## [Não lançado]
### Adicionado
- ...

## [v1.0.0] - 2025-07-10
### Adicionado
- Estrutura inicial do repositório
- README principal
- ROADMAP v1.0.0
- Templates padronizados
```

### 6.3 Ordem de Prioridade para Documentação

Para cada tela ou processo descoberto, documentar sempre nesta ordem:

```
1. processo.md → O que o processo faz hoje
2. tela.md     → Como a tela funciona hoje
3. Problemas   → O que está errado / doloroso
4. Insights    → Oportunidades de melhoria
5. historia-usuario.md → O que o usuário precisa
6. requisito.md        → O que o sistema deve fazer
```

---

## 7. Configuração Inicial do Repositório

### 7.1 Arquivos obrigatórios na raiz

```
README.md       ✅
ROADMAP.md      ✅
CONTRIBUTING.md ✅ (este arquivo)
CHANGELOG.md    ✅
.gitignore      ✅
```

### 7.2 .gitignore

```gitignore
# Sistemas operacionais
.DS_Store
Thumbs.db
desktop.ini

# IDEs
.vscode/
.idea/
*.swp
*.swo

# Dependências (futuro, quando houver código)
node_modules/
dist/
build/
.env
.env.local
.env.production

# Arquivos temporários
*.tmp
*.log
```

---

*Versão: 1.0.0 | Criado em: 2025*
