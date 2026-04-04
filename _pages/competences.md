---
layout: single
title: "Compétences"
permalink: /competences/
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
.skills-grid { display: grid; grid-template-columns: repeat(auto-fill, minmax(280px, 1fr)); gap: 1.4rem; margin-top: 2rem; }
.skill-card { background: #161b22; border: 1px solid #21262d; border-radius: 12px; padding: 1.2rem; transition: border-color 0.2s; }
.skill-card:hover { border-color: #4fc3f7; }
.skill-card h3 { font-size: 0.95rem; color: #e6edf3; margin: 0 0 1rem; display: flex; align-items: center; gap: 0.5rem; }
.skill-tags { display: flex; flex-wrap: wrap; gap: 0.4rem; }
.skill-tag { font-size: 0.78rem; padding: 3px 10px; border-radius: 14px; background: rgba(79,195,247,0.1); color: #4fc3f7; border: 1px solid rgba(79,195,247,0.2); }
.lang-section { margin-top: 2.5rem; }
.lang-section h2 { color: #e6edf3; font-size: 1.3rem; margin-bottom: 1rem; }
.lang-grid { display: flex; gap: 1rem; flex-wrap: wrap; }
.lang-card { background: #161b22; border: 1px solid #21262d; border-radius: 8px; padding: 0.8rem 1.5rem; color: #8b949e; font-size: 0.9rem; }
.lang-card strong { color: #e6edf3; }
</style>

<div class="skills-grid">
{% for group in site.data.skills %}
  <div class="skill-card">
    <h3><i class="{{ group.icon }}" style="color:#4fc3f7"></i> {{ group.category }}</h3>
    <div class="skill-tags">
      {% for item in group.items %}<span class="skill-tag">{{ item }}</span>{% endfor %}
    </div>
  </div>
{% endfor %}
</div>

<div class="lang-section">
  <h2>Langues</h2>
  <div class="lang-grid">
    <div class="lang-card"><strong>Français</strong> — Langue maternelle</div>
    <div class="lang-card"><strong>Anglais</strong> — B1</div>
    <div class="lang-card"><strong>Espagnol</strong> — A1</div>
  </div>
</div>
