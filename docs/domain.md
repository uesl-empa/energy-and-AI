---
title: Urban Energy Systems
nav_order: 3
---

# Urban Energy Systems

We are not an AI group that happens to look at energy. We are an urban energy systems
laboratory that applies AI — and that ordering matters. The methods on this site were built
against real building stock, real measured data, and real decisions that cities and utilities
have to make, which is what keeps them useful outside a benchmark.

## Modelling platforms we build and maintain

Open-source tools developed in the lab, most of them physics- or optimisation-based rather than
learned. They are the substrate the machine-learning work attaches to.

**[CESAR-P](https://github.com/uesl-empa/cesar-p-core)** — Combined Energy Simulation And
Retrofitting. Calculates energy demand bottom-up for a district or larger site, running
EnergyPlus simulations to estimate heating, cooling, and hot water demand together with costs,
emissions, and the effect of retrofit measures. With clustering and upscaling it reaches
national scale.

**[ehubX](https://github.com/uesl-empa/ehubx)** — Energy system design and operation posed as
mixed-integer linear programming: which technologies to install, at what size, and how to run
them.

**[Digicities platform and ontology](https://digicities.info/)** — Data architecture, semantic
models, and digital twins for energy planning at municipal and utility scale.

**[geoninja](https://github.com/uesl-empa/geoninja)** — Geospatial analysis for Aquifer Thermal
Energy Storage feasibility.

**[NESTli](https://github.com/uesl-empa/nestli)** — Benchmarking building automation and control
systems.

**[Dynamic carbon factor tool](https://github.com/uesl-empa/dynamic-carbon-factor-tool)** —
Time-resolved carbon intensity of the Swiss electricity grid.

## Testing on real buildings

Methods developed here are validated on occupied buildings rather than only in simulation. The
transfer-learning work on this site, for instance, uses measurements from the UMAR unit of the
**NEST** demonstrator building in Dübendorf, and the reinforcement-learning heating controller
was run as a living lab experiment rather than a simulation study alone. Real buildings behave
in ways that expose what a model got wrong.

NEST also serves as a Leader Pilot in
[ENERGENIUS]({{ '/docs/projects/' | relative_url }}), the site that trials the most advanced
tooling before it is adapted for wider deployment.

## Who we work with

**Federal and national.** The Swiss Federal Office of Energy (SFOE) and Innosuisse fund work
represented on this site, including [Digicities]({{ '/docs/projects/' | relative_url }}) and the
DecarbAI project behind [DecarbAI Demands]({{ '/docs/projects/' | relative_url }}).

**Cities, cantons, and utilities.** Municipal and utility energy planning is the setting these
tools are built for — CESAR-P and ehubX exist to answer questions about a specific district,
city, or supply area, and Digicities is explicitly about the data barriers those organisations
run into.

**Academic partners.** MOTEL is built with the **ETH Energy Science Center**, supported by the
ETH Board's Open Research Data Program. Much of the control and optimisation work on this site
is joint with academic groups in Switzerland and abroad.

**International.** ENERGENIUS runs under **Horizon Europe** across 17 partners and 10
demonstrator sites. Digicities runs under **ERA-Net Smart Energy Systems** with funding from
SFOE, the Austrian Research Promotion Agency (FFG), and the EU Horizon 2020 programme. DecarbAI
is a **UK–Switzerland** bilateral collaboration.

## Where AI enters

The domain sets the problems; AI addresses specific bottlenecks within them. See the
[Overview]({{ '/docs/' | relative_url }}) for how the two connect, and
[Research papers]({{ '/docs/papers/' | relative_url }}) for the work itself.
