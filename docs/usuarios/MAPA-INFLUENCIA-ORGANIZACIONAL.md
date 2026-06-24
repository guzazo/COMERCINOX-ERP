---
id: ORG-INFLU-001
título: Mapa de Influência Organizacional + Matrizes — Comercinox
status: em-revisão
versão: 1.0.0
criado-em: 2026-06-23
origem: personas v2 (descoberta organizacional)
objetivo: orientar engajamento, validação e estratégia de adoção do ERP
---

# Mapa de Influência Organizacional

> Base para **estratégia de adoção** e ordem de envolvimento. Escalas de descoberta — validar.

---

## 1. Mapa de influência (quem influencia quem)

```mermaid
flowchart TD
    W["WANDERSON<br/>Proprietário · decisão final"]
    R["ROBERTA<br/>Admin/Financeiro · conselheira"]
    G["GUILHERME<br/>Inovação · possível PO"]
    B["BRENDO<br/>Fiscal/Caixa · champion técnico"]
    BE["BENINI<br/>Estoque/Operações"]
    T["TARGINO<br/>Vendedor"]
    P["POLYANA<br/>Vendedora"]
    L["LEANDRO<br/>Motorista"]

    R -->|aconselha / forte influência| W
    G -->|propõe modernização| W
    G -->|alinha requisitos| R
    W -->|aprova desconto / decisões| T
    W -->|aprova desconto / decisões| P
    R -->|comissão, crédito, devolução| T
    R -->|comissão, crédito, devolução| P
    BE -->|confirma devolução física| R
    B -->|caixa / fiscal| R
    L -->|formulário de horas| R
    classDef hi fill:#162F52,stroke:#F5A623,color:#fff;
    class W,R hi;
```

> **Caminho de adoção:** Guilherme (PO) → conquista **Roberta** → Roberta sustenta junto a **Wanderson**.
> Sem Roberta convencida, a decisão de Wanderson não se sustenta no dia a dia.

---

## 2. Matriz Poder × Interesse

```mermaid
quadrantChart
    title Poder x Interesse no projeto ERP
    x-axis "Baixo Interesse" --> "Alto Interesse"
    y-axis "Baixo Poder" --> "Alto Poder"
    quadrant-1 "Gerenciar de perto"
    quadrant-2 "Manter satisfeito"
    quadrant-3 "Monitorar"
    quadrant-4 "Manter informado/engajar"
    Wanderson: [0.48, 0.95]
    Roberta: [0.82, 0.80]
    Guilherme: [0.95, 0.28]
    Brendo: [0.80, 0.32]
    Benini: [0.45, 0.24]
    Targino: [0.50, 0.20]
    Polyana: [0.52, 0.20]
    Leandro: [0.20, 0.10]
```

| Quadrante | Pessoas | Estratégia |
|---|---|---|
| Gerenciar de perto (poder+interesse altos) | **Roberta** | Co-criar, decisões de processo |
| Manter satisfeito (poder alto, interesse médio) | **Wanderson** | Mostrar valor sem tirar autonomia; demos curtas |
| Manter informado/engajar (interesse alto, poder baixo) | **Guilherme, Brendo** | PO e piloto — protagonistas da implantação |
| Monitorar (baixo/baixo) | Targino, Polyana, Benini, Leandro | Treinar; ouvir dores; simplicidade |

---

## 3. Matriz Resistência à Mudança × Impacto na adoção

| Pessoa | Resistência | Maturidade | Impacto se resistir | Estratégia |
|---|---|---|---|---|
| **Wanderson** | Média/Alta | 2/5 | 🔴 Crítico (decide tudo) | Envolver cedo; ERP como apoio à decisão, não substituto; ganhos visíveis |
| **Roberta** | Média | 3/5 | 🔴 Crítico (usuária-chave) | Respeitar Excel (importar/exportar); migração gradual; co-design |
| **Benini** | Média/Alta | 2/5 | 🟡 Médio (operacional) | UI simples; treinar no físico (devolução/estoque) |
| **Targino** | Média | 2/5 | 🟡 Médio | Treino prático; mostrar velocidade no orçamento |
| **Polyana** | Média | 2/5 | 🟡 Médio | Idem; revisar processo de confirmação WhatsApp |
| **Leandro** | n/d | 1/5 | 🟢 Baixo (externo) | Fora do MVP; eventual app simples no futuro |
| **Brendo** | Baixa | 4/5 | 🟢 Baixo (aliado) | **Champion / piloto** |
| **Guilherme** | Muito baixa | 5/5 | 🟢 Baixo (motor) | **PO / condutor** |

> **Risco-chave de adoção:** combinação **alto poder + alta resistência + baixa maturidade** =
> **Wanderson**. Mitigar com entregas pequenas, valor imediato (comissão/dashboard) e zero perda de controle.

---

## 4. Usuários-chave para entrevistas e implantação

| Prioridade | Pessoa | Papel na descoberta | Papel na implantação |
|---|---|---|---|
| 1 | **Roberta** | Comissão, crédito, devolução, fechamento | Usuária-âncora / validação |
| 2 | **Wanderson** | Decisão, aprovação de desconto, carteira | Patrocinador |
| 3 | **Brendo** | Caixa/fiscal | **Piloto / champion técnico** |
| 4 | **Benini** | Devolução física, estoque | Validação operacional |
| 5 | **Targino + Polyana** | Carteira, orçamento, WhatsApp | Usuários diários |
| 6 | **Leandro** | Horas extras/pernoite (externo) | Fora do MVP |

---

## Histórico de Versões
| 1.0.0 | 2026-06-23 | Criação — mapa de influência, Poder×Interesse, Resistência, usuários-chave |
