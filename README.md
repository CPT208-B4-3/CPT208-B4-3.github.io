# Bridge of Time

**CPT208 Human-Centric Computing | Group B4-3 | XJTLU AY2025-26 S2**

Bridging Generations Through Playful Shared Experiences

## About

Bridge of Time is a mobile web application designed to strengthen emotional bonds between grandparents and grandchildren through playful, culturally-rooted shared activities during family gatherings such as the Chinese New Year's Eve dinner.

**Topic**: B4 - Relation between Generations

## Live URLs

| Resource | URL |
|----------|-----|
| Portfolio | https://cpt208-b4-3.github.io/ |
| Interactive Prototype | https://cpt208-b4-3.github.io/prototype/ |

## Core Features

1. **Family Stories** — Voice-recorded intergenerational storytelling
2. **Cook Together** — Collaborative step-by-step dumpling recipe with role-based tasks
3. **Traditions Quiz** — Cultural knowledge quiz where grandparents are the experts
4. **Memory Album** — Timeline-based family photo collection

## Tech Stack

### Prototype (React App)
- **Framework**: React 18 + TypeScript
- **Build Tool**: Vite 6
- **Styling**: Tailwind CSS 4
- **State Management**: React Context (font accessibility) + component-level useState
- **Deployment**: GitHub Pages (static)

### Portfolio (Static Site)
- **Stack**: Pure HTML + CSS + JavaScript
- **Fonts**: Google Fonts (Playfair Display, Inter)
- **Hosting**: GitHub Pages

## Local Development

### Prerequisites
- Node.js 18+
- npm 9+

### Running the Prototype Locally

```bash
cd cpt208code
npm install
npm run dev
```

The dev server starts at `http://localhost:5173/prototype/`

### Building for Production

```bash
npm run build
```

Output goes to `dist/` — copy contents to the `prototype/` folder in this repo to deploy.

## Project Structure

```
.
├── index.html          # Portfolio main page
├── style.css           # Portfolio styles
├── script.js           # Portfolio interactions
├── prototype/          # Built React app (deployed)
│   ├── index.html
│   └── assets/
├── ai-logs/            # AI coding prompts documentation
│   └── README.md
└── README.md           # This file
```

## Team

| Member | Student ID | Role |
|--------|-----------|------|
| Haoyu Huang | 2254070 | UI Design & Development |
| Yilang Zhou | 2362835 | Documentation |
| Huixin Zhang | 2360890 | Video & Survey Design |
| Mingze Yin | 2360890 | Literature Research |

## AI Tools Used

| Tool | Usage |
|------|-------|
| Claude (Anthropic) | Vibe coding React prototype components, accessibility implementation, deployment assistance |
| Figma | Wireframing and mid-fidelity prototype design |

All AI usage is documented in detail in the [`/ai-logs`](./ai-logs/) folder.

## License

Academic project — Xi'an Jiaotong-Liverpool University, 2026.
