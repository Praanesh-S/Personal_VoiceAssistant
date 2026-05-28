# 🤖 Praans Agent — Personal AI Voice Assistant

> A locally-run, voice-enabled AI assistant with a clean React interface — built from scratch using a FastAPI backend, Groq LLM inference, and real-time text-to-speech.

![Stack](https://img.shields.io/badge/Frontend-React_+_Tailwind-61DAFB?style=flat&logo=react)
![Stack](https://img.shields.io/badge/Backend-FastAPI-009688?style=flat&logo=fastapi)
![Stack](https://img.shields.io/badge/AI-Groq_LLaMA_3.1-FF6B35?style=flat)
![Stack](https://img.shields.io/badge/Voice-pyttsx3-8B5CF6?style=flat)

---

## ✨ Features

- 🎙️ **Voice Output** — Agent speaks every response aloud via text-to-speech
- 💬 **Conversational Memory** — Maintains context across the last 10 messages per session
- ⚡ **Groq-Powered AI** — Ultra-fast inference using LLaMA 3.1 8B via Groq API
- 🖥️ **Clean React UI** — Polished dark-mode chat interface built with Tailwind CSS
- 🔌 **Decoupled Architecture** — Separate FastAPI backend and React frontend communicating via REST API
- 🛡️ **Secure by Design** — API keys managed via environment variables, never exposed in code

---

## 🛠️ Tech Stack

| Layer | Technology |
|-------|-----------|
| Frontend | React 18 + Vite + Tailwind CSS |
| Backend | Python + FastAPI + Uvicorn |
| AI Model | LLaMA 3.1 8B via Groq API |
| Voice | pyttsx3 (text-to-speech) |
| HTTP Client | Axios |
| Environment | python-dotenv |

---

## 📁 Project Structure

```
praans-agent/
├── backend/
│   ├── main.py              # FastAPI server, AI logic, voice output
│   ├── requirements.txt     # Python dependencies
│   ├── .env                 # API keys (not committed)
│   └── venv/                # Python virtual environment
├── frontend/
│   ├── src/
│   │   ├── App.jsx          # Main React component
│   │   └── index.css        # Tailwind styles
│   ├── package.json
│   └── vite.config.js
└── README.md
```

---

## 🚀 Getting Started

### Prerequisites
- Python 3.10+
- Node.js 18+
- A free [Groq API key](https://console.groq.com)

### 1. Clone the repository
```bash
git clone https://github.com/Praanesh-S/Personal_VoiceAssistant.git
cd Personal_VoiceAssistant
```

### 2. Set up the backend
```bash
cd backend
python3 -m venv venv
source venv/bin/activate        # On Windows: venv\Scripts\activate
pip install -r requirements.txt
```

### 3. Configure environment variables
Create a `.env` file inside the `backend` folder:
```
GROQ_API_KEY=your_groq_api_key_here
```
Get your free API key at [console.groq.com](https://console.groq.com)

### 4. Start the backend
```bash
python3 -m uvicorn main:app --reload --port 8000
```

### 5. Set up and start the frontend
```bash
cd ../frontend
npm install
npm run dev
```

### 6. Open the app
Visit `http://localhost:5173` in your browser.

---

## 🗺️ Roadmap

- [x] AI chat with conversational memory
- [x] Voice output (text-to-speech)
- [ ] Voice input (speech-to-text)
- [ ] Wake word detection (custom trained model)
- [ ] Web search integration (DuckDuckGo)
- [ ] Persistent memory across sessions
- [ ] Daily briefing mode
- [ ] Document/PDF chat

---

## 🧠 Architecture Overview

```
User types message
       ↓
React Frontend (localhost:5173)
       ↓ POST /chat via Axios
FastAPI Backend (localhost:8000)
       ↓
Groq API → LLaMA 3.1 8B inference
       ↓
Response returned to frontend + spoken via pyttsx3
```

---

## 👨‍💻 Author

**Praanesh S** — First Year B.Tech CSE (Data Science), VIT Chennai

[![GitHub](https://img.shields.io/badge/GitHub-Praanesh--S-181717?style=flat&logo=github)](https://github.com/Praanesh-S)

---

> Built during first year summer break as part of learning full-stack AI product development.
> This project explores real-time LLM integration, REST API design, and voice-enabled interfaces.
