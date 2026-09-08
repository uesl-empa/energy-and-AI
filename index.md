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
{%- assign projects_page = site.pages | where: "title", "Projects" | first -%}
{%- assign paper_count = papers_page.content | split: '### ' | size | minus: 2 -%}
{%- assign project_count = projects_page.content | split: '### ' | size | minus: 2 -%}

<section class="hero">
  <h1>AI &amp; Urban Energy Systems</h1>
  <p class="hero-subtitle">
    The <a href="https://www.empa.ch/web/s313">Urban Energy Systems Laboratory (UESL)</a> at
    <a href="https://www.empa.ch">Empa (Swiss Federal Laboratories for Materials Science and
    Technology)</a>, an
    <a href="https://ethrat.ch/en/eth-domain/portrait-eth-domain/">ETH Domain</a> research
    institute, researches how energy systems can be designed, operated and transformed towards
    a sustainable energy future.
  </p>
  <p class="hero-subtitle">
    AI and data-driven methods are increasingly part of this research, alongside
    energy-system modelling, optimisation, control and engineering.
  </p>
</section>

<section class="section">
  <h2>AI in our energy-system research</h2>
  <p class="lede">
    AI is becoming an increasingly useful tool in energy-system research. At UESL, we apply
    AI and machine-learning methods to problems in
    <a href="{{ '/docs/domain/' | relative_url }}">buildings, districts and energy systems</a>,
    combining them with our expertise in energy-system modelling, physics, optimisation and
    control.
  </p>
  <p class="lede">
    Our focus is not on developing AI methods for their own sake, but on investigating how AI
    can be applied to relevant energy-system challenges.
  </p>
</section>

<section class="section">
  <h2>Evidence of our research</h2>
  <p class="lede">
    Our work spans forecasting, physics-informed and hybrid modelling, learning-based control,
    optimisation and other applications of AI in energy systems.
  </p>

  <div class="stats-row">
    <a class="stat" href="{{ '/docs/papers/' | relative_url }}">
      <span class="stat-number">{{ paper_count }}+</span>
      <span class="stat-label">AI publications since 2023</span>
    </a>
    <a class="stat" href="{{ '/docs/projects/' | relative_url }}">
      <span class="stat-number">{{ project_count }}+</span>
      <span class="stat-label">AI related projects and platforms</span>
    </a>
  </div>

  <p class="section-lead">Research areas</p>
  <ul class="list-columns">
    <li><a href="{{ '/docs/papers/' | relative_url }}#forecasting-and-prediction">Forecasting and prediction</a></li>
    <li><a href="{{ '/docs/papers/' | relative_url }}#physics-consistent-and-hybrid-modelling">Physics-consistent and hybrid modelling</a></li>
    <li><a href="{{ '/docs/papers/' | relative_url }}#learning-based-control">Learning-based control</a></li>
    <li><a href="{{ '/docs/papers/' | relative_url }}#optimisation-and-controller-tuning">Optimisation and controller tuning</a></li>
    <li><a href="{{ '/docs/papers/' | relative_url }}#system-identification-planning-and-grid-applications">System identification, planning and grid applications</a></li>
  </ul>

  <a class="text-link" href="{{ '/docs/papers/' | relative_url }}">See all research &rarr;</a>
</section>

<section class="section" id="collaboration">
  <h2>Collaboration</h2>
  <p class="lede">
    We are interested in collaborating with researchers, technology groups and organisations
    with strong expertise in AI and machine learning who are interested in applying these
    methods to energy-system challenges. Potential areas include buildings, urban energy
    systems, energy networks, forecasting, control, optimisation and energy-system modelling.
  </p>
  <ul class="list-columns">
    <li>Joint research</li>
    <li>New applications of AI in energy systems</li>
    <li>Joint research proposals</li>
    <li>Applied research</li>
    <li>Experimental and demonstrator projects</li>
    <li>Collaboration with AI specialists</li>
  </ul>
</section>

<section class="section" id="contact">
  <h2>Contact</h2>
  <p class="lede">
    Interested in exploring AI applications for energy systems or a potential research
    collaboration?
  </p>
  <ul class="contact-list">
    <li>
      <a href="https://www.empa.ch/web/mag">Georgios Mavromatidis</a> — Head of Laboratory —
      <a href="mailto:georgios.mavromatidis@empa.ch">georgios.mavromatidis@empa.ch</a>
    </li>
    <li>
      <a href="https://www.empa.ch/web/muro">Robin Mutschler</a> — Leader of Marco-Energy
      Systems Group — <a href="mailto:robin.mutschler@empa.ch">robin.mutschler@empa.ch</a>
    </li>
  </ul>
</section>
