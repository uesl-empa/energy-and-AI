---
title: Papers
nav_order: 1
---

<!--
==============================================================================
TEMPLATE — copy the block below into the right sub-field section and fill it in.
Entries are newest-first within each section.

### Full title of the paper

**2024** · Surname A., Surname B., Surname C. et al. · *Journal or Conference*
[10.xxxx/yyyyy](https://doi.org/10.xxxx/yyyyy)

**AI method:** one line — what kind of AI/ML is used and what it does here.

<details markdown="1">
<summary>More</summary>

Two to four sentences on method, what it was used for, and how the AI part
relates to the energy question. Written for a non-specialist reader.

</details>

Notes:
- Authors: list the first three, then "et al." (list all if there are three or fewer).
- The <details> block is optional — drop it entirely if you have no summary yet.
  Keep the blank lines inside it and the markdown="1" attribute, or the text
  inside will not render properly.
- The home page counts entries by counting the level-3 headings in this file, and
  subtracts one for the example heading above. Keep exactly one example heading in
  this comment, and do not write a level-3 heading marker inline anywhere else.
==============================================================================
-->

# Papers

Publications from the lab involving artificial intelligence and machine learning, grouped by
what the AI is doing. Click **More** under an entry to read what the paper does.

{% capture newline %}
{% endcapture %}{% capture h2marker %}
## {% endcapture %}
{%- assign sections = page.content | split: h2marker -%}
<ul class="subfield-toc">
{%- for section in sections offset: 1 -%}
  {%- assign heading = section | split: newline | first | strip -%}
  {%- assign entries = section | split: '### ' | size | minus: 1 -%}
  <li>
    <a href="#{{ heading | slugify }}">{{ heading }}</a>
    <span>{{ entries }}</span>
  </li>
{%- endfor -%}
</ul>

## Forecasting and prediction

Learning patterns from historical data to predict demand, emissions, comfort, and available
flexibility.

### Integrating the expected future in load forecasts with contextually enhanced transformer models

**2026** · Theiler R., Von Krannichfeldt L., Sansavini G. et al. · *Energy Reports*
[10.1016/j.egyr.2026.109223](https://doi.org/10.1016/j.egyr.2026.109223)

**AI method:** Transformer models — the architecture behind modern language models — adapted
to energy load forecasting.

<details markdown="1">
<summary>More</summary>

Most forecasting methods look only at historical data, but operators often already know
something about the future: timetables, scheduled events, planned building occupancy. This
work reformulates forecasting so that such forward-looking context can be fed to a
transformer model alongside the history. On nationwide railway energy consumption, adding
timetable data cut the average forecasting error by 26.6%; on building energy using planned
office occupancy, by 56.3%.

</details>

### Machine learning approaches for the prediction of public EV charge point flexibility

**2025** · Bellizio F., Dijkstra B., Fertig A. et al. · *Sustainable Energy, Grids and Networks*
[10.1016/j.segan.2025.101657](https://doi.org/10.1016/j.segan.2025.101657)

**AI method:** Machine learning to predict how much scheduling flexibility public EV charging
points offer the grid.

### Data-driven personalized thermal comfort model for office workers in Switzerland

**2025** · Chatterjee A., Heer P. · *Journal of Physics: Conference Series*
[10.1088/1742-6596/3140/11/112008](https://doi.org/10.1088/1742-6596/3140/11/112008)

**AI method:** Learns individual comfort preferences from data rather than applying a single
standard comfort model to everyone.

### Non-Intrusive Load Monitoring (NILM) with very low-frequency data from smart meters in Switzerland

**2025** · Chatterjee A., Heer P.

**AI method:** Disaggregating total household consumption into individual appliances from
smart meter data alone.

### Machine learning approaches for predictions of CO₂ emissions in the building sector

**2024** · Giannelos S., Bellizio F., Strbac G. et al. · *Electric Power Systems Research*
[10.1016/j.epsr.2024.110735](https://doi.org/10.1016/j.epsr.2024.110735)

**AI method:** Machine learning models for predicting CO₂ emissions from buildings.

## Physics-consistent and hybrid modelling

Combining physical laws with learned components, so models stay accurate without producing
physically impossible answers.

### Integrating physics-based and data-driven approaches for probabilistic building energy modeling

**2026** · Von Krannichfeldt L., Orehounig K., Fink O. · *Energy and Buildings*
[10.1016/j.enbuild.2025.116838](https://doi.org/10.1016/j.enbuild.2025.116838)

**AI method:** Systematic comparison of five ways to combine physics-based building models
with neural networks, under uncertainty.

<details markdown="1">
<summary>More</summary>

Building energy models are traditionally either physics-based or purely learned from data;
hybrids try to get the strengths of both. This study compares five hybrid strategies for
predicting building thermodynamics probabilistically — that is, predicting a range rather
than a single number, so that weather and occupant uncertainty is represented. Residual
learning with a feedforward neural network performed best on average, and was the only
approach that still produced physically sensible predictions on conditions it had not seen
during training.

</details>

### Fully data-driven and modular building thermal control with physically consistent modeling

**2025** · Montazeri M., Remlinger C., Bejar Haro B. et al. · *Applied Energy*
[10.1016/j.apenergy.2025.125770](https://doi.org/10.1016/j.apenergy.2025.125770)

**AI method:** Building thermal control learned entirely from data, with model structure
constrained so its predictions stay physically consistent.

### Combining physics-based and data-driven modeling for building energy systems

**2025** · Von Krannichfeldt L., Orehounig K., Fink O. · *Applied Energy*
[10.1016/j.apenergy.2025.125853](https://doi.org/10.1016/j.apenergy.2025.125853)

**AI method:** Hybrid modelling that pairs physics-based building models with learned
components.

### Towards scalable physically consistent neural networks: an application to data-driven multi-zone thermal building models

**2023** · Di Natale L., Svetozarevic B., Heer P. et al. · *Applied Energy*
[10.1016/j.apenergy.2023.121071](https://doi.org/10.1016/j.apenergy.2023.121071)

**AI method:** Physically Consistent Neural Networks (PCNNs) — neural networks whose structure
mathematically guarantees they obey physical laws, rather than merely fitting the data.

<details markdown="1">
<summary>More</summary>

An ordinary neural network can predict building temperatures accurately while remaining
entirely ignorant of physics, which makes it capable of confidently producing impossible
answers in situations it was not trained on — a real risk when the predictions drive
decisions about a physical building. PCNNs constrain the architecture so physical consistency
is guaranteed by construction, and this work scales them to multi-zone building temperature
dynamics. They reach state-of-the-art accuracy — even beating unconstrained neural networks —
and improve on other physically consistent methods by 17–35%.

</details>

### Physically consistent neural ODEs for learning multi-physics systems

**2023** · Zakwan M., Di Natale L., Svetozarevic B. et al. · *22nd IFAC World Congress*
[10.1016/j.ifacol.2023.10.079](https://doi.org/10.1016/j.ifacol.2023.10.079)

**AI method:** Neural ODEs constrained by port-Hamiltonian structure so that learned models
cannot violate the laws of thermodynamics.

<details markdown="1">
<summary>More</summary>

Neural networks that learn system dynamics from data are usually physics-agnostic, so their
predictions can drift into physically impossible territory. This work embeds the learning
inside an irreversible port-Hamiltonian formulation, so the parameters are learned from data
while thermodynamic consistency holds by construction. It is demonstrated on building
thermodynamics and on a gas-piston system.

</details>

### Regularised learning with selected physics for power system dynamics

**2023** · Xie H., Bellizio F., Cremer J. L. et al. · *IEEE Belgrade PowerTech 2023*
[10.1109/PowerTech55446.2023.10202688](https://doi.org/10.1109/PowerTech55446.2023.10202688)

**AI method:** Selected Physics Informed Neural Networks (SPINNs) — a step beyond standard
physics-informed networks, feeding only chosen parts of the physical model into training.

<details markdown="1">
<summary>More</summary>

Checking whether a power system will stay stable under changing operating conditions is
computationally expensive, so machine learning is often used to speed it up — but purely
learned models throw away everything already known about the system's physics. SPINNs use a
two-level network, one predicting generator rotor angles and one adapting to varying
operating conditions. On an IEEE 9-bus test system this cut the training data required, and
the model successfully extrapolated to timescales longer than anything in its training set.

</details>

## Learning-based control

Controllers that learn how to operate a system from data or experience, rather than being
hand-designed for it.

### Price-responsive control using deep reinforcement learning for heating systems: simulation and living lab experiment

**2025** · Mokhtari R., Montazeri M., Cai H. et al. · *Energy*
[10.1016/j.energy.2025.138517](https://doi.org/10.1016/j.energy.2025.138517)

**AI method:** Deep reinforcement learning for heating control that responds to electricity
prices, tested both in simulation and in a real occupied building.

### Prescribing optimal health-aware operation for urban air mobility with deep reinforcement learning

**2025** · Montazeri M., Kulkarni C. S., Fink O. · *Reliability Engineering & System Safety*
[10.1016/j.ress.2025.110897](https://doi.org/10.1016/j.ress.2025.110897)

**AI method:** Deep reinforcement learning for operating urban air mobility vehicles in a way
that accounts for component health and degradation.

### Transfer learning for thermal building modeling

**2025** · Varathan A., Remlinger C., Montazeri M. et al. · *IEEE Conference on Control Technology and Applications (CCTA 2025)*
[10.1109/CCTA53793.2025.11151506](https://doi.org/10.1109/CCTA53793.2025.11151506)

**AI method:** Transfer learning — reusing a model trained on one building to model another
with far less data.

<details markdown="1">
<summary>More</summary>

Data-driven building models need a lot of measurements, which new buildings simply do not
have yet. This study tests several transfer-learning strategies for carrying a model trained
on one building over to another, using data from the UMAR unit of the NEST building in
Dübendorf and from multiple US cities. Models adapted this way come close to the accuracy of
models trained directly on the target building, and an ensemble of models transferred from
several sources can beat it outright.

</details>

### Data-driven predictive control for demand side management: theoretical and experimental results

**2024** · Yin M., Cai H., Gattiglio A. et al. · *Applied Energy*
[10.1016/j.apenergy.2023.122101](https://doi.org/10.1016/j.apenergy.2023.122101)

**AI method:** Predictive control built directly from measured data instead of a hand-built
physical model, validated experimentally.

### Computationally efficient reinforcement learning: targeted exploration leveraging simple rules

**2023** · Di Natale L., Svetozarevic B., Heer P. et al. · *IEEE Conference on Decision and Control (CDC 2023)*
[10.1109/CDC49753.2023.10383956](https://doi.org/10.1109/CDC49753.2023.10383956)

**AI method:** Makes reinforcement learning cheaper to train by using simple known rules to
steer where the algorithm explores.

## Optimisation and controller tuning

Finding good settings and designs when every trial is expensive and constraints must not be
breached — largely Bayesian optimisation and learned surrogate models.

### Utilizing Artificial Intelligence (AI) for the optimal design of geothermal cogeneration systems in zero energy building

**2025** · Assareh E., Zoghi M., Zare A. et al. · *Results in Engineering*
[10.1016/j.rineng.2025.104873](https://doi.org/10.1016/j.rineng.2025.104873)

**AI method:** AI-driven optimisation of geothermal cogeneration system design for zero-energy
buildings.

### AI-aided surrogate model for prediction of HVAC optimization strategies in future conditions in the face of climate change

**2025** · Bazazzadeh H., Hoseinzadeh S., Mohammadi M. M. et al. · *Energy Reports*
[10.1016/j.egyr.2025.01.033](https://doi.org/10.1016/j.egyr.2025.01.033)

**AI method:** An AI surrogate model — a fast learned stand-in for a slow simulation — used to
find HVAC optimisation strategies under future climate scenarios.

### Violation-aware contextual Bayesian optimization for controller performance optimization with unmodeled constraints

**2024** · Xu W., Jones C. N., Svetozarevic B. et al. · *Journal of Process Control*
[10.1016/j.jprocont.2024.103212](https://doi.org/10.1016/j.jprocont.2024.103212)

**AI method:** Bayesian optimisation for tuning controllers, designed to limit how often it
violates constraints it has no model for while searching.

### Data-driven adaptive building thermal controller tuning with constraints: a primal–dual contextual Bayesian optimization approach

**2024** · Xu W., Svetozarevic B., Di Natale L. et al. · *Applied Energy*
[10.1016/j.apenergy.2023.122493](https://doi.org/10.1016/j.apenergy.2023.122493)

**AI method:** Contextual Bayesian optimisation that tunes a building thermal controller
automatically while respecting operating constraints.

### Principled Bayesian optimisation in collaboration with human experts

**2024** · Xu W., Adachi M., Jones C. N. et al. · *NeurIPS 2024*

**AI method:** Bayesian optimisation that incorporates human expert input into the search,
with guarantees on the result.

### Principled preferential Bayesian optimization

**2024** · Xu W., Wang W., Jiang Y. et al. · *International Conference on Machine Learning (ICML 2024), PMLR 235*

**AI method:** Bayesian optimisation driven by preference comparisons rather than numeric
measurements — useful where "better" can be judged but not measured.

### Primal-dual contextual Bayesian optimization for control system online optimization with time-average constraints

**2023** · Xu W., Jiang Y., Svetozarevic B. et al. · *IEEE Conference on Decision and Control (CDC 2023)*
[10.1109/CDC49753.2023.10383653](https://doi.org/10.1109/CDC49753.2023.10383653)

**AI method:** Bayesian optimisation that tunes a running control system online when both the
goal and the constraints are unknown functions disturbed by outside conditions.

<details markdown="1">
<summary>More</summary>

Tuning a controller while it runs means searching for better settings without a model of how
those settings affect performance or whether they will breach safety limits. This algorithm
provably converges towards the moving optimum while keeping the *average* constraint
violation at zero, and is demonstrated on a chemical reactor tuning problem — where competing
methods either perform poorly or breach constraints badly.

</details>

### Constrained efficient global optimization of expensive black-box functions

**2023** · Xu W., Jiang Y., Svetozarevic B. et al. · *International Conference on Machine Learning (ICML 2023), PMLR 202*

**AI method:** Optimising expensive-to-evaluate functions under constraints, where each trial
costs real time or money so the number of trials must be kept small.

## System identification, planning and grid applications

Learning models of real systems from measurements, and applying AI at the scale of grids,
fleets, and long-term investment decisions.

### Machine learning-based uncertainty quantification in capacity expansion models

**2026** · Shaltout Y., Upadhyay A., Oudalov A. et al. · *Energy and AI*
[10.1016/j.egyai.2026.100802](https://doi.org/10.1016/j.egyai.2026.100802)

**AI method:** Machine learning for uncertainty quantification in energy system capacity
expansion models.

### A self-assessment framework for evaluating efficiency of data centers

**2026** · Kuzay M., Demirel E., Bayraktar B. et al. · *Energy Informatics*
[10.1186/s42162-026-00652-7](https://doi.org/10.1186/s42162-026-00652-7)

### SIMBa: system identification methods leveraging backpropagation

**2025** · Di Natale L., Zakwan M., Heer P. et al. · *IEEE Transactions on Control Systems Technology*
[10.1109/TCST.2024.3477301](https://doi.org/10.1109/TCST.2024.3477301)

**AI method:** Uses backpropagation — the training algorithm behind neural networks — to fit
classical control models, with stability guaranteed by construction.

<details markdown="1">
<summary>More</summary>

System identification means building a mathematical model of how a system behaves from
measured data, which is the first step in designing a controller for it. SIMBa applies
machine-learning optimisation tooling to this classical problem while mathematically
guaranteeing the resulting model is stable, and can be told to respect known structure or
known values in the system. It consistently outperforms traditional subspace identification
methods, and is released as an open-source toolbox.

</details>

### Data-driven incentive mechanisms for federated learning in vehicular networks

**2025** · Fathi F., Montazeri M., Naraabi B. et al. · *IEEE Transactions on Vehicular Technology*
[10.1109/TVT.2025.3547866](https://doi.org/10.1109/TVT.2025.3547866)

**AI method:** Federated learning — training a shared model across many vehicles without any
of them handing over their raw data — plus deep neural networks used to design the
participation incentives.

<details markdown="1">
<summary>More</summary>

Federated learning lets vehicles collaboratively train a model while keeping their data
local, which protects privacy but means participants must be given a reason to spend their
computing resources. This work designs a contract between roadside units and vehicles that
rewards them according to the quality of the data they contribute, and is the first to use
deep neural networks to compute near-optimal such contracts. A traffic sign recognition case
study demonstrates the approach.

</details>

### High-performance office building: a novel, designerly and data-driven approach to integrating shading types and HVAC system details

**2025** · Azimi M., Mahdavinejad M., Hosseini S. M. et al. · *Case Studies in Thermal Engineering*
[10.1016/j.csite.2025.107108](https://doi.org/10.1016/j.csite.2025.107108)

### Stable linear subspace identification: a machine learning approach

**2024** · Di Natale L., Zakwan M., Svetozarevic B. et al. · *European Control Conference (ECC 2024)*
[10.23919/ECC64448.2024.10590843](https://doi.org/10.23919/ECC64448.2024.10590843)

**AI method:** Recasts a classical control-theory problem, subspace identification, as a
machine learning problem while guaranteeing model stability.

### Spatio-temporal data-driven and machine learning-based applications for transmission systems

**2024** · Segundo Sevilla F. R., Liu Y., Korba P. et al. · *IEEE Power & Energy Society General Meeting (PESGM 2024)*
[10.1109/PESGM51994.2024.10688546](https://doi.org/10.1109/PESGM51994.2024.10688546)

**AI method:** Survey of machine learning applications that exploit the spatial and temporal
structure of transmission grid measurements.
