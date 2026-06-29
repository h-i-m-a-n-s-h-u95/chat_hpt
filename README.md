# 🤖chat_hpt (Next.js + Groq API)

A modern AI chatbot built with **Next.js** and powered by the **Groq API**.
This project replicates a ChatGPT-like interface with fast responses and a clean UI.

---

## 🌐 Live Demo

👉 https://chat-hpt-seven.vercel.app/

---

## ⚙️ Tech Stack

* **Frontend:** Next.js (App Router)
* **Styling:** Tailwind CSS (or your styling system)
* **AI Backend:** Groq API (LLaMA / Mixtral models)
* **Deployment:** Vercel

---

## ✨ Features

* 💬 ChatGPT-like UI
* ⚡ Fast responses using Groq inference
* 🧠 Context-based conversation
* 📱 Responsive design
* 🔄 Streaming responses (if implemented)
* 🌙 Clean modern interface

---

## 📁 Project Structure

```
app/
  page.tsx
  assistant.tsx

components/
  thread.tsx
  chat-input.tsx
  message.tsx

lib/
  groq.ts
```

---

## 🔑 Environment Variables

Create a `.env.local` file:

```
GROQ_API_KEY=your_groq_api_key_here
```

---

## ▶️ Getting Started

Clone the repo:

```
git clone https://github.com/your-username/your-repo.git
cd your-repo
```

Install dependencies:

```
npm install
```

Run development server:

```
npm run dev
```

---

## 🚀 Deployment

Deployed on **Vercel**:

```
vercel
```

Or connect your GitHub repo directly to Vercel.

---

## 🧠 How It Works

1. User enters a prompt
2. Request is sent to Groq API
3. Model generates response (LLaMA / Mixtral)
4. UI updates in real-time

---

## ⚠️ Notes

* Ensure your Groq API key is secure
* Add rate limiting for production
* Improve error handling for API failures

---

## 📸 Preview

ChatGPT-style interface with:

* Sidebar (optional)
* Chat thread
* Input box
* Streaming responses

---

## 🙌 Future Improvements

* Authentication
* Chat history persistence (DB)
* Multi-model switching
* Voice input/output
* File uploads

---

## ⭐ Contributing

Feel free to fork and improve this project!

---

## 📄 License

MIT License
