<h1 align="center"> 🛒 E-commerce API </h1>

<p align="center">
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python">
  <img src="https://img.shields.io/badge/Flask-000000?style=for-the-badge&logo=flask&logoColor=white" alt="Flask">
  <img src="https://img.shields.io/badge/SQLAlchemy-D71F00?style=for-the-badge&logo=sqlalchemy&logoColor=white" alt="SQLAlchemy">
  <img src="https://img.shields.io/badge/SQLite-003B57?style=for-the-badge&logo=sqlite&logoColor=white" alt="SQLite">
  <img src="https://img.shields.io/badge/Swagger-85EA2D?style=for-the-badge&logo=swagger&logoColor=black" alt="Swagger">
</p>

> 🎓 **Projeto Acadêmico - FATEC Assis** <br>
> Este projeto foi concebido e desenvolvido como um trabalho acadêmico prático na **FATEC Assis**, pela turma de **Gestão da Tecnologia da Informação (GTI)**.

<br>

## 📖 Sobre o Projeto

A **E-commerce API** é uma API REST desenvolvida para simular o back-end de um sistema de comércio eletrônico. O projeto cobre funcionalidades essenciais de um e-commerce real: gerenciamento de produtos, autenticação de usuários, carrinho de compras e checkout.

A aplicação foi construída com **Flask**, um microframework leve e flexível para Python, utilizando **Flask-SQLAlchemy** como ORM para persistência de dados com **SQLite**. A documentação completa dos endpoints foi estruturada com **Swagger (OpenAPI 2.0)**.

---

## 📑 Índice

- [Funcionalidades](#-funcionalidades)
- [Tecnologias Utilizadas](#-tecnologias-utilizadas)
- [Estrutura do Projeto](#-estrutura-do-projeto)
- [Como Executar o Projeto](#%EF%B8%8F-como-executar-o-projeto)
- [Endpoints da API](#-endpoints-da-api)
- [Autor](#-autor)

---

## 🚀 Funcionalidades

- **📦 CRUD de Produtos:** Criação, listagem, busca por ID, atualização e remoção de produtos.
- **🔐 Autenticação:** Login e logout de usuários via sessão.
- **🛒 Carrinho de Compras:** Adição e remoção de itens, visualização do carrinho e checkout.
- **🔍 Busca de Produtos:** Endpoint dedicado para pesquisa de produtos por query.
- **📄 Documentação Swagger:** Contrato completo da API documentado em `swagger.yaml`.

---

## 🛠️ Tecnologias Utilizadas

| Tecnologia | Uso |
|---|---|
| **Python** | Linguagem principal |
| **Flask** | Framework web para construção da API REST |
| **Flask-SQLAlchemy** | ORM para mapeamento objeto-relacional |
| **Flask-Login** | Gerenciamento de sessão e autenticação de usuários |
| **Flask-CORS** | Liberação de requisições cross-origin |
| **SQLite** | Banco de dados relacional local |
| **Swagger / OpenAPI 2.0** | Documentação dos endpoints da API |

---

## 📁 Estrutura do Projeto

```
ecommerce-api/
│
├── app.py              # Ponto de entrada; modelos e rotas da aplicação
├── swagger.yaml        # Documentação completa da API (OpenAPI 2.0)
├── requirements.txt    # Dependências do projeto
│
├── ecommerce.db        # Banco de dados SQLite (gerado automaticamente)
├── .gitignore          # Arquivos ignorados pelo Git
└── README.md           # Documentação do projeto
```

---

## ⚙️ Como Executar o Projeto

### Pré-requisitos

- Python 3.10 ou superior instalado
- `pip` para gerenciamento de pacotes

### Passo a passo

1. **Clone o repositório:**
   ```bash
   git clone https://github.com/seu-usuario/ecommerce-api.git
   cd ecommerce-api
   ```

2. **Crie e ative um ambiente virtual:**
   ```bash
   python -m venv venv

   # Windows
   venv\Scripts\activate

   # Linux / macOS
   source venv/bin/activate
   ```

3. **Instale as dependências:**
   ```bash
   pip install -r requirements.txt
   ```

4. **Inicie o banco de dados e execute o servidor:**
   ```bash
   python app.py
   ```

5. **A API estará disponível em:**
   ```
   http://127.0.0.1:5000
   ```

---

## 📡 Endpoints da API

### Autenticação

| Método | Rota | Descrição |
|---|---|---|
| `POST` | `/login` | Realiza o login do usuário |
| `POST` | `/logout` | Encerra a sessão do usuário |

### Produtos — `/api/products`

| Método | Rota | Descrição |
|---|---|---|
| `GET` | `/api/products` | Lista todos os produtos |
| `GET` | `/api/products/<id>` | Retorna detalhes de um produto |
| `GET` | `/api/products/search?q=` | Busca produtos por nome |
| `POST` | `/api/products/add` | Adiciona um novo produto |
| `PUT` | `/api/products/update/<id>` | Atualiza um produto existente |
| `DELETE` | `/api/products/delete/<id>` | Remove um produto |

### Carrinho — `/api/cart`

| Método | Rota | Descrição |
|---|---|---|
| `GET` | `/api/cart` | Visualiza o carrinho do usuário |
| `POST` | `/api/cart/add/<product_id>` | Adiciona item ao carrinho |
| `DELETE` | `/api/cart/remove/<item_id>` | Remove item do carrinho |
| `POST` | `/api/cart/checkout` | Finaliza a compra e limpa o carrinho |

---

## 👨‍💻 Autor

<p align="center">
  Desenvolvido com 🛒 por <strong>Marco Guilherme Vitorino Moreira</strong><br>
</p>
3