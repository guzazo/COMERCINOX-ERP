---
id: USR-001
título: Personas de Usuários — Comercinox
status: rascunho (validar após entrevistas)
versão: 1.0.0
criado-em: 2025
---

# Personas de Usuários — Comercinox

> ⚠️ **Atenção:** Estas personas são **hipóteses iniciais** baseadas no contexto conhecido.
> Devem ser validadas e refinadas após as entrevistas da SPRINT-01.

---

## Persona 1: O Proprietário / Gestor

| Campo | Valor |
|---|---|
| Nome fictício | Seu João / Sua Maria |
| Cargo | Proprietário / Gestor |
| Frequência de uso do ERP | Diária |
| Nível técnico | Baixo a médio |
| Dispositivos | Desktop (Windows) + possivelmente celular |
| Principal interesse no sistema | Ver resultados, vendas, inadimplência, estoque |

### Dores hipotéticas (validar)
- Dificuldade de ver resumo do dia/semana de forma rápida
- Não sabe quais clientes estão inativos
- Precisa de mais de uma tela para ter visão geral do negócio
- Dificuldade com relatórios complexos do ZUMA

### O que mais valoriza (hipótese)
- Simplicidade: poucas telas, informação direta
- Dashboard com os números mais importantes
- Não depender de terceiros para gerar relatórios

### Tarefas típicas no sistema
- [ ] Ver vendas do dia/semana/mês
- [ ] Verificar inadimplência
- [ ] Consultar estoque de produtos principais
- [ ] Ver comissão de vendedores

---

## Persona 2: O Responsável Comercial / Vendedor

| Campo | Valor |
|---|---|
| Nome fictício | Carlos / Ana |
| Cargo | Vendedor / Responsável Comercial |
| Frequência de uso do ERP | Diária — várias vezes ao dia |
| Nível técnico | Médio |
| Dispositivos | Desktop + celular (WhatsApp é primário) |
| Principal interesse | Gerenciar clientes, orçamentos, follow-ups |

### Dores hipotéticas (validar)
- Histórico de clientes espalhado no WhatsApp
- Follow-ups esquecidos
- Dificuldade para saber quais clientes não compram há tempo
- Orçamentos perdidos
- Não sabe em qual estágio do funil está cada cliente

### O que mais valoriza (hipótese)
- Acesso rápido ao histórico de cada cliente
- Lembretes de follow-up
- Poder ver orçamentos enviados e pendentes
- Interface simples e rápida

### Tarefas típicas no sistema
- [ ] Consultar/cadastrar cliente
- [ ] Criar orçamento
- [ ] Registrar interação com cliente
- [ ] Ver clientes sem contato recente
- [ ] Registrar follow-up

---

## Persona 3: O Responsável Administrativo / Financeiro

| Campo | Valor |
|---|---|
| Nome fictício | Dona Rosa |
| Cargo | Administrativo / Financeiro |
| Frequência de uso do ERP | Diária |
| Nível técnico | Médio-baixo |
| Dispositivos | Desktop (Windows) |
| Principal interesse | Contas a pagar/receber, notas fiscais, financeiro |

### Dores hipotéticas (validar)
- Processo de emissão de NF-e é complexo no ZUMA
- Controle de contas a receber exige muitos cliques
- Conciliação bancária manual
- Relatórios financeiros difíceis de entender

### O que mais valoriza (hipótese)
- Processo de NF-e simples e sem erros
- Visão clara do que vai vencer esta semana (CR e CP)
- Menos chance de erro nas rotinas fiscais

### Tarefas típicas no sistema
- [ ] Emitir NF-e
- [ ] Controlar contas a receber
- [ ] Registrar pagamentos
- [ ] Emitir boletos / cobranças

---

## Mapa de Funcionalidades por Persona

| Funcionalidade | Proprietário | Comercial | Administrativo |
|---|---|---|---|
| Dashboard de Vendas | ✅ Principal | ✅ | 👁️ Consulta |
| Cadastro de Clientes | 👁️ | ✅ Principal | 👁️ |
| Funil de Vendas | ✅ | ✅ Principal | ❌ |
| Follow-ups | ❌ | ✅ Principal | ❌ |
| Orçamentos | 👁️ | ✅ Principal | 👁️ |
| Contas a Receber | ✅ | ❌ | ✅ Principal |
| Contas a Pagar | ✅ | ❌ | ✅ Principal |
| Emissão de NF-e | ❌ | ❌ | ✅ Principal |
| Estoque | ✅ | 👁️ | ❌ |
| Relatórios | ✅ Principal | 👁️ | ✅ |

**Legenda:** ✅ Usa muito | 👁️ Consulta | ❌ Não usa

---

## Próximos Passos

- [ ] Validar estas personas com entrevistas reais (SPRINT-01)
- [ ] Atualizar dores, tarefas e preferências com dados reais
- [ ] Identificar se há mais usuários não mapeados aqui

---

## Histórico de Versões

| Versão | Data | Mudanças |
|---|---|---|
| 1.0.0 | 2025 | Criação de personas hipotéticas (pré-entrevistas) |
