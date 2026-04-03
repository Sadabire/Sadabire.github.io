---
layout: single
title: "Compétences"
permalink: /competences/
author_profile: true
---

<style>
.skills-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(260px, 1fr));
  gap: 1.4rem;
  margin-top: 1.5rem;
}
.skill-card {
  border: 1px solid #e0e0e0;
  border-radius: 10px;
  padding: 1.1rem 1.2rem;
  background: #fff;
}
.skill-card h3 {
  font-size: 0.95rem;
  margin-top: 0;
  margin-bottom: 0.8rem;
  display: flex;
  align-items: center;
  gap: 0.5rem;
}
.skill-tags { display: flex; flex-wrap: wrap; gap: 0.4rem; }
.skill-tag {
  font-size: 0.78rem;
  padding: 3px 10px;
  border-radius: 14px;
  background: #f3f3f3;
  color: #333;
  border: 1px solid #e0e0e0;
}
</style>

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

---

## Langues

- **Français** — Langue maternelle
- **Anglais** — B1
- **Espagnol** — A1