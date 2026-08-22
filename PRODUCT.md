# Product

<!-- impeccable:product-schema 1 -->

## Platform

web

## Stack

static HTML/CSS/JS, no build step (confirmed: matches sibling projects — Life Balance Index, Midori, Runaway, Vial, Voluma all deploy as static GitHub Pages sites with no build tooling; hosting confirmed as GitHub Pages with a Cloudflare-managed apex record for plainpoint.net)

## Users

Two audiences, in priority order:
1. **Google Play Console reviewers** — checking that "Plain Point Studio" (the developer name registered in Play Console) has a real, credible developer website. This is the triggering use case for building the site.
2. **Curious visitors** — anyone who finds one of the apps (via Play Store, GitHub, or word of mouth) and lands here to see who made it and what else they've built.

Neither audience is mid-task inside a product; they are evaluating the developer's credibility and browsing available work.

## Product Purpose

A single-page developer profile for the indie studio "Plain Point Studio," listing its live apps with links out to each. Exists to (a) satisfy Google Play Console's developer-website requirement and (b) act as a durable home base at the domain's apex (plainpoint.net) that ties together the subdomain-hosted apps (lbi.plainpoint.net, midori.plainpoint.net). Success = a visitor immediately understands who Plain Point Studio is and can reach any live app in one click; a reviewer sees a legitimate, maintained developer presence.

## Positioning

Not a company site or a growth-marketing landing page — a small, honest indie-dev profile. The differentiator across the portfolio (and the site's own implicit claim) is **small, focused, privacy-first, local-first apps**: no accounts, no servers, no tracking, data stays on-device (localStorage) except where an app explicitly opts into a backend (Runaway uses Supabase for its shared leaderboard — the one deliberate exception). The site itself should practice what it lists: no analytics, no trackers, no third-party scripts.

## Operating Context

- Root domain `plainpoint.net` registered via Cloudflare; DNS for the apex will point to GitHub Pages.
- Sibling apps already live at subdomains of the same domain, each its own GitHub Pages deployment with its own `CNAME` file: `lbi.plainpoint.net` (Life Balance Index, public repo), `midori.plainpoint.net` (Midori — Leafy Ledger, private repo). Runaway, Vial, and Voluma are currently on `seehighxb.github.io/<repo>/` paths, not custom subdomains.
- This site will live in its own new repo under the `SEEHIGHxb` GitHub account, deployed to GitHub Pages with `CNAME` = `plainpoint.net`.
- No contact form or public email for now (explicit user decision) — omit any contact section rather than stub one out.

## Capabilities and Constraints

- Single page: hero (studio name + tagline) + portfolio grid of 5 apps + footer. No routing, no build pipeline, no framework.
- Each portfolio card links out to that app's live URL (external link, new tab).
- Midori and Vial cards must note their privacy-first/local-only nature (explicit user requirement) — no server, data stays on the device.
- No contact info displayed (explicit user decision, revisit later).
- No fabricated testimonials, user counts, press mentions, or metrics — none exist and none should be implied.

## Brand Commitments

- Studio/developer name: **Plain Point Studio** — this is the exact name registered in Google Play Console and must appear as such.
- Tagline (confirmed, user-supplied verbatim): **"Indie developer building small, focused, privacy-first apps."**
- Portfolio apps and their one-line identities (from each app's own README, not invented):
  - **Life Balance Index** — formal self-assessment dashboard tracking eight life aspects with weekly check-ins. Live at lbi.plainpoint.net.
  - **Midori (Leafy Ledger)** — offline-first personal finance ledger, multi-currency, local-only data.
  - **Runaway** — real-time group run tracker for a small friend circle; shared leaderboard via Supabase.
  - **Vial** — private medical companion for tracking weekly medicine injections; local-only, single-user (built for a nurse).
  - **Voluma** — client-side audio waveform editor/splitter, 100% local via Web Audio API, no uploads.

## Evidence on Hand

- Each app's README (read directly from its repo) is the source of truth for its description — do not paraphrase into marketing claims the README doesn't support.
- No logos/icon assets confirmed yet for the studio itself (apps have their own SVG art, e.g. Midori's `image/midori-animation.svg`, Vial's `image/vial-animation.svg`). Studio-level mark, if any, is new work, not an existing asset.
- No screenshots, testimonials, press, or user metrics exist for any app — must not be fabricated.

## Product Principles

1. Practice the pitch: the site itself carries no analytics, no trackers, no third-party embeds — consistent with the "privacy-first" claim made about the portfolio.
2. Say only what the README evidence supports; no invented traction, quotes, or numbers.
3. One click from studio to any live app — the portfolio grid is the primary content, not decoration around it.
4. Stay consistent with sibling deploys: static files, GitHub Pages, apex CNAME — no added infrastructure.
5. Credible-but-modest: this needs to read as a real, maintained developer presence to a Play Console reviewer, not an oversold marketing page.

## Accessibility & Inclusion

No project-specific requirement established beyond standard WCAG AA baseline (semantic HTML, sufficient contrast, keyboard-navigable links) — no explicit request for anything further.
