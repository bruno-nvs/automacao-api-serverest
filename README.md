# Automação de API - ServeRest

Projeto de automação de testes de API utilizando a plataforma ServeRest, com foco na validação de fluxos reais de autenticação e manipulação de dados.

---

## 🎯 Objetivo

Validar operações essenciais de backend:

- Consulta de produtos
- Autenticação de usuário
- Cadastro de produto autenticado

---

## 🛠️ Stack

- Postman  
- Newman  
- htmlextra (relatórios)

---

## 🧪 Cenários Automatizados

### 🔍 Consulta de produtos
- Requisição GET para listagem
- Validação de status e retorno da API

---

### 🔐 Autenticação
- Login com usuário válido
- Captura automática do token JWT
- Armazenamento em variável de ambiente

---

### ➕ Cadastro de produto
- Requisição POST autenticada (Bearer Token)
- Uso dinâmico do token obtido no login
- Validação de criação do recurso

---

## ⚙️ Integração Contínua (CI)
Este projeto conta com uma esteira de CI/CD configurada através do **GitHub Actions**. 
Toda vez que um novo código é enviado (Push/Pull Request) para a branch `main`, o pipeline realiza as seguintes etapas de forma automatizada:
1. Prepara o ambiente Ubuntu na nuvem.
2. Instala o Node.js e as dependências (Newman e htmlextra).
3. Executa a suíte de testes da API.
4. Gera e armazena o relatório `.html` como um *Artifact* disponível para download na aba Actions.

## ▶️ Execução dos testes

1. Clone este repositório na sua máquina:
`git clone https://github.com/bruno-nvs/automacao-api-serverest.git`

2. Instale o Newman e o gerador de relatórios (requer Node.js):
`npm install -g newman newman-reporter-htmlextra`

3. Execute a automação:
```bash
newman run serverest.json -r htmlextra
