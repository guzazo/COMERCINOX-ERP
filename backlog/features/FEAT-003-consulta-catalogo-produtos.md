---
id: FEAT-003
épico: EPIC-001
título: Consulta de Catálogo de Produtos para Orçamento
módulo: CRM / Orçamentos
prioridade: Alta
status: rascunho
versão: 1.0.0
criado-em: 2025-06-19
origem: TELA-003, TELA-004 — engenharia reversa ZUMA
---

# FEAT-003 — Consulta de Catálogo de Produtos para Orçamento

## Origem
Derivada da TELA-004 (Pesquisa de Produtos) — necessária para o módulo de orçamentos.
O ERP Comercialinox precisa consultar o catálogo de 2.335 produtos do ZUMA.

## Problema Real
Para gerar um orçamento, o vendedor hoje precisa:
1. Abrir o ZUMA
2. Navegar até Produtos
3. Selecionar a tabela de preço manualmente
4. Buscar o produto
5. Copiar o preço
6. Abrir o WhatsApp ou e-mail e digitar o orçamento manualmente

Não há registro de orçamento no ZUMA para acompanhamento posterior.

## Estratégia para o MVP

### Opção A — Sincronização de catálogo (recomendada)
- Exportar produtos do ZUMA periodicamente (CSV/planilha)
- Importar para o banco do ERP Comercialinox
- Exibir catálogo com busca, filtro e saldo de estoque
- Atualizar manualmente ou via script agendado

### Opção B — Consulta em tempo real (Fase 3)
- Integração via API com o ZUMA (se existir)
- Saldo de estoque em tempo real

### Escopo MVP (Opção A)
- [ ] Catálogo de produtos importado do ZUMA
- [ ] Busca por descrição com modo "Contendo" como padrão
- [ ] Tabela de preço auto-selecionada pelo perfil do cliente (REVENDA ou CONSUMIDOR)
- [ ] Indicador visual de disponibilidade: ✅ Em estoque / ⚠️ Baixo / ❌ Sem estoque
- [ ] Saldo atualizado com última sincronização visível
- [ ] Preço à vista e a prazo exibidos lado a lado

## Regras de Negócio Críticas
- RN-PRD-002: Estoque negativo deve gerar alerta visual (não bloquear silenciosamente)
- RN-PRD-003: Duas tabelas de preço — auto-seleção pelo cliente
- RN-PRD-004: Prazo ~15% mais caro que à vista

## Dependências
- FEAT-001 (Cadastro de Clientes — define qual tabela de preço usar)
- Exportação de produtos do ZUMA (processo manual no MVP)
- FEAT-004 (Orçamentos — consome esta feature)
