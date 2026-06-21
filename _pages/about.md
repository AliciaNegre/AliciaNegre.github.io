---
title: "About"
layout: gridlay
sitemap: false
permalink: /about/
---

## About

<div class="section-card">
<div class="pi-card">
<img src="{{ site.url }}{{ site.baseurl }}/images/{{ site.photo }}" class="pi-photo" alt="{{ site.name }}" loading="lazy">
<div>
<h3 class="pi-name">{{ site.name }}</h3>
<p style="font-style: italic; color: var(--text-secondary);">{{ site.title }}, {{ site.institution }}</p>
<div class="pi-links">
{% if site.email %}<a href="mailto:{{ site.email }}" class="icon-link" title="Email"><i class="fa-solid fa-envelope"></i></a>{% endif %}
{% if site.links.cv and site.links.cv != "" %}<a href="{{ site.url }}{{ site.baseurl }}/{{ site.links.cv }}" class="icon-link" title="CV"><i class="ai ai-cv"></i></a>{% endif %}
{% if site.links.google_scholar and site.links.google_scholar != "" %}<a href="{{ site.links.google_scholar }}" class="icon-link" title="Google Scholar"><i class="ai ai-google-scholar"></i></a>{% endif %}
{% if site.links.github and site.links.github != "" %}<a href="{{ site.links.github }}" class="icon-link" title="GitHub"><i class="fa-brands fa-github"></i></a>{% endif %}
{% if site.links.linkedin and site.links.linkedin != "" %}<a href="{{ site.links.linkedin }}" class="icon-link" title="LinkedIn"><i class="fa-brands fa-linkedin"></i></a>{% endif %}
{% if site.links.researchgate and site.links.researchgate != "" %}<a href="{{ site.links.researchgate }}" class="icon-link" title="ResearchGate"><i class="ai ai-researchgate"></i></a>{% endif %}
</div>
</div>
</div>
</div>

<div class="section-card" id="research">
<h3>Research</h3>
<p>My research lies at the interface of applied mathematics and quantum chemistry, with a focus on quantum embedding methods for strongly correlated systems. Click a topic to read more.</p>

<div class="chip-container" markdown="0">
<button type="button" class="chip" data-toggle-target="topic-dmet">Density-Matrix Embedding Theory</button>
<button type="button" class="chip" data-toggle-target="topic-grassmann">Grassmann Manifold Optimization</button>
<button type="button" class="chip" data-toggle-target="topic-scs">Strongly Correlated Quantum Systems</button>
<button type="button" class="chip" data-toggle-target="topic-esm">Electronic Structure Methods</button>
</div>

<div class="pub-collapse" id="topic-dmet"><p>Development and mathematical analysis of Density-Matrix Embedding Theory (DMET), a quantum embedding method that decomposes large strongly correlated quantum systems into smaller fragment problems coupled to a bath. My work introduces a generalized DMET framework that relaxes conventional constraints and allows for more flexible bath space construction.</p></div>

<div class="pub-collapse" id="topic-grassmann"><p>Analysis of the mathematical and numerical structure of optimization problems over the Grassmann manifold arising in quantum embedding methods. This includes identifying conditions under which a non-convex quadratic objective admits a globally optimal solution via a convex relaxation, and designing efficient Riemannian optimization and SCF algorithms.</p></div>

<div class="pub-collapse" id="topic-scs"><p>Study of quantum systems where electron-electron interactions cannot be treated perturbatively. Quantum embedding methods provide a divide-and-conquer strategy to make these problems computationally tractable while retaining the essential physics of strong correlations.</p></div>

<div class="pub-collapse" id="topic-esm"><p>Development of rigorous mathematical frameworks for electronic structure calculations, combining tools from functional analysis, optimization on manifolds, and numerical linear algebra to design and analyze ab initio methods in quantum chemistry.</p></div>
</div>

<div class="section-card">
<h3>Media</h3>
<ul>
<li><a href="https://www.isae-supaero.fr/isae-supaero-6/notre-newsroom/toutes-nos-actualites/zoom-sur-la-physique-quantique-a-lisae-supaero-un-parcours-etudiant/" target="_blank">Zoom sur la physique quantique à l'ISAE-SUPAERO : un parcours étudiant</a></li>
</ul>
</div>

<div class="section-card">
<h3>Outreach</h3>
<ul>
<li>Science outreach talks on astrophysics and quantum mechanics for middle and high school students (collège et lycée)</li>
</ul>
</div>

<div class="section-card">
<h3>Service</h3>
<ul>
<li>Member of the Finance Committee, <a href="https://cjcma2026.sciencesconf.org" target="_blank">CJCMA 2026</a> (Congrès des Jeunes Chercheur·e·s en Mathématiques Appliquées), École des Ponts et Chaussées, Champs-sur-Marne, March 2&#8211;4, 2026</li>
</ul>
</div>

{% if site.data.grants %}
<div class="section-card">
<h3>Grants</h3>
<ul>
{% for grant in site.data.grants %}
<li>{{ grant.name }}</li>
{% endfor %}
</ul>
</div>
{% endif %}

{% if site.data.awards %}
<div class="section-card">
<h3>Awards</h3>
<ul>
{% for award in site.data.awards %}
<li>{{ award.name | replace: "-","&#8211;" }}</li>
{% endfor %}
</ul>
</div>
{% endif %}

{% if site.data.people %}
<div class="section-card">
<h3>Students and Mentoring</h3>
<ul>
{% for student in site.data.people %}
<li>{{ student.name }}, {{ student.location }} ({{ student.degree }}, {{ student.year }})</li>
{% endfor %}
</ul>
</div>
{% endif %}

{% if site.data.funders %}
<div class="section-card">
<h4>Sponsors</h4>
<div class="sponsor-logos" style="display: flex; flex-wrap: wrap; align-items: center; justify-content: center; gap: var(--space-6);">
{% for funder in site.data.funders %}
<a href="{{ funder.url }}" target="_blank"><img src="{{ site.url }}{{ site.baseurl }}/images/{{ funder.image }}" alt="Funder logo" style="max-height: 80px; max-width: 200px; border-radius: 0;" loading="lazy"></a>
{% endfor %}
</div>
</div>
{% endif %}
