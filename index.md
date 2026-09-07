---
layout: default
title: Home
---

{%- comment -%}
Counts the "### " entry headings in each docs page so these numbers cannot go
stale. Subtracts 2: one because splitting on N occurrences yields N+1 parts,
one for the example heading inside each file's template comment.
{%- endcomment -%}
{%- assign papers_page = site.pages | where: "title", "Papers" | first -%}
{%- assign projects_page = site.pages | where: "title", "Projects" | first -%}
{%- assign tools_page = site.pages | where: "title", "Tools" | first -%}
{%- assign paper_count = papers_page.content | split: '### ' | size | minus: 2 -%}
{%- assign project_count = projects_page.content | split: '### ' | size | minus: 2 -%}
{%- assign tool_count = tools_page.content | split: '### ' | size | minus: 2 -%}

# AI & Urban Energy Systems

Artificial intelligence is changing how energy systems are designed, forecast, and operated.
At the **[Urban Energy Systems Laboratory (UESL)](https://www.empa.ch/web/s313)** at Empa it
runs through our work on buildings, districts, and grids.

- **[{{ paper_count }} papers]({{ '/docs/papers/' | relative_url }})** published since 2023,
  applying AI and machine learning to energy questions
- **[{% if project_count > 0 %}{{ project_count }} projects{% else %}Projects{% endif %}]({{ '/docs/projects/' | relative_url }})**
  built around AI methods
- **[{% if tool_count > 0 %}{{ tool_count }} tools{% else %}Tools{% endif %}]({{ '/docs/tools/' | relative_url }})**
  we release as software, models, and datasets

We are open to collaboration in this direction — joint research, industry partnerships, and
student projects. If something here is relevant to your work, please get in touch.

## Contact

**[Georgios Mavromatidis](https://www.empa.ch/web/mag)** — Head of Laboratory
[georgios.mavromatidis@empa.ch](mailto:georgios.mavromatidis@empa.ch)

**[Robin Mutschler](https://www.empa.ch/web/muro)** — Leader of Marco-Energy Systems Group
[robin.mutschler@empa.ch](mailto:robin.mutschler@empa.ch)

**[Barton Yi-Chung Chen](https://www.empa.ch/web/chyi)** — Scientist for Energy Systems Modelling
[yi-chung.chen@empa.ch](mailto:yi-chung.chen@empa.ch)
