---
title: Projects and Tools
nav_order: 2
---

<!--
==============================================================================
TEMPLATE — copy the block below and fill it in.

### Name

**Project** or **Tool** · funding, partners, licence, or language as appropriate
[Link](https://...) · [Repository](https://github.com/...)

**AI method:** one line — what kind of AI/ML is involved and what it does here.

<details markdown="1">
<summary>More</summary>

Two to four sentences: what it is for, what role AI plays, and who benefits.
Written for a non-specialist reader.

</details>

Notes:
- Start the metadata line with Project or Tool in bold so the two are still told
  apart without splitting the page into sections.
- The <details> block is optional — drop it if you have no description yet.
  Keep the blank lines inside it and the markdown="1" attribute.
- The home page counts entries by counting the level-3 headings in this file, and
  subtracts one for the example heading above. Keep exactly one example heading in
  this comment, and do not write a level-3 heading marker inline anywhere else.
==============================================================================
-->

# Projects and Tools

Research projects applying AI to energy questions, and the software, models, and data
frameworks that come out of them.

### ENERGENIUS

**Project** · Horizon Europe · 17 partners across 10 demonstrator sites in Europe · Empa
contributes the **NEST** demonstrator as a Leader Pilot
[Project site](https://energenius-project.eu/)

**AI method:** Digital twins and AI-driven energy analytics, delivered to end users through
gamified learning and an AI advisor rather than as specialist software.

<details markdown="1">
<summary>More</summary>

ENERGENIUS works on the gap between knowing how a building performs and actually doing
something about it, combining gamified learning with AI and digital twin models to make
energy saving accessible and human-centred. Our contribution is the digital twins, the
AI-driven energy analytics, and the interoperable data frameworks tested within the project,
alongside NEST as a Leader Pilot — the sites that set the standard with the most advanced
tooling before it is adapted for wider use. The collaboration gives us insight into how
digitalisation can turn energy performance data into strategies that measurably cut
consumption.

</details>

### Digicities

**Project** · ERA-Net Smart Energy Systems · Funded by the Swiss Federal Office of Energy
(SFOE), the Austrian Research Promotion Agency (FFG), and the EU Horizon 2020 programme
[Project site](https://digicities.info/) ·
[Platform](https://github.com/uesl-empa/digicities-platform) ·
[Ontology](https://github.com/uesl-empa/digicities-ontology)

**AI method:** Builds the machine-readable data foundation — semantic models, linked data, and
digital twins — that learning-based methods need before they can be applied to a real city's
energy system.

<details markdown="1">
<summary>More</summary>

Energy planning at municipal and utility scale is held back less by a shortage of methods than
by a shortage of usable data: the information exists, but it is fragmented across owners who
have good reasons not to share it freely. Digicities develops data architectures that automate
the integration of these sources into a digital twin of the energy system while preserving
data sovereignty and privacy, alongside a survey of grid operators and users to understand what
actually blocks and incentivises sharing.

</details>

### DecarbAI Demands

**Tool** · Python · Apache 2.0 · Developed under the Innosuisse **DecarbAI** project, a
UK–Switzerland bilateral research collaboration
ML models and methodology: Hassan Bazazzadeh and Georgios Mavromatidis, Urban Energy Systems
Laboratory, Empa
[Repository](https://github.com/urban-sympheny/decarbai-demands)

**AI method:** Per-city, per-building-type XGBoost ensembles with PCA feature reduction,
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

### MOTEL — Methodology for Open Technology Data in Energy Models

**Tool** · Empa Urban Energy Systems Lab with the ETH Energy Science Center, supported by the
ETH Board's Open Research Data Program
[Platform](https://uesl-empa.github.io/motel-platform/) ·
[Repository](https://github.com/uesl-empa/motel-platform)

**AI method:** A local large language model (Ollama, qwen3:14b) does the harmonisation work —
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
