# 🌐 NexusLang — AI-Powered Language Translator

> Translate Instantly. Connect Effortlessly. Break Boundaries, Not Conversations.

A futuristic AI-powered translator supporting 100+ languages with real-time translation,
speech support, auto language detection, and a cyberpunk-inspired interface.

---

## ✨ Features

| Feature | Description |
|---|---|
| 🌍 100+ Languages | Powered by Google Translate via deep-translator |
| ⚡ Real-Time Translation | Fast responses via FastAPI backend |
| 🔍 Auto Language Detection | Detects source language automatically |
| 🔊 Text-to-Speech | gTTS-powered audio for any language |
| 📋 One-Click Copy | Copy translation instantly |
| 🔄 Language Swap | Flip source ↔ target in one click |
| 🎨 Cyberpunk UI | Animated circuit scan lines, neon palette |
| 📱 Mobile Friendly | Fully responsive layout |

---

## 🛠️ Tech Stack

**Frontend:** HTML · CSS · JavaScript  
**Backend:** Python · FastAPI · Uvicorn  
**Libraries:** deep-translator · langdetect · gTTS

---

## 🚀 Setup & Run

### 1. Clone the repo

```bash
git clone <your-repo-url>
cd translator
```

### 2. Install dependencies

```bash
pip install -r requirements.txt
```

### 3. Start the server

```bash
python main.py
```

Or with uvicorn directly:

```bash
uvicorn main:app --host 0.0.0.0 --port 8000 --reload
```

### 4. Open in browser

```
http://localhost:8000
```

---

## 📁 Project Structure

```
translator/
├── main.py              # FastAPI backend
├── requirements.txt     # Python dependencies
├── README.md
└── static/
    └── index.html       # Full frontend (HTML + CSS + JS)
```

---

## 🔌 API Endpoints

| Method | Endpoint | Description |
|---|---|---|
| GET  | `/` | Serves the frontend |
| GET  | `/api/languages` | Returns all supported languages |
| POST | `/api/translate` | Translates text |
| POST | `/api/detect` | Detects language of text |
| POST | `/api/tts` | Returns MP3 audio for given text |

### Example — `/api/translate`

**Request:**
```json
{
  "text": "Hello, how are you?",
  "source": "auto",
  "target": "hi"
}
```

**Response:**
```json
{
  "translated": "नमस्ते, आप कैसे हैं?",
  "detected_language": "en",
  "detected_name": "English"
}
```

---
**LIVE DEMO **
https://codealpha-nexuslang.onrender.com/


** SCREENSHOT**
<img width="1895" height="953" alt="image" src="https://github.com/user-attachments/assets/22b41ab8-fd4d-42db-8615-cf99954b28ae" />

<img width="1885" height="843" alt="image" src="https://github.com/user-attachments/assets/c45e40d1-64e9-4832-b179-158fb1c41a7d" />



** AUTHOR**
SHIVAM KUMAR RAY
www.linkedin.com/in/shivam-kumar-ray-ba45b0204

## 📝 Notes

- Max input: **5000 characters**
- TTS audio is capped at 500 characters per request
- `source: "auto"` enables automatic language detection
- The app falls back to browser Speech Synthesis API if the TTS endpoint is unreachable
