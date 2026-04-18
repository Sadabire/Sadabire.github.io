# 🗂️ Portfolio — Joël DABIRE
### sadabire.github.io

> Portfolio personnel de **Saânbèterfaa Joël DABIRE**, étudiant en fin de BUT Science des données et futur ingénieur IA & Big Data à l'ESIGELEC de Poitiers. En recherche d'alternance de 36 mois dès septembre 2026.

---

## 🔗 Lien

**[sadabire.github.io](https://sadabire.github.io)**

---

## 🛠️ Stack technique

| Outil | Usage |
|---|---|
| **Jekyll** | Générateur de site statique |
| **Minimal Mistakes** | Thème de base (remote theme) |
| **GitHub Pages** | Hébergement & déploiement automatique |
| **HTML / CSS / JS** | Design custom (blanc & orange) |
| **Font Awesome** | Icônes |
| **Devicons** | Logos des technologies |
| **Google Fonts** | Typographies Syne & DM Sans |

---

## 📁 Structure du projet

```
Sadabire.github.io/
│
├── _config.yml              # Configuration Jekyll (thème, auteur, plugins)
│
├── index.md                 # Page d'accueil (hero, stats, expertise)
│
├── _pages/
│   ├── about.md             # Page À propos
│   ├── projets.md           # Page Projets
│   ├── competences.md       # Page Compétences
│   ├── experiences.md       # Page Expériences & Formations
│   ├── veille.md            # Page Veille technologique
│   └── contact.md           # Page Contact
│
├── _data/
│   ├── projects.yml         # Données des projets (titre, description, tags, image...)
│   ├── skills.yml           # Données des compétences par catégorie
│   ├── veille.yml           # Ressources de veille technologique
│   └── navigation.yml       # Liens de la navbar
│
├── assets/
│   ├── css/
│   │   └── joel.css         # Fichier CSS principal du design
│   ├── js/
│   │   └── scroll-reveal.js # Animations au scroll
│   └── img/
│       ├── avatar.jpg       # Photo de profil
│       └── projects/        # Captures d'écran des projets
│           ├── croissance.png
│           ├── migration.png
│           ├── deepfake.png
│           ├── ventes.png
│           ├── imputation.png
│           └── powerbi.png
│
├── assets/
│   └── cv-joel-dabire.pdf   # CV téléchargeable
│
└── Gemfile                  # Dépendances Ruby/Jekyll
```

---

## 🚀 Lancer en local

### Prérequis
- Ruby >= 2.7
- Bundler : `gem install bundler`

### Installation
```bash
git clone https://github.com/Sadabire/Sadabire.github.io.git
cd Sadabire.github.io
bundle install
```

### Démarrer le serveur
```bash
bundle exec jekyll serve
```
Ouvrir **http://localhost:4000**

---

## 📦 Déploiement

Chaque push sur la branche `main` déclenche le déploiement automatique via GitHub Pages.

```bash
git add .
git commit -m "description du changement"
git push origin main
```

---

## ➕ Ajouter un projet

Ouvrir `_data/projects.yml` et ajouter un bloc :

```yaml
- id: mon-projet
  title: "Titre du projet"
  description: >-
    Description courte du projet.
  results: >-
    Résultats clés obtenus.
  tags: [Python, Pandas, scikit-learn]
  category: "Machine Learning"
  status: "en_cours"       # ou "terminé"
  github: "https://github.com/Sadabire/mon-repo"
  image: "/assets/img/projects/mon-projet.png"
  demo: ""
  date: 2026
```

Ajouter ensuite la capture d'écran dans `assets/img/projects/`.

---

## 📬 Contact

- **Email** : jodabire18@gmail.com
- **LinkedIn** : [linkedin.com/in/dabsanj18](https://linkedin.com/in/dabsanj18)
- **GitHub** : [github.com/Sadabire](https://github.com/Sadabire)
- **Tél** : 07 80 54 61 99

---

## 📄 Licence

Portfolio personnel — tous droits réservés © 2026 Joël DABIRE.
