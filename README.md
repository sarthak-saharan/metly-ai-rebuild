# Metly — AI-First Product Experiment

**Built by:** Sarthak Saharan, AI Product Manager  
**Live demo → [sarthak-saharan.github.io/metly-ai-rebuild](https://sarthak-saharan.github.io/metly-ai-rebuild)**

---

## What I built and why

Metly is a pharma intelligence platform. Like most early-stage B2B SaaS, our conversion funnel had a gap: prospects landing on the site had no way to *feel* what Metly actually does for *their* role before booking a 30-minute demo with the sales team.

The old path: **Landing page → Book a demo → Wait for a call → Hope they show up.**

The problem with that path is that it asks for commitment before delivering value. A BD Director and a Market Access Director have completely different intelligence needs — but they were both looking at the same generic marketing page.

I decided to fix that. Not by writing a spec and waiting for an engineering sprint. By building it myself, in a single session, using Claude as my execution layer.

---

## Before: What the funnel looked like

| Problem | Impact |
|---|---|
| Generic landing page — no role personalisation | High bounce, low intent signal |
| "Book a demo" as the only CTA | Asked for commitment before showing value |
| Demo experience identical for every prospect | Sales team had to re-qualify every lead from scratch |
| No self-serve way to experience Metly's intelligence | Prospects dropped off before ever talking to us |
| No mobile experience | Lost any prospect who discovered us on their phone |

The team was spending time on demo calls with prospects who didn't fully understand what Metly was — or worse, who weren't the right fit at all.

---

## After: What I shipped

A two-page interactive prototype that personalises the Metly experience before anyone talks to sales.

### Page 1 — Landing page (`index.html`)
A clean, conversion-focused landing page that replaces the generic "Book a demo" CTA with **"See Metly in Action"** — a lower-commitment, higher-curiosity entry point.

- Rotating headline that cycles through roles (BD / CI / pipeline / strategy / team)
- Social proof from pharma names prospects already trust
- Seny the mascot — Metly's brand character — floating in with a direct hook
- Fully mobile-responsive

### Page 2 — Role-based demo (`metly-live-intelligence.html`)
A 3-step quiz that personalises the entire intelligence experience:

1. **Who are you?** — 6 roles: BD Director, CI Lead, VP Strategy, Medical Affairs Director, Brand Director, Market Access Director
2. **What slows you down?** — role-specific challenges, not generic pain points
3. **What's your TA?** — typed or picked from chips; pulls signals framed for your role

The results page then shows simulated intelligence cards (clinical trial movements, competitor filings, regulatory signals) framed specifically through the lens of that role and challenge. A BD Director sees licensing windows. A Market Access Director sees payer pushback trends. Same underlying data, completely different story.

End CTA: *"This is less than 1% of what Metly monitors — book a personalised demo."* The prospect arrives at that call pre-qualified, already having experienced value.

---

## How I built it — AI-First PM workflow

I didn't open Figma. I didn't write a PRD. I didn't wait for a designer or an engineer.

I used **Claude (claude.ai/code)** as my execution layer and shipped the full prototype in one session:

- Described what I wanted in plain English
- Iterated on design, copy, and UX through conversation
- Claude wrote every line of HTML, CSS, and JS
- I directed: positioning, tone, role logic, animation feel, mobile behaviour
- Total engineering time on my end: zero

This is what AI-first product management looks like in practice. The PM's job shifts from *writing specs for others to build* to *making product decisions at execution speed*.

---

## Metrics this experiment is designed to move

### Primary
| Metric | Hypothesis |
|---|---|
| **Demo-to-booking conversion rate** | Role-personalised experience increases intent before the CTA — prospects who complete the quiz are warmer leads |
| **Lead quality score** | Sales arrives at calls with role + TA + challenge context already captured — less time re-qualifying |
| **Self-serve engagement rate** | Prospects can experience value without a human in the loop — increases top-of-funnel throughput |

### Secondary
| Metric | Hypothesis |
|---|---|
| **Bounce rate on landing page** | "See Metly in Action" lowers the commitment bar vs "Book a demo" — more prospects continue |
| **Time-on-site** | Personalised quiz flow increases engagement depth vs a static page |
| **Mobile conversion** | Fully responsive experience captures prospects who discover Metly on their phones |
| **Sales cycle length** | Pre-qualified, pre-educated leads should move faster through the funnel |

### What the sales team gets
Every prospect who completes the quiz and books a demo arrives with three data points already captured:
- Their **role** (who they are in the org)
- Their **primary challenge** (what they're trying to solve)
- Their **therapeutic area** (where they operate)

That's a pre-filled discovery call — before anyone picks up the phone.

---

## Stack

Vanilla HTML/CSS/JS. No framework. No build step. Deployed on GitHub Pages.

The point wasn't to build production infrastructure. It was to validate the concept fast enough to learn from it.
