---
layout: single
title: "Projets"
permalink: /projets/
author_profile: true
---

<style>
.projects-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(320px, 1fr));
  gap: 1.8rem;
  margin-top: 1.5rem;
}
.project-card {
  border: 1px solid #e0e0e0;
  border-radius: 12px;
  overflow: hidden;
  position: relative;
  transition: box-shadow 0.25s, transform 0.25s;
  background: #fff;
}
.project-card:hover {
  box-shadow: 0 8px 28px rgba(0,0,0,0.12);
  transform: translateY(-3px);
}
.project-img {
  width: 100%;
  height: 180px;
  object-fit: cover;
  display: block;
  background: linear-gradient(135deg, #0d1b2a, #1a3a5c);
}
.project-img-placeholder {
  width: 100%;
  height: 180px;
  background: linear-gradient(135deg, #0d1b2a 0%, #1a3a5c 60%, #0d2137 100%);
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 2.5rem;
}
.project-body { padding: 1.1rem 1.2rem 1rem; }
.badge-status {
  position: absolute;
  top: 0.8rem; right: 0.8rem;
  font-size: 0.7rem;
  font-weight: 700;
  padding: 3px 10px;
  border-radius: 20px;
  text-transform: uppercase;
  letter-spacing: 0.05em;
}
.badge-en_cours { background: #fff3cd; color: #856404; border: 1px solid #ffc107; }
.badge-terminé  { background: #d1e7dd; color: #0a3622; border: 1px solid #198754; }
.project-category { font-size: 0.7rem; color: #888; text-transform: uppercase; letter-spacing: 0.08em; margin-bottom: 0.3rem; }
.project-card h3 { margin: 0 0 0.5rem; font-size: 1rem; line-height: 1.4; }
.project-desc { font-size: 0.86rem; color: #555; margin-bottom: 0.6rem; line-height: 1.6; }
.project-results {
  font-size: 0.83rem;
  background: #f0f7ff;
  border-left: 3px solid #4fc3f7;
  padding: 0.5rem 0.7rem;
  border-radius: 0 6px 6px 0;
  margin-bottom: 0.8rem;
  color: #1a3a5c;
}
.project-results strong { display: block; font-size: 0.72rem; text-transform: uppercase; letter-spacing: 0.05em; color: #4fc3f7; margin-bottom: 0.2rem; }
.project-tags { display: flex; flex-wrap: wrap; gap: 0.35rem; margin-bottom: 0.8rem; }
.tag { font-size: 0.72rem; background: #f3f3f3; color: #444; padding: 2px 8px; border-radius: 12px; border: 1px solid #e5e5e5; }
.project-links a { font-size: 0.82rem; margin-right: 0.8rem; text-decoration: none; color: #0d6efd; }
.project-links a:hover { text-decoration: underline; }
</style>

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
