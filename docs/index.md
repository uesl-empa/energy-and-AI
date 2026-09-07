---
title: Overview
nav_order: 0
---

# Overview

What the lab is doing with AI in energy research, grouped by type.

- [Papers]({{ '/docs/papers/' | relative_url }}) — publications applying AI and machine learning
- [Projects]({{ '/docs/projects/' | relative_url }}) — research projects behind the methods
- [Tools]({{ '/docs/tools/' | relative_url }}) — software, models, and datasets we release
- [Urban Energy Systems]({{ '/docs/domain/' | relative_url }}) — the domain this work sits in,
  the platforms we maintain, and who we work with

## Where AI fits

The lab's core work is modelling energy at the scale of buildings, districts, and cities, and
most of that rests on physics and optimisation rather than machine learning — simulation
platforms like CESAR-P and optimisation frameworks like ehubX, described on the
[Urban Energy Systems]({{ '/docs/domain/' | relative_url }}) page.

Neither is an AI tool. But they define where AI becomes useful, and most of our machine-learning
work sits at one of these five joints:

**Speed.** A detailed simulation that takes hours cannot be run thousands of times inside an
optimisation loop or a design study. Learned surrogate models stand in for the simulation and
answer in seconds.

**Accuracy where physics runs out.** Real buildings deviate from their models, because of
occupants, control quirks, and construction reality. Hybrid and physics-consistent approaches
correct a physical model with measured data while keeping its predictions physically possible.

**Inputs.** These models need forecasts — demand, prices, occupancy, available flexibility —
and forecasting is where machine learning is strongest.

**Operation.** Designing a system is one problem; running it well day to day is another.
Reinforcement learning and learned controllers close that loop.

**Data foundations.** None of the above works on data that is scattered, undocumented, or
locked away. AI-ready data frameworks — harmonised, machine-readable, and traceable — are a
prerequisite rather than an afterthought, and building them is a research problem in itself.
