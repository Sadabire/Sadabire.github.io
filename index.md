---
layout: single
author_profile: false
header:
  overlay_color: "#08101f"
  overlay_filter: 0.7
  actions:
    - label: "Voir mes projets"
      url: /projets/
    - label: "Contactez-moi"
      url: /contact/
excerpt: >-
  Data Scientist & Ingénieur Machine Learning créant des solutions data-driven
  modernes, scalables et impactantes pour les organisations ambitieuses.
---

<style>
.home-hero {
  display: grid;
  gap: 3rem;
  grid-template-columns: minmax(0, 1.1fr) minmax(280px, 0.9fr);
  align-items: center;
  margin-bottom: 3rem;
}
@media (max-width: 900px) {
  .home-hero { grid-template-columns: 1fr; }
}
.hero-panel {
  color: white;
}
.hero-eyebrow {
  text-transform: uppercase;
  letter-spacing: 0.25rem;
  color: #8ab7ff;
  margin-bottom: 1rem;
  font-weight: 700;
  font-size: 0.95rem;
}
.hero-title {
  font-size: clamp(3rem, 3.8vw, 4.5rem);
  line-height: 1.02;
  margin: 0 0 1.2rem;
  letter-spacing: -0.05em;
}
.hero-title strong {
  color: #7c92ff;
}
.hero-text {
  max-width: 680px;
  font-size: 1.05rem;
  line-height: 1.9;
  color: #dce6ff;
  margin-bottom: 2rem;
}
.hero-actions {
  display: flex;
  flex-wrap: wrap;
  gap: 1rem;
}
.hero-card-wrap {
  display: grid;
  grid-template-columns: repeat(3, minmax(0, 1fr));
  gap: 1rem;
  margin-top: 2rem;
}
@media (max-width: 720px) {
  .hero-card-wrap { grid-template-columns: 1fr; }
}
.hero-card {
  padding: 1.2rem 1.3rem;
  border-radius: 22px;
  background: rgba(255,255,255,0.09);
  backdrop-filter: blur(16px);
  border: 1px solid rgba(255,255,255,0.12);
}
.hero-card strong {
  display: block;
  font-size: 2rem;
  color: #fff;
  margin-bottom: 0.35rem;
}
.hero-card span {
  color: #a6b7d9;
  font-size: 0.92rem;
}
.hero-visual {
  position: relative;
  min-height: 420px;
  border-radius: 32px;
  overflow: hidden;
  background: radial-gradient(circle at top left, rgba(124,146,255,0.65), transparent 30%),
              radial-gradient(circle at bottom right, rgba(39,214,203,0.18), transparent 28%),
              linear-gradient(180deg, rgba(15,29,62,0.95) 0%, rgba(10,17,31,0.98) 100%);
  box-shadow: 0 30px 80px rgba(0,0,0,0.2);
}
.hero-visual::before {
  content: "";
  position: absolute;
  inset: 0;
  background-image: radial-gradient(circle at 20% 20%, rgba(255,255,255,0.18), transparent 15%),
                    radial-gradient(circle at 80% 30%, rgba(124,146,255,0.16), transparent 18%),
                    radial-gradient(circle at 50% 85%, rgba(39,214,203,0.12), transparent 20%);
}
.hero-visual-inner {
  position: absolute;
  inset: 0;
  display: grid;
  place-items: center;
  padding: 2rem;
}
.hero-visual-panel {
  width: 100%;
  max-width: 380px;
  border-radius: 32px;
  background: rgba(10, 17, 31, 0.75);
  border: 1px solid rgba(255,255,255,0.08);
  padding: 1.8rem;
  box-shadow: 0 22px 50px rgba(0,0,0,0.18);
}
.hero-visual-panel h3 {
  margin: 0 0 1rem;
  font-size: 1.15rem;
  color: #fff;
}
.hero-visual-panel p {
  margin: 0 0 1.35rem;
  color: #b8c6e4;
  line-height: 1.75;
}
.hero-badge {
  display: inline-flex;
  align-items: center;
  gap: 0.55rem;
  padding: 0.45rem 0.85rem;
  border-radius: 999px;
  font-size: 0.8rem;
  background: rgba(255,255,255,0.09);
  color: #e5ecff;
  border: 1px solid rgba(255,255,255,0.12);
}
.section-title {
  margin-top: 4rem;
  margin-bottom: 1rem;
  color: white;
  font-size: 2.1rem;
}
.section-subtitle {
  color: #c4d0f2;
  max-width: 720px;
  line-height: 1.8;
}
.feature-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(240px, 1fr));
  gap: 1.4rem;
  margin-top: 1.8rem;
}
.feature-card {
  padding: 1.4rem 1.35rem;
  border-radius: 20px;
  background: rgba(255,255,255,0.07);
  border: 1px solid rgba(255,255,255,0.10);
  backdrop-filter: blur(16px);
}
.feature-card h3 {
  margin: 0 0 0.65rem;
  color: white;
}
.feature-card p {
  margin: 0;
  color: #b8c6e4;
  line-height: 1.7;
}
.cta-banner {
  margin-top: 3rem;
  padding: 2rem 2rem 1.8rem;
  border-radius: 24px;
  background: linear-gradient(135deg, rgba(124,146,255,0.18), rgba(39,214,203,0.12));
  border: 1px solid rgba(255,255,255,0.12);
}
.cta-banner h2 {
  margin: 0 0 0.75rem;
  color: white;
  font-size: 1.95rem;
}
.cta-banner p {
  margin: 0 0 1.5rem;
  color: #e3ecff;
  line-height: 1.8;
}
.cta-banner a {
  display: inline-block;
  text-decoration: none;
}

.projects-grid {
  display: grid;
  gap: 1.8rem;
  grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
  margin-top: 2rem;
}
.project-card {
  border: 1px solid rgba(255,255,255,0.1);
  border-radius: 24px;
  overflow: hidden;
  position: relative;
  transition: box-shadow 0.25s, transform 0.25s;
  background: rgba(255,255,255,0.06);
  backdrop-filter: blur(12px);
}
.project-card:hover {
  box-shadow: 0 18px 50px rgba(0,0,0,0.22);
  transform: translateY(-3px);
}
.project-img {
  width: 100%;
  height: auto;
  max-height: 260px;
  object-fit: cover;
  background: #0a1525;
  display: block;
}
.project-img-placeholder {
  width: 100%;
  height: 220px;
  background: linear-gradient(135deg, rgba(124,146,255,0.22), rgba(39,214,203,0.16));
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 2.5rem;
  color: #eef5ff;
}
.project-body { padding: 1.3rem 1.4rem 1.4rem; }
.badge-status {
  position: absolute;
  top: 1rem;
  right: 1rem;
  font-size: 0.72rem;
  font-weight: 700;
  padding: 6px 12px;
  border-radius: 999px;
  text-transform: uppercase;
  letter-spacing: 0.08em;
}
.badge-en_cours { background: rgba(255,229,153,0.18); color: #f2c94c; border: 1px solid rgba(242,201,76,0.24); }
.badge-terminé { background: rgba(111,199,167,0.18); color: #2d6a50; border: 1px solid rgba(111,199,167,0.24); }
.project-category { font-size: 0.74rem; color: #aab9d7; text-transform: uppercase; letter-spacing: 0.08em; margin-bottom: 0.45rem; }
.project-card h3 { margin: 0 0 0.75rem; font-size: 1.02rem; line-height: 1.35; color: white; }
.project-desc { font-size: 0.92rem; color: #d7e2fe; margin-bottom: 0.75rem; line-height: 1.7; }
.project-results {
  font-size: 0.82rem;
  background: rgba(64,102,240,0.12);
  border-left: 3px solid #7c92ff;
  padding: 0.7rem 0.85rem;
  border-radius: 0 10px 10px 0;
  margin-bottom: 1rem;
  color: #e7f0ff;
}
.project-results strong { display: block; font-size: 0.72rem; text-transform: uppercase; letter-spacing: 0.05em; color: #9fc8ff; margin-bottom: 0.2rem; }
.project-tags { display: flex; flex-wrap: wrap; gap: 0.45rem; margin-bottom: 1rem; }
.tag { font-size: 0.72rem; background: rgba(255,255,255,0.08); color: #d4e0ff; padding: 5px 11px; border-radius: 999px; border: 1px solid rgba(255,255,255,0.08); }
.project-links a { font-size: 0.86rem; margin-right: 0.8rem; text-decoration: none; color: #a5c6ff; }
.project-links a:hover { text-decoration: underline; color: #fff; }
</style>

<div class="home-hero">
  <div class="hero-panel">
    <div class="hero-eyebrow">Portfolio ultra moderne</div>
    <h1 class="hero-title">Data Scientist<br><strong>Ingénieur Machine Learning</strong></h1>
    <p class="hero-text">
      Je conçois des expériences data-driven et des solutions IA qui transforment des problématiques complexes en décisions opérationnelles.
      Ce portfolio met en avant des réalisations concrètes, des projets en cours et une approche produit plutôt que le CV classique.
    </p>

    <div class="hero-actions">
      <a class="btn btn--primary btn--large" href="/projets/">Voir mes projets</a>
      <a class="btn btn--inverse btn--large" href="/contact/">Contactez-moi</a>
    </div>

    <div class="hero-card-wrap">
      <div class="hero-card">
        <strong>+ 5</strong>
        <span>projets présentés</span>
      </div>
      <div class="hero-card">
        <strong>+ 3</strong>
        <span>solutions IA étudiées</span>
      </div>
      <div class="hero-card">
        <strong>+ 15</strong>
        <span>KPI & dashboards monitorés</span>
      </div>
    </div>
  </div>

  <div class="hero-visual">
    <div class="hero-visual-inner">
      <div class="hero-visual-panel">
        <span class="hero-badge">Exploration · Data · Algorithmes</span>
        <h3>Focus produit</h3>
        <p>Une démarche pragmatique : architecture data robuste, modèles IA interprétables et livrables actionnables pour les équipes métier.</p>
        <div class="feature-grid">
          <div class="feature-card">
            <h3>Architecture data</h3>
            <p>Conception ETL/ELT, SQL/NoSQL et pipelines fiables pour gérer des volumes réels.</p>
          </div>
          <div class="feature-card">
            <h3>IA explicable</h3>
            <p>Modèles lisibles, métriques métier et visualisations claires pour des décisions validées.</p>
          </div>
          <div class="feature-card">
            <h3>Livrables opérationnels</h3>
            <p>Dashboards, prototypes et documentation prêts à être intégrés dans une équipe.</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</div>

<div class="section-explore">
  <h2 class="section-title">Sélection de projets</h2>
  <p class="section-subtitle">Des études de cas centrées sur l'impact métier, la qualité des données et des résultats concrets. Le portfolio s'enrichit au fil des prochains projets.</p>
</div>

<div class="projects-grid">
{% for project in site.data.projects limit:3 %}
  <div class="project-card">
    <span class="badge-status badge-{{ project.status }}">
      {% if project.status == "en_cours" %}En cours{% else %}Terminé{% endif %}
    </span>
    {% if project.image and project.image != "" %}
      <img class="project-img" src="{{ project.image }}" alt="{{ project.title }}">
    {% else %}
      <div class="project-img-placeholder">📈</div>
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

<div class="cta-banner">
  <h2>Prêt à construire la prochaine solution data ?</h2>
  <p>J'accélère les projets qui nécessitent une vision technique solide et une approche produit. Contactez-moi pour un partenariat concret autour de l'IA et du Big Data.</p>
  <a class="btn btn--primary btn--large" href="/contact/">Échanger</a>
</div>
