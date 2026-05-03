#  StudyAI — Your Intelligent Study Companion

A beautiful, production-grade student productivity app built with React. Manage assignments, track attendance, plan study sessions, and get AI-powered academic help — all in one sleek dark-themed mobile interface.

---

##  Features

| Feature | Description |
|---|---|
|  **Assignment Tracker** | Add, prioritize, and complete assignments with deadlines |
|  **Attendance Monitor** | Track attendance per subject with percentage calculations |
|  **Study Planner** | Manage study tasks with priority levels and durations |
|  **AI Chat Assistant** | Ask anything academic — powered by Claude AI |
|  **Daily Streak System** | Earn streaks by completing all tasks every day |
|  **Celebration Overlay** | Full-screen confetti celebration when all tasks are done |
|  **Google OAuth Login** | Real Google account chooser via Google Identity Services |
|  **Premium Dark UI** | Glassmorphism design with smooth animations throughout |

---

##  Preview

> Dark-themed mobile UI (max-width 480px) with purple/cyan gradient accents, glassmorphism cards, and fluid animations.

---

##  Getting Started

### Prerequisites

- Node.js 18+ installed
- A Google Cloud account (for Google login — free)

### Installation

```bash
# Clone the repository
git clone https://github.com/YOUR_USERNAME/StudyAI.git
cd StudyAI

# Install dependencies
npm install

# Start the development server
npm start
```

Then open [http://localhost:3000](http://localhost:3000) in your browser.

> If using **Vite** instead of Create React App:
> ```bash
> npm run dev
> ```
> Then open [http://localhost:5173](http://localhost:5173)

StudyAI/
├── StudentAI.jsx        # Complete single-file React app
├── README.md            # This file
└── package.json         # Dependencies (if applicable)
```

> This is a single-file React app. All components, styles, and logic live in `StudentAI.jsx` for simplicity.

---

##  AI Assistant Setup

The in-app AI chat is powered by the **Anthropic Claude API**.

1. Get an API key at [https://console.anthropic.com](https://console.anthropic.com)
2. In `StudentAI.jsx`, find the `AIChat` component and add your key to the API call headers:

```js
headers: {
  "x-api-key": "YOUR_ANTHROPIC_API_KEY",
  ...
}
```

>  Never commit your API key to a public repository. Use environment variables in production.

---

## 🔥 Streak System

- Complete **all assignments + all study tasks** in a day → streak increases by 1
- Leave any task incomplete → streak resets next day
- Current streak is shown on the Dashboard and Sidebar
- A premium celebration overlay fires with confetti when you hit 100% completion

---

## 🛠 Tech Stack

- **React 18** — UI framework
- **Google Identity Services (GIS)** — OAuth 2.0 login
- **Anthropic Claude API** — AI chat assistant
- **CSS-in-JS** — All styles via `<style>` tag with CSS variables
- **Google Fonts** — Syne (display) + DM Sans (body)

---

## Recommended `package.json`

If starting from scratch with Create React App:

```json
{
  "name": "studyai",
  "version": "1.0.0",
  "dependencies": {
    "react": "^18.2.0",
    "react-dom": "^18.2.0",
    "react-scripts": "5.0.1"
  },
  "scripts": {
    "start": "react-scripts start",
    "build": "react-scripts build"
  }
}
```

Or with Vite:

```json
{
  "name": "studyai",
  "version": "1.0.0",
  "dependencies": {
    "react": "^18.2.0",
    "react-dom": "^18.2.0"
  },
  "devDependencies": {
    "@vitejs/plugin-react": "^4.0.0",
    "vite": "^5.0.0"
  },
  "scripts": {
    "dev": "vite",
    "build": "vite build"
  }
}
```

---

## Deploying to Production

### Vercel (recommended — free)

```bash
npm install -g vercel
vercel
```

### Netlify

```bash
npm run build
# Drag the /build folder to https://app.netlify.com/drop
```

After deploying, add your production URL to **Authorized JavaScript origins** in Google Cloud Console.

---

## 📄 License

MIT — free to use, modify, and distribute.

---

## 🙌 Credits

Built with ❤️ using React and Claude AI by Anthropic.
