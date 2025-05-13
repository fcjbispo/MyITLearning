# Configuração do Ambiente de Execução com Docker

Este documento fornece instruções detalhadas para configurar um ambiente de desenvolvimento usando Docker. O ambiente suporta desenvolvimento frontend e backend, pode ser executado localmente ou remotamente, e é compatível com chamadas de `code execution` por agentes de IA via APIs REST ou comandos Docker.

---

## Pré-requisitos
- Docker instalado em sua máquina ou servidor.
- Docker Compose instalado.
- Conhecimento básico de Docker e comandos de terminal.

---

## Estrutura do Ambiente
O ambiente inclui:
- **Backend:** Contêiner Node.js com Express.
- **Frontend:** Contêiner React.
- **Banco de Dados:** Contêiner PostgreSQL.
- **Agente de IA (opcional):** Contêiner para execução de código via API.

---

## Passos para Configuração

### 1. Criar Dockerfile para o Backend
No diretório do backend, crie um arquivo `Dockerfile` com o seguinte conteúdo:
```dockerfile
FROM node:14
WORKDIR /app
COPY package*.json ./
RUN npm install
COPY . .
EXPOSE 3000
CMD ["node", "server.js"]
