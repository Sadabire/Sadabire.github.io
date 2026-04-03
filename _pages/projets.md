---
layout: single
title: "Projets"
permalink: /projets/
author_profile: true
---

<div class="page-intro">
  <span class="page-eyebrow">Études de cas</span>
  <h1 class="page-main-title">Projets data & IA</h1>
  <p>Un portfolio orienté solutions métiers, structuré par impact, technologie et résultats. Je montre mes projets les plus pertinents pour prouver ma capacité à transformer des données en décisions.</p>
</div>

<div class="projects-grid">
{% for project in site.data.projects %}
  <div class="project-card">
    <span class="badge-status badge-{{ project.status }}">
      {% if project.status == "en_cours" %}En cours{% else %}Terminé{% endif %}
    </span>

    {% if project.image and project.image != "" %}
      <img class="project-img" src="{{ project.image }}" alt="{{ project.title }}">
    {% else %}
      <div class="project-img-placeholder">
        {% if project.category == "Machine Learning" %}🤖
        {% elsif project.category == "Bases de données" %}🗄️
        {% elsif project.category == "Data Visualisation" %}📊
        {% elsif project.category == "IA & Éthique" %}🧠
        {% else %}📈{% endif %}
      </div>
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

<div class="cta-banner page-footer-cta">
  <h2>Envie d’un projet structuré autour des données ?</h2>
  <p>Je prends en charge la phase analytique, le prototypage IA et la livraison métier.</p>
  <a class="btn btn--primary btn--large" href="/contact/">Contactez-moi</a>
</div>
