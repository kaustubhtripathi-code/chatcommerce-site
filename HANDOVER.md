# HANDOVER — chatcommerce-site

Marketing site for **ChatCommerce OS** (the WhatsApp-storefront product at
`OneDrive\Documents\Claude\Projects\Whatsappcommerce-os` — read ITS CLAUDE.md for product
state). Single self-contained `index.html` + promo video + product screenshots.

- Repo: `kaustubhtripathi-code/chatcommerce-site` · deployed via GitHub Pages
  (https://kaustubhtripathi-code.github.io/chatcommerce-site/).
- Redeploy = commit + push to the default branch; Pages serves from root.
- Keep claims in sync with the product repo (pricing/features live THERE; this site is
  downstream). Screenshots came from the real app — if the UI changes materially, re-shoot.
- User steps: none pending for the site itself. Product go-live steps are in the product's
  CLAUDE.md.

Last audit: 2026-07-12 (state = last commit `1357226`, 2026-07-07).

## 2026-07-25 responsive + honesty pass
- Mobile nav no longer deleted at <=900px — collapses into a `<details>` hamburger (no JS).
- Fixed 150px horizontal overflow at 375px: `.hero::before` (a decorative radial at
  `right:-150px`) now clipped by `overflow:hidden` on `.hero`.
- Four dead `href="#"` CTAs -> `mailto:kaustubh.trt@gmail.com` with per-plan subjects.
- The orphaned contact strip that sat *outside* `</footer>` is now inside the footer.
- **Stat band reframed.** 550M+ / 98% / 3-5x / 47% are published channel benchmarks, not
  ChatCommerce OS results — the band is now labelled "Why the channel works" and carries an
  explicit note saying so. Do not re-present them as product metrics; there are no customers
  yet. Replace with real numbers only when there are real numbers.
