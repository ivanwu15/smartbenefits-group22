# 🐷 SmartBenefits — HSA Gamified Learning App

> A gamified health literacy learning app that helps college students understand Health Savings Accounts (HSAs) through interactive, story-based modules.

![Status](https://img.shields.io/badge/Status-In%20Development-yellow)
![React](https://img.shields.io/badge/React-18.2-blue)
![License](https://img.shields.io/badge/License-MIT-green)

---

## 📋 Table of Contents

- [About](#about)
- [Target Users](#target-users)
- [Features](#features)
- [Game Modules](#game-modules)
- [Gamification Design](#gamification-design)
- [Tech Stack](#tech-stack)
- [Getting Started](#getting-started)
- [Project Structure](#project-structure)
- [Development Roadmap](#development-roadmap)
- [Team](#team)
- [References](#references)

---

## About

Healthcare costs in the U.S. reached $5.3 trillion in 2024, yet many young adults lack the financial literacy to navigate health insurance and Health Savings Accounts (HSAs). Existing HSA education platforms primarily target users who already have employer-sponsored high-deductible health plans, leaving a gap for college students and young adults.

**SmartBenefits** bridges this gap with a gamified, story-based learning experience that teaches:
- Healthcare insurance fundamentals
- HSA eligibility, contribution limits, and tax advantages
- Practical next steps for exploring and participating in HSAs

Unlike passive FAQs and articles, SmartBenefits uses interactive narrative scenarios, immediate feedback, and a progression system to make learning engaging and actionable.

---

## Target Users

**Undergraduate students at the University of California, Irvine** who are currently enrolled or approaching graduation.

- Often covered under parental or student health plans with limited HSA exposure
- Face complex insurance decisions at graduation with little preparation
- Have the lowest HSA participation and contribution rates among all age groups
- Need early, accessible education before encountering real financial consequences

---

## Features

### 🎮 Gamified Learning
- **3 progressive modules** with increasing difficulty (Easy → Medium → Hard)
- **Point system**: Recall questions (+25 pts), Apply questions (+75 pts)
- **Streak bonuses**: 3+ correct answers = double points
- **Rank progression**: Newcomer → Health Explorer → Benefits Pro → HSA Master
- **Module unlock system**: Complete each module to unlock the next

### 🐷 Interactive Mascot
- Piggy bank mascot provides guidance and encouragement throughout
- Delivers immediate explanatory feedback after every question

### 📊 Progress Tracking
- Real-time progress bars per module
- Overall game completion percentage
- Personal stats dashboard (points, streak, modules completed)

### 🎯 Realistic Scenarios
- Job offer health plan selection
- HSA contribution planning with interactive slider
- Real-time tax savings calculator

---

## Game Modules

### Module 1: Intro to Healthcare (Easy · 0–150 pts)
- Differentiate healthcare plans (employer, Medicaid, Medicare, HDHP, etc.)
- Understand copayments, deductibles, and premiums
- Interactive scenario: choose a health plan for a new job

### Module 2: HSAs — What Are They? (Medium · 150–300 pts)
- HSA eligibility criteria (HDHP, no Medicare, not a dependent, etc.)
- Contribution limits ($4,300 individual / $8,550 family for 2025)
- Triple tax advantage and fund rollover rules
- Qualified medical expenses

### Module 3: HSAs — Sign Me Up! (Hard · 300–450 pts)
- Apply all knowledge in comprehensive scenarios
- Personalized next steps to explore HSAs further
- Resources: research providers, check eligibility, plan contributions, talk to benefits advisor

---

## Gamification Design

Based on Lander's Theory of Gamified Learning and empirical research from Guilan University of Medical Sciences:

| Element | Implementation |
|---------|---------------|
| Narrative | Job offer scenario, health plan decisions |
| Avatar/Mascot | 🐷 Piggy bank guide with contextual messages |
| Points | +25 recall / +75 apply / streak bonus 2× |
| Levels | 3 modules with progressive difficulty |
| Progress Bars | Per-module % and overall completion |
| Feedback | Immediate explanatory feedback per question |
| Challenge | Timed sessions (~5-8 min), increasing complexity |
| Rank System | 4-tier progression based on total points |

**Learning Loop**: Scenario Choice → Immediate Feedback → Checkpoint Quiz → Points/Level Progression

---

## Tech Stack

| Layer | Technology |
|-------|-----------|
| Frontend | React 18 |
| Styling | CSS-in-JS (inline styles) |
| Fonts | Google Fonts (DM Sans, Playfair Display, DM Mono) |
| Build Tool | Vite |
| Deployment | GitHub Pages |
| Version Control | Git + GitHub |

---

## Getting Started

### Prerequisites

- [Node.js](https://nodejs.org/) (v18 or higher)
- [Git](https://git-scm.com/)
- A GitHub account

### Installation

```bash
# 1. Clone the repository
git clone https://github.com/YOUR_USERNAME/smartbenefits.git
cd smartbenefits

# 2. Install dependencies
npm install

# 3. Start development server
npm run dev
```

Open `http://localhost:5173` in your browser.

### Build for Production

```bash
npm run build
```

### Deploy to GitHub Pages

```bash
npm run deploy
```

---

## Project Structure

```
smartbenefits/
├── public/
│   └── favicon.ico
├── src/
│   ├── components/
│   │   ├── Nav.jsx              # Navigation bar (Home, All Modules, My Progress)
│   │   ├── ModuleCard.jsx       # Module selection card with status badges
│   │   ├── Mascot.jsx           # Piggy bank mascot with speech bubble
│   │   ├── CircleProgress.jsx   # Circular progress ring
│   │   ├── ProgressBar.jsx      # Linear progress bar
│   │   ├── PointsPopup.jsx      # Points animation overlay
│   │   └── Button.jsx           # Reusable button component
│   ├── screens/
│   │   ├── Home.jsx             # Dashboard with stats and module cards
│   │   ├── AllModules.jsx       # Module overview list
│   │   ├── MyProgress.jsx       # Progress stats and completed modules
│   │   ├── module1/
│   │   │   ├── Scenario.jsx     # Job offer health plan choice
│   │   │   ├── Quiz.jsx         # HDHP recall question
│   │   │   ├── Slider.jsx       # HSA contribution slider
│   │   │   └── Result.jsx       # Module 1 completion
│   │   ├── module2/
│   │   │   ├── Intro.jsx        # Module 2 learning objectives
│   │   │   └── Quiz.jsx         # HSA eligibility question
│   │   └── module3/
│   │       ├── Intro.jsx        # Final challenge overview
│   │       ├── Final.jsx        # Completion + rank earned
│   │       └── NextSteps.jsx    # Resources and action items
│   ├── App.jsx                  # Main app with routing and state
│   ├── main.jsx                 # Entry point
│   └── index.css                # Global styles
├── docs/
│   ├── wireframe.html           # Interactive wireframe prototype
│   ├── userflow.html            # User flow diagram
│   ├── project-proposal.pdf     # Project proposal document
│   └── gamified-learning-research.pdf
├── package.json
├── vite.config.js
└── README.md
```

---

## Development Roadmap

### Sprint 1 (Weeks 1–2) ✅
- [x] Requirements document
- [x] User research (surveys, interviews)
- [x] Gamified learning research

### Sprint 2 (Weeks 3–4) ✅
- [x] Lo-fi wireframes
- [x] Mid-fi wireframes
- [x] Interactive wireframe prototype
- [x] User flow diagram
- [x] Brand identity

### Sprint 3 (Weeks 5–6) 🔄
- [ ] Hi-fi prototype in Figma
- [ ] React project setup
- [ ] Component development
- [ ] Module 1 implementation
- [ ] Module 2 implementation
- [ ] Module 3 implementation

### Sprint 4 (Week 7)
- [ ] Final testing and polish
- [ ] GitHub Pages deployment
- [ ] Final report and video

---

## Team

**Group 22** — University of California, Irvine

| Role | Responsibilities |
|------|-----------------|
| Lead | Team coordination, requirements docs, presentation |
| UI/UX | Wireframes, prototypes, visual design |
| CTO | Project website, code implementation |
| Research | Gamified learning research, content design |

---

## References

- Casagrande, S. S., & Lawrence, J. M. (2025). Trends in delaying and forgoing medical care due to cost. *BMJ Open Diabetes Research & Care*.
- Choi, A. Y., & Rosso, R. J. (2025). Health Savings Accounts (HSAs). *Congress.gov*.
- Khoshnoodifar, M., et al. (2023). Effectiveness of gamification in enhancing learning and attitudes. *JAMP, 11*(4), 230–239.
- Kaya, O. S., & Ercag, E. (2023). The impact of challenge-based gamification on students' learning outcomes. *Education and Information Technologies*.
- Machireddy, J. R. (2021). Data-Driven Insights: Analyzing the Effects of Underutilized HRAs and HSAs. *JBAI*.
- Waters, A. R., et al. (2022). Health insurance literacy among AYA cancer survivors. *Supportive Care in Cancer*.

---

## License

This project is for educational purposes as part of a university course at UC Irvine.
#   s m a r t b e n e f i t s - g r o u p 2 2  
 