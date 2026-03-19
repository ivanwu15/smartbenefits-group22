# 🐷 SmartBenefits — HSA Gamified Learning App

> A gamified health literacy learning app that helps college students understand Health Savings Accounts (HSAs) through interactive, story-based modules.

![Status](https://img.shields.io/badge/Status-Live-brightgreen)
![License](https://img.shields.io/badge/License-MIT-green)
![UCI](https://img.shields.io/badge/UCI-INF%20172-0064A4)

**🎮 [Try the Live Demo](https://ivanwu15.github.io/smartbenefits-group22/demo/SmartBenefitsDemo.html)** &nbsp;|&nbsp; **🌐 [Project Website](https://ivanwu15.github.io/smartbenefits-group22/)** &nbsp;|&nbsp; **🎨 [Figma Prototype](https://www.figma.com/design/gQVFUtKSjuvcVmH6Ys6a0N/INF-172-Health-Literacy-App?node-id=46-78&p=f&t=00PJUWiBODkfjgm6-0)**

---

## 📋 Table of Contents

- [About](#about)
- [Target Users](#target-users)
- [Features](#features)
- [Game Modules](#game-modules)
- [Gamification Design](#gamification-design)
- [Tech Stack](#tech-stack)
- [Project Structure](#project-structure)
- [Development Roadmap](#development-roadmap)
- [Team](#team)
- [References](#references)

---

## About

Healthcare costs in the U.S. reached $5.3 trillion in 2024, yet many young adults lack the financial literacy to navigate health insurance and Health Savings Accounts (HSAs). Our research found that **87.5% of UCI undergraduates had never heard of HSAs** before taking our survey — despite HSAs being one of the most powerful tax-advantaged financial tools available to them.

**SmartBenefits** bridges this gap with a gamified, story-based learning experience that teaches:

- Healthcare insurance fundamentals (PPO vs. HDHP)
- HSA eligibility, contribution limits, and triple tax advantages
- Practical HSA usage in real-world medical expense scenarios

Unlike passive FAQs and articles, SmartBenefits follows **Alex** — a new grad navigating his first job offer — through three story-driven modules with immediate feedback, a progression system, and achievement badges.

---

## Target Users

**Undergraduate students at the University of California, Irvine** who are currently enrolled or approaching graduation.

- Often covered under parental or student health plans with limited HSA exposure
- Face complex insurance decisions at graduation with little preparation
- Have the lowest HSA participation and contribution rates among all age groups
- Need early, accessible education before encountering real financial consequences

**Research basis:** Pre-survey of 32 UCI undergraduates — 87.5% had never heard of HSAs, 60.8% felt overwhelmed by healthcare decisions, and 50% reported low confidence in understanding insurance concepts.

---

## Features

### 🎮 Gamified Learning

- **3 progressive modules** with story-driven scenarios
- **Extra Credit** advanced challenge section
- **Point system**: Recall questions (+25 pts), Apply questions (+75 pts)
- **Achievement badges**: Earn a unique badge per completed module
- **Module unlock system**: Complete each module to unlock the next

### 🐷 Interactive Mascot

- Piggy bank mascot (Alex) provides guidance and encouragement throughout
- Delivers immediate, per-option explanatory feedback after every question

### 📊 Progress Tracking

- Real-time progress bar and dot indicators per module
- My Progress dashboard with arc-circle completion visualization
- localStorage persistence — resume mid-session at any time

### 🎯 Realistic Scenarios

- Job offer health plan selection (PPO vs. HDHP)
- HSA contribution math and tax advantage calculation
- Real-world qualified expense decision-making

---

## Game Modules

### Module 1: The Offer Letter (Healthcare Basics)

- Differentiate healthcare plans (PPO, HMO, EPO, HDHP)
- Understand deductibles, premiums, and copays
- Interactive scenario: Alex receives a job offer and must choose a health plan
- **Badge earned:** 📋 Plan Pro

### Module 2: HSA Fundamentals

- HSA eligibility criteria
- Triple tax advantage (contributions, growth, withdrawals)
- Contribution limits ($4,150 individual for 2024)
- Comparison with FSAs
- **Badge earned:** 🎓 HSA Scholar

### Module 3: HSA in Action

- Qualified vs. non-qualified medical expenses
- Real-world spending decisions with Alex's HSA balance
- Long-term HSA growth strategies
- **Badge earned:** 💰 HSA Pro

### ⭐ Extra Credit

- Advanced compound growth calculation challenge
- Tests mastery of HSA investment and long-term strategy concepts

---

## Gamification Design

Based on Lander's Theory of Gamified Learning and empirical research:

| Element | Implementation |
|---|---|
| Narrative | Job offer scenario, Alex's first year of insurance decisions |
| Avatar/Mascot | 🐷 Piggy bank guide with contextual, per-option messages |
| Points | +25 recall / +75 apply questions |
| Levels | 3 modules with progressive difficulty + Extra Credit |
| Progress | Per-step dot indicators + arc-circle overall completion |
| Feedback | Immediate per-option explanatory feedback |
| Achievements | Module completion badges with unique names |
| Final Results | Dynamic 4-scenario result page based on EC completion |

**Learning Loop**: Scenario Presentation → Answer Selection → Immediate Feedback → Points → Module Badge → Unlock Next

---

## Tech Stack

| Layer | Technology |
|---|---|
| Frontend | Vanilla HTML, CSS, JavaScript (single-page app) |
| Fonts | Google Fonts (Inter, Playfair Display) |
| State | localStorage persistence via custom STATE object |
| Assets | Base64-encoded inline SVG mascots (assets.js) |
| Deployment | GitHub Pages (`/docs` subfolder) |
| Version Control | Git + GitHub |

> The demo is built as a standalone single-file HTML app — no build tools or frameworks required. Just open `SmartBenefitsDemo.html` alongside `assets.js` in any browser.

---

## Project Structure

```
smartbenefits-group22/
├── docs/                          # GitHub Pages root
│   ├── index.html                 # Project portfolio website
│   ├── demo/
│   │   ├── SmartBenefitsDemo.html # Main interactive demo (~1MB)
│   │   └── assets.js              # Base64 mascot/logo assets (~784KB)
│   └── web/                       # Portfolio website images
│       ├── hf-home.png            # Hi-fi screenshots
│       ├── lf-home.png            # Lo-fi wireframes
│       ├── persona.png            # User persona
│       ├── survey result.png      # Survey data
│       └── ...
├── src/                           # React prototype (Sprint 2)
├── public/
├── package.json
├── vite.config.js
└── README.md
```

---

## Development Roadmap

### Sprint 1 (Weeks 1–2) ✅
- [x] User research — pre-HSA survey (n=32 undergraduates)
- [x] Student interviews (10-minute sessions)
- [x] Gamified learning literature review
- [x] Requirements document

### Sprint 2 (Weeks 3–4) ✅
- [x] Lo-fi wireframes (6 screens)
- [x] Mid-fi interactive wireframe prototype
- [x] User flow diagram
- [x] Brand identity and design system

### Sprint 3 (Weeks 5–6) ✅
- [x] Hi-fi Figma prototype
- [x] Full SmartBenefits demo — all 3 modules
- [x] Extra Credit section
- [x] Gamification system (points, badges, streaks)
- [x] My Progress dashboard
- [x] Final Results page (4 dynamic scenarios)

### Sprint 4 (Week 7) ✅
- [x] Usability testing
- [x] GitHub Pages deployment
- [x] Final report and video presentation

### Sprint 5 (Week 10) ✅ Shipped
- [x] Full demo polish and bug fixes
- [x] Project portfolio website (`docs/index.html`)
- [x] Live deployment at GitHub Pages

---

## Team

**Group 22** — University of California, Irvine · INF 172 · Winter 2026

| Name | Role | Responsibilities |
|---|---|---|
| Lisa Wu | Project Manager | Team coordination, timeline, requirements, presentations |
| Patricia Abenoja | Design Lead | Wireframes, Figma prototype, visual design |
| Sammi Li | Design Lead | Wireframes, Figma prototype, visual design |
| Yifan Wu | Tech Lead | Demo development, project website, GitHub deployment |
| Samantha Hong | Content Lead | Gamified learning research, HSA content strategy |

---

## References

- Casagrande, S. S., & Lawrence, J. M. (2025). Trends in delaying and forgoing medical care due to cost. *BMJ Open Diabetes Research & Care*.
- Choi, A. Y., & Rosso, R. J. (2025). Health Savings Accounts (HSAs). *Congress.gov*.
- Hartman, M., Martin, A. B., Lassman, D., & Catlin, A. (2026). National health care spending increased 7.2 percent in 2024. *Health Affairs*.
- Johnson, D., Deterding, S., Kuhn, K. A., et al. (2016). Gamification for health and wellbeing: a systematic review. *Internet Interventions*.
- Kaya, O. S., & Ercag, E. (2023). The impact of challenge-based gamification on students' learning outcomes. *Education and Information Technologies*.
- Khoshnoodifar, M., et al. (2023). Effectiveness of gamification in enhancing learning and attitudes. *JAMP, 11*(4), 230–239.
- Machireddy, J. R. (2021). Data-Driven Insights: Analyzing the Effects of Underutilized HRAs and HSAs. *JBAI*.
- Waters, A. R., et al. (2022). Health insurance literacy among AYA cancer survivors. *Supportive Care in Cancer*.

---

## License

This project is for educational purposes as part of INF 172 at the University of California, Irvine.
