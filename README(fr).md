# 🚀 Pipline GSS : Hugo + Blowfish + GitHub Pages

Ce dépôt est un **template prêt à l’emploi** pour créer un site statique avec [Hugo](https://gohugo.io/) et le thème [Blowfish](https://blowfish.page/), automatiquement déployé sur **GitHub Pages**.

---

## 🧪 Étapes pour créer un nouveau blog

### 1. 📄 Créer un nouveau repo avec ce template

- Clique sur le bouton **"Use this template"** (en haut à droite sur GitHub)
- Choisis un **nom de repo** (ex : `mon-blog`)
- Assure-toi qu’il est **public**
- Valide

---

### 2. ⚙️ Activer Action > GitHub Pages

- Va dans `Settings` → `Pages`
- Dans **Build and Deployment**, choisis :
  - Source : `GitHub Actions`
- C’est tout. GitHub Pages va attendre le workflow.

---

### 3. 🛠️ Modifier `hugo.toml`

Avant de déployer en local, édite le fichier `hugo.toml` :

```toml
baseURL = 'https://<ton-user>.github.io/<nouveau-repo>/'
languageCode = 'fr-fr'
title = 'Mon blog'
theme = 'blowfish'

[params]
  defaultTheme = "auto"
  ShowReadingTime = true
  ShowPostNavLinks = true
```

exemple 
pages : https://wilonweb.github.io/test-template/
code : https://github.com/wilonweb/test-template

### 4 Preaprer la homepage. 

Une fois les images, couleur, police choisie. 
Pour cela dans le hugo.toml

[params.homepage]
  layout = "profile"                      # ← important
  homepageImage = "/img/background.svg"   # fond

### 5 Les images 

Blowfish recommande une miniature 16:9, environ :
👉 1280 × 720 px
ou
👉 1600 × 900 px (qualité un peu meilleure)

C’est ce qui donne le meilleur rendu dans :
la page d’accueil (liste des posts)
les sections / catégories
les composants card et featured posts

Pourquoi 16:9 ?
Parce que Blowfish utilise par défaut le mode cover dans les cards, donc une image horizontale large remplit mieux l’espace.

## TODO 
Deployer test-template en local
