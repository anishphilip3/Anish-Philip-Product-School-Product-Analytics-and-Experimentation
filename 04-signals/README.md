# 04 · The Signals — Data & Analytics (Module 4)

**Deliverable:** the data pattern found + the chosen leading and lagging indicators.

- **Signals dashboard (open in a browser):** [`signals-dashboard.html`](signals-dashboard.html)
- **Live link:** https://claude.ai/code/artifact/452920b0-bf60-4f88-b46f-540d71c98f45
- **Presentation deck:** [`the-signals-presentation.html`](the-signals-presentation.html) — 9-slide green-editorial deck covering Aim·Move·Prove, pattern diagnosis, correlation finding, and the two-experiment priority split.

## Aim · Move · Prove

| Layer | Metric | Why |
|---|---|---|
| 🎯 **Aim · North Star** | # of trial users who **import financial data and reach their first modeling output** | The single behavior that proves a user felt core value. |
| ⚙️ **Move · Leading 1** | **Get-Started Import Usage %** | Gateway to the North Star; at the Trial→Paid drop-off, stuck at a ~40% ceiling with headroom. |
| ⚙️ **Move · Leading 2** | **Financial Modeling Usage %** | Reaching a modeling output *is* the Aha — the closest proxy for felt value. |
| ✓ **Prove · Lagging** | **Net Dollar Retention / ARR growth** | Earned by lifting activation → conversion + retention; confirms the strategy at scale. |

## The pattern diagnosis (13-month trends)

| Metric | Pattern |
|---|---|
| Trial-to-Paid Conversion | **Ceiling** — flat 1.87–2.08%, a hard cap |
| Get-Started Import Usage % | **Ceiling** — ~40% plateau |
| Financial Modeling Usage % | **Growth** (doesn't fit cleanly) — the one metric rising |
| Avg Session Duration | **Cliff** — sharp mid-2024 drop |
| Avg Sessions / User | **Slow Leak** then recovery (U-shape) |

## The correlation finding (the important part)

Indexing **Modeling Usage** vs **Conversion** to 100 at Oct '23: modeling climbs to ~187 while conversion never leaves the 97–108 band. A direct scatter confirms it: **Pearson r ≈ 0.24 — weak and not significant** (n=13; p=0.05 threshold ≈ 0.55).

**Hypothesis, sharpened:** the leak is partly confirmed (activation is weak), but since deepening modeling usage did **not** move conversion, the **2% is a structural ceiling** (pricing / paywall / packaging), not an activation-depth problem. Priority splits: (a) lift **Import Usage** to grow the North Star pool, and (b) run a **separate pricing/paywall experiment** — which sets up Module 6.

_Method note: single-axis (indexed) charts — no dual-axis; series colors validated for color-blind safety._
