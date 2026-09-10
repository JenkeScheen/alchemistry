---
layout: page
title: Alchemistry 2027 Blind Challenge — Tutorial
sitemap: false
---

# Challenge Tutorial

*Materials are being prepared and will be published here before submissions open on
**1 November 2026**.*

This page will host the walkthrough for the **Alchemistry 2027 Antiviral Blind
Challenge**: predicting binding free energies for a series of compounds against the
**Dengue-2 NS2B-NS3 protease** using alchemical free energy methods.

## What will be here

- **A step-by-step walkthrough** — loading the test set, setting up and running the
  free energy calculations, and assembling a submission file.
- **Baseline notebooks** — a worked reference calculation you can run end to end and
  compare against, so you can check your pipeline before committing compute to the
  full set.
- **A validation script** — run it against your file *before* uploading. It checks the
  row count, the required columns and their types, so a formatting mistake costs you
  seconds locally rather than a rejected submission and a wait for the next
  rate-limited slot.

## Submission format, in brief

Predictions are submitted as a single `.parquet` (preferred) or `.csv` file with one
row per test-set compound. Alongside each prediction you also report an **uncertainty
estimate** for it, in the same units as the prediction itself (kcal/mol). The exact
column names and a worked example are shown on the **Submit** tab of the challenge
Space, generated directly from the challenge configuration so they cannot drift out of
date.

## Getting help

Questions about the science, the data, or submission mechanics are welcome in the
**#alchemistry-2027** channel on [our Discord](https://discord.gg/R5JwtQqaN).
Automated validation receipts for your submissions are posted to
**#alchemistry-2027-submissions**.

## Timeline

| Date | Milestone |
|---|---|
| 5 October 2026 | Challenge announced |
| 1 November 2026 | Test set released; submissions open |
| 15 January 2027 | Deadline for the interim leaderboard |
| 25 January 2027 | Interim leaderboard released |
| 25 March 2027 | Submissions close |
| From 1 April 2027 | Final leaderboard; results and talks at Alchemistry 2027 |
