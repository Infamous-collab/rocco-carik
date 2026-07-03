# Rocco Carik — Private Health Insurance Website

## What this is
A premium single-page marketing site for **Rocco Carik**, an independent licensed
health insurance agent based in South Florida.
Built as a 1-to-1-but-better remake of his competitor's site: https://oxana.care/

**Branding rule (2026-07-03, per Isaac):** the site must NOT mention USHEALTH
Advisors or UnitedHealthcare anywhere. Positioning is "Independent Licensed Agent."
Do not reintroduce carrier names.

- **Live URL (send this to people):** https://infamous-collab.github.io/rocco-carik/
- **Repo:** github.com/Infamous-collab/rocco-carik
- **Owner of project:** Isaac (does marketing for Rocco). Rocco is the client/friend.

## Rocco's real info (do not change without checking)
- Name: Rocco Carik — Independent Licensed Agent
- Email: carikhealths@gmail.com (replaced Rocco.Carik@ushadvisors.com on 2026-07-03)
- Phone (561) 702-7836 is NOT shown on the site anymore — Rocco calls leads himself
  after they book. No `tel:`/`sms:` links; all CTAs go to Calendly.
- Calendly: **PLACEHOLDER** — every CTA points to `https://calendly.com/ROCCO-CALENDLY-LINK`.
  Find/replace that string with the real link when Rocco provides it. Do not push to
  `main` (auto-deploys) while the placeholder is in place.
- Photo: `assets/rocco.webp` (portrait in navy quarter-zip in front of silver phoenix wall)

## Stack & structure
Deliberately zero-build: one static page, no framework, no npm.
- `index.html` — everything: markup, CSS (in `<style>`), JS (in `<script>` at bottom)
- `assets/rocco.webp` — his portrait, used in hero + about section
- Fonts: Google Fonts — **Fraunces** (serif display headlines) + **Manrope** (body/UI)
- Design tokens are CSS variables in `:root` (ink navy `#0b1f3a`, paper cream `#faf7f2`,
  blue `#2f6fed`, gold `#c8a24a` accents). Keep all new styles on these tokens.
- JS features: sticky nav scroll state, mobile hamburger, IntersectionObserver
  `.reveal` fade-ups (add `reveal` + optional `d1–d4` delay classes to new elements),
  FAQ accordion.

## Deployment
GitHub Pages (legacy build) off `main` branch, root path. **Any push to `main`
auto-deploys in ~1–2 min.** No build step, no CI file. To verify:
`curl -s -o /dev/null -w "%{http_code}" https://infamous-collab.github.io/rocco-carik/`

## Copy strategy (why the sections say what they say)
All copy is built from Rocco's Target Audience & Marketing Brief. The audience is
people who earn "too much" for ACA subsidies ($75K–$300K+ household) and are stuck
with expensive options. Sections map to the brief's four core scenarios:
1. Self-employed over the subsidy cliff
2. Employer plan too expensive
3. Adding spouse/kids through employer is unaffordable
4. Lost coverage, COBRA is 2–3× market (60-day election window = urgency angle)

Positioning: "the third option" — private plans not listed on the Marketplace;
one agent with a direct line vs. call centers; $0 to work with him; independent
agent shopping major nationally recognized carriers, with personal accountability.

## Compliance guardrails — IMPORTANT
Health insurance marketing has state/platform rules. Keep these intact:
- **No fabricated testimonials, reviews, or credentials.** There are intentionally
  none on the site. Only add real Google reviews when Rocco provides them.
- No guaranteed-savings claims — copy uses "often", "typically", "can".
- Pre-existing-conditions FAQ answer is intentionally honest (private plans don't
  fit everyone); don't oversell it.
- Footer disclaimer must stay.

## Known TODOs / likely next requests
- **Replace the Calendly placeholder** `https://calendly.com/ROCCO-CALENDLY-LINK`
  with Rocco's real Calendly URL (4 occurrences in index.html), then push to deploy.
- Add real **Google reviews/testimonials** section when available.
- Possible custom domain (e.g. roccocarik.com) → CNAME + Pages settings.
- Possible lead-capture form (needs a backend/formspree-style service — currently
  none, site is fully static).
- Facebook ad landing variants may be requested later (brief mentions FB ads,
  Google/SEO, TikTok).
