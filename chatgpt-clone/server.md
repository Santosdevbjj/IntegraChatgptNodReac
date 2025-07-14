## 1️⃣ Back‑end (folder server)

**a) Inicialização**

cd server
npm init -y
npm install express cors dotenv openai
npm install --save-dev nodemon

**Atualize o package.json:**

"scripts": {
  "start": "node index.js",
  "dev": "nodemon index.js"
}

**b) index.js**

require('dotenv').config();
const express = require('express');
const cors = require('cors');
const { Configuration, OpenAIApi } = require('openai');

const app = express();
app.use(cors());
app.use(express.json());

const config = new Configuration({
  apiKey: process.env.OPENAI_API_KEY,
});
const openai = new OpenAIApi(config);

app.post('/api/chat', async (req, res) => {
  try {
    const { messages } = req.body;

    const response = await openai.createChatCompletion({
      model: 'gpt-3.5-turbo',
      messages
    });

    res.json({ data: response.data.choices[0].message });
  } catch (err) {
    console.error(err);
    res.status(500).json({ error: 'Erro interno no servidor' });
  }
});

const PORT = process.env.PORT || 5000;
app.listen(PORT, () => console.log(`Backend rodando em http://localhost:${PORT}`));

**c) Configuração .env**

OPENAI_API_KEY=your_api_key_here

**🎯 Rodando o back‑end:**

npm run dev

O servidor escuta por padrão na porta 5000.






