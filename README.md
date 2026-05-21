Para facilitar, aqui está o conteúdo formatado exatamente como deve ficar dentro do seu arquivo.

Basta usar o botão **"Copiar código"** no canto superior direito do bloco abaixo, abrir o Bloco de Notas (ou seu editor de código), colar o texto e salvar o arquivo com o nome **`README.md`** (ou `README.txt`, se preferir) na raiz do seu projeto.

```text
# Projeto IDW 🚀

> Laboratório prático de Desenvolvimento Web focado na implementação de um CRUD completo de usuários utilizando arquitetura de containers.

Este projeto atende aos objetivos pedagógicos do plano de ensino de desenvolvimento web, substituindo a stack tradicional em PHP por uma arquitetura moderna baseada em Node.js e Express, totalmente conteinerizada com Docker.

---

## 🛠️ Tecnologias e Stack Utilizadas

O ecossistema do projeto é dividido de forma isolada e profissional:

* Frontend: HTML5 (estruturação semântica), CSS3 (layout responsivo) e JavaScript Vanilla (consumo da API via Fetch).
* Servidor Web (Frontend): NGINX (utilizado para servir os arquivos estáticos).
* Backend (API): Node.js com o framework Express.
* Banco de Dados: MySQL 8.0 com persistência de dados.
* Orquestração: Docker & Docker Compose.

---

## 📂 Estrutura do Projeto

A estrutura final do laboratório segue o padrão de responsabilidades divididas:

lab-mysql-docker/
├── docker-compose.yml           # Orquestração dos serviços (App, DB, NGINX)
├── db/
│   └── init.sql                 # Script de inicialização do Banco de Dados
├── frontend/                    # Interface do usuário (Servida pelo NGINX)
│   ├── index.html
│   ├── styles.css
│   └── app.js
├── nginx/
│   └── default.conf             # Configuração de proxy/servidor do NGINX
└── app/                         # Backend / API REST (Node.js + Express)
    ├── Dockerfile
    ├── package.json
    ├── server.js                # Inicialização e middlewares da API
    ├── db.js                    # Pool de conexão com o MySQL
    ├── routes/                  # Definição dos endpoints (Usuários e Auth)
    ├── controllers/             # Regras de negócio e tratamento de req/res
    └── services/                # Consultas diretas e manipulação do Banco

---

## ⚙️ Funcionalidades Implementadas

* [x] Interface Responsiva: Design adaptável para dispositivos móveis e desktops.
* [x] CRUD Completo de Usuários:
  - Create: Cadastro de novos usuários via formulário dinâmico.
  - Read: Listagem em tempo real e busca por ID.
  - Update: Edição de registros direto na tabela.
  - Delete: Remoção física com confirmação em tela.
* [x] Camada de Validação: Tratamento de campos obrigatórios no cliente e no servidor.
* [x] Autenticação Simples: Estrutura base para controle de sessão utilizando express-session.

---

## 🚀 Como Executar o Projeto

Graças ao Docker, você não precisa instalar o Node.js ou o MySQL localmente na sua máquina. Você só precisará do Git e do Docker instalados.

### 1. Clonar o repositório
git clone https://github.com/DeivissonAmorim/ProjetoIDW.git
cd ProjetoIDW

### 2. Subir o ambiente com o Docker
Execute o comando abaixo para construir as imagens e rodar os containers em segundo plano:
docker compose up --build -d

### 3. Acessar a aplicação
Após o Docker finalizar a inicialização, você poderá acessar os serviços nos seguintes endereços:

* Frontend (Interface Web): http://localhost:8080
* Backend (API REST): http://localhost:3000
* Status da API (Healthcheck): http://localhost:3000/health

Para derrubar o ambiente quando finalizar os testes:
docker compose down

---

## 🧑‍💻 Autor

Desenvolvido por Deivisson Monteiro Amorim.

* GitHub: @DeivissonAmorim

---

## 📄 Licença

Este projeto está sob a licença MIT.

```