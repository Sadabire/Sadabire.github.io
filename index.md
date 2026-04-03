---
layout: single
author_profile: false
header:
  overlay_color: "#08101f"
  overlay_filter: 0.7
  actions:
    - label: "Voir mes projets"
      url: /projets/
    - label: "Contactez-moi"
      url: /contact/
excerpt: >-
  Data Scientist & Ingénieur Machine Learning créant des solutions data-driven
  modernes, scalables et impactantes pour les organisations ambitieuses.
---

<div class="home-hero">
  <div class="hero-panel">
    <div class="hero-eyebrow">Portfolio ultra moderne</div>
    <h1 class="hero-title">Data Scientist &<br><strong>Ingénieur Machine Learning</strong></h1>
    <p class="hero-text">Je conçois des expériences data-driven et des solutions IA qui transforment les problématiques complexes en décisions opérationnelles. Plus qu'un CV, ce portfolio dévoile mes projets, mes méthodologies et mes résultats.</p>

    <div class="hero-actions">
      <a class="btn btn--primary btn--large" href="/projets/">Voir mes projets</a>
      <a class="btn btn--inverse btn--large" href="/contact/">Contactez-moi</a>
    </div>

    <div class="hero-card-wrap">
      <div class="hero-card">
        <strong>+ 5</strong>
        <span>études de cas publiées</span>
      </div>
      <div class="hero-card">
        <strong>+ 3</strong>
        <span>solutions IA analysées</span>
      </div>
      <div class="hero-card">
        <strong>+ 15</strong>
        <span>KPI & dashboards monitorés</span>
      </div>
    </div>
  </div>

  <div class="hero-visual">
    <div class="hero-visual-inner">
      <div class="hero-visual-panel">
        <span class="hero-badge">Exploration · Data · Algorithmes</span>
        <h3>Focus produit</h3>
        <p>J'accompagne les organisations avec une approche orientée résultats et produit : architecture data solide, IA explicable, livrables opérationnels.</p>
        <div class="feature-grid">
          <div class="feature-card">
            <h3>Architecture data</h3>
            <p>Chaînes ETL/ELT, stockage SQL/NoSQL et pipelines réutilisables.</p>
          </div>
          <div class="feature-card">
            <h3>IA explicable</h3>
            <p>Modèles lisibles et métriques métier pour des décisions fiables.</p>
          </div>
          <div class="feature-card">
            <h3>Livrables opérationnels</h3>
            <p>Dashboards, prototypes Python et documentation prête à l'intégration.</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</div>

<div class="section-panel">
  <h2 class="section-title">Sélection de projets</h2>
  <p class="section-subtitle">Des études de cas concrètes, structurées autour de l'impact métier, des données et des résultats. Le portfolio évolue au rythme des prochains projets.</p>
</div>

<div class="projects-grid">
{% for project in site.data.projects limit:3 %}
  <div class="project-card">
    <span class="badge-status badge-{{ project.status }}">
      {% if project.status == "en_cours" %}En cours{% else %}Terminé{% endif %}
    </span>
    {% if project.image and project.image != "" %}
      <img class="project-img" src="{{ project.image }}" alt="{{ project.title }}">
    {% else %}
      <div class="project-img-placeholder">📈</div>
    {% endif %}

    <div class="project-body">
      <div class="project-category">{{ project.category }}</div>
      <h3>{{ project.title }}</h3>
      <p class="project-desc">{{ project.description }}</p>
      {% if project.results and project.results != "" %}
      <div class="project-results">
        <strong>Résultats clés</strong>
        {{ project.results }}
      </div>
      {% endif %}
      <div class="project-tags">
        {% for tag in project.tags %}
          <span class="tag">{{ tag }}</span>
        {% endfor %}
      </div>
      <div class="project-links">
        {% if project.github and project.github != "" %}
          <a href="{{ project.github }}" target="_blank">⚙ GitHub</a>
        {% endif %}
        {% if project.demo and project.demo != "" %}
          <a href="{{ project.demo }}" target="_blank">🔗 Demo</a>
        {% endif %}
      </div>
    </div>
  </div>
{% endfor %}
</div>

<div class="cta-banner">
  <h2>Prêt à lancer un projet data moderne ?</h2>
  <p>Je crée des solutions IA et Big Data qui produisent des résultats clairs et exploitables.</p>
  <a class="btn btn--primary btn--large" href="/contact/">Échanger</a>
</div>
