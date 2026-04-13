# Orkla Data & Analytics — Solutions Catalog

## What This Is
Customer-facing microsite for an internal Orkla team offering **data & analytics solutions** to portfolio companies and business units. The flagship offering unifies fragmented commercial data into trusted, decision-ready views. Deployed via GitHub Pages.

- **Live**: https://mathiasagain.github.io/solutions-catalog/
- **Repo**: https://github.com/MathiasAgain/solutions-catalog
- **Branch**: `master`
- **Deploy**: Auto via `.github/workflows/pages.yml` on push

## Tooling — RTK (required)

**Always prefix shell commands with `rtk`** — including inside `&&` chains. RTK ([rtk-ai/rtk](https://github.com/rtk-ai/rtk)) filters noisy output from git, gh, build tools, tests, file ops, and more, saving 60–90% of token output. If RTK has no dedicated filter for a command it passes through unchanged, so it's always safe to use.

Examples for this project:
- `rtk git status` / `rtk git add index.html` / `rtk git commit -m "..."` / `rtk git push`
- `rtk ls` / `rtk grep "pattern"` / `rtk wc -l index.html`
- `rtk python -m http.server 8765` for local preview

## Files

| File | Purpose | Audience |
|------|---------|----------|
| `index.html` | Main page — the complete solutions catalog (single page) | Business stakeholders |
| `engagement-guide.html` | Engagement Guide — effort estimates, interactive tools, starter packs, roadmap | Business planners, project sponsors |

## Key Context

### Who We Are
Internal Orkla team (not external vendors). We hand over everything deployed in the customer's environment. No licensing model. Our edge is the **Orkla Accelerator**: a continuously evolving toolkit of proven methods refined across every engagement. Each customer gets a copy; we keep the evolving version.

### Delivery Model
- **Orkla Accelerator** — our toolkit, forked for each engagement (matching, processing, quality)
- **Business Rules & Configuration** — customer-owned (source definitions, matching rules, KPI formulas)
- **Infrastructure** — customer-owned platform, managed by Orkla IT, all data stays with customer

### Engagement Types
- **Build** — new deployment (project engagement)
- **Upgrade** — apply latest accelerator improvements
- **Support** — optional retainer for managed ops
- **Expand** — new use cases (analytics, automation, additional sources)

## Design System

### Colors (Orkla-branded)
```
--navy:    #7E0626   (Orkla burgundy — primary brand color)
--navy2:   #5A0419   (darker burgundy — gradients)
--teal:    #0D7C66   (Tier 1)
--blue:    #2E5090   (Tier 2)
--purple:  #6B4FA0   (Tier 3)
--amber:   #C17817   (add-ons, infrastructure)
--bg:      #FAF8F6   (warm off-white background)
--line:    #E6DED6   (warm border)
```

### Tier Colors (consistent across both docs)
- Tier 1 Foundation → **teal**
- Tier 2 Multi-Source → **blue**
- Tier 3 Enterprise → **purple**
- Currency & Calendar Alignment → **amber** (add-on)

## Canonical Numbers

### Tiers
| Tier | Hours | Timeline | Platform/mo | Eng Support/mo |
|------|-------|----------|-------------|----------------|
| Foundation | 180–220h | ~5.5 weeks | $50–300 | 8–20h |
| Multi-Source | 290–685h | 9–14 weeks | $150–600 | 16–40h |
| Enterprise | 820–1,900h | 27–36+ weeks | $400–1,500 | 40–120h |

### Add-Ons (6 total)
| Add-On | Hours | Monthly |
|--------|-------|---------|
| Power BI Reports | 40–80h | $20–80 |
| Data Quality & Alerts | 40–80h | $20–80 |
| Business Review Portal | 60–120h | $30–100 |
| Historical Tracking | 30–50h | +$10–40 |
| Additional Data Source | 40–85h/src | +$30–100 |
| Currency & Calendar Alignment | 120–320h | $50–200 |

**Important**: If you change a number, update it in BOTH HTML files.

## Main Page Section Order (index.html)
1. Hero (with audience statement)
2. **Tiers** (our offerings + tier selection guide)
3. Proof-point banner
4. Challenge (FMCG-specific pain)
5. **Outcomes** (what changes for your team)
6. **How We Work** (delivery model — 3 pillars)
7. Add-Ons (6 cards)
8. Investment (cost table with explanatory footnotes)
9. FAQ (4 questions)
10. CTA

## Design & Tone Guidelines
- **Business-first language** — no technical jargon
- **Orkla branded** — burgundy primary color (#7E0626), warm backgrounds
- **Outcome-focused** — lead with what the business gets
- **No overselling** — confident but understated
- **Infrastructure is managed by Orkla IT**, not customer's local IT

## Known Issues / Pending Work
- `contact@example.com` placeholder in CTA — replace when real email provided
- Engagement guide still has hidden sections (mapping, SOW, risks) — to be cleaned or repurposed for internal technical twin

## Reference Document
`C:\Users\medelm\Sales_Data_Harmonization_Estimate.md` — original effort estimate used as source of truth for Tier 1 numbers. Not in the repo.
