---
layout: single
title: "Veille technologique"
permalink: /veille/
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
.veille-grid { display: grid; grid-template-columns: repeat(auto-fill, minmax(280px, 1fr)); gap: 1.4rem; margin-top: 2rem; }
.veille-category h3 { font-size: 0.95rem; color: #4fc3f7; border-left: 3px solid #4fc3f7; padding-left: 0.6rem; margin-bottom: 0.8rem; }
.veille-item { margin-bottom: 0.8rem; padding: 0.8rem 1rem; background: #161b22; border: 1px solid #21262d; border-radius: 8px; transition: border-color 0.2s; }
.veille-item:hover { border-color: #4fc3f7; }
.veille-item a { font-weight: 600; font-size: 0.9rem; text-decoration: none; color: #4fc3f7; }
.veille-item p { font-size: 0.82rem; color: #8b949e; margin: 0.2rem 0 0; }
</style>

<p style="color:#8b949e; margin-top:1rem;">
  Je maintiens une veille active sur les domaines qui me passionnent : l'IA, la data, le cloud et les marchés financiers.
</p>

<div class="veille-grid">
{% for group in site.data.veille %}
  <div class="veille-category">
    <h3>{{ group.category }}</h3>
    {% for item in group.items %}
      <div class="veille-item">
        <a href="{{ item.url }}" target="_blank">{{ item.title }}</a>
        <p>{{ item.note }}</p>
      </div>
    {% endfor %}
  </div>
{% endfor %}
</div>
