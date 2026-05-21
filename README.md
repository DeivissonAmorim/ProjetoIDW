# Projeto IDW 🚀

> Laboratório prático de Desenvolvimento Web focado na implementação de um CRUD completo de usuários utilizando arquitetura de containers. 

Este projeto atende aos objetivos pedagógicos do plano de ensino de desenvolvimento web, substituindo a stack tradicional em PHP por uma arquitetura moderna baseada em **Node.js** e **Express**, totalmente conteinerizada com **Docker**.

---

## 🛠️ Tecnologias e Stack Utilizadas

O ecossistema do projeto é dividido de forma isolada e profissional:

* **Frontend:** HTML5 (estruturação semântica), CSS3 (layout responsivo com variáveis CSS) e JavaScript Vanilla (consumo da API via Fetch).
* **Servidor Web (Frontend):** NGINX (utilizado para servir de forma otimizada os arquivos estáticos).
* **Backend (API):** Node.js com o framework Express.
* **Banco de Dados:** MySQL 8.0 com persistência de dados (volumes).
* **Orquestração:** Docker & Docker Compose.

---

## 📂 Estrutura do Arquitetura do Projeto

A estrutura final do laboratório segue o padrão de responsabilidades divididas:

```text
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