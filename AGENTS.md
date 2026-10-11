# AGENTS.md — chatcommerce-site

Public marketing site for ChatCommerce OS (WhatsApp storefront for Indian D2C brands). Single
self-contained `index.html` + promo video + product screenshots, served by GitHub Pages at
https://kaustubhtripathi-code.github.io/chatcommerce-site/. Status: active, low-churn.
**This repo is PUBLIC** — never commit secrets, private notes or customer data.

Product context: the canonical product repo is `whatsappcommerce-os` (private). The sibling repos
`chatcommerce-os` and `whatsapp-commerce-mvp` are superseded iterations. This site is downstream:
pricing/feature claims must match `whatsappcommerce-os`.

## Stack & layout
- Static HTML/CSS (inline), no build step, no JS framework. Google Fonts via `<link>`.
- `index.html`, `assets/` (og-image.png, promo.mp4), `shots/` (real app screenshots).
- `ci/site_check.py` — validates local references/JS and stages tracked assets into `_site/`.

## Setup
None (Python 3.12 + Node 22 only for the check).

## Run / build / test / lint
- `python ci/site_check.py --repo chatcommerce-site --output /tmp/site_out` (verified 2026-10-11).
  Default output `_site/` must not already exist; delete it afterwards (not committed).
- Preview: `python -m http.server` and open `/index.html` (unverified).

## Environment variables
None required.

## Codex cloud environment
- Setup script: none needed (python3 and node are preinstalled in the default image).
- Internet during agent phase: off is fine.
- Secrets to add: none.

## Rules for agents
- Pushing to `main` deploys to GitHub Pages (CI-gated). Work on a branch; PRs never deploy.
- The stat band (550M+ / 98% / 3-5x / 47%) shows published channel benchmarks, labelled
  "Why the channel works". Never present them as ChatCommerce OS results — there are no customers yet.
- Contact links are `mailto:` with per-plan subjects; use the plain address, never `+alias` variants.
- Keep the mobile nav as the no-JS `<details>` hamburger; keep `.hero { overflow:hidden }` (prevents
  horizontal scroll at 375px).
- If the product UI changes materially, re-shoot `shots/` from the real app; the promo video is
  rendered in the product repo (`marketing/video`) and copied to `assets/promo.mp4`.

## Open work
- None pending. Branch `ci/portfolio-20260907` is identical to `main`.
