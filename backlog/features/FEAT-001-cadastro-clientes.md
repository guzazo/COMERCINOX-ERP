---
id: FEAT-001
épico: EPIC-001
título: Cadastro de Clientes
módulo: CRM
prioridade: Alta
status: rascunho
versão: 1.0.0
criado-em: 2025-06-19
origem: TELA-001 — engenharia reversa ZUMA
---

# FEAT-001 — Cadastro de Clientes

## Origem
Derivada da engenharia reversa da TELA-001 do ZUMA ERP.
Substitui o cadastro atualmente em Financeiro → A Receber → Clientes.

## O que o ZUMA faz hoje
- Cadastro via menu Financeiro (caminho não intuitivo)
- 3 abas: Dados Cadastrais / Dados Complementares / Informações Adicionais
- Grid de múltiplos contatos
- Grid de múltiplos endereços de entrega
- Ficha financeira automática (primeira compra, atrasos, crédito)
- Bloqueio por prazo e por entrega independentes

## O que o ERP Comercialinox deve fazer

### Escopo do MVP
- [ ] Cadastro acessível em menu principal CRM (não em Financeiro)
- [ ] Campos obrigatórios destacados com asterisco + validação em tempo real
- [ ] CNPJ/CPF com validação automática e busca de dados via API (ReceitaWS)
- [ ] Busca de cliente por Nome como padrão (não CNPJ)
- [ ] Auto-preenchimento de endereço por CEP
- [ ] Status do cliente visível como badge: Ativo / Inativo / Bloqueado prazo / Bloqueado entrega
- [ ] Múltiplos contatos (telefone, WhatsApp, e-mail) com tipo e flag de principal
- [ ] Segmento/Atividade como lista clara: Metalúrgica / Laticínio / Prestador de Serviço / Outro
- [ ] Vendedor responsável vinculado
- [ ] Campo Observações sempre visível (não apenas na pesquisa)
- [ ] Histórico de compras visível no cadastro (leitura — alimentado pelo ZUMA no MVP)
- [ ] Estágio no funil: Frio / Médio / Quente / Recorrente

### Fora do MVP (Fase 3)
- Múltiplos endereços de entrega
- Integração de limite de crédito com módulo financeiro
- Foto do cliente
- Campos fiscais avançados (DIFAL, tipo contribuinte)

## Regras de Negócio Herdadas do ZUMA
RN-CLI-001 a RN-CLI-015 — ver RN-MASTER-sprint01.md

## Problemas de UX a Evitar
UX-005, UX-008, UX-017, UX-019, UX-023, UX-024 — ver PROB-001-ux-sprint01.md

## Dependências
- Cadastro de Vendedores (FEAT-002) deve existir antes
- Segmentos de cliente precisam ser definidos com usuários (entrevistas SPRINT-01)
