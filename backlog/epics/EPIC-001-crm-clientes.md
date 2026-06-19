---
id: EPIC-001
título: CRM — Gestão de Clientes e Relacionamento Comercial
módulo: CRM
prioridade: Alta
status: em-revisão
versão: 1.0.0
criado-em: 2025
---

# EPIC-001: CRM — Gestão de Clientes e Relacionamento Comercial

## Declaração do Épico

**Como** equipe comercial da Comercinox,
**Queremos** um sistema centralizado para gerenciar clientes, contatos e o ciclo comercial,
**Para que** possamos substituir o controle manual via WhatsApp e Excel, aumentar a eficiência de vendas e ter visibilidade real do funil.

---

## Contexto de Negócio

O CRM é o módulo mais crítico para iniciar porque:

1. **Dor real imediata:** Atualmente clientes são gerenciados por WhatsApp, planilhas e memória dos vendedores
2. **Sem risco fiscal:** Não envolve emissão de nota fiscal nem integração com SEFAZ
3. **Valor visível rápido:** Os proprietários verão resultado em semanas
4. **Menor complexidade técnica:** Ponto de entrada seguro para o primeiro módulo
5. **Base para tudo:** Todos os outros módulos dependem de um bom cadastro de clientes

---

## Problema que resolve

| Problema Atual | Solução Esperada |
|---|---|
| Histórico de clientes espalhado no WhatsApp | Histórico centralizado e pesquisável |
| Follow-ups esquecidos | Lembretes e agenda de follow-up |
| Nenhuma visibilidade do funil | Dashboard com funil visual |
| Clientes inativos não identificados | Alertas de inatividade automáticos |
| Orçamentos perdidos em e-mail/WhatsApp | Módulo de orçamentos integrado |

---

## Escopo do Épico

### Dentro do escopo (IN)
- Cadastro de clientes (CNPJ, dados, segmento)
- Cadastro de contatos por cliente
- Histórico de interações comerciais
- Funil de vendas (Frio → Médio → Quente → Recorrente)
- Follow-ups com data e responsável
- Dashboard comercial básico
- Orçamentos (criação e histórico)

### Fora do escopo (OUT)
- Emissão de NF-e (permanece no ZUMA)
- Controle de estoque (permanece no ZUMA)
- Financeiro (permanece no ZUMA)
- Integração com WhatsApp (fase futura)
- App mobile (fase futura)

---

## Features do Épico

| ID | Feature | Prioridade | Status |
|---|---|---|---|
| FEAT-001 | Cadastro de Clientes | Alta | Não iniciado |
| FEAT-002 | Cadastro de Contatos | Alta | Não iniciado |
| FEAT-003 | Histórico Comercial | Alta | Não iniciado |
| FEAT-004 | Funil de Vendas | Alta | Não iniciado |
| FEAT-005 | Follow-ups e Lembretes | Alta | Não iniciado |
| FEAT-006 | Dashboard Comercial | Média | Não iniciado |
| FEAT-007 | Módulo de Orçamentos | Média | Não iniciado |

---

## Critérios de Conclusão do Épico

- [ ] Todas as features IN do escopo implementadas e testadas
- [ ] Validado com proprietários e equipe comercial por 30 dias em produção
- [ ] Dados reais de clientes migrados do Excel/ZUMA para o novo sistema
- [ ] Nenhum retorno ao processo manual por mais de 2 semanas
- [ ] Satisfação dos usuários ≥ 7/10 (avaliação informal)

---

## Dependências

| Dependência | Tipo | Observação |
|---|---|---|
| Mapeamento do ZUMA (Fase 0) | Pré-requisito | Deve ser concluída antes do desenvolvimento |
| Entrevistas com usuários | Pré-requisito | Validar escopo e prioridades |
| Wireframes validados | Pré-requisito | Nenhum código antes de validação |
| Stack tecnológica definida (ADR) | Pré-requisito | |

---

## Notas

> O funil de vendas já tem uma estrutura definida no projeto ComercialIndus (Frio/Médio/Quente/Recorrente).
> Esta estrutura deve ser considerada como ponto de partida e validada com os usuários antes da implementação.

---

## Histórico de Versões

| Versão | Data | Autor | Mudanças |
|---|---|---|---|
| 1.0.0 | 2025 | Guilherme | Criação do épico |
