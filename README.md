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

Na pasta `agenttaskmanager`, crie um arquivo `.env` com base no arquivo `.env.exemplo`.

Configure as variáveis:

```env
GOOGLE_API_KEY=sua_chave_google
GOOGLE_GENAI_USE_VERTEXAI=0

TRELLO_API_KEY=sua_chave_trello
TRELLO_API_SECRET=seu_segredo_trello
TRELLO_TOKEN=seu_token_trello
```

As credenciais devem ser obtidas nos respectivos serviços.

**Importante:** nunca publique o arquivo `.env` contendo credenciais reais. O projeto utiliza `.gitignore` para evitar seu envio ao GitHub.

Também é necessário configurar o quadro do Trello utilizado pelo agente, conforme a implementação em `agenttaskmanager/agent.py`.

## ▶️ Como executar

Com o ambiente virtual ativado, execute na pasta principal do projeto:

```bash
adk web
```

Abra no navegador o endereço indicado pelo terminal, normalmente:

```text
http://127.0.0.1:8000
```

Na interface do Google ADK, selecione o agente `agenttaskmanager` e envie suas solicitações.

## 💬 Exemplos de utilização

**Criar uma tarefa:**

> Adicione uma tarefa chamada "Estudar Python" na lista A fazer.

**Criar uma tarefa com prazo:**

> Adicione uma tarefa chamada "Entregar relatório" para amanhã às 15h.

**Consultar tarefas:**

> Liste as tarefas cadastradas no Trello.

**Atualizar o status:**

> Mova a tarefa "Estudar Python" para Concluído.

## 🧪 Testes realizados

Durante o desenvolvimento, foram realizados testes de integração entre o agente e o Trello, incluindo:

- Criação de cartões no quadro.
- Listagem de tarefas existentes.
- Movimentação de cartões entre as listas.
- Interpretação de prazos em linguagem natural.
- Execução do agente pela interface web do Google ADK.

As funcionalidades principais foram verificadas durante o desenvolvimento.

## 🔐 Segurança

As chaves de API e os tokens de autenticação são armazenados em variáveis de ambiente.

O arquivo `.env` não deve ser versionado. O repositório disponibiliza apenas um arquivo de exemplo para orientar a configuração.

## 📚 Aprendizados

Este projeto permitiu praticar:

- Desenvolvimento de agentes de IA com Google ADK.
- Integração de modelos Gemini com ferramentas Python.
- Consumo de APIs externas.
- Automação de tarefas no Trello.
- Interpretação de comandos em linguagem natural.
- Gerenciamento de credenciais e variáveis de ambiente.
- Versionamento de código com Git e GitHub.

## 👨‍💻 Autor

**Joel Pereira**

GitHub: [@JoelPereira31](https://github.com/JoelPereira31)

Projeto desenvolvido para fins educacionais como parte de um desafio da **DIO — Digital Innovation One**.