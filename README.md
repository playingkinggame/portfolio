# A Yathin Kumar — AI/ML Portfolio

A single-page, cyberpunk-themed personal portfolio website for **A Yathin Kumar**, a B.Tech CSC (AI-ML) student at VIT Chennai. Built entirely with vanilla HTML, CSS, and JavaScript — no frameworks, no build step.

🔗 **Live repo:** [github.com/playingkinggame/portfolio](https://github.com/playingkinggame/portfolio)

---

## ✨ Features

- **Animated splash/intro screen** — 3D rotating wireframe cubes and particle network rendered on `<canvas>`, with a typewriter tagline effect.
- **Custom cursor** — glowing dot-and-ring cursor that reacts to hoverable elements (disabled automatically on touch devices).
- **Six interactive tabs (SPA-style, no page reloads):**
  | Tab | Description |
  |---|---|
  | `01. Home` | Hero intro, quick-stat cards, top skills, languages spoken, education & contact |
  | `02. Projects` | Browsable project list (JARVIS, Voice Recognition Engine, TTS Module, AI Dashboard GUI) with animated "AI core" visual and feature/stat breakdown |
  | `03. Skills` | Skill bars by category (Languages, Web Dev, AI/ML Tools, Dev Tools), a learning roadmap, education timeline, and achievements |
  | `04. Bio` | About section, personality traits, contact cards (call / email / maps), a "quick message" form, and languages spoken |
  | `05. GitHub` | GitHub-style stats, a mock contribution heatmap, repo cards, and social links |
  | `06. Terminal` | A playable fake CLI (`help`, `about`, `skills`, `projects`, `contact`, `education`, `goals`, `jarvis`, `clear`) |
- **Live IST clock** in the navbar and footer.
- **Animated background network** of connected particles that respond to mouse movement (desktop only).
- **Fully responsive** — dedicated layouts and a slide-out mobile nav drawer for tablet/mobile breakpoints (1024px / 768px / 480px).
- **Google Sign-In integration** — lets a signed-in user edit and persist profile fields (name, phone, location, bio) via a small backend API.

## 🧱 Tech Stack

- **Frontend:** HTML5, CSS3 (custom properties, Grid/Flexbox, keyframe animations), vanilla JavaScript, HTML5 Canvas
- **Fonts:** [Orbitron](https://fonts.google.com/specimen/Orbitron), [Space Mono](https://fonts.google.com/specimen/Space+Mono), [Syne](https://fonts.google.com/specimen/Syne) (via Google Fonts)
- **Auth:** Google Identity Services (Google Sign-In)
- **Backend (optional, separate service):** A REST API for auth + profile persistence, expected at the URL configured in `window.PORTFOLIO_API_BASE`

## 📁 Project Structure

```
.
├── index.html      # Entire site — markup, styles, and scripts in one file
├── robots.txt      # Search-engine crawl rules
└── sitemap.xml     # Sitemap for SEO
```

## 🚀 Getting Started

This is a static site with no build tooling required.

1. Clone the repo:
   ```bash
   git clone https://github.com/playingkinggame/portfolio.git
   cd portfolio
   ```
2. Open `index.html` directly in a browser, or serve it locally:
   ```bash
   python3 -m http.server 8000
   ```
3. Visit `http://localhost:8000`.

### Optional: connecting the backend

The Google Sign-In / profile-editing feature calls a backend API. Point the site at your backend by setting `window.PORTFOLIO_API_BASE` in `index.html` (defaults to `http://localhost:4000` if unset), and configure your own Google OAuth `client_id`. Without a backend running, sign-in will simply fail gracefully with a toast notification — the rest of the site works fully offline.

## 🛠️ Customization

Most personal content (name, project descriptions, skills, contact details, social links) lives directly in the `PD` (project data) object and the HTML markup inside `index.html` — search for the relevant tab section (`t1`–`t6`) to edit it.

## 📄 License

© 2026 A Yathin Kumar — All rights reserved.