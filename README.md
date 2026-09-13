# 🏋️ Academia Brother Gil — Personal Trainer Virtual (Carapicuíba - SP)

Aplicação web de chat com IA que simula um personal trainer virtual. O assistente, chamado Gilmar, tira dúvidas sobre treinos, execução de exercícios e nutrição esportiva, e recomenda academias exclusivamente na cidade de Carapicuíba - SP.

## 💡 Sobre o projeto

O foco deste projeto foi ir além de um chatbot genérico: o assistente tem uma persona definida, um escopo de atuação restrito (só fala sobre fitness e sobre academias de Carapicuíba) e regras de comportamento bem definidas via engenharia de prompt — por exemplo, ele recusa educadamente perguntas sobre programação ou sobre academias de outras cidades, mesmo que o usuário insista.

## 🚀 Funcionalidades

- **Persona com escopo definido** — responde apenas sobre treino, nutrição esportiva e academias de Carapicuíba - SP, recusando educadamente qualquer assunto fora desse contexto.
- **Interface responsiva** — tema azul marinho moderno, adaptável a celular e desktop.
- **Modo claro / escuro** — alternância de tema com um clique.
- **Histórico persistente** — as conversas ficam salvas automaticamente no `localStorage` do navegador.
- **Respostas em Markdown** — textos formatados (negrito, listas) com botão de copiar.
- **Contador e horário** — exibe o total de mensagens e o horário de cada uma.

## 🛠️ Tecnologias utilizadas

- **Front-end:** HTML5, CSS3, JavaScript (ES6+), Marked.js
- **Back-end:** Node.js, Express, CORS, Dotenv
- **IA:** API OpenAI / Azure OpenAI

## 🏗️ Como funciona

O front-end (HTML/CSS/JS puro, sem framework) envia cada mensagem para um back-end em Node/Express. O back-end monta um system prompt dinâmico — com data e hora atuais, a persona do "Gilmar" e as regras de escopo — e repassa a conversa para a API de IA, devolvendo a resposta para o navegador. Isso mantém a chave da API protegida no servidor, sem expô-la no front-end.

## ⚙️ Como executar localmente

**Passo 1 — Clone o repositório e instale as dependências:**
```bash
git clone https://github.com/Gilmar9374/AcademiaBrotherGil.git
cd AcademiaBrotherGil
npm install
```

**Passo 2 — Crie um arquivo `.env` dentro da pasta `Back-end` com suas credenciais:**
```
OPENAI_API_KEY=sua_chave_aqui
OPENAI_BASE_URL=sua_base_url_aqui
MODEL_NAME=gpt-5.6-luna
PORT=3000
```

**Passo 3 — Inicie o servidor:**
```bash
npm start
```

**Passo 4 — Acesse `http://localhost:3000` no navegador.**

## 📁 Estrutura do projeto

```
AcademiaBrotherGil/
├── Back-end/
│   ├── server.js        # Servidor Express + integração com a API de IA
│   └── package.json
└── frontend/
    ├── index.html
    ├── script.js         # Lógica do chat, tema e histórico
    └── style.css
```

## 🎯 Habilidades demonstradas

Integração com API de IA generativa, engenharia de prompt (definição de persona, escopo e regras de comportamento), arquitetura cliente-servidor com Node.js/Express, proteção de chaves de API via variáveis de ambiente, e desenvolvimento front-end com JavaScript puro (manipulação de DOM, `localStorage`, temas dinâmicos).

## 🔜 Próximos passos

- Publicar uma versão online (deploy) para demonstração ao vivo.
- Adicionar testes automatizados para o endpoint `/chat`.
