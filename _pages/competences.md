---
layout: single
title: "Compétences"
permalink: /competences/
author_profile: true
---

<div class="page-intro">
  <span class="page-eyebrow">Compétences</span>
  <h1 class="page-main-title">Un ensemble complet d’expertises data</h1>
  <p>Je combine des compétences en data engineering, machine learning, visualisation et analyse pour concevoir des solutions adaptées aux besoins métier.</p>
</div>

<div class="skills-grid">
{% for group in site.data.skills %}
  <div class="skill-card">
    <h3><i class="{{ group.icon }}"></i> {{ group.category }}</h3>
    <div class="skill-tags">
      {% for item in group.items %}
        <span class="skill-tag">{{ item }}</span>
      {% endfor %}
    </div>
  </div>
{% endfor %}
</div>

<div class="page-section">
  <h2>Langues</h2>
  <ul>
    <li><strong>Français</strong> — Langue maternelle</li>
    <li><strong>Anglais</strong> — B1</li>
    <li><strong>Espagnol</strong> — A1</li>
  </ul>
</div>
