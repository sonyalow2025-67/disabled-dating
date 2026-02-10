# ♿ Accessible Social Companion (Hackathon MVP)

An **accessibility-first social interaction assistant**, demonstrated through a dating app UI.  
This project explores how **context-aware assistive tools** (text-to-speech, visual accessibility controls, and communication support) can help people with disabilities navigate everyday social interactions more confidently.

> ⚠️ This is a **front-end MVP built for a hackathon**. Backend features are mocked or simplified to prioritise UI, accessibility, and concept clarity.

---

## 🎯 Problem Statement

Many people with disabilities face **barriers in daily social interactions**, such as:
- Difficulty reading or processing text
- Visual accessibility challenges (small text, low contrast)
- Communication friction in chat-based or unfamiliar contexts

Hackathon challenge prompts often focus on **single-use or daily assistive tools**.  
Our solution reframes dating and social interaction as a **real-world context** where assistive features are immediately useful.

---

## 💡 Solution Overview

We built a **context-aware accessibility companion**, showcased through a dating app experience.  
Instead of focusing purely on matchmaking, the app highlights **assistive tools that can be reused in everyday life**, such as:

- 🔊 Text-to-speech for reading profiles and messages
- 🎨 Font size and high-contrast visual controls
- 👆 Gesture-based interactions (swipe instead of complex UI)
- ⚙️ Centralised accessibility preferences via a global provider

The dating interface acts as a **demo environment** to show how these tools can support real social interactions.

---

## ✨ Key Features

- Swipeable profile discovery (gesture-friendly)
- Text-to-speech for profiles and chat messages
- Font size toggle (small / medium / large)
- High-contrast mode for visual accessibility
- Centralised accessibility state using React Context
- Modular, reusable assistive components
- Responsive design (mobile-first)

---

## 🛠 Tech Stack

- **Next.js (App Router)** – routing & layouts
- **TypeScript** – type safety
- **Tailwind CSS** – rapid, responsive styling
- **shadcn/ui** – accessible UI primitives
- **Framer Motion** – swipe animations
- **Web Speech API** – text-to-speech
- **Supabase (planned / mocked)** – auth & data
- **Vercel (optional)** – deployment

---

## 📁 Project Structure

```txt
src/
  app/
    (auth)/
      login/page.tsx
      signup/page.tsx
    (app)/
      discover/page.tsx
      matches/page.tsx
      chat/[matchId]/page.tsx
      profile/page.tsx
      settings/page.tsx
      layout.tsx        # Bottom navigation
    onboarding/page.tsx
    layout.tsx          # Root layout with AccessibilityProvider
    page.tsx            # Landing page

  components/
    ui/                 # shadcn components
    ProfileCard.tsx
    ChatBubble.tsx
    BottomNav.tsx
    AccessibilityProvider.tsx
    TTSButton.tsx

  lib/
    supabase.ts
    hooks/
      useAuth.ts
      useProfile.ts
      useTTS.ts
    utils.ts