---
id: TELA-004
título: Pesquisa de Produtos
módulo: Estoque / Produtos
sistema: ZUMA
status: em-revisão
versão: 1.0.0
criado-em: 2025-06-19
atualizado-em: 2025-06-19
relacionado-com: RN-PRD-007 a RN-PRD-010, FEAT-003, PROB-001
---

# Pesquisa de Produtos

## 1. Identificação

| Campo | Valor |
|---|---|
| Sistema | ZUMA ERP 9.25.2.2 |
| Módulo | Estoque / Produtos |
| Frequência de uso | Diário |
| Usuários | Comercial / Estoque |
| Prioridade | **Crítica** — MVP: **Sim (consulta para orçamentos)** |

---

## 2. Objetivo da Tela

Localizar produtos no catálogo para consulta de preço e estoque — base para o futuro
módulo de orçamentos do ERP Comercialinox.

---

## 3. Estrutura

- **2.335 produtos** cadastrados.
- **10 tipos de busca** (radio button); padrão = **"Contendo"** (adequado para inox,
  ex.: "304 1x1/8").
- Tabela de preço selecionada manualmente na pesquisa.
- **Atalhos:** F2 consulta estoque · F5 imagem · F12 fator de conversão ·
  Ctrl+F6 formação de preço.
- Preview do produto com muitos campos vazios (Prateleira, Setor, Cor, Embalagem).

---

## 4. Regras de Negócio

- **RN-PRD-007:** catálogo com 2.335 produtos.
- **RN-PRD-008:** busca em modo "Contendo" como padrão.
- **RN-PRD-009:** tabela de preço selecionada na pesquisa define o preço exibido.
- **RN-PRD-010 (❓):** Ctrl+F6 "Formação de Preço" — precificação além da tabela fixa.

---

## 5. Problemas de UX

- **UX-016 (🔴):** produtos com estoque zero aparecem sem destaque — risco de orçar item indisponível.
- **UX-018 (🔴):** tabela de preço selecionada manualmente — erro se errada.
- **UX-022 (🟡):** Ctrl+F6 não documentado visivelmente.
- **UX-028/UX-029 (🟡):** preview com campos vazios; 10 filtros raramente usados.

---

## 6. Melhorias Possíveis (→ FEAT-003)

Filtro "Somente com estoque" por padrão, badge de disponibilidade (✅/⚠️/❌),
auto-seleção da tabela de preço pelo perfil do cliente, preço à vista e a prazo
lado a lado, no máximo 3 filtros visíveis.

> ⚠️ **2.335 produtos** inviabilizam cadastro manual → necessária **estratégia de
> sincronização/importação de catálogo** do ZUMA.

---

## 7. Histórico de Versões

| Versão | Data | Mudanças |
|---|---|---|
| 1.0.0 | 2025-06-19 | Criação — 2.335 produtos, crítica para orçamentos |
