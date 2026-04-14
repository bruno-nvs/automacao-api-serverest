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

## ▶️ Execução dos testes

```bash
newman run serverest.json -r htmlextra
