# Aplicação de Login Simples

## Descrição

Este projeto é uma aplicação de login simples. A aplicação é dockerizada e utiliza Docker Compose para orquestrar os contêineres.

## Como executar a aplicação

### Pré-requisitos
- Docker
- Docker Compose

### Passos para executar

1. Clone o repositório:
```bash
git clone https://github.com/IzaiasBirth/aplicacao-teste.git
cd  aplicacao-teste
```
2. Construa e inicie os containers:
```bash
docker-compose up --build
```
3. Acesse a aplicação:
- Frontend: `http://localhost:3000`
- Backend:  `http://localhost:8081`

## Como o pipeline de CI/CD funciona
O pipeline de CI/CD configurado no GitHub Actions realiza os seguintes passos:

1. Faz o checkout do código do repositório.
2. Configura o Docker Buildx para a construção das imagens.
3. Faz login no Docker Hub usando as credenciais armazenadas nos segredos do repositório.
4. Constrói as imagens Docker do backend e frontend.
5. Executa o Docker Compose para iniciar os serviços.
6. Executa testes básicos para verificar se as páginas do frontend e backend estão acessíveis.