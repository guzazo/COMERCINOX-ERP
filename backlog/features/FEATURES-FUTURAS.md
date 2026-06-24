---
id: FEAT-FUTURAS-001
título: Features Futuras derivadas das descobertas (PROC-001..006)
status: backlog (não priorizado)
versão: 1.0.0
criado-em: 2026-06-23
aviso: NENHUMA destas entra no MVP sem evidência de uso recorrente + validação. Lista de candidatos.
---

# Features Futuras (candidatas)

> Derivadas das descobertas recentes. **Não** são compromisso de escopo. MVP atual permanece:
> FEAT-001 (Clientes), FEAT-002 (Vendedores/Comissão), FEAT-003 (Catálogo).
> Fase: 🟡 Fase 2 · 🟠 Fase 3 · ⚪ Oportunidade futura/externo.

| ID | Feature | Origem | Fase | Pré-condição de validação |
|---|---|---|---|---|
| FEAT-F01 | **Workflow de aprovação de desconto** (vendedor→proprietário, histórico) | PROC-aprovação, RN-APR | 🟡 | Pergunta 7 (teto por vendedor) |
| FEAT-F02 | **Gestão de bloqueio** (motivo, data, responsável, histórico de liberações) | PROC-004, RN-CLI-017 | ⚪ | Validar uso recorrente (não-MVP) |
| FEAT-F03 | **Concessão de crédito** (Serasa, 3 referências, parecer, limite) | PROC-003, RN-CRE | 🟠 | Perguntas 21–23 |
| FEAT-F04 | **Devolução digital com geração de crédito** (substitui papel) | PROC-005, RN-DEV-001 | 🟡 | Perguntas 12–14 |
| FEAT-F05 | **Gestão de carteira/região** + regra de comissão por atendimento | PROC-002, RN-CAR | 🟡 | Perguntas 8, 17, 18 (lacuna RN-CAR-002) |
| FEAT-F06 | **Override de % de comissão por cliente** | PROC-001, RN-COM-007 | ⚪ | Pergunta 1 (há outros além da Lucilene?) |
| FEAT-F07 | **Automação do fechamento mensal** + exportação p/ contabilidade | PROC-001/006 | ⚪ | Mapear formato aceito pela contadora |
| FEAT-F08 | **Digitalização de horas extras** do motorista | PROC-006, RN-BEN | ⚪ | Fórmula trabalhista (contadora) |
| FEAT-F09 | **Gestão de benefícios/alimentação** | PROC-006, RN-BEN-001..003 | ⚪ | Confirmar regras e exceções |
| FEAT-F10 | **Metas de vendas** (definição + acompanhamento) | RN-VND-008 | 🟡 | Pergunta 10 |
| FEAT-F11 | **Logística / Romaneio de entregas** | TELA-016, RN-LOG | 🟠 | Escopo de logística |
| FEAT-F12 | **Leitura de previsão financeira/recebíveis** no dashboard | TELA-013, RN-FIN | 🟠 | Integração de leitura com ZUMA |

---

## Notas de priorização
- **Mais próximas do MVP (Fase 2):** FEAT-F01 (aprovação de desconto), FEAT-F04 (devolução digital),
  FEAT-F05 (carteira) e FEAT-F10 (metas) — todas extensões diretas do núcleo comercial/comissão.
- **Dependentes de validação antes mesmo de especificar:** FEAT-F02, FEAT-F05, FEAT-F06.
- **Externas/contábeis (menor prioridade de produto):** FEAT-F07, F08, F09.

## Histórico de Versões
| 1.0.0 | 2026-06-23 | Criação — 12 features futuras candidatas |
