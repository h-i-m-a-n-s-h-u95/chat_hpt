# chat_hpt

A chat application built with [Next.js](https://nextjs.org/) and [assistant-ui](https://www.assistant-ui.com/), powered by [Groq](https://groq.com/) for fast LLM inference.

**Live demo:** [chat-hpt-seven.vercel.app](https://chat-hpt-seven.vercel.app/)

## Tech Stack

- **Framework:** Next.js 16 (App Router, Turbopack)
- **Chat UI:** assistant-ui (`@assistant-ui/react`, `@assistant-ui/react-ai-sdk`)
- **LLM Provider:** Groq (`@ai-sdk/groq`) running `llama-3.3-70b-versatile`
- **AI SDK:** Vercel AI SDK v6
- **Styling:** Tailwind CSS + shadcn/ui components
- **Language:** TypeScript
- **Hosting:** Vercel

## Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/h-i-m-a-n-s-h-u95/chat_hpt.git
cd chat_hpt
```

### 2. Install dependencies

```bash
npm install
```

### 3. Set up environment variables

Copy the example file and fill in your own API key:

```bash
cp .env.example .env.local
```

Then open `.env.local` and add your [Groq API key](https://console.groq.com/keys):

```
GROQ_API_KEY=your_groq_api_key_here
```

### 4. Run the development server

```bash
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) to view the app.

## Available Scripts

| Command | Description |
|---|---|
| `npm run dev` | Start the local dev server (Turbopack) |
| `npm run build` | Create a production build |
| `npm run start` | Run the production build locally |
| `npm run lint` | Lint the codebase |
| `npm run lint:fix` | Lint and auto-fix issues |
| `npm run format` | Check code formatting |
| `npm run format:fix` | Auto-format the codebase |

## Project Structure

```
app/
  api/chat/route.ts       # API route that streams responses from the Groq model
  assistant.tsx           # Main assistant/chat page composition
  page.tsx                # App entry route
components/
  assistant-ui/           # Chat UI primitives (thread, composer, tool rendering, etc.)
  ui/                     # Shared shadcn/ui components
lib/
  utils.ts                # Shared utility helpers
hooks/
  use-mobile.ts            # Responsive layout hook
```

## Deployment

This project is deployed on [Vercel](https://vercel.com) at **[chat-hpt-seven.vercel.app](https://chat-hpt-seven.vercel.app/)**.

To deploy your own copy:

1. Import the GitHub repository into Vercel.
2. Add the required environment variable in the Vercel project settings (**Settings → Environment Variables**):
   - `GROQ_API_KEY`
3. Deploy — Vercel automatically detects the Next.js framework and runs the build.
4. If you add or change an environment variable after the first deploy, trigger a redeploy — Vercel does not pick up env var changes on a running deployment automatically.

## Notes

- `node_modules/` and `.env.local` are intentionally excluded from version control (see `.gitignore`). Use `.env.example` as a reference for required environment variables.
- The model used in `app/api/chat/route.ts` can be swapped for any [Groq-supported model](https://console.groq.com/docs/models) or another AI SDK provider (e.g. `@ai-sdk/openai`, `@ai-sdk/google`) by updating the import and `model:` field.
