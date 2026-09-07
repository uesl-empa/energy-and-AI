---
title: Tools
nav_order: 3
---

<!--
==============================================================================
TEMPLATE — copy the block below for each new tool and fill it in.

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
- The home page counts entries by counting "### " in this file, and subtracts one
  for the example heading above. Keep exactly one example heading in this comment.
==============================================================================
-->

# Tools

Software, models, and datasets released by the lab.

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
