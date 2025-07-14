## 2️⃣ Front‑end (folder web)

**a) Criação inicial**

cd ../web
npx create-react-app .
npm install axios

**b) Estrutura de pastas**

src/
├── components/
│   ├── Chat.js
│   ├── Message.js
│   ├── Sidebar.js
│   └── CSS/
│       └── App.css
└── App.js

**c) Componente principal App.js**

import React, { useState } from 'react';
import Chat from './components/Chat';
import Sidebar from './components/Sidebar';
import './components/CSS/App.css';

function App() {
  const [messages, setMessages] = useState([]);

  const handleSend = async (text) => {
    const newMsg = { role: 'user', content: text };
    const updated = [...messages, newMsg];
    setMessages(updated);

    const response = await fetch('http://localhost:5000/api/chat', {
      method: 'POST',
      headers: { 'Content-Type': 'application/json' },
      body: JSON.stringify({ messages: updated }),
    });

    const { data } = await response.json();
    setMessages([...updated, data]);
  };

  return (
    <div className="app">
      <Sidebar />
      <Chat messages={messages} onSend={handleSend} />
    </div>
  );
}

export default App;

**d) Chat.js e Message.js**

Chat.js: renderiza lista de mensagens + input para enviar.

Message.js: usa SVG do ChatGPT para bot, mostra avatar e bolhas diferentes.


**e) Sidebar.js**

Menu lateral com opções, temas, etc. Estilizar via CSS.

**f) Estilização**

Use CSS puro ou módulos para layout, cores, responsividade, declarações .app, .chat-container, .message, etc.


