---
id: ROTEIRO-ENTREVISTA-001
título: Roteiro de Entrevista (imprimível) — por pessoa
status: pronto-para-uso
versão: 1.0.0
criado-em: 2026-06-23
objetivo: validar lacunas de negócio antes de Requisitos e Wireframes (Fase 0 → Validação)
prioridades: 1) Comissão e carteira · 2) Crédito e bloqueio · 3) Devoluções · 4) Estoque · 5) Fechamento financeiro · 6) Benefícios e folha
---

# Roteiro de Entrevista — Comercinox

> **Como usar:** uma página por pessoa. Marque ☐ e anote ao lado. Foco em **entender o processo real**,
> não em propor solução. Não prometer funcionalidades. Duração sugerida: 30–45 min por pessoa.

**Abertura (para todos):** "Quero entender como você faz hoje, com suas próprias palavras — inclusive o
que é feito fora do sistema, em papel ou Excel. Não há resposta errada."

---

## 🧑‍💼 WANDERSON — Proprietário  · *(prioridades 1, 2)*
1. ☐ Como você decide aprovar um **desconto** que o vendedor pede? Existe um teto antes de te consultar?
2. ☐ Quando **um vendedor atende cliente do outro**, **quem fica com a comissão**? *(RN-CAR-002)*
3. ☐ Os clientes que "só falam com você" — quantos são? Isso muda a comissão de alguém?
4. ☐ Existem **metas** de venda? Como define? *(o ZUMA tem o item desabilitado)*
5. ☐ O **limite de crédito** de um cliente **impede** a venda, ou é só um aviso?
6. ☐ Que **informação** você gostaria de ver para decidir melhor (compra de estoque, cliente, margem)?
7. ☐ Confirma que **opera só 1 CNPJ** (os outros 2 estão parados)?

## 🧮 ROBERTA — Administrativo/Financeiro  · *(prioridades 1, 2, 3, 5)*
1. ☐ Passo a passo do **fechamento de comissão**: de onde tira o número, como calcula, onde registra?
2. ☐ **Só a Lucilene** tem % diferente (0,5%)? Há outros clientes com regra especial?
3. ☐ Como entra a **devolução** no cálculo? E quando ela chega **depois** do fechamento?
4. ☐ Como funcionam os **adiantamentos** dos vendedores?
5. ☐ Quem decide **bloquear** um cliente? Onde anota o **motivo** (já que o ZUMA não tem campo)?
6. ☐ O **crédito de devolução** lançado no cliente é usado como abatimento depois? Como?
7. ☐ Quais **controles em Excel/papel** você mantém hoje? Quais não larga de jeito nenhum?
8. ☐ O que mais te **toma tempo** ou gera retrabalho no mês?

## 📦 BENINI — Estoque/Operações  · *(prioridades 3, 4)*
1. ☐ Como confere se o **material devolvido voltou** ao estoque? Há prazo?
2. ☐ O que acontece quando o material **não** retorna (ainda está com o cliente)?
3. ☐ A devolução **baixa o estoque** no ZUMA automaticamente ou é manual?
4. ☐ Como organiza recebimento e **preparação de caminhões** hoje?
5. ☐ O **estoque negativo** acontece? Como vocês lidam quando o saldo fica abaixo de zero?

## 🧾 BRENDO — Atendimento/Fiscal/Caixa  · *(prioridades 3, 5)*
1. ☐ Seu papel na **devolução** vs. o do Benini — onde começa e termina cada um?
2. ☐ Como é a **abertura e fechamento de caixa**? Com que frequência fecha?
3. ☐ **Cancelamento de nota** — quando acontece e qual o procedimento?
4. ☐ A **licença do ZUMA NF-e** trava quando outra pessoa está usando? Atrapalha?
5. ☐ Você toparia ser o **piloto** do novo sistema nos testes?

## 🤝 TARGINO — Vendedor  · *(prioridades 1, 3)*
1. ☐ Como você sabe **qual cliente é "seu"**? Existe lista/carteira?
2. ☐ Com que frequência atende **cliente da Polyana** (e vice-versa)? Gera atrito de comissão?
3. ☐ No **orçamento**, você aplica desconto sozinho ou pede ao Wanderson?
4. ☐ O que consulta do cliente **antes de orçar** (status, crédito, histórico)?
5. ☐ Como registra uma **devolução** quando o cliente pede?

## 💬 POLYANA — Vendedora  · *(prioridades 1, 3 + hipótese de processo)*
1. ☐ Me mostra como fecha um pedido pelo **WhatsApp**, do orçamento ao "ok" do cliente?
2. ☐ Já aconteceu de um "ok" virar **devolução/divergência** depois? Com que frequência? *(hipótese de processo — investigar o fluxo, sem culpar)*
3. ☐ Em que momento você considera a **venda confirmada**?
4. ☐ Mesmas perguntas de carteira/desconto/devolução do Targino (itens 1–5).

## 🚚 LEANDRO — Motorista  · *(prioridade 6 — externo ao MVP)*
1. ☐ Como anota **horas extras** e **pernoites** hoje (formulário)?
2. ☐ A quem entrega o formulário e quando?
3. ☐ O que seria útil ter no **celular** para facilitar (entregas/rota)? *(exploratório, futuro)*

---

## Cobertura das prioridades × pessoa

| Prioridade | Quem responde |
|---|---|
| 1. Comissão e carteira | Wanderson, Roberta, Targino, Polyana |
| 2. Crédito e bloqueio | Wanderson, Roberta *(+ mãe do proprietário, se possível)* |
| 3. Devoluções | Roberta, Benini, Brendo, Targino, Polyana |
| 4. Estoque | Benini |
| 5. Fechamento financeiro | Roberta, Brendo |
| 6. Benefícios e folha | Leandro, Roberta |

> **Lacunas críticas a fechar nesta rodada:** RN-CAR-002 (comissão por atendimento cruzado) e
> comportamento do **limite de crédito** (bloqueia vs informa). Sem elas, não avançar para Requisitos.

## Histórico de Versões
| 1.0.0 | 2026-06-23 | Criação — roteiro por pessoa (7), priorizado pelos 6 temas |
