# Sistema Delivery

## Estrutura

```text
Sistema-delivery/
├── data/
│   └── menu-state.json
├── public/
│   └── index.html
├── scripts/
│   └── generate-password-hash.js
├── .env.example
├── .gitignore
├── package.json
├── README.md
└── server.js

# 🍔 Sistema Delivery - Full Stack

Um sistema completo e inteligente para gestão de pedidos de delivery, criado do zero. Este projeto permite aos clientes montarem as suas marmitas de forma interativa e envia o pedido formatado diretamente para o WhatsApp do restaurante. Possui também um painel administrativo seguro para gestão do cardápio e das configurações da loja.

## 🚀 O Exemplo Prático (O que o sistema faz?)
Imagine um restaurante onde os clientes podem pedir pratos montados (ex: arroz, feijão e carne) ou pratos executivos/especiais fechados (ex: Feijoada, Yakisoba). 
O sistema atua como um "garçom digital rigoroso":
- Se o cliente escolhe um prato normal, o sistema obriga-o a escolher os acompanhamentos (1 a 4 guarnições e 1 a 2 proteínas).
- Se o cliente escolhe um prato especial (ex: Feijoada), o sistema entende que é um prato único e liberta o pedido sem exigir guarnições extras.

## 🛠️ Tecnologias Utilizadas

**Frontend (A Interface do Cliente):**
- HTML5, CSS3 e JavaScript puro (Vanilla JS).
- Design Responsivo (Mobile-first).
- Validação inteligente de carrinho de compras cruzando IDs do frontend com o cardápio global.

**Backend (O Servidor e a Lógica):**
- **Node.js** com **Express** (API RESTful).
- **Segurança:** Autenticação usando JWT (`jsonwebtoken`) e criptografia de senhas com `bcryptjs`.
- Preparado para ambiente Serverless (sem falhas de permissão de escrita/Read-Only).

**Banco de Dados & Infraestrutura:**
- **Neon (PostgreSQL):** Banco de dados relacional na nuvem para guardar o cardápio e configurações.
- **Vercel:** Hospedagem na nuvem tanto do Frontend quanto do Backend.

## ✨ Principais Funcionalidades

- [x] **Cardápio Digital Dinâmico:** Atualizado em tempo real pelo banco de dados.
- [x] **Regras de Negócio Avançadas:** Validação estrita de combinações de pratos (Proteínas Solo vs. Montagem Tradicional).
- [x] **Integração com WhatsApp:** Geração automática da mensagem com o resumo do pedido, endereço e troco.
- [x] **Painel Administrativo:** Área restrita para o dono do restaurante adicionar/remover produtos e alterar horários de funcionamento, chave PIX e contato.

## ⚙️ Como rodar o projeto localmente

Se quiser clonar e testar este projeto no seu computador, siga estes passos:

1. **Clone o repositório:**
   ```bash
   git clone [https://github.com/JeffRodFer/sistema-delivery.git](https://github.com/JeffRodFer/sistema-delivery.git)
