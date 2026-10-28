---
layout: challenge
title: Blind Challenge
# Everything under `challenge` drives the page header, link cards and 3D viewer.
# Leave a url empty ("") to show its button as "Available at launch".
# The challenge itself (data, submissions, leaderboards, full rules) lives on Hugging Face;
# this page summarises it and links there. Details below follow the Space's config.py.
challenge:
  eyebrow: Alchemistry 2027
  tagline: Predict binding free energies for 54 Dengue-2 NS2B-NS3 protease inhibitors before the experimental values are released.
  status: Opens November 1, 2026
  facts:
    - icon: bullseye
      label: Predict
      value: ΔG for 54 compounds
    - icon: calendar-check
      label: Submissions open
      value: November 1, 2026
    - icon: hourglass-end
      label: Final deadline
      value: March 25, 2027
    - icon: users
      label: Results
      value: Presented at the May 2027 workshop
  resources:
    - title: Challenge on Hugging Face
      icon: hugging-face
      text: Full description, rules and FAQ, the submission portal and the live leaderboards.
      button: Go to the challenge
      url: https://huggingface.co/spaces/openadmet/alchemistry-2027-challenge
    - title: Challenge dataset
      icon: database
      text: The 54 compounds as CXSMILES and a reference X-ray structure, released November 1.
      button: Get the data
      # Public from November 1: https://huggingface.co/datasets/openadmet/alchemistry-2027-antiviral-blind-challenge
      url: ""
    - title: Discuss on Discord
      icon: discord
      icon_style: brands
      text: Ask questions and talk with other participants and the organisers.
      button: Join the Discord
      url: https://discord.gg/fC3XGwEJW
  # Companies offering participants licences and compute; leave `logo` empty to show the name instead
  compute_support:
    - name: Cresset
      url: https://cresset-group.com/
      logo: /assets/images/sponsors/Cresset.png
    - name: OpenEye Cadence Molecular Sciences
      url: https://www.eyesopen.com/
      logo: /assets/images/sponsors/OpenEye.png
    - name: Rowan
      url: https://rowansci.com/
      logo: /assets/images/sponsors/Rowan.svg
  # Set to the Space's direct URL (https://<owner>-<space>.hf.space) to embed the leaderboard on this page
  leaderboard_embed: ""
  # Use `file:` instead of `pdb:` for a structure kept in the repo
  structure:
    pdb: 9T4P
    caption: "Dengue-2 NS2B-NS3 protease (PDB 9T4P), solved by the ASAP Discovery Consortium. The reference X-ray structure for pose generation is provided with the challenge dataset on Hugging Face."
---

## About the challenge

Alchemical free energy calculations are now a routine part of structure-enabled drug discovery, but the field lacks an open, prospective test of how well they work when the answer is not already known. The Alchemistry Blind Challenge provides one: predict binding free energies for 54 compounds whose experimental potencies have not been published, then see how your method compares once the measurements are revealed.

The compounds form a congeneric series from the [ASAP Discovery Consortium](https://asapdiscovery.org/)'s open pan-flavivirus antiviral programme, explored during hit-to-lead and lead optimisation against the Dengue-2 NS2B-NS3 protease. The series is centred on a single scaffold, so both relative and absolute free energy methods apply, and it is small enough to take part with modest hardware. Machine learning methods are welcome too and are ranked on their own leaderboard.

The challenge is organised by the Alchemistry 2027 committee with ASAP Discovery, [OpenADMET](https://openadmet.org/) and [OpenBind](https://openbind.uk/), and is hosted on Hugging Face, where you will find the data, the full rules and the submission portal. Top performers will be invited to present their work at the [2027 workshop]({{ '/' | relative_url }}).

## How it works

<ol class="challenge-steps">
    <li class="challenge-step">
        {% include icon.html name="book-open" %}
        <h3>Get the data</h3>
        <p>From November 1, download the 54 compounds as CXSMILES and a reference X-ray structure from Hugging Face.</p>
    </li>
    <li class="challenge-step">
        {% include icon.html name="atom" %}
        <h3>Compute</h3>
        <p>Predict a binding free energy for each compound in kcal/mol, with an uncertainty, using any method on your own hardware.</p>
    </li>
    <li class="challenge-step">
        {% include icon.html name="cloud-arrow-up" %}
        <h3>Submit</h3>
        <p>Upload a CSV of predictions and a short description of your method on Hugging Face. Entries are anonymous by default.</p>
    </li>
    <li class="challenge-step">
        {% include icon.html name="chart-line" %}
        <h3>Compare</h3>
        <p>Follow the live leaderboards, then hear the results and top-performing methods at the workshop.</p>
    </li>
</ol>

Relative (edge-based) methods also submit the ΔΔG for each edge of their perturbation network, and participants are asked to share their predicted poses. The exact file formats are described on the [challenge page](https://huggingface.co/spaces/openadmet/alchemistry-2027-challenge){: .intro-link}.

## Challenge target

The target is the NS2B-NS3 protease of Dengue virus serotype 2. The protease is essential for viral replication and maturation, which makes it a prime target for antiviral drugs against a mosquito-borne disease that affects millions of people worldwide. Drag to rotate the structure, hold Ctrl or ⌘ and scroll (or pinch) to zoom, and Ctrl-drag to move it.

{% include structure_viewer.html pdb=page.challenge.structure.pdb file=page.challenge.structure.file ligand=page.challenge.structure.ligand caption=page.challenge.structure.caption %}

Because ASAP is an open science discovery centre, the experimental details behind the data are public: the [construct protocol](https://www.protocols.io/view/dengue-virus-serotype-2-ns2b-ns3-protease-fusion-c-4r3l2qqdpl1y/v2){: .intro-link}, the [assay protocol](https://www.protocols.io/view/assay-for-screening-of-compounds-that-inhibit-enzy-kqdg32m87v25/v1){: .intro-link} and the [Target Enabling Package](https://asapdiscovery.org/outputs/target-enabling-packages/#ASAP-DENV-NS2B-NS3){: .intro-link}.

{% if page.challenge.leaderboard_embed and page.challenge.leaderboard_embed != "" %}
## Live leaderboard

<iframe class="challenge-embed" src="{{ page.challenge.leaderboard_embed }}" title="Blind challenge leaderboard" loading="lazy"></iframe>
{% endif %}

## Timeline

All submission deadlines are 23:59 UTC.

| Milestone | Date |
|-----------|------|
| Challenge announced | October 22, 2026 |
| Test set released and submissions open | November 1, 2026 |
| Deadline for the intermediate leaderboard | January 15, 2027 |
| Intermediate leaderboard released | January 25, 2027 |
| Submissions close | March 25, 2027 |
| Final leaderboard released | From April 1, 2027 |
| Results discussed at the workshop | May 3–5, 2027 |
{:.dates-table}

## Evaluation

The primary metric is Kendall's τ, which measures how well a method ranks the compounds by potency, the question that matters most to medicinal chemists. The leaderboards also report Spearman's ρ, Pearson R², ST-RAE and the mean absolute error. Until the intermediate leaderboard, live scores are computed on a subset of the test set. The full scoring protocol is described on the [challenge page](https://huggingface.co/spaces/openadmet/alchemistry-2027-challenge){: .intro-link}.

## Compute support

You don't need a room full of GPUs to take part. Participants will be able to request software licences for system preparation and compute tokens from the companies below, on a first-come, first-served basis. Terms and offerings differ between companies, and details will be announced.

<div class="challenge-partners">
    {%- for company in page.challenge.compute_support %}
    <a href="{{ company.url }}" target="_blank" rel="noopener" title="{{ company.name }}">
        {%- if company.logo and company.logo != "" %}
        <img src="{{ company.logo | relative_url }}" alt="{{ company.name }}">
        {%- else %}
        <span class="challenge-sponsor-name">{{ company.name }}</span>
        {%- endif %}
    </a>
    {%- endfor %}
</div>

## Questions

Email [alchemistry@omsf.io](mailto:alchemistry@omsf.io){: .intro-link} with any questions about the challenge. Announcements will also be posted on the [Latest News]({{ '/news/' | relative_url }}){: .intro-link} page.

## Acknowledgments

The challenge is run in collaboration with ASAP Discovery, OpenADMET and OpenBind. The data were generated by ASAP under NIH NIAID Antiviral Drug Discovery (AViDD) grant U19AI171399. We thank [Open Free Energy](https://openfree.energy){: .intro-link} and the [Open Molecular Software Foundation (OMSF)](https://omsf.io){: .intro-link} for their support of the Alchemistry Blind Challenge.

<div class="challenge-partners">
    <a href="https://openfree.energy" target="_blank" rel="noopener" title="Open Free Energy">
        <img src="{{ '/assets/images/partners/OpenFE.png' | relative_url }}" alt="Open Free Energy">
    </a>
    <a href="https://omsf.io" target="_blank" rel="noopener" title="Open Molecular Software Foundation">
        <img src="{{ '/assets/images/partners/OMSF.png' | relative_url }}" alt="Open Molecular Software Foundation">
    </a>
</div>
