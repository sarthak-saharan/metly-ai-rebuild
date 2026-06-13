# Metly — Pharma Intelligence Platform

A two-page interactive prototype for [Metly](https://metly.ai), a pharma intelligence SaaS that monitors competitive signals across BD, CI, strategy, medical affairs, commercial, and market access teams.

**Live site → [sarthak-saharan.github.io/metly-ai-rebuild](https://sarthak-saharan.github.io/metly-ai-rebuild)**

---

## Pages

### `index.html` — Landing page
Recreates the Metly marketing site with:
- Rotating hero headline animation
- "See Metly in Action" CTA linking to the demo
- Social proof logos (AZ, Roche, Pfizer, etc.)
- Seny the mascot with floating animation and speech bubble

### `metly-live-intelligence.html` — Role-based demo
A personalised intelligence demo with a 3-step quiz:
1. **Role selection** — BD Director, CI Lead, VP Strategy, Medical Affairs, Brand Director, Market Access Director
2. **Challenge picker** — role-specific pain points
3. **TA selection** — therapeutic area (typed or from chips)

After the quiz, a tailored results page shows simulated intelligence cards (clinical trials, competitive signals, regulatory events) framed through the lens of the user's role and challenge.

---

## Stack

Vanilla HTML/CSS/JS — no frameworks, no build step. Single-file pages with Google Fonts (Inter + Fraunces).

Assets:
- `metly-logo.png` — Metly wordmark
- `Pip.png` — Seny the mascot (1254×1254 PNG)

---

## Local dev

```bash
npx serve -p 4321 .
```

Open `http://localhost:4321`.

---

## Hosting

Hosted on GitHub Pages from the `main` branch root. To update, push to `main` and Pages redeploys automatically.
