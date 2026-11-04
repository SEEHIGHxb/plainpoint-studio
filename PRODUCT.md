# Product

<!-- impeccable:product-schema 1 -->

## Platform

web

## Stack

static HTML/CSS, no JavaScript, no build step (confirmed: matches sibling projects — Life Balance Index, Midori, Runaway, Vial, Voluma all deploy as static GitHub Pages sites with no build tooling; hosting confirmed as GitHub Pages with a Cloudflare-managed apex record for plainpoint.net)

## Users

Three audiences (revised November 2026, when the site became a hiring portfolio):
1. **Prospective clients** arriving from LinkedIn or Fiverr, deciding whether to hire Passakorn for an Android or web app. They scan for: who this is, proof of shipped work, what he takes on, how to get in touch.
2. **Google Play Console reviewers** checking that "Plain Point Studio" (the developer name registered in Play Console) has a real, credible developer website and privacy policy.
3. **Curious visitors** who found one of the apps and want to see who made it.

None of them is mid-task inside a product; they are evaluating credibility and browsing work.

## Product Purpose

A one-page portfolio and developer profile for "Plain Point Studio" at plainpoint.net. It leads with two flagship case studies, **NgernNgok** (Android money tracker, bound for Google Play; the codebase is `Midori-Ledger`, but the portfolio uses the store name only, by explicit user decision) and **Asterism** (wellbeing self-assessment, live at asterism.plainpoint.net), then services, smaller work and contact. Success = a client understands in one screen what Passakorn builds and can reach him in one click; a reviewer sees a legitimate, maintained developer presence.

## Positioning

Not a company site or a growth-marketing landing page — a small, honest indie-dev profile. The differentiator across the portfolio (and the site's own implicit claim) is **small, focused, privacy-first, local-first apps**: no accounts, no servers, no tracking, data stays on-device (localStorage) except where an app explicitly opts into a backend (Runaway uses Supabase for its shared leaderboard — the one deliberate exception). The site itself should practice what it lists: no analytics, no trackers, no third-party scripts.

## Operating Context

- Root domain `plainpoint.net` registered via Cloudflare; DNS for the apex will point to GitHub Pages.
- Sibling apps already live at subdomains of the same domain, each its own GitHub Pages deployment with its own `CNAME` file: `lbi.plainpoint.net` (Life Balance Index, public repo), `midori.plainpoint.net` (Midori — Leafy Ledger, private repo). Runaway, Vial, and Voluma are currently on `seehighxb.github.io/<repo>/` paths, not custom subdomains.
- This site will live in its own new repo under the `SEEHIGHxb` GitHub account, deployed to GitHub Pages with `CNAME` = `plainpoint.net`.
- Contact (decision reversed November 2026): email at hello@plainpoint.net (to be routed by Cloudflare Email Routing), plus LinkedIn and Fiverr profile links once their URLs are supplied. Still no contact form, so the site keeps running no JavaScript.

## Capabilities and Constraints

- Single page: top bar, hero with calls to action, two case studies (NgernNgok, Asterism), services, More work (Vial, Voluma, Runaway, Table of Five), contact, footer. Plus privacy.html and 404.html. No routing, no build pipeline, no framework, no JavaScript.
- Each portfolio card links out to that app's live URL (external link, new tab).
- Every app states its real data handling. Vial, Voluma and Asterism are local-only. NgernNgok (originally required to read "no server, data stays on the device") gained optional Supabase sync, Sentry crash reports and Play Billing in Aug–Oct 2026, so it now reads "works without an account, no ads" alongside honest notes, and privacy.html defers to its own policy at midori.plainpoint.net/privacy.
- Contact: hello@plainpoint.net, LinkedIn and Fiverr (see Operating Context). Fiverr forbids steering its buyers off-platform, so the Fiverr profile itself should not link here for contact purposes.
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
  - **Table of Five** — browser virtual tabletop for one D&D party; server-authoritative rolls via a Supabase Edge Function. Private build, not offered to the public, so outside the privacy policy's scope.

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
