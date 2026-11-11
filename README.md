# 🤖 Agente de IA para Gerenciamento de Tarefas no Trello

Projeto desenvolvido como parte de um desafio da **Digital Innovation One (DIO)**, com o objetivo de criar um agente de Inteligência Artificial capaz de gerenciar tarefas no Trello por meio de comandos em linguagem natural.

A solução utiliza **Python**, **Google Agent Development Kit (ADK)**, **Google Gemini** e a API do **Trello**.

## 🎯 Objetivo

Desenvolver um assistente inteligente que permita ao usuário organizar suas tarefas de maneira simples, utilizando mensagens em linguagem natural para interagir com um quadro do Trello.

## 🚀 Funcionalidades

O agente permite:

- **Adicionar tarefas:** criar cartões no Trello a partir de comandos em linguagem natural.
- **Listar tarefas:** consultar as tarefas cadastradas no quadro.
- **Alterar o status:** movimentar tarefas entre as listas do quadro.
- **Definir prazos:** interpretar solicitações com datas e horários e registrar vencimentos.
- **Consultar o contexto temporal:** utilizar informações de data e hora para auxiliar na interpretação de prazos.

### 📋 Organização do quadro

O projeto utiliza três listas:

| Lista | Descrição |
|---|---|
| A fazer | Tarefas pendentes |
| Em andamento | Tarefas em execução |
| Concluído | Tarefas finalizadas |

## 🛠️ Tecnologias utilizadas

- **Python:** linguagem principal do projeto.
- **Google ADK:** framework para desenvolvimento do agente.
- **Google Gemini:** modelo de IA responsável pela interpretação das solicitações.
- **Trello API:** integração com os quadros e cartões.
- **py-trello:** biblioteca Python para comunicação com o Trello.
- **python-dotenv:** gerenciamento de variáveis de ambiente.
- **Git e GitHub:** versionamento e publicação do código.

## 📁 Estrutura do projeto

```text
dio-agente-ia-trello/
├── agenttaskmanager/
│   ├── __init__.py
│   ├── agent.py
│   └── .env.exemplo
├── .gitignore
├── requirements.txt
└── README.md
```

## ⚙️ Instalação e configuração

### 1. Clonar o repositório

```bash
git clone https://github.com/JoelPereira31/dio-agente-ia-trello.git
cd dio-agente-ia-trello
```

### 2. Criar um ambiente virtual

```bash
python -m venv .venv
```

No Windows PowerShell:

```powershell
.\.venv\Scripts\Activate.ps1
```

### 3. Instalar as dependências

```bash
pip install -r requirements.txt
```

### 4. Configurar as credenciais

Na pasta `agenttaskmanager`, crie um arquivo `.env` com base