---
layout: single
title: ""
permalink: /projets/
author_profile: false
classes: wide
---

<link rel="stylesheet" href="/assets/css/joel.css">
<script src="/assets/js/scroll-reveal.js" defer></script>
<nav class="jd-nav">
  <a href="/" class="jd-nav-logo">J<span>.</span>DABIRE</a>
  <ul class="jd-nav-links">
    <li><a href="/">Accueil</a></li><li><a href="/about/">À propos</a></li>
    <li><a href="/projets/">Projets</a></li><li><a href="/competences/">Compétences</a></li>
    <li><a href="/experiences/">Expériences</a></li><li><a href="/veille/">Veille</a></li>
    <li><a href="/contact/" class="jd-nav-cta">Contactez-moi</a></li>
  </ul>
</nav>

<div class="jd-page">
  <div class="jd-page-header">
    <span class="jd-page-eyebrow">Réalisations</span>
    <h1 class="jd-page-title">Mes Projets</h1>
    <p style="color:var(--text-mid);margin-top:0.5rem;font-size:1rem;">
      Des études de cas centrées sur l'impact métier, la qualité des données et des résultats concrets.
    </p>
  </div>
  <div class="jd-page-body">
    <div class="jd-projects-grid">
      {% for project in site.data.projects %}
      <div class="jd-project-card reveal">
        <span class="jd-badge {% if project.status == 'en_cours' %}jd-badge-wip{% else %}jd-badge-done{% endif %}">
          {% if project.status == "en_cours" %}En cours{% else %}Terminé{% endif %}
        </span>
        {% if project.image and project.image != "" %}
          <img class="jd-project-img" src="{{ project.image }}" alt="{{ project.title }}">
        {% else %}
          <div class="jd-project-placeholder">
            {% if project.category == "Machine Learning" %}🤖{% elsif project.category == "Bases de données" %}🗄️{% elsif project.category == "Data Visualisation" %}📊{% elsif project.category == "IA & Éthique" %}🧠{% else %}📈{% endif %}
          </div>
        {% endif %}
        <div class="jd-project-body">
          <div class="jd-project-cat">{{ project.category }}</div>
          <h3 class="jd-project-title">{{ project.title }}</h3>
          <p class="jd-project-desc">{{ project.description }}</p>
          {% if project.results and project.results != "" %}
          <div class="jd-project-results"><strong>Résultats clés</strong>{{ project.results }}</div>
          {% endif %}
          <div class="jd-tags">{% for tag in project.tags %}<span class="jd-tag">{{ tag }}</span>{% endfor %}</div>
          {% if project.github and project.github != "" %}
            <a href="{{ project.github }}" target="_blank" class="jd-link">⚙ Voir sur GitHub →</a>
          {% endif %}
        </div>
      </div>
      {% endfor %}
    </div>
  </div>
</div>
