## Formação ChatGPT for Devs. Ministrado pela DIO.me.

![chadevpor](https://github.com/user-attachments/assets/e8c2ec72-7d82-4b13-aa72-8f28bcbdae7b)


**Integrando o ChatGPT com Node e React.**



✨ 🚀 **DESCRIÇÃO:**

   Crie uma aplicação completa utilizando o recurso oficial da OpenAI, a inteligência por trás do chatGPT e crie um front-end clone da ferramenta mais popular do mercado para integrar com um back-end funcional.
   

🔹


**🎵 ChatGPT Clone FullStack** 

Uma aplicação **Clone do ChatGPT**, desenvolvida com **Node.js + Express** no back-end e **React** no front-end, utilizando a API oficial da OpenAI. Inclui modo “Especialista em Música” para estudos sobre escalas (Dó, Sol, Fá, Ré, Mi, Si) e sugestões de músicas em Lá menor, Dó, Sol e Ré.


🔹


## 🚀 Funcionalidades

- Conversa em tempo real com ChatGPT (modelo `gpt-3.5-turbo`)
- Modo “Especialista em Música” com prompts personalizados
- Layout inspirado no ChatGPT, com bolhas, avatars e SVG original
- Histórico de conversas persistido via `localStorage`
- Modo claro/escuro
- Indicador "Digitando..."
- Estilização responsiva (desktop & mobile)


🔹


## 🧰 Tecnologias Utilizadas

**Back‑end (server/)**  
- Node.js (v18+)  
- Express  
- CORS  
- dotenv  
- OpenAI SDK (`openai`)

**Front‑end (web/)**  
- React  
- Axios / Fetch  
- Hooks (`useState`, `useEffect`)  
- CSS puro (estrutura modular)



## ⚙️ Pré-requisitos

- Node.js v18 ou superior  
- NPM ou Yarn  
- Conta na OpenAI e chave API válida  



## ⬇️ Instalação & Execução

Clone este repositório:

```bash
git clone https://github.com/seu-usuario/node-react-chatgpt-clone.git
cd node-react-chatgpt-clone

🖥️ Back‑end

cd server
npm install
echo "OPENAI_API_KEY=SuaApiKeyAqui" > .env
npm run dev

O servidor iniciará em http://localhost:5000.

🌐 Front‑end

cd ../web
npm install
npm start

O front‑end abrirá em http://localhost:3000.


🔹

🎧 Modo "Especialista em Música"

Ao inicializar a conversa, um prompt inicial orienta o modelo para explicar teoria musical:

Você é um especialista em teoria musical...

Teste criando conversas sobre escalas de Dó, Sol, Fá, Ré, Mi, Si e peça músicas em Lá menor, Dó, Sol e Ré.


🔹


🗂️ Estrutura de Pastas

chatgpt-clone/
├── server/       # API com Express + OpenAI
└── web/          # Front‑end em React

No web/src/components/, temos:

Chat.js (fluxo de mensagens)

Message.js (renderiza cada mensagem)

Sidebar.js (menu, temas)

CSS modular em /CSS/


🔹


🤝 Contribuição

Contribuições são bem-vindas!

1. Faça um fork


2. Crie uma branch (feature/nome-da-sua-melhoria)


3. Commit suas alterações


4. Abra um pull request


🔹


 🎯 Sobre

Este clone foi inspirado em projetos como o de Felipe Aguiar.


