---
layout: default
title: Home
---

{%- comment -%}
Counts the "### " entry headings in each docs page so these numbers cannot go
stale. Subtracts 2: one because splitting on N occurrences yields N+1 parts,
one for the example heading inside each file's template comment.
{%- endcomment -%}
{%- assign papers_page = site.pages | where: "title", "Research papers" | first -%}
{%- assign work_page = site.pages | where: "title", "Projects and Tools" | first -%}
{%- assign paper_count = papers_page.content | split: '### ' | size | minus: 2 -%}
{%- assign work_count = work_page.content | split: '### ' | size | minus: 2 -%}

# AI & Urban Energy Systems

Artificial intelligence is changing how energy systems are designed, forecast, and operated.
At the **[Urban Energy Systems Laboratory (UESL)](https://www.empa.ch/web/s313)** at Empa it
runs through our work on buildings, districts, and grids.

- **[{{ paper_count }} papers]({{ '/docs/papers/' | relative_url }})** published since 2023,
  applying AI and machine learning to energy questions
- **[{{ work_count }} projects and tools]({{ '/docs/projects-and-tools/' | relative_url }})**
  built around AI methods, including software we release openly

## What we can provide

**Knowledge, research capacity, and experience.** Years of published, peer-reviewed work
applying AI across forecasting, physics-consistent modelling, control, and optimisation in
real energy systems — not a one-off pilot.

**Network.** Established links to federal bodies, cities and utilities, and academic partners
across Switzerland and Europe, built through the projects on this site.

**Data, platforms, and tools.** Open simulation and optimisation platforms, demonstrator
buildings, and AI-ready data frameworks already running in the urban energy systems domain —
see [Urban Energy Systems]({{ '/docs/domain/' | relative_url }}) for what we maintain and who
we work with.

**Openness to joint development.** We are open to collaboration in this direction — joint
research, industry partnerships, and student projects applying AI to your energy questions.
If something here is relevant to your work, please get in touch.

## Contact

**[Georgios Mavromatidis](https://www.empa.ch/web/mag)** — Head of Laboratory
[georgios.mavromatidis@empa.ch](mailto:georgios.mavromatidis@empa.ch)

**[Robin Mutschler](https://www.empa.ch/web/muro)** — Leader of Marco-Energy Systems Group
[robin.mutschler@empa.ch](mailto:robin.mutschler@empa.ch)
