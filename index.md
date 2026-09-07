---
layout: default
title: Home
---

{%- assign papers_page = site.pages | where: "title", "Papers" | first -%}
{%- comment -%}
Counts the "### " entry headings in docs/papers.md. Subtracts 2: one because
splitting on N occurrences yields N+1 parts, one for the example heading inside
that file's template comment. If you change the template comment, check this.
{%- endcomment -%}
{%- assign paper_count = papers_page.content | split: '### ' | size | minus: 2 -%}

# AI & Urban Energy Systems

Artificial intelligence is changing how energy systems are designed, forecast, and operated —
turning models that once took hours to run into ones that answer in seconds, and letting
controllers learn from a building instead of being hand-tuned for it.

At the **[Urban Energy Systems Laboratory (UESL)](https://www.empa.ch/web/s313)** at Empa, this
is not a side interest. Machine learning runs through our work on buildings, districts, and
grids: **{{ paper_count }} of our publications** apply AI methods to energy questions, and two
spin-off companies have taken that research to market.

[Browse the publications →]({{ '/docs/papers/' | relative_url }})

## Where we apply AI

**Forecasting.** Predicting electricity demand, and the flexibility that EV charging offers the
grid — including transformer models that use timetables and planned occupancy to see ahead
rather than only backwards.

**Physics-consistent learning.** Neural networks whose structure guarantees they obey physical
laws, so a model cannot produce a confident but impossible answer when it meets conditions it
was never trained on.

**Control and optimisation.** Deep reinforcement learning for price-responsive heating, and
Bayesian optimisation that tunes controllers while they run without breaching operating limits.

**System identification.** Machine-learning tooling applied to building mathematical models of
real systems from measured data, with stability guaranteed by construction.

**Uncertainty quantification.** Predicting ranges rather than single numbers, so that weather,
occupant behaviour, and long-term investment risk are represented honestly.

## Working with us

We are open to collaboration in this direction — joint research projects, industry partnerships,
student projects, and applications of these methods to new energy domains. If something here is
relevant to your work, please get in touch.

## Spin-offs and commercial applications

**[viboo AG](https://viboo.io)**
Physics-informed machine learning algorithms for predictive HVAC control.

**[Sympheny AG](https://sympheny.com)**
Spatial data analytics and energy scenario optimisation platform.

## Contact

**[Georgios Mavromatidis](https://www.empa.ch/web/mag)** — Head of Laboratory
[georgios.mavromatidis@empa.ch](mailto:georgios.mavromatidis@empa.ch)

**[Robin Mutschler](https://www.empa.ch/web/muro)** — Leader of Marco-Energy Systems Group
[robin.mutschler@empa.ch](mailto:robin.mutschler@empa.ch)

**[Barton Yi-Chung Chen](https://www.empa.ch/web/chyi)** — Scientist for Energy Systems Modelling
[yi-chung.chen@empa.ch](mailto:yi-chung.chen@empa.ch)
