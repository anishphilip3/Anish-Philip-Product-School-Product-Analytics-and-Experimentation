# The Validation · FinWise

> Module 5 · Experimentation Methods. The experiment brief that tests the bet.

## Method

**A/B test** — clean per-user randomization, 50/50 split. Chosen over MAB (no scarce-conversion pressure), Holdout (signal appears in first session), Geo-Test (no marketplace effects), and Switchback (no temporal carry-over). We have enough traffic and a clean user-level split for the onboarding change.

_____

## Hypothesis + primary metric

If we add an "Explore with sample data" path on the Get-Started screen for new trial users, then more of them reach their first modeling output — the North Star activation event.

- **Primary metric:** % of new trial users reaching first modeling output within 7 days
- **Success threshold:** significant (p < 0.05), ≥5pp absolute lift
- **If successful:** ship → Holdout → pricing experiment (M6)
- **If not:** instrument Get-Started to find the true drop-off

_____

## Guardrail + read date

- **Guardrail:** Trial→Paid conversion must not significantly drop.
- **Read date:** ~6 weeks, pre-set — no peeking.
