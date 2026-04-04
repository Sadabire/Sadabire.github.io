---
layout: single
title: "Contact"
permalink: /contact/
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
.contact-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 3rem; margin-top: 2rem; }
.contact-info h3 { color: #4fc3f7; font-size: 1rem; margin-bottom: 0.3rem; }
.contact-info p { color: #8b949e; font-size: 0.9rem; margin-bottom: 1.5rem; }
.contact-info a { color: #4fc3f7; text-decoration: none; }
.contact-form input, .contact-form textarea {
  width: 100%; padding: 0.75rem 1rem;
  margin-bottom: 1rem;
  background: #161b22; border: 1px solid #21262d;
  color: #e6edf3; border-radius: 8px;
  font-size: 0.95rem; font-family: inherit;
  box-sizing: border-box; transition: border-color 0.2s;
}
.contact-form input:focus, .contact-form textarea:focus { border-color: #4fc3f7; outline: none; }
.contact-form textarea { min-height: 140px; resize: vertical; }
.contact-form button {
  background: #e53935; color: #fff; border: none;
  padding: 0.75rem 2rem; border-radius: 8px;
  font-size: 0.95rem; cursor: pointer; transition: background 0.2s;
}
.contact-form button:hover { background: #c62828; }
@media(max-width:768px){ .contact-grid { grid-template-columns: 1fr; } }
</style>

<div class="contact-grid">
  <div class="contact-info">
    <h3>📧 Email</h3>
    <p><a href="mailto:jodabire18@gmail.com">jodabire18@gmail.com</a></p>

    <h3>📞 Téléphone</h3>
    <p><a href="tel:+33780546199">07 80 54 61 99</a></p>

    <h3>📍 Localisation</h3>
    <p>Aurillac · Mobilité nationale</p>

    <h3>💼 LinkedIn</h3>
    <p><a href="https://linkedin.com/in/dabsanj18" target="_blank">linkedin.com/in/dabsanj18</a></p>

    <h3>⚙ GitHub</h3>
    <p><a href="https://github.com/Sadabire" target="_blank">github.com/Sadabire</a></p>
  </div>

  <div>
    <form class="contact-form" action="https://formspree.io/f/XXXXXXXX" method="POST">
      <input type="text"  name="name"     placeholder="Votre nom" required>
      <input type="email" name="_replyto" placeholder="Votre email" required>
      <input type="text"  name="subject"  placeholder="Objet">
      <textarea name="message" placeholder="Votre message..." required></textarea>
      <button type="submit">Envoyer le message</button>
    </form>
  </div>
</div>
