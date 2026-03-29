# Portfolio — Joël DABIRE
## Sadabire.github.io

Portfolio personnel construit avec **Jekyll** et le thème **Minimal Mistakes**.

---

## Mise en place locale

### 1. Prérequis
- Ruby >= 2.7 ([installer Ruby](https://www.ruby-lang.org/fr/documentation/installation/))
- Bundler : `gem install bundler`

### 2. Cloner et installer
```bash
git clone https://github.com/Sadabire/Sadabire.github.io.git
cd Sadabire.github.io
bundle install
```

### 3. Lancer en local
```bash
bundle exec jekyll serve
# → Ouvrir http://localhost:4000
```

---

## Déploiement sur GitHub Pages

Chaque `git push` sur la branche `main` déclenche le déploiement automatique.

```bash
git add .
git commit -m "feat: mise à jour portfolio"
git push origin main
```

Le site est accessible sur : **https://sadabire.github.io**

---

## Ajout de projet

 Dans `_data/projects.yml`  j'ajoute un bloc :

```yaml
- id: mon-nouveau-projet
  title: "Titre du projet"
  description: >-
    Description courte du projet.
  tags: [Python, Pandas, scikit-learn]
  category: "Machine Learning"
  status: "en_cours"      # ou "terminé"
  github: "https://github.com/Sadabire/mon-repo"
  date: 2026
```

---

## Structure des fichiers

```
Sadabire.github.io/
├── _config.yml          ← configuration principale
├── _data/
│   ├── projects.yml     ← liste des projets
│   ├── skills.yml       ← compétences
│   ├── veille.yml       ← ressources de veille
│   └── navigation.yml  ← menu de navigation
├── _pages/
│   ├── about.md
│   ├── competences.md
│   ├── projets.md
│   ├── experiences.md
│   ├── veille.md
│   └── contact.md
├── assets/
│   ├── img/avatar.jpg   ← ma photo de profil
│   └── cv-joel-dabire.pdf ← mon CV à télécharger
└── index.md             ← page d'accueil
```

