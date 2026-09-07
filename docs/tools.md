---
title: Tools
nav_order: 3
---

<!--
==============================================================================
TEMPLATE — copy the block below into the right section and fill it in.

### Tool name

**Python** · MIT licence · Maintained by: Name Surname
[Repository](https://github.com/...) · [Documentation](https://...)

**AI angle:** one line — what the AI/ML component does inside the tool.

<details markdown="1">
<summary>More</summary>

Two to four sentences: what problem the tool solves, who it is for, and how to
get started with it. Written for someone deciding whether it is useful to them.

</details>

Notes:
- The <details> block is optional — drop it if you have no description yet.
  Keep the blank lines inside it and the markdown="1" attribute.
- The home page counts entries by counting the level-3 headings in this file, and
  subtracts one for the example heading above. Keep exactly one example heading in
  this comment, and do not write a level-3 heading marker inline anywhere else.
==============================================================================
-->

# Tools

Software, models, and datasets released by the lab and its spin-offs.

## AI models and applications

Tools where a trained model does the work.

### DecarbAI Demands

Python · Apache 2.0 · Developed under the Innosuisse **DecarbAI** project, a UK–Switzerland
bilateral research collaboration
ML models and methodology: Hassan Bazazzadeh and Georgios Mavromatidis, Urban Energy Systems
Laboratory, Empa
[Repository](https://github.com/urban-sympheny/decarbai-demands)

**AI angle:** Per-city, per-building-type XGBoost ensembles with PCA feature reduction,
replacing a full building simulation with a model that answers immediately.

<details markdown="1">
<summary>More</summary>

Producing an hourly energy demand profile for a building normally means setting up and running
a simulation. DecarbAI Demands predicts the full year — all 8760 hours of heating, cooling,
electricity, and domestic hot water demand — for Swiss buildings directly from 17 building
characteristics such as dimensions, construction year, window-to-wall ratios, and insulation
values. It runs as an interactive Dash dashboard. Predictions are most reliable when the inputs
fall inside the ranges the models were trained on.

</details>

## AI-ready data frameworks

Infrastructure that makes energy data usable by machine-learning methods in the first place —
harmonised, documented, and machine-readable. See also
[Digicities]({{ '/docs/projects/' | relative_url }}) under projects.

### MOTEL — Methodology for Open Technology Data in Energy Models

Empa Urban Energy Systems Lab with the ETH Energy Science Center, supported by the ETH Board's
Open Research Data Program
[Platform](https://uesl-empa.github.io/motel-platform/) ·
[Repository](https://github.com/uesl-empa/motel-platform)

**AI angle:** A local large language model (Ollama, qwen3:14b) does the harmonisation work —
standardising technology names, semantically matching records to existing registries when no
exact match exists, and filling in missing schema fields.

<details markdown="1">
<summary>More</summary>

The cost, efficiency, and lifetime assumptions behind energy system models are usually
scattered across spreadsheets and model-specific files, which makes them hard to trace and
almost impossible to compare between studies. MOTEL provides a reproducible workflow for
preparing, harmonising, documenting, and reusing that technology data. It runs in two stages —
ingestion and harmonisation, then ontology mapping — turning heterogeneous source material
into linked, machine-readable datasets suitable for knowledge graphs.

</details>
