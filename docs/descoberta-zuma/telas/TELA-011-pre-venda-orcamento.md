---
id: TELA-011
título: Pré-venda / Orçamento (ZumaPDV — LOJA)
módulo: Comercial
sistema: ZUMA · ZumaPDV
status: em-revisão
versão: 1.0.0
criado-em: 2026-06-23
confiança-evidência: A (screenshot nítido)
relacionado-com: FEAT-003, EPIC-001, RN-VND, TELA-004, TELA-016
---

# Pré-venda / Orçamento (ZumaPDV)

## 1. Identificação
| Campo | Valor |
|---|---|
| Sistema | ZumaPDV [LOJA] (app separado do ERP) |
| Módulo | Comercial — Pré-venda |
| Frequência | Diário (núcleo da operação de vendas) |
| Usuários | Comercial/Vendedor |
| Prioridade | **Crítica** — MVP: **Sim** (é o orçamento/pedido) |

## 2. Objetivo
Montar a **pré-venda** (orçamento que vira pedido): selecionar cliente, itens, condição de
pagamento, descontos e enviar. É o que hoje materializa o "orçamento" da Comercinox — a
descoberta corrige a IA, que tratava "Orçamentos" como módulo abstrato.

## 3. Campos
Pré-Venda (nº) · Cliente · **Condição de pagamento (À Vista / À Prazo — À Prazo marcado)** ·
Carga · Itens (Código, Descrição, Unidade, Quantidade, Valor, SubTotal) · % Desconto ·
IPI · Despesas · Frete · Desconto · **Total da Pré-Venda**. Rodapé: "Última pré-venda: 78911".

## 4. Ações (toolbar + menu Alt+P)
[F2] Pré-Venda · [F3] Produtos · [F10] Troca · [F5] Alterar · [Alt+P] menu · Opções · Inf. Extras ·
Atual. Preços. **Menu Alt+P:** Pré-venda por e-mail (HTML / PDF / com impostos), Rastrear produto,
Pré-venda travada, **Lucratividade da venda**, Cadastro de veículo, Requisição de material,
Exportar pré-venda, Estatística de pré-venda, **Separação de mercadoria**, Pré-venda matricial,
Contrato por pré-venda, **Clonar pré-venda**, Planilha, Listagem (Ctrl+L), Modelo personalizado,
Mensagem promocional, Relação de canceladas, Painel solicitação produção, **Painel de entregas**, SAC.

## 5. Regras de negócio (novas + confirmadas)
- **RN-PRV-001:** condição de pagamento À Vista/À Prazo na pré-venda — **À Prazo é o padrão** (confirma RN-VND-004, 87% a prazo).
- **RN-PRV-002:** pré-venda calcula IPI, Despesas, Frete e Desconto no total.
- **RN-PRV-003:** "Lucratividade da venda" disponível no ato — margem por pré-venda.
- **RN-PRV-004:** pré-venda pode ser **travada** (liberação controlada) e **clonada**.
- **RN-PRV-005:** pré-venda gera **separação de mercadoria** e alimenta o **painel de entregas/romaneio** (liga a TELA-016).
- **RN-PRV-006:** envio por e-mail em PDF/HTML (canal de envio de orçamento ao cliente).
- **RN-PRV-007:** numeração sequencial contínua de pré-venda (ex.: 78911).

## 6. Dependências
Cliente (TELA-001) · Catálogo/Produtos (TELA-004, tabela de preço) · Vendedor · Estoque ·
Romaneio/Entregas (TELA-016) · Produção (painel solicitação — grupo JAPA?).

## 7. Problemas de UX
- Tela densa estilo planilha; muitos atalhos só por tecla (F2/F3/F10) sem rótulo visível.
- "Pré-venda travada" e fluxo de liberação não são autoexplicativos.
- Sem registro/visão de funil do orçamento (enviado/aceito/perdido) — só lista de pré-vendas.

## 8. Melhorias possíveis (MVP)
- Orçamento com **prazo como padrão** e auto-seleção de tabela de preço pelo cliente.
- **Status do orçamento** (rascunho/enviado/aceito/perdido) — base de CRM/funil.
- Enviar por WhatsApp/PDF em 1 clique; lucratividade visível inline (controlada por permissão).
- Conversão orçamento→pedido→separação rastreável.

## 9. Histórico de Versões
| Versão | Data | Mudanças |
|---|---|---|
| 1.0.0 | 2026-06-23 | Criação — pré-venda do ZumaPDV identificada como o orçamento/pedido real |
