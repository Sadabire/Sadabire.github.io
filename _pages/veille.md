---
layout: single
title: "Veille technologique"
permalink: /veille/
author_profile: true
---

Je maintiens une veille active sur les domaines qui me passionnent : l'IA, la data,
le cloud et les marchés financiers. Voici les ressources que je consulte régulièrement.

<style>
.veille-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(260px, 1fr));
  gap: 1.4rem;
  margin-top: 1.5rem;
}
.veille-category { margin-bottom: 0.5rem; }
.veille-category h3 {
  font-size: 0.95rem;
  border-left: 3px solid #0d6efd;
  padding-left: 0.6rem;
  margin-bottom: 0.8rem;
}
.veille-item {
  margin-bottom: 0.8rem;
  padding: 0.7rem 0.9rem;
  border: 1px solid #e8e8e8;
  border-radius: 8px;
  background: #fafafa;
}
.veille-item a { font-weight: 600; font-size: 0.9rem; text-decoration: none; }
.veille-item a:hover { text-decoration: underline; }
.veille-item p { font-size: 0.82rem; color: #666; margin: 0.2rem 0 0; }
</style>

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
