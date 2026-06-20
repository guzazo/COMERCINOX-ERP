---
id: TELA-002
título: Tela Inicial (Home)
módulo: Sistema / Geral
sistema: ZUMA
status: em-revisão
versão: 1.0.0
criado-em: 2025-06-19
atualizado-em: 2025-06-19
relacionado-com: RN-SIS-001 a RN-SIS-004, PROB-001
---

# Tela Inicial (Home)

## 1. Identificação

| Campo | Valor |
|---|---|
| Sistema | ZUMA ERP 9.25.2.2 |
| Módulo | Sistema / Geral |
| Caminho de acesso | Tela de abertura após login |
| Frequência de uso | Diário (permanente) |
| Usuários | Todos |
| Prioridade | **Importante** — MVP: **Sim (dashboard com KPIs)** |

---

## 2. Objetivo da Tela

Ponto de entrada do ERP. Atualmente funciona como **tela de atalhos**, sem nenhum
indicador de negócio (sem dashboard).

---

## 3. Estrutura

- **Atalhos:** Produtos, Pedido de Compra, Recebimentos, Emissão de Boleto, Grade de Pagamentos.
- Dois painéis sem diferença clara: **"Painel Local"** vs **"Painel Web"**.
- Rodapé mostra usuário logado durante toda a sessão.
- **Ctrl+F** abre pesquisa de menus em qualquer tela.
- **6 estações simultâneas** confirmadas, em rede local 192.168.15.x.

---

## 4. Regras de Negócio

- **RN-SIS-001:** sistema multiestação — 6 estações simultâneas, rede local.
- **RN-SIS-002:** usuário logado visível no rodapé em toda sessão.
- **RN-SIS-003:** Ctrl+F abre pesquisa de menus em qualquer tela.
- **RN-SIS-004:** acesso a Clientes fica em Financeiro → A Receber (problema de IA).

---

## 5. Problemas de UX

- **UX-001 (🔴):** home sem nenhum indicador de negócio — apenas atalhos.
- **UX-015 (🟡):** "Painel Local" vs "Painel Web" sem diferença clara.
- **UX-021 (🟡):** 11 itens no menu principal — navegação por memória.

---

## 6. Melhorias Possíveis

Dashboard inicial com KPIs em tempo real (vendas do dia/mês, ranking de vendedores,
comissão do período, alertas de estoque ≤ 0, inadimplência), substituindo a tela de
atalhos. Menu principal com ícones e agrupamento por área.

---

## 7. Decorrência Arquitetural

6 estações simultâneas + necessidade de acesso multiusuário → **ERP web-first**
(RN-SIS-001), sem instalação de client.

---

## 8. Histórico de Versões

| Versão | Data | Mudanças |
|---|---|---|
| 1.0.0 | 2025-06-19 | Criação — home sem dashboard, 6 estações confirmadas |
