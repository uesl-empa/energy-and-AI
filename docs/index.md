---
title: Overview
nav_order: 0
---

# Overview

What the lab is doing with AI in energy research, grouped by type.

- [Papers]({{ '/docs/papers/' | relative_url }}) — publications applying AI and machine learning
- [Projects]({{ '/docs/projects/' | relative_url }}) — research projects behind the methods
- [Tools]({{ '/docs/tools/' | relative_url }}) — software, models, and datasets we release

## Where AI fits in urban energy systems

The lab's core work is modelling energy at the scale of buildings, districts, and cities, and
most of that rests on physics and optimisation rather than machine learning. Two open platforms
we build and maintain give the picture:

- **[CESAR-P](https://github.com/uesl-empa/cesar-p-core)** (Combined Energy Simulation And
  Retrofitting) calculates energy demand bottom-up for a district or larger site, running
  EnergyPlus building simulations to estimate heating, cooling, and hot water demand along with
  the costs, emissions, and effect of retrofit measures. With clustering and upscaling it
  reaches national scale.
- **[ehubX](https://github.com/uesl-empa/ehubx)** formulates energy system design and operation
  as mixed-integer linear programming problems — deciding what technologies to install and how
  to run them.

Neither is an AI tool. But they define where AI becomes useful, and most of our machine-learning
work sits at one of these four joints:

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

## Who the results are for

This work is aimed at the people who actually have to make these decisions in Switzerland and
beyond: cities and cantons planning their energy transition, federal bodies such as the Swiss
Federal Office of Energy, energy suppliers and grid operators, and building owners weighing
retrofits. That audience shapes the research — it is why uncertainty quantification, physical
consistency, and computational speed keep recurring as themes rather than accuracy alone.
