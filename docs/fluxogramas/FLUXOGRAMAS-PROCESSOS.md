---
id: FL-PROC-001-005
título: Fluxogramas (AS-IS) — Comissão, Crédito, Bloqueio, Devolução
status: em-revisão
versão: 1.0.0
criado-em: 2026-06-23
origem: PROC-001..005 (esclarecimentos 2026-06-23)
nota: fluxos do ESTADO ATUAL (AS-IS), sem idealização. Diamantes = decisão; cinza = manual/externo.
---

# Fluxogramas dos Processos (AS-IS)

> Diagramas Mermaid do funcionamento **real atual**. Não representam o ERP futuro.

---

## 1. Fechamento de Comissão (PROC-001)

```mermaid
flowchart TD
    A["Início: 1ª semana do mês seguinte"] --> B["Roberta consulta relatório<br/>Vendas por Vendedor (ZUMA)"]
    B --> C["Verifica devoluções do período"]
    C --> D{"Devolução identificada<br/>ANTES do fechamento?"}
    D -- Não --> E["Não desconta<br/>(RN-COM-008)"]
    D -- Sim --> F["Confirma com Brendo:<br/>material voltou ao estoque?"]
    F --> G{"Confirmação<br/>física OK?"}
    G -- Não --> E
    G -- Sim --> H["Remove itens devolvidos da base"]
    E --> I["Calcula comissão à mão:<br/>1% x venda líquida<br/>(Lucilene 0,5%)"]
    H --> I
    I --> J["Registra valores em papel"]
    J --> K["Paga junto ao salário<br/>(último dia útil da 1ª semana)"]
    K --> L["Fim"]

    classDef manual fill:#162F52,stroke:#F5A623,color:#fff;
    class B,C,F,H,I,J,K manual;
```

**Problemas:** 100% manual; sem histórico; sem rastreabilidade; depende de Roberta e Brendo.

---

## 2. Concessão de Crédito (PROC-003)

```mermaid
flowchart TD
    A["Cliente solicita compra a prazo / crédito"] --> B["Mãe do proprietário inicia análise"]
    B --> C["Consulta Serasa"]
    C --> D["Avalia histórico:<br/>1ª forma de pagamento + relacionamento"]
    D --> E["Solicita 3 comprovantes de<br/>pagamento a fornecedores semelhantes"]
    E --> F["Avalia capacidade financeira:<br/>maior compra, pontualidade,<br/>capital/contrato social, porte, IR"]
    F --> G{"Análise completa<br/>aprovada?"}
    G -- Não --> H["Crédito negado /<br/>solicita mais documentos"]
    G -- Sim --> I["Crédito aprovado<br/>(define limite)"]
    H --> J["Fim"]
    I --> J

    classDef manual fill:#162F52,stroke:#F5A623,color:#fff;
    class B,C,D,E,F,I manual;
```

**Problemas:** sem workflow formal; critérios não documentados; decisão concentrada em 1 pessoa.

---

## 3. Bloqueio de Clientes (PROC-004)

```mermaid
flowchart TD
    A["Cliente com débito em aberto"] --> B{"Inadimplência<br/>justifica bloqueio?"}
    B -- Não --> C["Mantém liberado"]
    B -- Sim --> D["Bloqueia no ZUMA<br/>(~15% dos inadimplentes)"]
    D --> E["ZUMA NÃO registra<br/>motivo / data / responsável<br/>(RN-CLI-017)"]
    E --> F{"Cliente bloqueado<br/>tenta comprar?"}
    F -- "À vista" --> G["Venda permitida à vista;<br/>débito antigo permanece<br/>(RN-CLI-016)"]
    F -- "A prazo" --> H["Bloqueado para prazo"]
    C --> I["Fim"]
    G --> I
    H --> I

    classDef gap fill:#3a1620,stroke:#E5484D,color:#fff;
    class E gap;
```

**Oportunidade (não-MVP até validar):** registrar motivo, data, responsável e histórico de liberações.

---

## 4. Devolução com Geração de Crédito (PROC-005)

```mermaid
flowchart TD
    A["Cliente devolve material"] --> B["Vendedor preenche<br/>formulário padrão de devolução"]
    B --> C["Documento entregue a Benini (estoque)"]
    C --> D["Benini verifica fisicamente<br/>o retorno ao estoque"]
    D --> E{"Material retornou<br/>ao estoque?"}
    E -- Não --> F["Pendente — não gera crédito"]
    E -- Sim --> G["Roberta confirma a devolução"]
    G --> H["Crédito lançado manualmente<br/>no cadastro do cliente"]
    H --> I{"Antes do fechamento<br/>de comissão?"}
    I -- Sim --> J["Reduz base de comissão<br/>(liga PROC-001)"]
    I -- Não --> K["Não afeta comissão já paga"]
    F --> L["Fim"]
    J --> L
    K --> L

    classDef manual fill:#162F52,stroke:#F5A623,color:#fff;
    class B,C,D,G,H manual;
```

**Problemas:** baseado em papel; conferência manual; sem rastreabilidade digital.

---

## Histórico de Versões
| Versão | Data | Mudanças |
|---|---|---|
| 1.0.0 | 2026-06-23 | Criação — 4 fluxogramas AS-IS (comissão, crédito, bloqueio, devolução) |
