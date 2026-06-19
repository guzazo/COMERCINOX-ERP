---
id: US-[000]
épico: [EPIC-000]
feature: [FEAT-000]
título: [Título da História]
módulo: [CRM / Estoque / Financeiro / etc.]
prioridade: Alta | Média | Baixa
status: rascunho | em-revisão | aprovado | implementado | descartado
estimativa: [número de horas ou pontos]
sprint: [SPRINT-00]
versão: 1.0.0
criado-em: YYYY-MM-DD
atualizado-em: YYYY-MM-DD
---

# História de Usuário: [Título]

## História

> **Como** [tipo de usuário],
> **Quero** [ação / funcionalidade],
> **Para que** [benefício / objetivo].

---

## Contexto

> Descreva brevemente o contexto de negócio que originou esta história.

---

## Critérios de Aceitação

> Lista de condições que devem ser atendidas para considerar esta história completa.
> Use o formato: **Dado** [contexto] **Quando** [ação] **Então** [resultado]

### Cenário 1: [Nome do cenário — fluxo principal]
- **Dado** que [contexto/precondição]
- **Quando** [ação do usuário]
- **Então** [resultado esperado]

### Cenário 2: [Nome do cenário — fluxo alternativo]
- **Dado** que [contexto]
- **Quando** [ação]
- **Então** [resultado]

### Cenário 3: [Nome do cenário — fluxo de erro]
- **Dado** que [contexto de erro]
- **Quando** [ação]
- **Então** [sistema deve reagir com...]

---

## Regras de Negócio Aplicáveis

| ID | Regra |
|---|---|
| RN01 | [Descrição] |
| RN02 | [Descrição] |

---

## Wireframe / Protótipo

```
[Link: /figma/wireframes/WF-[módulo]-[tela]-v1.png]
```

---

## Dependências

| ID | Descrição | Tipo |
|---|---|---|
| [US-000] | [História que deve ser concluída antes] | Bloqueante |
| [FEAT-000] | [Feature relacionada] | Informativa |

---

## Notas Técnicas

> Observações técnicas relevantes para o desenvolvimento. (Preencher durante refinamento)

---

## Definição de Pronto (Definition of Done)

- [ ] Critérios de aceitação todos passando
- [ ] Código revisado
- [ ] Testes básicos realizados
- [ ] Documentação atualizada
- [ ] Validado com usuário real

---

## Histórico de Versões

| Versão | Data | Autor | Mudanças |
|---|---|---|---|
| 1.0.0 | YYYY-MM-DD | [Nome] | Criação da história |
