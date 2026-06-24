---
id: USR-001
título: Personas Operacionais — Comercinox
status: em-revisão (validar nas entrevistas)
versão: 2.0.0
criado-em: 2025
atualizado-em: 2026-06-23
origem: descoberta organizacional 2026-06-23
relacionado-com: MAPA-INFLUENCIA-ORGANIZACIONAL, PERGUNTAS-ABERTAS, ROTEIRO-ENTREVISTA
---

# Personas Operacionais — Comercinox

> **v2.0:** substitui as personas hipotéticas por **pessoas reais** identificadas na operação.
> Maturidade digital e resistência são escalas de 1–5 / baixa-alta (autoavaliação de descoberta, validar).

---

## PERSONA-001 — WANDERSON · Fundador / Proprietário (41)
- **Empresa** fundada em 2019. Já faturou ~R$1 mi/mês; hoje ~R$300 mil/mês; em reestruturação.
- **Perfil:** domínio do mercado de inox, networking, comunicação, confiança da equipe.
- **Comportamento:** não usa todo o ZUMA; prefere prática a processo; compra estoque por *feeling*;
  não abre mão de autonomia/controle; pouca familiaridade com gestão moderna.
- **Classificação:** Poder **Muito Alto** · Maturidade digital **2/5** · Resistência **Média/Alta**.
- **Implicação de produto:** o ERP **não substitui** o processo decisório dele — **apoia com informação**
  (dashboard, margem, histórico). Não impor fluxo rígido.

## PERSONA-002 — ROBERTA · Administrativo / Financeiro (39)
- **Responsabilidades:** contas a pagar, fechamento de caixa, **comissão**, benefícios, folha
  (operacional), **crédito de clientes**.
- **Perfil:** forte no Excel, muito papel, cria controles paralelos, confia mais em planilha que em sistema.
- **Influência:** **principal conselheira de Wanderson**; participa de decisões estratégicas.
- **Classificação:** Poder **Alto** · Maturidade **3/5** · Resistência **Média**.
- **Implicação:** **principal usuária administrativa** do ERP. Migração **gradual**, respeitar/importar
  Excel, co-criar. Conquistá-la = adoção; perdê-la = projeto trava.

## PERSONA-003 — GUILHERME · Inovação / Desenvolvimento (18)
- Estudante de Ciência da Computação; automação, software, modernização.
- **Perfil DISC: AP** — analítico, orientado a processos, busca eficiência.
- Projetos: ERP Comercialinox, Mercado Livre, automações internas.
- **Classificação:** Poder **Baixo** · Maturidade **5/5** · Resistência **Muito baixa**.
- **Implicação:** **possível Product Owner** do ERP — ponte entre operação e desenvolvimento.

## PERSONA-004 — BENINI · Estoque / Operações (+5 anos)
- **Responsabilidades:** recebimento, **conferência de devoluções**, organização do estoque,
  preparação de caminhões, abertura da empresa.
- **Perfil:** muito confiável, forte conhecimento operacional e logístico.
- **Classificação:** Maturidade **2/5** · Resistência **Média/Alta** · Poder baixo (operacional crítico).
- **Implicação:** dono do passo físico da devolução (PROC-005) e do estoque — UI simples, pouco texto.

## PERSONA-005 — TARGINO · Vendedor (+5 anos)
- Atendimento comercial, WhatsApp, telefone, orçamentos.
- **Classificação:** Maturidade **2/5** · Resistência **Média** · Poder baixo.
- **Implicação:** usuário diário do orçamento/cliente; velocidade e simplicidade.

## PERSONA-006 — POLYANA · Vendedora (+4 anos)
- Atendimento comercial, WhatsApp, telefone, orçamentos.
- **Hipótese de processo (não erro individual):** confirmação de pedido por WhatsApp — cliente
  responde "ok" após disponibilidade, a venda é tida como confirmada e depois há devolução/divergência.
  **Investigar se o processo induz isso** (liga a PROC-005 devoluções e ao funil de orçamento).
- **Classificação:** Maturidade **2/5** · Resistência **Média** · Poder baixo.

## PERSONA-007 — LEANDRO · Motorista
- Entregas, **horas extras**, **pernoites**. Usa **formulários impressos**, **não usa ZUMA**.
- **Classificação:** Maturidade **1/5** · Poder muito baixo.
- **Implicação:** processos dele são externos/manuais (PROC-006) — fora do MVP.

## PERSONA-008 — BRENDO · Atendimento / Fiscal / Caixa
- Emissão de NF-e, entrada de materiais, cancelamento de notas, abertura/fechamento de caixa.
- **Perfil:** aprende rápido, boa adaptação tecnológica.
- **Classificação:** Maturidade **4/5** · Resistência baixa.
- **Implicação:** **possível usuário-chave para testes e implantação** (champion técnico).

---

## Mapa de Funcionalidades × Persona (atualizado)

| Funcionalidade | Wanderson | Roberta | Targino/Polyana | Benini | Brendo |
|---|---|---|---|---|---|
| Dashboard / indicadores | ✅ Principal | ✅ | 👁️ | ❌ | 👁️ |
| Clientes / CRM | 👁️ | ✅ | ✅ Principal | ❌ | 👁️ |
| Orçamentos | ✅ (aprova desconto) | 👁️ | ✅ Principal | ❌ | 👁️ |
| Comissão | ✅ | ✅ Principal | 👁️ (própria) | ❌ | ❌ |
| Devoluções | 👁️ | ✅ (confirma) | ✅ (inicia) | ✅ (física) | 👁️ |
| Crédito / bloqueio | ✅ (decide) | ✅ | 👁️ | ❌ | 👁️ |
| Caixa / Fiscal (ZUMA) | 👁️ | ✅ | ❌ | ❌ | ✅ Principal |
| Estoque / entregas | 👁️ | 👁️ | 👁️ | ✅ Principal | ✅ |

**Legenda:** ✅ Usa muito · 👁️ Consulta · ❌ Não usa

---

## Próximos Passos
- [ ] Validar maturidade/resistência nas entrevistas (autoavaliação atual)
- [ ] Confirmar Guilherme como Product Owner
- [ ] Confirmar Brendo como usuário-piloto

## Histórico de Versões
| Versão | Data | Mudanças |
|---|---|---|
| 1.0.0 | 2025 | Personas hipotéticas (pré-entrevistas) |
| 1.1.0 | 2026-06-23 | Mapa de atores reais (apêndice) |
| 2.0.0 | 2026-06-23 | Reescrita — 8 personas operacionais reais + mapa funcionalidade×persona |
