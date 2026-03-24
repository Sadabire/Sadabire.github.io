---
layout: home
author_profile: true
header:
  overlay_color: "#0a0a1a"
  overlay_filter: 0.85
  overlay_image: /assets/img/hero-bg.jpg
  actions:
    - label: "Voir mes projets"
      url: /projets/
    - label: "Me contacter"
      url: /contact/
excerpt: >-
  Étudiant ingénieur **IA & Big Data** à l'ESIGELEC · Alternance 36 mois dès sept. 2026
  · Analyse de données · Machine Learning · Big Data
---

<style>
#hero-canvas-wrap {
  width: 100%;
  background: linear-gradient(135deg, #0a0a1a 0%, #0d1b2a 50%, #0a1628 100%);
  padding: 3rem 1rem 2rem;
  overflow: hidden;
  position: relative;
  border-radius: 12px;
  margin-bottom: 2rem;
}
#hero-canvas { display: block; width: 100%; height: 320px; }
.hero-stats {
  display: flex;
  justify-content: center;
  gap: 2rem;
  flex-wrap: wrap;
  margin-top: 1.5rem;
}
.stat-box { text-align: center; color: #fff; }
.stat-box .stat-num { font-size: 2rem; font-weight: 700; color: #4fc3f7; display: block; }
.stat-box .stat-label { font-size: 0.78rem; color: #aaa; text-transform: uppercase; letter-spacing: 0.08em; }
.hero-intro {
  text-align: center;
  color: #e0e0e0;
  font-size: 1rem;
  max-width: 600px;
  margin: 1.2rem auto 0;
  line-height: 1.7;
}
.hero-intro strong { color: #4fc3f7; }
</style>

<div id="hero-canvas-wrap">
  <canvas id="hero-canvas"></canvas>
  <div class="hero-stats">
    <div class="stat-box"><span class="stat-num">6+</span><span class="stat-label">Projets data & IA</span></div>
    <div class="stat-box"><span class="stat-num">2+</span><span class="stat-label">Ans d'expérience</span></div>
    <div class="stat-box"><span class="stat-num">10+</span><span class="stat-label">Technologies maîtrisées</span></div>
    <div class="stat-box"><span class="stat-num">36</span><span class="stat-label">Mois alternance dès 09/2026</span></div>
  </div>
  <p class="hero-intro">
    De la <strong>statistique inférentielle</strong> au <strong>Deep Learning</strong>,
    du <strong>Burkina Faso</strong> à la <strong>France</strong> — je construis des solutions
    data robustes et actionnables.
  </p>
</div>

<script>
(function() {
  const canvas = document.getElementById('hero-canvas');
  const ctx = canvas.getContext('2d');
  function resize() { canvas.width = canvas.offsetWidth; canvas.height = canvas.offsetHeight; }
  resize();
  window.addEventListener('resize', resize);
  const layers = [4, 6, 6, 4, 2];
  const nodeR = 7;
  let nodes = [];
  function buildNet() {
    nodes = [];
    const W = canvas.width, H = canvas.height * 0.62;
    const xStep = W / (layers.length + 1);
    layers.forEach((count, li) => {
      const x = xStep * (li + 1);
      const yStep = H / (count + 1);
      for (let ni = 0; ni < count; ni++) {
        nodes.push({ x, y: yStep * (ni + 1) + H * 0.05, li, ni, pulse: Math.random() * Math.PI * 2 });
      }
    });
  }
  buildNet();
  const chartData = Array.from({length: 30}, (_, i) => 0.3 + 0.5 * Math.sin(i * 0.4) + Math.random() * 0.15);
  const barData = [0.6, 0.8, 0.5, 0.9, 0.7, 0.85, 0.65];
  let t = 0;
  function draw() {
    const W = canvas.width, H = canvas.height;
    ctx.clearRect(0, 0, W, H);
    const netH = H * 0.62;
    nodes.forEach(n => {
      nodes.forEach(m => {
        if (m.li !== n.li + 1) return;
        const w = 0.15 + 0.6 * Math.abs(Math.sin(t * 0.02 + n.pulse + m.pulse));
        const pulse = 0.4 + 0.4 * Math.sin(t * 0.04 + n.pulse);
        ctx.beginPath(); ctx.moveTo(n.x, n.y); ctx.lineTo(m.x, m.y);
        ctx.strokeStyle = `rgba(79,195,247,${w * pulse * 0.35})`; ctx.lineWidth = 0.8; ctx.stroke();
      });
    });
    nodes.forEach(n => {
      const glow = 0.5 + 0.5 * Math.sin(t * 0.05 + n.pulse);
      ctx.beginPath(); ctx.arc(n.x, n.y, nodeR, 0, Math.PI * 2);
      ctx.fillStyle = `rgba(79,195,247,${0.5 + 0.4 * glow})`; ctx.fill();
      ctx.strokeStyle = `rgba(129,212,250,${0.6 + 0.3 * glow})`; ctx.lineWidth = 1.5; ctx.stroke();
    });
    const gx = 20, gy = netH + 10, gw = W * 0.55, gh = H * 0.28;
    ctx.fillStyle = 'rgba(255,255,255,0.04)';
    ctx.beginPath(); ctx.roundRect(gx, gy, gw, gh, 6); ctx.fill();
    ctx.fillStyle = 'rgba(79,195,247,0.7)'; ctx.font = '11px sans-serif'; ctx.fillText('Accuracy curve', gx + 8, gy + 16);
    const pts = chartData.length, step = (gw - 20) / (pts - 1);
    ctx.beginPath();
    chartData.forEach((v, i) => {
      const cx2 = gx + 10 + i * step, cy2 = gy + gh - 10 - v * (gh - 24);
      i === 0 ? ctx.moveTo(cx2, cy2) : ctx.lineTo(cx2, cy2);
    });
    ctx.strokeStyle = '#4fc3f7'; ctx.lineWidth = 1.8; ctx.stroke();
    const bx = gx + gw + 15, by = gy, bw = W - bx - 15, bh = gh;
    ctx.fillStyle = 'rgba(255,255,255,0.04)';
    ctx.beginPath(); ctx.roundRect(bx, by, bw, bh, 6); ctx.fill();
    ctx.fillStyle = 'rgba(129,212,250,0.7)'; ctx.fillText('Model scores', bx + 8, by + 16);
    const labels = ['KNN','LDA','LR','RF','SVM','XGB','NN'];
    const barW = (bw - 20) / barData.length - 4;
    barData.forEach((v, i) => {
      const bxi = bx + 10 + i * ((bw - 20) / barData.length);
      const anim = v * (0.7 + 0.3 * Math.sin(t * 0.03 + i));
      const bhi2 = anim * (bh - 28);
      const grad = ctx.createLinearGradient(bxi, by + bh - 10 - bhi2, bxi, by + bh - 10);
      grad.addColorStop(0, 'rgba(79,195,247,0.9)'); grad.addColorStop(1, 'rgba(41,182,246,0.3)');
      ctx.fillStyle = grad; ctx.beginPath(); ctx.roundRect(bxi, by + bh - 10 - bhi2, barW, bhi2, 2); ctx.fill();
      ctx.fillStyle = 'rgba(200,230,255,0.6)'; ctx.font = '9px sans-serif'; ctx.fillText(labels[i], bxi + 1, by + bh - 2);
    });
    t++; requestAnimationFrame(draw);
  }
  draw();
})();
</script>

## Qui suis-je ?

Fort d'une expérience concrète en analyse de données au **Burkina Faso** et en **France**,
je poursuis un cycle ingénieur généraliste spécialisé en **Intelligence Artificielle & Big Data**
à l'ESIGELEC de Poitiers.

Je recherche une **alternance de 36 mois** à partir de septembre 2026 dans un environnement
où la donnée et les algorithmes sont au cœur des enjeux techniques et stratégiques.

[Découvrir mes projets](/projets/){: .btn .btn--primary .btn--large}
[Télécharger mon CV](/assets/cv-joel-dabire.pdf){: .btn .btn--inverse .btn--large}
