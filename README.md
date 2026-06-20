# Deepak S

Full Stack Developer | React.js Developer | AI/ML Enthusiast

<div align="center">

[![Portfolio Live](https://img.shields.io/badge/Portfolio-deepak--portfolio--06.vercel.app-0ea5e9?style=for-the-badge&logo=vercel&logoColor=white)](https://deepak-portfolio-06.vercel.app/)
[![GitHub](https://img.shields.io/badge/GitHub-Deepak--1006S-181717?style=for-the-badge&logo=github)](https://github.com/Deepak-1006S)
[![React](https://img.shields.io/badge/React.js-18+-61DAFB?style=for-the-badge&logo=react&logoColor=black)](https://reactjs.org/)
[![Node.js](https://img.shields.io/badge/Node.js-LTS-339933?style=for-the-badge&logo=node.js&logoColor=white)](https://nodejs.org/)
[![MongoDB](https://img.shields.io/badge/MongoDB-Atlas-47A248?style=for-the-badge&logo=mongodb&logoColor=white)](https://mongodb.com/)
[![Deployed on Vercel](https://img.shields.io/badge/Deployed-Vercel-black?style=for-the-badge&logo=vercel)](https://deepak-portfolio-06.vercel.app/)

**A production-grade developer portfolio built with a custom dark-mode design system, 10 live-deployed projects, and zero CSS frameworks.**

🌐 **[deepak-portfolio-06.vercel.app](https://deepak-portfolio-06.vercel.app/)**

[Projects →](#-projects-showcase) · [Skills →](#-skills--tech-stack) · [Architecture →](#-architecture-overview) · [Local Setup →](#-installation--local-development)

</div>

---

## Table of Contents

- [Project Overview](#-project-overview)
- [Why This Portfolio Stands Out](#-why-this-portfolio-stands-out)
- [Key Features](#-key-features)
- [Tech Stack](#-tech-stack)
- [Architecture Overview](#-architecture-overview)
- [Folder Structure](#-folder-structure)
- [Design System](#-design-system)
- [Projects Showcase](#-projects-showcase)
- [Skills & Tech Stack](#-skills--tech-stack)
- [Installation & Local Development](#-installation--local-development)
- [Engineering Decisions](#-engineering-decisions)
- [Screenshots](#-screenshots)
- [Future Enhancements](#-future-enhancements)
- [Skills Demonstrated](#-skills-demonstrated)

---

## 🧩 Project Overview

This repository is the complete source for **Deepak S's professional developer portfolio** — a 5-page, fully responsive web application built with a handcrafted CSS design system, IntersectionObserver-driven animations, and client-side interactivity written entirely in vanilla JavaScript.

The portfolio is not a template. Every layout, animation curve, color token, and component was written from scratch. It is engineered to be maintainable and consistent across 5 separate pages without a single CSS framework or JavaScript bundler.

> **Architectural intent:** demonstrate that clean, performant UI doesn't require a framework — and that the same engineering discipline applied to the portfolio shell also shows up across 10 live-deployed projects.

---

## 💡 Why This Portfolio Stands Out

| Dimension | What Was Done |
|-----------|---------------|
| **Design System** | Custom CSS token architecture shared across 5 pages via a single `style.css` — mirrors how Atlassian, Shopify, and IBM manage design tokens in production |
| **Zero build step for the shell** | The portfolio itself runs without webpack or Vite — a deliberate choice that demonstrates understanding of when tooling is and isn't needed |
| **Animation without libraries** | IntersectionObserver stagger reveals, `requestAnimationFrame` counters, and CSS `cubic-bezier` easing — all hand-written |
| **DOM as source of truth** | Project filter reads `data-cat` attributes directly — no JavaScript state array, no framework |
| **Accessibility** | Semantic HTML5, `aria-label` on interactive elements, keyboard-navigable mobile menu |
| **100% deployment rate** | Every project linked from this portfolio is publicly live — no placeholders, no "coming soon" |

---

## ✨ Key Features

### Home Page (`index.html`)
- **Typewriter role rotator** — hand-written state machine (no library) cycles through 5 developer roles
- **Animated profile card** — live stat grid with blinking availability status indicator
- **CSS-only blob accents** — decorative `radial-gradient` shapes, zero extra DOM nodes

### About Page (`about.html`)
- **Dual vertical timeline** — Education and Internship history, shared `::before` pseudo-element track line
- **Certifications grid** — 5-card responsive layout (Full Stack, AI/ML, MongoDB, Tally Grade A, UI/UX)
- **Achievement banner** — research paper presentation highlight

### Projects Page (`projects.html`)
- **Client-side filter** — 10 projects filterable by `all`, `fullstack`, `frontend` with live result counter
- **`data-cat` attribute routing** — filter reads DOM attributes, no JavaScript state array needed
- **Animated left accent bar** — `::before` with `scaleX()` slides in on hover
- **10 live Vercel deployments** — every project links to a working demo and its source

### Skills Page (`skills.html`)
- **5-domain skill taxonomy** — Frontend Dev, UI/UX, API & Backend, Problem Solving, Tools
- **IntersectionObserver progress bars** — fills triggered on scroll enter, `1.3s cubic-bezier` transition
- **Staggered card reveals** — `90ms` per-card delay via `setTimeout` inside the observer callback
- **`requestAnimationFrame` stat counters** — ease-out cubic easing, no counter library
- **Sticky filter bar** — `position: sticky` with `backdrop-filter: blur(20px)` frosted glass
- **React Hooks spotlight** — secondary display listing all 7 hooks actively used across projects

### Contact Page (`contact.html`)
- **Clipboard API** — phone copy-to-clipboard with timed feedback text swap
- **Mailto form composer** — constructs a `mailto:` URI with pre-filled subject and encoded body
- **Subject-aware routing** — dropdown maps to human-readable email subject lines
- **Availability pulse** — green dot with CSS `box-shadow` glow animation

---

## 🔧 Tech Stack

### Portfolio Shell

| Layer | Technology |
|-------|-----------|
| Markup | HTML5 (semantic landmarks, ARIA) |
| Styling | CSS3 — Custom Properties, Grid, Flexbox, Keyframe Animations |
| Interactivity | Vanilla JavaScript ES6+ |
| Deployment | Vercel |

### Technologies Used Across Showcased Projects

| Category | Technologies |
|----------|-------------|
| **Frontend** | React.js 18, React Hooks, Context API, JSX, Vite, TypeScript |
| **Styling** | Tailwind CSS, CSS Modules, Responsive/Mobile-First Design |
| **Backend** | Node.js, Express.js, REST APIs |
| **Database** | MongoDB (Atlas Cloud) |
| **Auth** | JWT (JSON Web Tokens), Role-Based Authorization |
| **Payments** | Razorpay Payment Gateway |
| **AI Integration** | GPT-4o API — used in Interview-Ace AI for mock interviews and ATS scoring |
| **DevOps** | Vercel, Netlify, Git, GitHub, npm |
| **Design Tools** | Figma → Code handoff |

---

## 🏛 Architecture Overview

```
┌──────────────────────────────────────────────────────────────┐
│                   PORTFOLIO ARCHITECTURE                     │
├──────────────────────────────────────────────────────────────┤
│                                                              │
│   style.css  ──  Single CSS Token Layer                      │
│   (--blue, --surface, --radius, --nav-h, --shadow, …)        │
│         │                                                    │
│         ▼  linked by all 5 pages                             │
│   ┌─────────────────────────────────────────────┐            │
│   │           Page Layer                         │            │
│   │  index.html   about.html   projects.html     │            │
│   │  skills.html  contact.html                   │            │
│   └─────────────────────────────────────────────┘            │
│         │                                                    │
│         ▼  shared across all pages                           │
│   nav.js  ──  hamburger toggle · active page detection       │
│                                                              │
│   Inline JS per page (scoped, no framework):                 │
│   ├── index.html    → typewriter state machine               │
│   ├── projects.html → data-cat DOM filter + counter          │
│   ├── skills.html   → IntersectionObserver + rAF counters    │
│   └── contact.html  → Clipboard API + mailto composer        │
│                                                              │
│   Animation pipeline:                                        │
│   IntersectionObserver → classList.add → CSS transition      │
│   Counter: IntersectionObserver → requestAnimationFrame      │
│                                                              │
└──────────────────────────────────────────────────────────────┘
```

**Key architectural decisions:**

1. **No build step for the portfolio shell.** The site works by opening `index.html`. This was intentional — it demonstrates understanding of when tooling adds value versus overhead.

2. **CSS Custom Properties as a design token system.** All colors, radii, shadows, and spacing live in `:root` in a single `style.css`, giving all 5 pages visual consistency without a preprocessor or design framework.

3. **IntersectionObserver over scroll listeners.** Scroll events fire on the main thread and cause jank. IntersectionObserver fires asynchronously on the compositor thread.

4. **`data-*` attributes as filter state.** Project cards carry `data-cat="fullstack"` or `data-cat="frontend"`. The filter reads these with `getAttribute()` — the DOM is the source of truth, no state array needed.

5. **`requestAnimationFrame` for counters.** The stat counters use a hand-written `rAF` loop with an ease-out cubic formula to decelerate smoothly — same easing Chrome uses natively.

---

## 📁 Folder Structure

```
deepak-portfolio/
│
├── index.html              # Home — hero, typewriter, profile card, featured strip
├── about.html              # About — sidebar, dual timeline, certifications grid
├── projects.html           # Projects — filterable 10-project card grid
├── skills.html             # Skills — animated bars, 5-domain taxonomy, counters
├── contact.html            # Contact — form, clipboard API, availability banner
│
├── style.css               # Global design system — tokens, layout, components
├── nav.js                  # Shared nav — hamburger, active state detection
│
├── assets/
│   └── photo.jpg           # Profile photograph
│
└── public/
    └── Deepak_S_Resume.pdf # Downloadable resume
```

---

## 🎨 Design System

All visual decisions are expressed as CSS custom properties, defined once in `:root` inside `style.css`. This is the same pattern used by production design systems at companies like Atlassian, Shopify, and GitHub.

```css
/* Color Tokens */
--blue:         #3b82f6   /* Primary actions, links */
--blue-light:   #60a5fa   /* Highlighted text */
--orange:       #f97316   /* Accent, gradient endpoints */
--green:        #10b981   /* Availability, success states */
--text:         #f1f5f9   /* Primary text */
--text-muted:   #94a3b8   /* Secondary text */
--text-dim:     #475569   /* Labels, meta */
--surface:      #111827   /* Card backgrounds */
--surface-2:    #1f2937   /* Nested surfaces, progress tracks */
--border:       #1e293b   /* Default borders */
--border-2:     #334155   /* Hover-state borders */

/* Shape & Spacing Tokens */
--radius:       14px      /* Standard cards */
--radius-lg:    20px      /* Hero card */
--nav-h:        64px      /* Referenced in sticky calc() values */

/* Shadow Tokens */
--shadow:       0 8px 32px rgba(0,0,0,0.4)
--shadow-lg:    0 20px 60px rgba(0,0,0,0.5)
```

---

## 📦 Projects Showcase

All 10 projects are live. Every link below opens a working deployment.

### Full Stack — MERN

| # | Project | Stack | Live | Source |
|---|---------|-------|------|--------|
| 01 | **Enterprise Store Management System** | React · Node · Express · MongoDB · JWT | [Live ↗](https://store-management-teal.vercel.app/) | [GitHub ↗](https://github.com/Deepak-1006S/store-management-2) |
| 04 | **FlowSync — Workflow Management** | React · Context API · Hooks | [Live ↗](https://flowsync-workflow-management.vercel.app/) | [GitHub ↗](https://github.com/Deepak-1006S/Flowsync-Workflow-Management.git) |
| 09 | **Interview-Ace AI** | React · Vite · Tailwind · GPT-4o API | [Live ↗](https://interview-ace-ai-frontend-sooty.vercel.app/) | [GitHub ↗](https://github.com/Deepak-1006S/Interview-Ace-AI-frontend) |
| 10 | **Railway-X — Reservation Platform** | React · Node · Express · MongoDB · JWT · Razorpay | [Live ↗](https://railway-x.vercel.app/) | [GitHub ↗](https://github.com/Deepak-1006S/Railway-X.git) |

### Frontend / UI

| # | Project | Stack | Live | Source |
|---|---------|-------|------|--------|
| 02 | **Harry Potter Chatbot** | Vanilla JS · State Machine | [Live ↗](https://harrypotter-chatbot.vercel.app/) | [GitHub ↗](https://github.com/Deepak-1006S/harrypotter-chatbot.git) |
| 03 | **Foodie App** | React · CSS · Cart System | [Live ↗](https://foodie-app-pink.vercel.app/) | [GitHub ↗](https://github.com/Deepak-1006S/FoodieApp.git) |
| 05 | **E-Commerce Platform** | React · Cart · localStorage | [Live ↗](https://ecommerce-amh3.vercel.app/) | [GitHub ↗](https://github.com/Deepak-1006S/ecommerce.git) |
| 06 | **Real-Time Collaboration Platform** | React · Presence UI | [Live ↗](https://scale-realtime-collabration.vercel.app/) | [GitHub ↗](https://github.com/Deepak-1006S/Scale--Realtime-collabration.git) |
| 07 | **AI CRM Dashboard** | React · TypeScript · Vite | [Live ↗](https://ai-crm-dashboard-two.vercel.app/) | [GitHub ↗](https://github.com/Deepak-1006S/AI-CRM-Dashboard) |
| 08 | **AI Customer Support Platform** | React · TypeScript · Ticket System | [Live ↗](https://ai-customer-support-platform-lac.vercel.app/) | [GitHub ↗](https://github.com/Deepak-1006S/AI-customer-support-platform) |

> 10 projects. 10 live deployments. Every one verifiable in under 5 seconds.

---

## 🛠 Skills & Tech Stack

Technologies verified from actual project source code and codebase — no self-assessed percentages.

**Languages**
`JavaScript (ES6+)` `TypeScript` `HTML5` `CSS3`

**Frontend**
`React.js 18` `React Hooks` `Context API` `JSX` `Vite` `Tailwind CSS` `Responsive Design` `Mobile-First` `CSS Grid` `Flexbox`

**Backend**
`Node.js` `Express.js` `REST API Design` `JWT Authentication` `Role-Based Authorization`

**Database**
`MongoDB` `MongoDB Atlas` `NoSQL Schema Design`

**Integrations**
`GPT-4o API` `Razorpay Payment Gateway` `Clipboard API` `Fetch API` `Axios`

**Browser APIs**
`IntersectionObserver` `requestAnimationFrame` `Clipboard API` `History API`

**Tools & DevOps**
`Git` `GitHub` `Vercel` `Netlify` `Postman` `Chrome DevTools` `VS Code` `Figma` `npm`

**React Hooks Used Across Projects**
`useState` `useEffect` `useMemo` `useCallback` `useRef` `useContext` `Custom Hooks`

---

## 🛠 Installation & Local Development

The portfolio shell has no build step. Clone and open.

```bash
# Clone
git clone https://github.com/Deepak-1006S/deepak-portfolio.git
cd deepak-portfolio

# Run with any static server — pick one:

# VS Code Live Server (recommended)
# Right-click index.html → Open with Live Server

# Python
python3 -m http.server 8080

# Node
npx http-server .

# Or just open the file directly
open index.html
```

### Running a MERN Project Locally

Each MERN project has its own repo with separate `frontend/` and `backend/` directories.

```bash
# Example — Store Management System
git clone https://github.com/Deepak-1006S/store-management-2.git
cd store-management-2

# Backend
cd backend && npm install
cp .env.example .env   # fill in MONGODB_URI and JWT_SECRET
npm run dev            # Express on :5000

# Frontend (new terminal)
cd ../frontend && npm install
npm run dev            # React/Vite on :5173
```

**`.env` required keys for MERN projects:**
```env
MONGODB_URI=mongodb+srv://<user>:<pass>@cluster.mongodb.net/<dbname>
JWT_SECRET=your_secret_key
PORT=5000
NODE_ENV=development
```

---

## ⚙️ Engineering Decisions

### Why IntersectionObserver instead of scroll events?

Scroll event listeners fire on the main thread on every scroll tick and block rendering. `IntersectionObserver` is async and runs off the main thread — the browser tells you when something enters the viewport rather than you having to poll for it.

```javascript
const obs = new IntersectionObserver((entries) => {
  entries.forEach((entry) => {
    if (!entry.isIntersecting) return;
    entry.target.classList.add('reveal');
    obs.unobserve(entry.target); // fire once, then stop watching
  });
}, { threshold: 0.08, rootMargin: '0px 0px -40px 0px' });
```

### Why `requestAnimationFrame` for counters?

`setInterval` fires on a fixed clock and has no awareness of whether the browser is ready to paint. `rAF` syncs to the browser's repaint cycle — typically 60fps — which eliminates dropped frames.

```javascript
function tick(now) {
  if (!startTime) startTime = now;
  const progress = Math.min((now - startTime) / duration, 1);
  const eased = 1 - Math.pow(1 - progress, 3); // ease-out cubic
  el.textContent = Math.floor(eased * target);
  if (progress < 1) requestAnimationFrame(tick);
}
requestAnimationFrame(tick);
```

### Why DOM attributes for filter state?

Keeping filter state in a JavaScript variable requires the JS and the DOM to stay in sync. Using `data-cat` on the cards themselves means the DOM is always the source of truth — no desync possible.

```javascript
cards.forEach(card => {
  const match = category === 'all' || card.getAttribute('data-cat') === category;
  card.classList.toggle('hidden', !match);
});
```

### Why no CSS framework for the portfolio shell?

Tailwind and Bootstrap add ~50–200KB of CSS (even with purging). A hand-authored design token system with CSS custom properties delivers the same design consistency at ~8KB, loads faster, and demonstrates deeper CSS knowledge.

---

## 📸 Screenshots

**Home — Hero Section**
![Home](https://deepak-portfolio-06.vercel.app/assets/photo.jpg)

> _Full page screenshots — capture these with [Screely](https://screely.com) or [GoFullPage](https://chrome.google.com/webstore/detail/gofullpage-full-page-scre/fdpohaocaechadadgiodloanknbeoaap) and add below:_

| Page | Screenshot |
|------|-----------|
| Home — Hero | `screenshots/home.png` |
| About — Timeline | `screenshots/about.png` |
| Projects — Grid | `screenshots/projects.png` |
| Skills — Progress Bars | `screenshots/skills.png` |
| Contact — Form | `screenshots/contact.png` |
| Mobile — Nav | `screenshots/mobile.png` |

**To add screenshots:**
```bash
mkdir screenshots
# Drop your .png files here, then update the table above
```

---

## 📈 GitHub Activity

<div align="center">

[![GitHub Stats](https://github-readme-stats.vercel.app/api?username=Deepak-1006S&show_icons=true&theme=tokyonight&hide_border=true&count_private=true)](https://github.com/Deepak-1006S)

[![Top Languages](https://github-readme-stats.vercel.app/api/top-langs/?username=Deepak-1006S&layout=compact&theme=tokyonight&hide_border=true)](https://github.com/Deepak-1006S)

[![GitHub Streak](https://streak-stats.demolab.com?user=Deepak-1006S&theme=tokyonight&hide_border=true)](https://github.com/Deepak-1006S)

[![Contribution Graph](https://github-readme-activity-graph.vercel.app/graph?username=Deepak-1006S&theme=tokyo-night&hide_border=true)](https://github.com/Deepak-1006S)

</div>

---

## 🔮 Future Enhancements

| Priority | Feature | Approach |
|----------|---------|----------|
| High | **Contact form backend** | Node.js + Nodemailer or EmailJS |
| High | **Dark/Light mode toggle** | CSS class swap on `<html>` + `localStorage` |
| Medium | **Project detail pages** | Per-project case study (problem → solution → outcome) |
| Medium | **Live GitHub stats** | GitHub REST API — dynamic commit and repo counts |
| Medium | **Blog section** | Markdown-driven with a headless CMS |
| Low | **CI/CD pipeline** | GitHub Actions: lint on PR, deploy on merge to `main` |
| Low | **Analytics** | Plausible or Umami (privacy-first, no cookie banner) |
| Low | **PWA** | `manifest.json` + service worker for installable portfolio |

---

## 🧠 Skills Demonstrated

**Software Engineering Practices**
- Component-based thinking without a component framework
- Progressive enhancement — content works without JavaScript, JS adds interactivity on top
- GPU-composited animations via `transform` and `opacity` exclusively (no `top`/`left` animation)
- Single source of truth patterns — DOM attributes, CSS custom properties

**Frontend Engineering**
- CSS design token systems (production pattern at Atlassian, Shopify, GitHub)
- `IntersectionObserver` for performant scroll-triggered animations
- `requestAnimationFrame` for 60fps counter animations
- `Clipboard API` with timed UX feedback
- CSS `auto-fill` / `minmax()` responsive grid patterns
- `::before` / `::after` pseudo-elements for decorative UI (zero extra DOM nodes)
- `backdrop-filter: blur()` frosted glass on sticky elements

**Full Stack Engineering** *(demonstrated in projects)*
- RESTful API design with Express.js
- JWT authentication + role-based authorization
- MongoDB schema design
- Razorpay payment gateway integration
- GPT-4o API integration for AI-powered interview prep
- React Context API for global state management

**Accessibility & Standards**
- Semantic HTML5 (`<header>`, `<main>`, `<nav>`, `<footer>`, `<section>`)
- `aria-label` on all interactive elements
- `aria-hidden` on decorative SVGs
- Keyboard-navigable hamburger menu

---
## Professional Experience

### Full Stack Developer Intern — VIPS Tech
- Developed and maintained web applications using React.js and JavaScript
- Worked on frontend development and API integration
- Participated in project development and testing

### AI/ML Intern — VIPS Tech
- Explored machine learning concepts and data analysis
- Worked on AI-powered application workflows

### UI/UX Design Intern — VIPS Tech
- Designed responsive interfaces and user-focused experiences
- Created wireframes and design prototypes
---

## 👤 About

**Deepak S** — Full Stack & AI/ML Developer, Chennai, India

- 🎓 BCA Final Year (2027) — Sree Muthukumaraswamy College, Chennai
- 💼 AI/ML Intern · Full Stack Intern · UI/UX Design Intern — VIPS Tech
- 🏆 Technical Research Paper Presenter — Gojan School of Business and Technology
- 📜 Certifications: Full Stack Web Development · AI & Machine Learning · MongoDB · UI/UX Design · Tally Accounting (Grade A)

[![GitHub](https://img.shields.io/badge/GitHub-Deepak--1006S-181717?style=flat-square&logo=github)](https://github.com/Deepak-1006S)
[![Portfolio](https://img.shields.io/badge/Portfolio-Live-0ea5e9?style=flat-square&logo=vercel)](https://deepak-portfolio-06.vercel.app/)

---

<div align="center">
<sub>Built from scratch · Deployed on Vercel · Zero CSS frameworks · 10 live projects</sub>
</div>
