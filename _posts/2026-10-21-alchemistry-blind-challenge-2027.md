---
layout: post
title: "The Alchemistry Blind Challenge: 2027 edition"
date: 2026-10-21
tag: Challenge
summary: "The Alchemistry 2027 committee is hosting a blind challenge with OpenADMET and OpenBind: predict binding free energies for 54 Dengue-2 NS2B-NS3 protease inhibitors before the measurements are released."
permalink: /news/:year/:month/:title/
---

<div class="post-banner">
    <img src="{{ '/assets/images/fe_workshop_logo_white.png' | relative_url }}" alt="Free Energy Workshop logo">
</div>

{:.post-lead}
The Alchemistry 2027 committee is hosting a blind challenge in collaboration with OpenADMET and OpenBind.

Physics-based alchemical free energy calculations have become an integral part of modern structure-enabled drug discovery workflows. Advances in software, force fields, sampling methods, and access to computational resources have made it possible to apply these methods routinely to large, chemically diverse problems, including small-molecule modalities and beyond. Free energy methods are widely applied in novel prospective drug discovery projects, but the field lacks an open prospective testing scenario that can fairly assess the generalizability of the wide range of available techniques.

This is particularly important for physics-based simulation methods, which promise predictive power beyond the chemical space represented in the data used to develop them. So, how well do these methods actually perform when the answer is not already known? *That's what we want to find out.*

<aside class="post-callout">
    <span class="post-callout-icon" aria-hidden="true">🤗</span>
    <p>The challenge will be hosted on <a href="https://huggingface.co/spaces/openadmet/alchemistry-2027-challenge">this HuggingFace page</a>. Top performers of this challenge will be invited to present their work at the 2027 Alchemistry conference in the US. To make this challenge possible, we are collaborating with <a href="https://asapdiscovery.org/">ASAP Discovery</a>, <a href="https://openadmet.org/">OpenADMET</a> and <a href="https://openbind.uk/">OpenBind</a>.</p>
</aside>

## Why should we care about blind challenges?

Blind prospective challenges have played an important role in computational science, offering communities a fair platform to benchmark a wide range of methods in an open, shared manner; finding what works, what fails and why.

This is what we hope to establish for the field of free energy calculations: prospective challenges where we can probe not only the accuracy of the calculations themselves, but also establish best practices around the many modelling choices available, from system setup through to alchemical strategy. By sharing these experiences, we hope to help practitioners increase their chances of success when applying free energy calculations prospectively.

So, while being at the top of the leaderboard is a fantastic achievement, this challenge is also a great opportunity to learn together and share ideas. We want to encourage as many people as possible to enter and share what they tried, even if it didn't work very well!

## Don’t we already have public benchmarks?

Yes! We have open, high-quality public benchmark datasets such as those compiled by [Ross et al](https://www.nature.com/articles/s42004-023-01019-9) and they have been instrumental to the field. They offer open and reproducible test cases which have established baseline accuracy for a wide range of methods and identified many areas of improvement. They also enable controlled comparisons between methods and have become an essential part of how free energy methods are developed and evaluated.

However, because these datasets and their experimental results are publicly available, it is difficult to disentangle how much of the performance reflects a method's ability to generalise to new chemistry and how much comes from years of method and protocol development informed by these established systems. While a sensible strategy, this does potentially underestimate the uncertainty of applying a particular workflow to a truly novel dataset in a real-world drug discovery setting.

## A challenge specifically designed for free energy methods – but all are welcome!

The challenge is designed to provide a suitable target for free energy calculations that we know is already predictive. We have selected 54 ligands forming a congeneric series from a real-world drug discovery program that is sufficiently centred on a single scaffold to enable both relative and absolute calculations. With this, we retain the realism of a prospective drug discovery setting while also being small enough to allow participants with limited hardware to compete.

That being said: we do not want to gatekeep methodologies. To that end, we are opening a leaderboard during this challenge where participants with pure machine-learning methods can participate. But beware: there is *very* little data in the public domain for this target. Ultimately this will be an exciting showdown between physics-based and data-driven methods: which is more able to extrapolate to new data?

<figure class="post-figure">
    <img src="{{ '/assets/images/news/blind-challenge-2027-workflow.png' | relative_url }}" alt="How the challenge works: 1, we provide 54 compounds as CXSMILES plus one X-ray structure; 2, you simulate on your own hardware with your own method (protein prep, ligand poses, alchemical setup, run simulations); 3, you submit predicted ΔG in kcal/mol as a CSV with setup notes; 4, we rank entries on two live leaderboards, free energy and machine learning.">
</figure>

## The competition will be centered around a viral variant of pandemic potential

The target of interest is the Dengue-2 NS2B-NS3 protease, which is a key enzyme in the viral replication cycle of the Dengue virus. Dengue-2 is a prolific serotype of the Dengue virus, which is a mosquito-borne virus that causes Dengue fever, a disease that affects millions of people worldwide. The Dengue virus is a significant public health concern, particularly in tropical and subtropical regions but with projected expansion to northern territories due to climate change. The NS2B-NS3 protease is essential for the virus's replication and maturation, making it a prime target for antiviral drug development. The compound series comes from [ASAP Discovery Consortium](https://asapdiscovery.org/)'s open pan-flavivirus antiviral programme, and was explored during hit-to-lead and lead-optimization against this serotype.

Because ASAP is an open science discovery center, we are able to provide you with very detailed experimental context that might help you decide on strategies for this challenge. Check out the [construct protocol](https://www.protocols.io/view/dengue-virus-serotype-2-ns2b-ns3-protease-fusion-c-4r3l2qqdpl1y/v2), the [assay protocol](https://www.protocols.io/view/assay-for-screening-of-compounds-that-inhibit-enzy-kqdg32m87v25/v1), the [Target Enabling Package](https://asapdiscovery.org/outputs/target-enabling-packages/#ASAP-DENV-NS2B-NS3) and this project’s [Target Candidate Profile](https://docs.google.com/presentation/d/1uZht18ZJnHuwMtwxY4prDBSl4SFMK-ics4ERhDgiJ2s/edit?slide=id.g285bac68500_0_340#slide=id.g285bac68500_0_340) (TCP).

## Details of the competition and how to participate

This will be a blind challenge, so the measured endpoint values will not be released until after the challenge has run its course. You will be able to monitor participants’ performance on our live leaderboard; we will use similar statistical analyses and leaderboard subsampling as with previous OpenADMET blind challenges.

The primary endpoint for this challenge will be the ranking coefficient Kendall’s τ, an interpretable statistic that embodies what matters to medicinal chemists: rank-ordering by potency. Submission will be straightforward: primarily we ask for a CSV file with your predictions (in kcal/mol) and any additional information and code you can give us about your system setup strategies: this way we will be able to disentangle what works well and what doesn’t. We will provide you with CXSMILES and a single X-ray structure as reference for compound pose generation. The series consists of 54 compounds with suitable dynamic range (2.4+ log units of biochemical potency).

This challenge will be run through HuggingFace and Discord just like previous challenges organized by OpenADMET. Also like previous challenges, participation is anonymous by default so unexpected performance can not be traced back to your organization. The live leaderboard on HuggingFace is populated with statistical analyses of participants’ entries; their data is validated on a subset of the test set. In January 2027, the first intermediate leaderboard (validated on the full test set) will be released. Full details on how this works and why we do it can be found on the challenge’s HuggingFace page.

<figure class="post-figure">
    <img src="{{ '/assets/images/news/blind-challenge-2027-timeline.png' | relative_url }}" alt="Challenge timeline: challenge announced; test set released 1 Nov 2026; intermediate deadline 15 Jan 2027, 23:59 UTC; intermediate leaderboard 25 Jan 2027; final submission deadline 25 Mar 2027, 23:59 UTC; final leaderboard from 1 Apr 2027, with talks at Alchemistry 2027. Predictions can be submitted from the test set release until the final deadline.">
</figure>

## You don’t own a room full of GPUs? You can still participate!

We understand that not everyone has access to a large cluster to run binding free energy calculation simulations on. Participants will be able to put in requests for licenses for system preparation and/or compute tokens with the following software vendors: Cresset, OpenEye, Rowan and potentially several more. Note that this will be on a first come first serve basis, that you will need to verify your identity and that the terms and offerings may differ between vendors – details to be announced.

## Other competitions to bite into – or cook your own

Go check out:

* [OpenBind’s Zika NS2B-NS3 ligand pose prediction challenge](https://openbind.uk/news/announcing-the-first-openbind-blind-challenge-zika-virus-ns2b-ns3-protease/)
* [The CYP blind challenge over at OpenADMET](https://huggingface.co/spaces/openadmet/cyp-challenge)

Would you like to build and stand up your own blind challenge portal, including a backend for hosting data and doing automated submission evaluations and leaderboard building? OpenADMET has recently published [a template for doing exactly this](https://github.com/OpenADMET/blind-challenge-template).

## Acknowledgements

The data featured in this challenge was generated by ASAP under NIH NIAID Antiviral Drug Discovery (AViDD) grant U19AI171399. OpenBind received funding from the UK Department of Science, Innovation and Technology under grant number G2-SCH-2025-06-16537. The OpenADMET team would like to thank Radial (part of the [Astera Institute](https://ror.org/00ydx1s47)) for continuing support of our blind challenge efforts.
