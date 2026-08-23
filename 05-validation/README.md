# 05 · The Validation — Experimentation Methods (Module 5)

**Deliverable:** the experimentation brief (method, hypothesis + primary metric, guardrail + read date), plus a real result read.

- **Experiment brief:** [`experiment-brief.html`](experiment-brief.html) · live: https://claude.ai/code/artifact/995d5628-ad57-4fe1-9be1-01d03e080749
- **A/B result analysis:** [`ab-analysis.html`](ab-analysis.html) · live: https://claude.ai/code/artifact/3b664932-97dc-46dd-84d4-3e6012e29d3d
- **Presentation deck:** [`the-validation-presentation.html`](the-validation-presentation.html) — 10-slide green-editorial deck covering Part 1 (experiment brief) and Part 2 (A/B analysis with real CSV data).

## Part 1 — The experiment brief: "Sample-Data On-Ramp"

**Method:** standard **A/B test** (user-level, 50/50). *Why:* a single onboarding-screen change randomizes cleanly per user and the signal appears within the first session — no need for MAB (no scarce-conversion pressure), Geo/Switchback (no marketplace effects), or Holdout (fast signal). Don't overcomplicate.

| Field | Decision |
|---|---|
| Objective | Lift the North Star (import + first modeling output) by removing the connect-a-bank wall. |
| Hypothesis | *If* we add an "Explore with sample data" path on the Get-Started screen, *then* more trial users reach a first modeling output, *measured by* the first-modeling-output rate (7-day). |
| Primary metric | % of new trial users reaching their first modeling output within 7 days. |
| Success threshold | Significant (p < 0.05) **≥ 5pp** absolute lift, read at a **pre-set ~6-week** date (extend rather than peek). |
| Guardrail | Trial→Paid conversion must not significantly drop (guards the vanity-activation trap). |

**If successful:** ship → run a Holdout for the retention tail → open the pricing/paywall experiment (Module 6). **If not:** instrument Get-Started to find the true drop-off, or pivot to pricing.

## Part 2 — Reading a real A/B result

Another team's landing-page test (hypothesis: Version B's simplified CTA + design beats A on conversion *and* engagement). Result: **A converts better, B engages better.**

Applying the four lenses (significance → MDE → CI → guardrails): both effects are real, but the metric that pays (conversion) favors A while B wins engagement.

- **Scenario:** **Mixed Signal** → **the call is Investigate.**
- **Recommendation:** keep A live as the conversion baseline; don't ship B on engagement alone, don't dismiss it either.
- **Next steps:** isolate the driver (B bundled CTA + design = colliding changes → test B's design with A's CTA); run a Holdout to see if B's engagement → downstream retention/LTV; segment the conversion loss.

_Numbers in `ab-analysis.html` are computed from the real experiment CSV (20 users, 10/group). At n=20, neither difference is statistically significant (p ≈ 0.36), reinforcing the Investigate call with an added recommendation to re-run at proper power (~500/arm)._
