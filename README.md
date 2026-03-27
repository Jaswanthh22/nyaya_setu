# Nyaya Setu — न्याय सेतु

> **AI-assisted legal triage and support for safer, faster access to justice in India.**
>
> Hackathon MVP · Frontend Only · No backend required

---

## 🚀 Quick Start

```bash
# 1. Install dependencies
npm install

# 2. Start the development server
npm run dev

# 3. Open in browser
open http://localhost:3000
```

---

## 📁 Folder Structure

```
src/
├── app/                   # Next.js 14 App Router pages
│   ├── layout.tsx         # Root layout (Navbar + Footer)
│   ├── page.tsx           # Landing page (/)
│   ├── file-case/         # Party A complaint form (/file-case)
│   ├── respond/           # Party B response form (/respond)
│   ├── dashboard/         # Judge/reviewer dashboard (/dashboard)
│   └── chat/              # Safety guidance chat (/chat)
│
├── components/
│   └── layout/
│       ├── Navbar.tsx     # Sticky top navigation
│       └── Footer.tsx     # Footer with helplines
│
├── lib/
│   ├── utils.ts           # cn(), generateCaseId(), formatDate()
│   └── constants.ts       # APP_NAME, categories, statuses, nav links
│
├── mock-data/
│   ├── cases.ts           # 5 rich mock cases with AI analysis
│   └── messages.ts        # Chat messages and mock AI response logic
│
├── hooks/
│   ├── useCases.ts        # Returns mock cases (swap for Supabase)
│   └── useChat.ts         # Chat state management (swap for Gemini)
│
└── services/
    ├── supabase.ts        # Supabase placeholder (instructions inside)
    └── gemini.ts          # Gemini API placeholder (instructions inside)
```

---

## 📝 Where to Edit Content

| What                         | File                                 |
|------------------------------|--------------------------------------|
| App name, nav links          | `src/lib/constants.ts`               |
| Case categories              | `src/lib/constants.ts`               |
| Landing page text/hero       | `src/app/page.tsx`                   |
| Mock cases                   | `src/mock-data/cases.ts`             |
| AI chat responses (mock)     | `src/mock-data/messages.ts`          |
| Navigation links             | `src/components/layout/Navbar.tsx`   |
| Footer helplines             | `src/components/layout/Footer.tsx`   |

---

## 🗄️ Connecting Supabase (Later)

1. Install the SDK:
   ```bash
   npm install @supabase/supabase-js
   ```
2. Create `.env.local` in the project root:
   ```env
   NEXT_PUBLIC_SUPABASE_URL=https://your-project.supabase.co
   NEXT_PUBLIC_SUPABASE_ANON_KEY=your-anon-key
   ```
3. Replace `src/services/supabase.ts` with the real client (instructions are in that file).
4. Update `src/hooks/useCases.ts` to call the real Supabase queries.

---

## 🤖 Connecting Gemini AI (Later)

1. Install the SDK:
   ```bash
   npm install @google/generative-ai
   ```
2. Add to `.env.local`:
   ```env
   GEMINI_API_KEY=your-api-key
   ```
3. Create `src/app/api/chat/route.ts` as a Next.js API route (example template in `src/services/gemini.ts`).
4. Update `src/hooks/useChat.ts` to call the real `/api/chat` endpoint instead of `getMockAssistantResponse`.

---

## 🎨 Design System

- **Colors:** Indigo/Slate palette — `primary-600` (#4f46e5) as accent
- **Typography:** Inter (Google Fonts) via CSS import
- **Components:** Custom CSS utility classes in `globals.css` + Radix UI primitives
- **Spacing:** Tailwind's standard scale, page container at `max-w-7xl`

---

## 📞 Emergency Helplines (India)

| Helpline                  | Number          |
|---------------------------|-----------------|
| National Emergency        | 112             |
| Women Helpline            | 1091            |
| Legal Aid Services        | 15100           |
| NCW Helpline              | 7827170170      |
| Cyber Crime               | cybercrime.gov.in |

---

## 🛠 Tech Stack

- **Next.js 14** — App Router
- **TypeScript** — Full type safety
- **Tailwind CSS** — Styling
- **Radix UI** — Accessible primitives
- **Lucide React** — Icons
- **Mock Data** — No backend required

---

*Built for social impact 🇮🇳 — Hackathon MVP*
# nyaya_setu
