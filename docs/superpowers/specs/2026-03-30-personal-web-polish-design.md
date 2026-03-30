# Personal Web Polish Design
**Date:** 2026-03-30
**Status:** Approved

## Overview

Polish the existing `index.html` personal website for Harris Yang by filling in real content from the resume, selecting top 4 featured projects, and adding a dedicated resume page.

---

## 1. Hero Section

**Changes to `index.html`:**

- **Label:** `PhD Researcher & AI Engineer`
- **Heading (`h1`):** `Harris Yang`
- **Tagline (`p`):** "PhD candidate at the University of Toronto studying how AI safety is practiced in the real world. I build LLM systems, teach analytics, and occasionally release rap albums."
- **CTA buttons (3):**
  1. `View My Work` → `#projects` (existing)
  2. `Resume` → `resume.html` (new, `btn-secondary`)
  3. `Get In Touch` → `#contact` (existing, `btn-secondary`)

---

## 2. About Me Section

**Replace placeholder text with two paragraphs:**

> I'm a PhD student in Information at the University of Toronto, where I research how LLM safety is understood and practiced by engineers in enterprise and start-up environments. My work bridges academic AI safety frameworks and the messy realities of production deployment — studying how practitioners' mental models shape the safety decisions they actually make.

> Outside academia, I work as an AI Engineer & Consultant at Maclear Data Solutions, building LLM-powered systems for financial regulators and European banks. I also teach at the University of Waterloo, where I redesigned the AFM 346 curriculum around AI and agentic systems — a course now adopted as a program-wide requirement starting 2027.

**Skills grid (4 items):**

| Title | Description |
|---|---|
| AI Researcher | LLM safety, practitioner studies, mixed-methods research |
| ML Engineer | Multi-agent pipelines, fine-tuning, production LLM systems |
| Educator | Teaching predictive analytics & AI at the University of Waterloo |
| Rapper | 6 remix albums on Spotify and NetEase Music |

---

## 3. Featured Projects

Replace the 2 placeholder cards with 4 real project cards. No project images exist; use the existing `project-placeholder` div style.

### Project 1 — LLM Safety Practitioner Engagement
- **Org:** University of Toronto | 12/2025 – Ongoing
- **Description:** Mixed-methods study examining how LLM safety is practiced across enterprise and start-up contexts. Investigates the gap between academic frameworks and real-world deployment decisions.
- **Tags:** `LLM Safety` `Mixed Methods` `University of Toronto`

### Project 2 — Automated Invoice Processing Pipeline
- **Org:** Maclear Data Solutions | 09/2025 – 03/2026
- **Description:** Multi-agent LLM pipeline on Azure automating financial invoice processing for enterprise clients. Includes OCR, dynamic schema determination, and human-in-the-loop checkpoints in a CI/CD framework.
- **Tags:** `Multi-agent LLM` `Azure` `CI/CD` `OCR`

### Project 3 — LLM Applications Survey
- **Org:** University of Waterloo | 05/2024 – Ongoing
- **Description:** Survey study examining how university students adopt and perceive LLMs in academic settings. Findings informed curriculum redesign at the University of Waterloo.
- **Tags:** `Survey Research` `LLM Adoption` `Education`

### Project 4 — Financial Scenario Generation Model
- **Org:** Maclear Data Solutions | 04/2023 – 10/2023
- **Description:** LSTM-VAE model for financial time series reconstruction and stress testing. Used to generate risk scenarios for portfolio evaluation and train a reinforcement learning trading agent.
- **Tags:** `LSTM-VAE` `Time Series` `Reinforcement Learning` `Finance`

---

## 4. Resume Page (`resume.html`)

**New file:** `resume.html`

- Shares the same CSS variables, fonts, and header/footer structure as `index.html`
- Nav links: About (→ `index.html#about`), Projects (→ `index.html#projects`), Contact (→ `index.html#contact`), Resume (active, current page)
- Page body:
  - Section heading: "Resume"
  - "Download Resume" button linking to `resume/resume_260330.pdf` (opens in new tab / triggers download)
  - Full-height `<iframe>` embedding `resume/resume_260330.pdf`

**Nav update in `index.html`:**
- Add `Resume` link pointing to `resume.html` alongside the existing About / Projects / Contact links

---

## 5. Misc Fixes

- Fix the broken `alt` attribute on the about image (`alt="Who forgets to put a picture here?""` has an extra `"`)
- Update contact email from `your.email@example.com` to `harris.yang@mail.utoronto.ca`
- Update footer copyright year from 2025 to 2026

---

## Files Changed

| File | Change |
|---|---|
| `index.html` | Hero, About Me, Featured Projects, nav, contact email, footer year |
| `resume.html` | New file — resume page with embedded PDF |
