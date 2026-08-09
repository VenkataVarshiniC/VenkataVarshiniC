# Venkata Varshini Chilukamarri — Portfolio

A personal portfolio site for **Venkata Varshini Chilukamarri** — Business Analyst, Strategy & Analytics — built to showcase business analysis, financial modeling, and AI strategy work through detailed case studies rather than a static resume.

**Live site:** _add your deployed URL here_
**Resume:** [View Resume](https://drive.google.com/file/d/15zo_ajf11Ir13OX7rUYxxm2_62JjSZjn/view?usp=sharing)

---

## Overview

This is a single-page React portfolio structured around a "consultant's casebook" narrative — every project is framed as **Problem → Analysis → Insight → Outcome**, rather than a plain list of bullet points. The design system pairs a warm cream/brass editorial palette with serif display type (Fraunces) and monospace labels (IBM Plex Mono), aiming for a look closer to a case-study document than a typical developer portfolio template.

## Sections

| Section | What it covers |
|---|---|
| **Hero** | Positioning statement + credibility strip (school, fellowship, hackathon placement, GPA) |
| **How I Create Impact** | Four flip cards (Structure / Analyze / Model / Influence) — front shows the principle, back reveals how it's applied in practice |
| **About** | Short narrative bio |
| **Experience** | Impact Consulting Fellowship (Le Chic Miami client engagement) and Capstone Initiative, each broken into approach steps, outcome bullets, and a lesson learned |
| **Selected Work** | Three flagship case studies with expandable "read the full case study" narratives: <br>• **Ledger** — BNPL profitability & risk platform ($470K modeled improvement) <br>• **Strategic Decision Intelligence Engine (SDIE)** — investment decision framework, back-tested against Blockbuster's 2000 Netflix decision <br>• **AI Adoption Paradox** — causal analysis of what actually predicts AI ROI (R² = 0.886) |
| **Leadership** | MDOT × Deloitte case competition, XR Social BuildFest (1st place), XR Club, Rewriting the Code |
| **By the Numbers** | Aggregate impact metrics across all projects |
| **Skills** | Business Analysis, Strategy & Finance, Analytics, AI & Tools |
| **Education** | UMD Smith (M.S. Information Systems & AI, Terrapin Scholar) and Keshav Memorial Institute of Technology |
| **Credentials** | Honors (Terrapin Scholar) and certifications (HackerRank SQL Advanced, Harvard Business Publishing, IBM, Forage/BCG, Anthropic, LinkedIn Learning) |
| **Contact** | LinkedIn, GitHub, email, resume download |

## Features

- **3D flip cards** for the "How I Create Impact" pillars — click or tap to flip, keyboard-accessible (Enter/Space)
- **Expandable case studies** — each project's Problem/Analysis/Insight/Outcome narrative toggles open without leaving the page
- **Scroll-triggered reveal animations** via `IntersectionObserver`
- **Sticky, blur-backed navigation** that condenses into a mobile menu below 860px
- Fully responsive down to small mobile viewports
- No external UI framework — plain CSS with a token-based design system (custom properties for color, spacing, radius, shadow)

## Tech Stack

- **React** (function components + hooks: `useState`, `useEffect`, `useRef`)
- **Plain CSS** via a single embedded `<style>` block using CSS custom properties
- **Google Fonts** — Fraunces (serif display), Inter (body/sans), IBM Plex Mono (labels/data)
- No build-tool-specific dependencies — works with Vite, Create React App, or Next.js with minimal wrapping

## Getting Started

This repo currently ships the portfolio as a single component (`Portfolio.jsx`). To run it locally with [Vite](https://vitejs.dev/):

```bash
# 1. Scaffold a Vite + React app (skip if you already have one)
npm create vite@latest my-portfolio -- --template react
cd my-portfolio

# 2. Drop this file in as the app's entry component
#    src/Portfolio.jsx

# 3. Render it from src/main.jsx
#    import Portfolio from "./Portfolio";
#    ReactDOM.createRoot(document.getElementById("root")).render(<Portfolio />);

# 4. Install dependencies and run
npm install
npm run dev
```

Then open `http://localhost:5173`.

## Customizing Content

All copy lives in typed data arrays at the top of `Portfolio.jsx` — no need to touch the JSX or CSS to update content:

| Constant | Controls |
|---|---|
| `PILLARS` | The four flip cards in "How I Create Impact" |
| `PROJECTS` | Selected Work case studies (metrics, flow steps, story beats) |
| `EXPERIENCE` | Work experience entries |
| `LEADERSHIP` | Leadership & professional engagement cards |
| `NUMBERS` | "By the Numbers" stat grid |
| `SKILLS` | Skills grid, grouped by category |
| `EDUCATION` | Education cards |
| `CERTIFICATIONS` / `HONORS` | Credentials section |
| `ABOUT_PARAGRAPHS` | About section copy |

Update the constants at the top of the file (`RESUME_VIEW_URL`, `LINKEDIN_URL`, `GITHUB_URL`, `EMAIL`) to point to your own links.

## Deployment

This is a static React app, so it deploys cleanly to any static host:

- **Vercel / Netlify** — connect the repo, framework preset "Vite" (or "Create React App"), default build command
- **GitHub Pages** — build with `npm run build`, then deploy the `dist/` (Vite) or `build/` (CRA) folder using [`gh-pages`](https://www.npmjs.com/package/gh-pages) or a GitHub Actions workflow

## License

Personal portfolio content — feel free to use the code structure as a template, but please don't reuse the personal content, project narratives, or metrics as your own.

## Contact

- **LinkedIn:** [venkata-varshini-chilukamarri](https://www.linkedin.com/in/venkata-varshini-chilukamarri-62b1782b7/)
- **GitHub:** [@VenkataVarshiniC](https://github.com/VenkataVarshiniC)
- **Email:** venkatavarshinic@gmail.com
