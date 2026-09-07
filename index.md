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
  <h1>AI for Real-World Energy Systems</h1>
  <p class="hero-subtitle">
    We combine artificial intelligence with energy-system engineering, physics and real-world
    data to develop smarter ways to design, operate and optimise buildings, districts and
    energy systems.
  </p>
  <div class="cta-row">
    <a class="btn btn-primary" href="#collaboration">Work with us</a>
    <a class="btn btn-secondary" href="{{ '/docs/papers/' | relative_url }}">Explore our research</a>
  </div>
</section>

<section class="section">
  <h2>What we do</h2>
  <div class="card-grid">
    <div class="card">
      <h3>Forecasting</h3>
      <p>Energy demand, renewable generation and system behaviour.</p>
    </div>
    <div class="card">
      <h3>Physics + AI</h3>
      <p>Combining machine learning with physical knowledge and engineering constraints.</p>
    </div>
    <div class="card">
      <h3>AI-based control</h3>
      <p>Intelligent operation and optimisation of buildings and energy systems.</p>
    </div>
    <div class="card">
      <h3>Optimisation</h3>
      <p>AI and optimisation for complex design and operational problems.</p>
    </div>
    <div class="card">
      <h3>Data-driven modelling</h3>
      <p>System identification, surrogate models and digital representations.</p>
    </div>
    <div class="card">
      <h3>Energy-system applications</h3>
      <p>Buildings, districts, grids and other urban energy systems.</p>
    </div>
  </div>
</section>

<section class="section">
  <h2>Why work with UESL</h2>
  <div class="why-grid">
    <div class="why-item">
      <h3>Energy expertise</h3>
      <p>Deep knowledge of buildings, energy systems, grids and urban infrastructure.</p>
    </div>
    <div class="why-item">
      <h3>AI expertise</h3>
      <p>Experience with machine learning, optimisation, reinforcement learning,
        physics-informed AI and data-driven modelling.</p>
    </div>
    <div class="why-item">
      <h3>Real-world application</h3>
      <p>Research based on real energy data, physical systems and practical energy
        challenges.</p>
    </div>
    <div class="why-item">
      <h3>Research depth</h3>
      <p>A growing body of peer-reviewed research, projects and open-source tools.</p>
    </div>
  </div>
  <blockquote class="callout">
    We don't simply apply generic AI to energy problems. We combine AI with deep
    energy-system and engineering expertise.
  </blockquote>
</section>

<section class="section">
  <h2>Evidence</h2>
  <div class="stats-row">
    <div class="stat">
      <span class="stat-number">{{ paper_count }}+</span>
      <span class="stat-label">AI publications since 2023</span>
    </div>
    <div class="stat">
      <span class="stat-number">{{ project_count }}+</span>
      <span class="stat-label">AI projects &amp; platforms</span>
    </div>
  </div>
  <p class="stats-caption">Research across forecasting, modelling, control and optimisation.</p>

  <p class="section-lead">Selected research</p>
  <div class="research-links">
    <a href="{{ '/docs/papers/' | relative_url }}#forecasting-and-prediction">Forecasting</a>
    <a href="{{ '/docs/papers/' | relative_url }}#physics-consistent-and-hybrid-modelling">Physics-informed AI</a>
    <a href="{{ '/docs/papers/' | relative_url }}#learning-based-control">AI-based control</a>
  </div>
  <a class="text-link" href="{{ '/docs/papers/' | relative_url }}">See all research &rarr;</a>
</section>

<section class="section" id="collaboration">
  <h2>Work with us</h2>
  <p>
    We collaborate with industry, utilities, cities, technology companies and research
    organisations through:
  </p>
  <ul class="collab-list">
    <li>Joint research</li>
    <li>Applied AI projects</li>
    <li>Pilot and demonstration projects</li>
    <li>Joint funding proposals</li>
    <li>Data and technology partnerships</li>
  </ul>
</section>

<section class="closing-cta">
  <h2>Have an energy challenge where AI could help?</h2>
  <p>
    We are interested in collaborating on AI applications for buildings, districts and
    energy systems.
  </p>
  <a class="btn btn-primary" href="#contact">Get in touch</a>
</section>

<section class="section" id="contact">
  <h2>Contact</h2>
  <div class="contact-grid">
    <div class="contact-card">
      <h3><a href="https://www.empa.ch/web/mag">Georgios Mavromatidis</a></h3>
      <p>Head of Laboratory</p>
      <a href="mailto:georgios.mavromatidis@empa.ch">georgios.mavromatidis@empa.ch</a>
    </div>
    <div class="contact-card">
      <h3><a href="https://www.empa.ch/web/muro">Robin Mutschler</a></h3>
      <p>Leader of Marco-Energy Systems Group</p>
      <a href="mailto:robin.mutschler@empa.ch">robin.mutschler@empa.ch</a>
    </div>
  </div>
</section>
