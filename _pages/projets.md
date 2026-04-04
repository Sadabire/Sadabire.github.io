---
layout: single
title: "Mes Projets"
permalink: /projets/
author_profile: false
classes: wide
---

<link rel="stylesheet" href="/assets/css/moderne.css">
<nav class="nav-moderne">
  <div class="nav-logo">JD</div>
  <ul class="nav-links">
    <li><a href="/">Accueil</a></li>
    <li><a href="/about/">À propos</a></li>
    <li><a href="/projets/">Portfolio</a></li>
    <li><a href="/competences/">Compétences</a></li>
    <li><a href="/experiences/">Expériences</a></li>
    <li><a href="/contact/" class="nav-cta">Contactez-moi</a></li>
  </ul>
</nav>

<style>
.projects-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(340px, 1fr));
  gap: 1.8rem;
  margin-top: 2rem;
}
.project-card {
  border-radius: 12px;
  overflow: hidden;
  position: relative;
  transition: all 0.25s;
  background: #161b22;
  border: 1px solid #21262d;
}
.project-card:hover {
  border-color: #4fc3f7;
  transform: translateY(-4px);
  box-shadow: 0 8px 32px rgba(79,195,247,0.1);
}
.project-img { width: 100%; height: auto; max-height: 220px; object-fit: contain; background: #0d1b2a; display: block; }
.project-img-placeholder {
  width: 100%; height: 180px;
  background: linear-gradient(135deg, #0d1b2a, #1a3a5c);
  display: flex; align-items: center; justify-content: center; font-size: 2.5rem;
}
.project-body { padding: 1.2rem; }
.badge-status {
  position: absolute; top: 0.8rem; right: 0.8rem;
  font-size: 0.7rem; font-weight: 700;
  padding: 3px 10px; border-radius: 20px; text-transform: uppercase;
}
.badge-en_cours { background: rgba(255,183,77,0.15); color: #ffb74d; border: 1px solid rgba(255,183,77,0.3); }
.badge-terminé  { background: rgba(129,199,132,0.15); color: #81c784; border: 1px solid rgba(129,199,132,0.3); }
.project-category { font-size: 0.7rem; color: #8b949e; text-transform: uppercase; letter-spacing: 0.08em; margin-bottom: 0.3rem; }
.project-card h3 { margin: 0 0 0.5rem; font-size: 1rem; color: #e6edf3; line-height: 1.4; }
.project-desc { font-size: 0.85rem; color: #8b949e; margin-bottom: 0.7rem; line-height: 1.6; }
.project-results {
  font-size: 0.82rem;
  background: rgba(79,195,247,0.08);
  border-left: 3px solid #4fc3f7;
  padding: 0.5rem 0.7rem;
  border-radius: 0 6px 6px 0;
  margin-bottom: 0.8rem;
  color: #8b949e;
}
.project-results strong { display: block; font-size: 0.7rem; text-transform: uppercase; color: #4fc3f7; margin-bottom: 0.2rem; }
.project-tags { display: flex; flex-wrap: wrap; gap: 0.35rem; margin-bottom: 0.8rem; }
.tag { font-size: 0.72rem; background: rgba(79,195,247,0.1); color: #4fc3f7; padding: 2px 8px; border-radius: 12px; border: 1px solid rgba(79,195,247,0.2); }
.project-links a { font-size: 0.82rem; margin-right: 0.8rem; text-decoration: none; color: #4fc3f7; }
</style>

<p style="color:#8b949e; margin-top:1rem;">
  Des études de cas centrées sur l'impact métier, la qualité des données et des résultats concrets.
</p>

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
        <strong>Résultats clés</strong>{{ project.results }}
      </div>
      {% endif %}
      <div class="project-tags">
        {% for tag in project.tags %}<span class="tag">{{ tag }}</span>{% endfor %}
      </div>
      <div class="project-links">
        {% if project.github and project.github != "" %}
          <a href="{{ project.github }}" target="_blank">⚙ GitHub</a>
        {% endif %}
      </div>
    </div>
  </div>
{% endfor %}
</div>
