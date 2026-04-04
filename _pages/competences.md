---
layout: single
title: ""
permalink: /competences/
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
    <span class="jd-page-eyebrow">Savoir-faire</span>
    <h1 class="jd-page-title">Compétences</h1>
  </div>
  <div class="jd-page-body">
    <div class="jd-skills-grid">
      {% for group in site.data.skills %}
      <div class="jd-skill-card reveal">
        <h3><i class="{{ group.icon }}"></i> {{ group.category }}</h3>
        <div class="jd-skill-tags">
          {% for item in group.items %}<span class="jd-skill-tag">{{ item }}</span>{% endfor %}
        </div>
      </div>
      {% endfor %}
    </div>

    <div style="margin-top:3rem;">
      <h2 class="reveal" style="font-family:'Syne',sans-serif;font-weight:800;font-size:1.4rem;color:var(--text-dark);margin-bottom:1.2rem;">Langues</h2>
      <div class="reveal" style="display:flex;gap:1rem;flex-wrap:wrap;">
        <div style="background:var(--bg2);border:1.5px solid var(--border);border-radius:12px;padding:1rem 1.8rem;text-align:center;">
          <div style="font-family:'Syne',sans-serif;font-weight:800;font-size:1.2rem;color:var(--text-dark);">Français</div>
          <div style="font-size:0.82rem;color:var(--text-light);margin-top:0.2rem;">Langue maternelle</div>
        </div>
        <div style="background:var(--bg2);border:1.5px solid var(--border);border-radius:12px;padding:1rem 1.8rem;text-align:center;">
          <div style="font-family:'Syne',sans-serif;font-weight:800;font-size:1.2rem;color:var(--text-dark);">Anglais</div>
          <div style="font-size:0.82rem;color:var(--text-light);margin-top:0.2rem;">Niveau B1</div>
        </div>
        <div style="background:var(--bg2);border:1.5px solid var(--border);border-radius:12px;padding:1rem 1.8rem;text-align:center;">
          <div style="font-family:'Syne',sans-serif;font-weight:800;font-size:1.2rem;color:var(--text-dark);">Espagnol</div>
          <div style="font-size:0.82rem;color:var(--text-light);margin-top:0.2rem;">Niveau A1</div>
        </div>
      </div>
    </div>
  </div>
</div>
