---
layout: page
title: Alchemistry 2027 Blind Challenge — Tutorial
sitemap: false
---

# Challenge Tutorial

A single notebook that walks the whole submission path end to end: downloading the test
set, looking at what you have been given, generating example predictions, writing
them in the required format, validating the file locally, and submitting it.

<p>
  <a href="https://github.com/omsf/alchemistry/blob/main/blind_challenges/2027/tutorial/alchemistry_2027_tutorial.ipynb">
    <strong>View the tutorial notebook on GitHub</strong></a>
  &nbsp;·&nbsp;
  <a href="{{ '/blind_challenges/2027/tutorial/alchemistry_2027_tutorial.ipynb' | relative_url }}" download>
    download the <code>.ipynb</code></a>
</p>

It runs locally in a few minutes and needs only `pandas`, `numpy`, `matplotlib`,
`rdkit` and `huggingface_hub`:

```bash
pip install pandas numpy matplotlib rdkit huggingface_hub pyarrow
```

**It does not run a free energy calculation.** 

## What it covers

1. **Getting the data** — the 54 blinded compounds and the reference crystal
   structure, pulled straight from the challenge dataset on Hugging Face.
2. **Exploring the test set** — property distributions, the scaffold group.
3. **The reference structure** — the NS2B–NS3 construct.
4. **Example predictions** — a deliberately crude molecular-weight baseline.
5. **Building the submission** — the exact column names, the units, and the
   uncertainty column.
6. **The edge file** — the ΔΔG schema for relative methods.
7. **Submitting** — the Submit tab on the challenge web UI.

## Submission format, in brief

Predictions are submitted as a single `.parquet` (preferred) or `.csv` file with one
row per test-set compound. Alongside each prediction you also report an **uncertainty
estimate** for it, in the same units as the prediction itself (kcal/mol). The exact
column names and a worked example are shown on the **Submit** tab of the challenge
Space.

Relative, edge-based methods must additionally submit the perturbation network they
ran, as one row per edge with its ΔΔG and uncertainty; the Space rejects a relative
submission that arrives without one. Note that error metrics are reported as
N/A for relative submissions.

## Getting help

Questions about the science, the data, or submission mechanics are welcome in the
**#😷alchemistry-2027-challenge** channel on [our Discord](https://discord.gg/U5XtzEVZ6).
Automated validation receipts for your submissions are posted to
**#😷alchemistry-2027-challenge-submissions**.

## Timeline

| Date | Milestone |
|---|---|
| October 2026 | Challenge announced |
| 1 November 2026 | Test set released; submissions open |
| 15 January 2027 | Deadline for the interim leaderboard |
| 25 January 2027 | Interim leaderboard released |
| 25 March 2027 | Submissions close |
| From 1 April 2027 | Final leaderboard; results and talks at Alchemistry 2027 |
