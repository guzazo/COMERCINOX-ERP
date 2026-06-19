# ROADMAP — ERP Comercialinox

> **Princípio fundamental:** Observar → Documentar → Entender → Modelar → Validar → Desenvolver

---

## 📊 Visão Geral das Fases

```
FASE 0          FASE 1          FASE 2          FASE 3          FASE 4
Descoberta  →   MVP Módulo  →   Validação   →   Expansão    →   Migração
                CRM             Operacional     de Módulos      Completa
(3–4 meses)     (2–3 meses)     (1–2 meses)     (6–12 meses)    (6–12 meses)
```

---

## 🔍 FASE 0 — Descoberta e Documentação
**Status:** 🟡 Em andamento
**Duração estimada:** 3–4 meses
**Critério de saída:** Mapeamento completo do ZUMA + validação com usuários

### Objetivos
- [ ] Mapear todas as telas do ZUMA utilizadas diariamente
- [ ] Documentar processos de negócio reais
- [ ] Identificar e entrevistar todos os usuários do sistema
- [ ] Catalogar regras de negócio implícitas e explícitas
- [ ] Identificar dores e problemas reais (UX, processo, tecnologia)
- [ ] Criar personas de usuários
- [ ] Gerar inventário de telas
- [ ] Gerar inventário de regras de negócio
- [ ] Criar backlog inicial priorizado

### Entregáveis
- [ ] Mapa de processos da Comercinox
- [ ] Inventário de telas do ZUMA
- [ ] Inventário de regras de negócio
- [ ] Personas de usuários
- [ ] Relatório de problemas priorizados
- [ ] Backlog inicial com épicos e features
- [ ] Wireframes de baixa fidelidade dos módulos prioritários
- [ ] Protótipo navegável no Figma para validação

### Módulos a mapear (ZUMA)
- [ ] Controle de Estoque
- [ ] Controle de Vendas / Comissão
- [ ] Contas a Receber
- [ ] Contas a Pagar
- [ ] Faturamento / NF-e
- [ ] Clientes / CRM
- [ ] Relatórios gerenciais mais usados

---

## 🏗️ FASE 1 — MVP: Módulo CRM
**Status:** ⚪ Não iniciado
**Duração estimada:** 2–3 meses
**Critério de saída:** Sistema em uso real com dados reais por 30 dias consecutivos

### Escopo do MVP CRM
O ERP Comercialinox começa pelo CRM pois:
1. Não depende de integração fiscal
2. Agrega valor imediato às vendas
3. O ZUMA tem CRM fraco
4. É o menor risco de migração

#### Funcionalidades do MVP CRM
- [ ] Cadastro de clientes
- [ ] Cadastro de contatos
- [ ] Histórico comercial por cliente
- [ ] Funil de vendas (Frio / Médio / Quente / Recorrente)
- [ ] Follow-ups e lembretes
- [ ] Dashboard comercial básico
- [ ] Módulo de orçamentos (básico)

### ZUMA permanece responsável (Fase 1)
- Estoque oficial
- Emissão fiscal (NF-e)
- Financeiro oficial
- Obrigações fiscais

---

## ✅ FASE 2 — Validação Operacional
**Status:** ⚪ Não iniciado
**Duração estimada:** 1–2 meses

### Objetivos
- [ ] Validar o CRM com os usuários reais por 30+ dias
- [ ] Coletar métricas de uso e satisfação
- [ ] Identificar bugs e melhorias
- [ ] Documentar lições aprendidas
- [ ] Decidir próximo módulo a desenvolver

---

## 📦 FASE 3 — Expansão de Módulos
**Status:** ⚪ Não iniciado
**Duração estimada:** 6–12 meses

### Módulos candidatos (ordem a validar)
1. Orçamentos avançados
2. Pedidos de venda
3. Integração Mercado Livre
4. Dashboard financeiro (leitura)
5. Gestão de entregas básica
6. Relatórios gerenciais customizados

> A prioridade exata será definida após validação da Fase 2.

---

## 🔄 FASE 4 — Migração Completa
**Status:** ⚪ Não iniciado
**Duração estimada:** 6–12 meses

### Módulos de migração crítica (alta complexidade)
- Estoque oficial (requer auditoria)
- Financeiro oficial
- Emissão fiscal (NF-e / NFC-e)
- Obrigações legais (SPED, CT-e)

> ⚠️ Esta fase só deve iniciar quando o sistema estiver comprovadamente estável em produção há pelo menos 6 meses.

---

## 💰 Análise de Viabilidade Financeira

| Item | Valor |
|---|---|
| Custo atual ZUMA (mensal) | R$ 1.300 |
| Custo atual ZUMA (anual) | R$ 15.600 |
| Custo ZUMA em 3 anos | R$ 46.800 |
| Custo ZUMA em 5 anos | R$ 78.000 |
| Investimento estimado (infra própria/mês) | R$ 200–500 |
| Break-even estimado | 12–18 meses após migração completa |

---

## ⏱️ Timeline Realista

```
2025 Q3      2025 Q4      2026 Q1      2026 Q2      2026 Q3      2026 Q4
│            │            │            │            │            │
├── FASE 0 ──────────────►│            │            │            │
│            │            ├── FASE 1 ──►│            │            │
│            │            │            ├── FASE 2 ──►│            │
│            │            │            │            ├──── FASE 3 ────►
```

> ⚠️ **Aviso:** Este timeline pressupõe 10–15 horas semanais dedicadas ao projeto, sozinho. Ajuste conforme sua disponibilidade real.

---

## 🎓 Habilidades Necessárias

### Já necessárias (Fases 0–1)
- [ ] Git / GitHub (básico-intermediário)
- [ ] Figma (wireframes e protótipos)
- [ ] Entrevista com usuários (UX Research básico)
- [ ] Documentação técnica em Markdown
- [ ] SQL básico (modelagem conceitual)

### Necessárias para Fase 1 (desenvolvimento)
- [ ] React + TypeScript (intermediário)
- [ ] Next.js (básico)
- [ ] Tailwind CSS (básico)
- [ ] NestJS (básico)
- [ ] PostgreSQL (intermediário)
- [ ] REST APIs (intermediário)

### Necessárias para Fases 3–4 (avançado)
- [ ] Integração com APIs externas (Mercado Livre, SEFAZ)
- [ ] Segurança (autenticação, autorização, LGPD)
- [ ] DevOps básico (deploy, CI/CD)
- [ ] Performance e escalabilidade

---

*Versão: 1.0.0 | Criado em: 2025*
