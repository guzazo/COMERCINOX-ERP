# COMERCINOX ERP
> Repositório oficial de descoberta, documentação, arquitetura e desenvolvimento do ERP Comercinox.

---

## 🎯 Visão do Projeto

A **Comercinox** é uma distribuidora B2B de produtos em aço inox que atende metalúrgicas, laticínios e prestadores de serviço industrial.

Este repositório é a **fonte única da verdade** (Single Source of Truth) para substituição gradual do ERP ZUMA por um sistema próprio, especializado e construído do zero — o **ERP Comercialinox**.

---

## 🧭 Objetivos Estratégicos

| # | Objetivo | Status |
|---|---|---|
| 1 | Melhorar continuamente a operação da Comercinox | 🔄 Em andamento |
| 2 | Transformar melhorias em casos reais para consultoria de automação industrial | 📋 Planejado |

> A Comercinox funciona como **laboratório de validação**. Toda solução criada deve primeiro resolver um problema real da empresa antes de ser considerada replicável.

---

## 📁 Estrutura do Repositório

```
COMERCINOX-ERP/
│
├── docs/                        # Toda documentação do projeto
│   ├── descoberta-zuma/         # Mapeamento do sistema atual (ZUMA)
│   ├── processos/               # Processos de negócio mapeados
│   ├── regras-negocio/          # Regras de negócio documentadas
│   ├── usuarios/                # Perfis de usuários (personas)
│   ├── requisitos/
│   │   ├── casos-de-uso/        # Casos de uso detalhados
│   │   └── historias-usuario/   # User stories no formato padrão
│   ├── fluxogramas/             # Diagramas de processo (Mermaid/Draw.io)
│   └── arquitetura/
│       ├── database/            # Modelos de dados, ERDs
│       ├── integracoes/         # Diagramas de integração
│       └── decisoes-tecnicas/   # ADRs (Architecture Decision Records)
│
├── figma/                       # Referências e exportações de design
│   ├── wireframes/              # Links e capturas de wireframes
│   ├── prototipos/              # Links e capturas de protótipos navegáveis
│   └── design-system/          # Tokens, componentes, guidelines
│
├── research/                    # Pesquisa com usuários
│   ├── entrevistas/             # Transcrições e notas de entrevistas
│   ├── problemas/               # Problemas identificados e priorizados
│   └── insights/                # Insights e oportunidades
│
├── backlog/                     # Gestão de produto
│   ├── epics/                   # Épicos do produto
│   ├── features/                # Features detalhadas
│   └── sprints/                 # Planejamento de sprints
│
├── templates/                   # Templates padronizados
│   ├── tela.md
│   ├── processo.md
│   ├── requisito.md
│   ├── historia-usuario.md
│   └── decisao-arquitetural.md
│
├── README.md                    # Este arquivo
├── ROADMAP.md                   # Roadmap do projeto
├── CONTRIBUTING.md              # Convenções e guia de contribuição
└── CHANGELOG.md                 # Histórico de mudanças
```

---

## 🗺️ Roadmap

Veja o roadmap completo em [ROADMAP.md](./ROADMAP.md).

**Fase atual: Fase 0 — Descoberta e Documentação**

---

## 🛠️ Stack Tecnológica Planejada

| Camada | Tecnologia |
|---|---|
| Frontend | React + Next.js + TypeScript + Tailwind CSS |
| Backend | NestJS + TypeScript |
| Banco de Dados | PostgreSQL |
| Design | Figma |
| Versionamento | Git + GitHub |
| IA | Claude Code |

---

## 👥 Equipe

| Papel | Responsável |
|---|---|
| Fundador / Tech Lead / Dev | Guilherme |
| Usuários-alvo (clientes internos) | Proprietários, Comercial, Administrativo |

---

## 🚦 Status do Projeto

**Fase 0 — Descoberta** está em andamento.

Nenhum código do ERP deve ser criado antes da conclusão do mapeamento do ZUMA e validação com usuários.

---

## 📋 Processo Obrigatório para Novos Módulos

Qualquer novo módulo deve obrigatoriamente seguir este fluxo:

```
1. Mapear processo atual
2. Mapear telas atuais
3. Identificar problemas
4. Criar documentação
5. Criar wireframes
6. Validar com usuários reais
7. Criar código somente após validação
```

---

## 📞 Contexto de Negócio

- **Clientes-alvo:** Metalúrgicas, laticínios, prestadores de serviço industrial
- **Canais de venda:** WhatsApp, Google, telefone, Mercado Livre
- **Sistema atual:** ZUMA ERP (R$1.300/mês)
- **Objetivo financeiro:** Substituição gradual do ZUMA por sistema próprio

---

*Última atualização: 2026 | Versão do documento: 1.0.0*
