💬 Support AI – Embeddable AI Customer Support (Next.js)
A full-stack embeddable AI customer support chatbot built using Next.js, MongoDB, and Scalekit with Google Gemini AI responses, one-line JavaScript embed, and serverless deployment on Vercel.
Live Demo: support-ai-liard.vercel.app

- Tech Stack
Frontend

Next.js 16 (App Router)
TypeScript
Tailwind CSS v4
Motion (animations)
Axios

Backend

Next.js API Routes (serverless)
MongoDB + Mongoose
Scalekit (Authentication)
Google Gemini 2.5 Flash (@google/genai)

Other

REST APIs
CORS
CI/CD via GitHub + Vercel
dotenv


✨ Features
👤 Business Owner

Register / Login via Scalekit
Configure business name, support email, and knowledge base
Get a one-line JavaScript embed snippet
Dashboard to manage chatbot settings

- AI Chatbot

Answers customer questions using your business knowledge base only
Friendly greeting responses
Falls back to "Please contact support" for unrelated questions
Never invents policies or information

- System

One-line embeddable JavaScript widget
Gemini 2.5 Flash AI with ~1s response latency
CORS-enabled API for cross-origin embedding
Serverless API routes on Vercel
Auto-deploy on every code push via CI/CD


📁 Project Structure
support-ai/
│
├── public/
│
└── src/
    ├── app/
    │   ├── api/
    │   │   ├── auth/          # Scalekit authentication routes
    │   │   ├── chat/          # AI chat endpoint (POST)
    │   │   └── settings/      # Chatbot configuration routes
    │   ├── dashboard/         # Owner dashboard page
    │   ├── embed/             # Embeddable chatbot UI
    │   ├── layout.tsx
    │   └── page.tsx           # Landing page
    ├── components/            # Reusable React components
    ├── lib/                   # DB connection, utilities
    ├── model/                 # Mongoose models
    ├── proxy.ts
    └── types.d.ts

- Embed on Any Website
👉 Try it live: support-ai-liard.vercel.app
After configuring your chatbot on the dashboard, paste this single line into any website:
html<script src="https://support-ai-liard.vercel.app/embed.js?ownerId=YOUR_OWNER_ID"></script>

- How AI Works
User Message → Fetch Business Settings (MongoDB) → Build Grounded Prompt → Gemini 2.5 Flash → Reply

AI answers only from the configured knowledge base
Handles greetings with a friendly welcome
Replies "Please contact support" for unrelated questions
Never invents policies or information
