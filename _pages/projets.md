---
layout: single
title: "Projets"
permalink: /projets/
author_profile: true
---

<style>
.projects-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
  gap: 1.5rem;
  margin-top: 1.5rem;
}
.project-card {
  border: 1px solid #e0e0e0;
  border-radius: 10px;
  padding: 1.2rem;
  position: relative;
  transition: box-shadow 0.2s;
  background: #fff;
}
.project-card:hover {
  box-shadow: 0 4px 18px rgba(0,0,0,0.10);
}
.project-card h3 { margin-top: 0.5rem; margin-bottom: 0.5rem; font-size: 1rem; }
.project-card p  { font-size: 0.88rem; color: #555; margin-bottom: 0.8rem; }
.badge-status {
  position: absolute;
  top: 1rem; right: 1rem;
  font-size: 0.72rem;
  font-weight: 600;
  padding: 3px 10px;
  border-radius: 20px;
  text-transform: uppercase;
  letter-spacing: 0.05em;
}
.badge-en_cours { background: #fff3cd; color: #856404; border: 1px solid #ffc107; }
.badge-terminé  { background: #d1e7dd; color: #0a3622; border: 1px solid #198754; }
.project-tags { display: flex; flex-wrap: wrap; gap: 0.4rem; margin-bottom: 0.8rem; }
.tag {
  font-size: 0.72rem;
  background: #f0f0f0;
  color: #333;
  padding: 2px 8px;
  border-radius: 12px;
}
.project-links a {
  font-size: 0.82rem;
  margin-right: 0.8rem;
  text-decoration: none;
  color: #0d6efd;
}
.project-links a:hover { text-decoration: underline; }
.category-label {
  font-size: 0.72rem;
  color: #888;
  text-transform: uppercase;
  letter-spacing: 0.06em;
  margin-bottom: 0.3rem;
}
</style>

<div class="projects-grid">
{% for project in site.data.projects %}
  <div class="project-card">
    <span class="badge-status badge-{{ project.status }}">
      {% if project.status == "en_cours" %}En cours{% else %}Terminé{% endif %}
    </span>
    <div class="category-label">{{ project.category }}</div>
    <h3>{{ project.title }}</h3>
    <p>{{ project.description }}</p>
    <div class="project-tags">
      {% for tag in project.tags %}
        <span class="tag">{{ tag }}</span>
      {% endfor %}
    </div>
    <div class="project-links">
      {% if project.github and project.github != "" %}
        <a href="{{ project.github }}" target="_blank">
          <i class="fab fa-github"></i> GitHub
        </a>
      {% endif %}
    </div>
  </div>
{% endfor %}
</div>
