# 🛒 E-commerce REST API

> Uma API RESTful desenvolvida em Python para gerenciar o backend de uma plataforma de e-commerce. O sistema oferece autenticação de usuários, gerenciamento completo do catálogo de produtos e um fluxo de carrinho de compras com checkout.

![Demonstração da Aplicação](https://via.placeholder.com/800x400?text=Sua+Imagem+ou+GIF+Aqui)
*Dica: Substitua a imagem acima por um print do Insomnia/Postman testando as rotas ou um GIF da aplicação.*

## 🛠️ Tecnologias Utilizadas

O projeto foi construído utilizando as seguintes tecnologias e bibliotecas:

- **Python 3** - Linguagem principal.
- **Flask (3.1.2)** - Microframework web para estruturação da API.
- **Flask-SQLAlchemy (3.1.1)** - ORM para comunicação e modelagem do banco de dados relacional.
- **Flask-Login (0.6.3)** - Gerenciamento de sessões e autenticação de usuários.
- **Flask-CORS (3.0.10)** - Para permitir o consumo da API por aplicações frontend.
- **Werkzeug (3.1.3)** - Biblioteca de utilitários WSGI.
- **SQLite** - Banco de dados leve e embutido.

## ✨ Principais Funcionalidades

- **Autenticação:** Login e Logout de usuários baseados em sessão (`@login_required`).
- **Catálogo de Produtos:** CRUD completo (Criar, Ler, Atualizar e Deletar) de produtos. Apenas usuários logados podem modificar o catálogo.
- **Carrinho de Compras:** 
  - Adicionar e remover itens específicos.
  - Visualizar o estado atual do carrinho do usuário logado.
  - Finalizar compra (Checkout), limpando o carrinho automaticamente.

## 🔀 Estrutura de Rotas (Endpoints)

| Rota | Método | Descrição | Autenticação |
|---|---|---|---|
| `/login` | `POST` | Autentica o usuário | ❌ Não |
| `/logout` | `POST` | Encerra a sessão do usuário | ✅ Sim |
| `/api/products` | `GET` | Lista todos os produtos | ❌ Não |
| `/api/products/<id>` | `GET` | Detalhes de um produto específico | ❌ Não |
| `/api/products/add` | `POST` | Cadastra um novo produto | ✅ Sim |
| `/api/products/update/<id>`| `PUT` | Atualiza dados de um produto | ✅ Sim |
| `/api/products/delete/<id>`| `DELETE`| Remove um produto | ✅ Sim |
| `/api/cart` | `GET` | Visualiza o carrinho do usuário | ✅ Sim |
| `/api/cart/add/<id>` | `POST` | Adiciona produto ao carrinho | ✅ Sim |
| `/api/cart/remove/<id>`| `DELETE`| Remove produto do carrinho | ✅ Sim |
| `/api/cart/checkout` | `POST` | Finaliza a compra | ✅ Sim |

## ⚙️ Como Executar o Projeto

### Pré-requisitos
- Python 3.x instalado
- Gerenciador de pacotes `pip`

### Passo a Passo

1. **Clone este repositório:**
```bash
$ git clone [https://github.com/seu-usuario/nome-do-repositorio.git](https://github.com/seu-usuario/nome-do-repositorio.git)
$ cd nome-do-repositorio
