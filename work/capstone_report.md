# Capstone Report — <your lane></your>

- **Author:** Tarik Sorguč
- **Lane:** Content Opportunity Scoring and Refresh
- **Repo:** [github.com/sorgerator/flyrank-internship.git](https://github.com/sorgerator/flyrank-internship.git)
- **Date:** August 31, 2026

> Copy this file to `work/capstone_report.md` and fill it in as you build. The eight
> sections mirror the Pass / Needs-Work rubric axes, so nothing here is optional.

## Abstract

This research addresses FlyRank's challenge of identifying high-value content that is actively losing search traffic before it falls off the first page. Using a dataset of 78.8 million daily performance records across 104 client properties, I engineered features around historical rank volatility and engagement momentum. By applying a Random Forest classifier in a strict time-series split, the model predicted active traffic decay with a Precision@50 of 98.0%, significantly outperforming traditional age-based heuristics. These predictions feed directly into a Content Action Playbook, giving editors a ranked queue of 2,916 high-confidence targets complete with diagnostic reason codes. Ultimately, this allows SEO teams to transition from reactive updates to predictive, targeted content refreshes that protect organic traffic.

## 1. Introduction

### The Tension

Traditional SEO strategies often rely on refreshing the oldest articles or those with the highest historical traffic. However, age does not equal decay; a five-year-old page might hold steady while a six-month-old page actively loses clicks to competitors. For FlyRank, updating based strictly on age wastes valuable editorial resources while actual decaying content slips through the cracks.

### The Resolution

This project transitions the SEO workflow from reactive updates to a predictive Content Action Playbook. By analyzing historical volatility, engagement drops, and competitive distance, the machine learning pipeline predicts the probability that a page is actively declining. It flags at-risk content and provides diagnostic reason codes, allowing editors to intercept and refresh high-value pages before their organic traffic plummets.

## 2. Data safety

Which data you used and which columns you deliberately excluded (and why). Leakage risks you
considered — especially label-derived fields (`trend_direction`, `trend_pct`) and pseudonymous
IDs (grouping only, never features). Confirm nothing client-identifying appears anywhere in
`work/`.

## 3. Baseline

The transparent rule or score you built first. Why it's a fair comparison, and its numbers on
the same data and metric as your model.

## 4. Model / analysis

Your method and why it fits the lane. The exact feature list (and what you left out on
purpose). The target or proxy definition, in one sentence.

## 5. Evaluation

Your split (grouped by client? time-aware?) and why. Metrics, model vs baseline **on the same
split**. What the errors look like — a short error analysis beats a big metric table.

## 6. Interpretation

What the model/clusters actually found. Feature importances or cluster profiles in plain
words. Surprises and negative results — a well-understood "no effect" is a valid result.

## 7. Recommendation

The ranked actions or decisions your output supports, and how a FlyRank editor would use them
tomorrow. State your confidence and the limits explicitly.

## 8. Reproducibility

The exact commands to re-run everything from a fresh clone, your random seeds, and your
environment (`pip freeze` highlights or `requirements.txt` deltas).

---

> **Claims checklist before submitting:** observed / measured / directional / decision-support
> **Metrics vs. base rate:** report your task's base rate (majority-class %) next to any
> precision@K or accuracy — a high score can just be a high base rate. AUC / lift over
> baseline are the honest discrimination numbers.
> language everywhere · no causal claims without an experiment or causal design · no
> "predicted Google's algorithm" · no client-identifying details · numbers in this report
> match a fresh re-run.
