---
layout: single
title: ""
permalink: /veille/
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
    <span class="jd-page-eyebrow">Curiosité active</span>
    <h1 class="jd-page-title">Veille technologique</h1>
    <p style="color:var(--text-mid);margin-top:0.5rem;font-size:1rem;">
      Je maintiens une veille active sur les domaines qui me passionnent : l'IA, la data, le cloud et les marchés financiers.
    </p>
  </div>
  <div class="jd-page-body">
    <div class="jd-veille-grid">
      {% for group in site.data.veille %}
      <div class="jd-veille-cat reveal">
        <h3>{{ group.category }}</h3>
        {% for item in group.items %}
        <div class="jd-veille-item">
          <a href="{{ item.url }}" target="_blank">{{ item.title }}</a>
          <p>{{ item.note }}</p>
        </div>
        {% endfor %}
      </div>
      {% endfor %}
    </div>
  </div>
</div>
