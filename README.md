# Street Life - Exercice 2 Portfolio

Projet HTML/CSS avancé présentant un blog et magazine de photographie street life avec une mise en page moderne utilisant Flexbox et Grid CSS.

## 🌐 Liens de démonstration

- **Portfolio** : https://portfolio.clairtyx.com
- **Démo en ligne** : https://html-avancer-1-devoir-exercice-2.clairtyx.com

## 📁 Structure du projet

```
exercice-2/
├── docs/                      # Site web principal
│   ├── index.html            # Page d'accueil avec articles en 3 colonnes
│   ├── about/                # Page "À propos"
│   ├── archives/             # Page des archives
│   ├── panorama/             # Galerie panorama
│   ├── contact/              # Formulaire de contact
│   ├── css/
│   │   └── style.css        # Styles Tailwind-inspired avec classes utilitaires
│   ├── img/                  # Images et icônes du site
│   ├── manifest.json         # Manifest PWA
│   └── browserconfig.xml     # Configuration Microsoft Tiles
├── docker-compose.yaml       # Configuration Docker Apache
├── apache.conf               # Configuration serveur Apache
└── README.md                 # Ce fichier
```

## 🎨 Caractéristiques techniques

### Architecture CSS moderne

Le projet utilise un système de classes utilitaires inspiré de Tailwind CSS :

```css
/* Layout Flexbox */
.flex { display: flex; }
.flex-col { flex-direction: column; }
.flex-row { flex-direction: row; }
.items-center { align-items: center; }
.justify-center { justify-content: center; }
.justify-between { justify-content: space-between; }

/* Spacing */
.gap-4 { gap: 1rem; }
.space-x-4 > * + * { margin-left: 1rem; }
.p-4 { padding: 1rem; }

/* Layout Grid */
.container { max-width: 1280px; }
.mx-auto { margin-left: auto; margin-right: auto; }
```

### Pages et fonctionnalités

#### Page d'accueil (`/docs/index.html`)
- **Layout 3 colonnes** responsive avec Flexbox
- **Articles** avec images, titres, dates et descriptions
- **Navigation** horizontale avec 5 sections
- **Footer** avec liens sociaux et copyright
- **219 lignes** de HTML sémantique

#### Page Archives (`/docs/archives/`)
- Liste chronologique des articles
- Grille responsive d'images
- Même navigation que l'accueil

#### Page Panorama (`/docs/panorama/`)
- Galerie d'images en mode panorama
- Mise en page Grid pour affichage optimal

#### Page Contact (`/docs/contact/`)
- Formulaire de contact structuré
- Validation HTML5

#### Page À propos (`/docs/about/`)
- Présentation du projet Street Life
- Informations sur l'équipe

### SEO et Progressive Web App

Chaque page inclut :
- **Meta tags** optimisés (description, viewport, charset)
- **Icônes multi-plateformes** : Apple Touch Icons (9 tailles), Android, Favicons
- **Manifest PWA** (`manifest.json`) pour installation sur mobile
- **Browserconfig.xml** pour tuiles Windows/Microsoft Edge
- **Titres descriptifs** correspondant au contenu de chaque page

Exemple :
```html
<link rel="apple-touch-icon" sizes="180x180" href="/img/apple-icon-180x180.png">
<link rel="icon" type="image/png" sizes="192x192" href="/img/android-icon-192x192.png">
<link rel="manifest" href="/manifest.json">
<meta name="msapplication-config" content="/browserconfig.xml">
<meta name="theme-color" content="#ffffff">
```

## 🚀 Déploiement

### Version locale avec Docker

```bash
# Démarrer le serveur Apache
docker compose up -d

# Accéder au site
open http://localhost:3001

# Arrêter le serveur
docker compose down
```

Le fichier `docker-compose.yaml` configure :
- **Image** : `httpd:alpine` (serveur Apache léger)
- **Port** : 3001:80 (évite les conflits avec d'autres services)
- **Volumes** : Monte `/docs` en lecture seule dans Apache
- **Configuration** : Utilise `apache.conf` personnalisé
- **Network** : Bridge pour isolation

### Version production avec GitHub Pages

Le dossier `/docs` est déployé automatiquement :
1. Push sur la branche `main`
2. GitHub Pages sert le contenu du dossier `/docs`
3. Accessible via le domaine personnalisé configuré dans `CNAME`

## 🎯 Approche de développement

### Philosophie Flexbox et Grid

Ce projet suit les **bonnes pratiques modernes** du CSS, utilisant massivement Flexbox et Grid pour :

- **Layout fluide** : Adaptation automatique aux différentes tailles d'écran
- **Code maintenable** : Classes utilitaires réutilisables et composables
- **Performance** : Rendu optimisé par les navigateurs modernes
- **Productivité** : Prototypage rapide directement dans le HTML

### Pourquoi ces technologies ?

**Flexbox** et **Grid** sont les standards de l'industrie pour plusieurs raisons :

1. **Alignement puissant** : Centrage vertical/horizontal trivial
2. **Responsive naturel** : Adaptation automatique sans media queries complexes
3. **Lisibilité** : Code plus expressif et maintenable
4. **Adoption massive** : Utilisés par Tailwind CSS, Bootstrap 5, Material UI

### Tailwind CSS comme référence

Le système de classes utilitaires est inspiré de **Tailwind CSS**, la référence incontournable en CSS moderne. Tailwind privilégie massivement Flexbox et Grid dans sa documentation et ses exemples, délaissant les anciennes techniques comme `display: table`.

## 🛠 Technologies utilisées

- **HTML5** : Structure sémantique moderne
- **CSS3** : Flexbox, Grid, variables CSS, classes utilitaires
- **Manifest PWA** : Support Progressive Web App
- **Docker** : Conteneurisation Apache httpd
- **GitHub Pages** : Hébergement statique
- **Apache httpd** : Serveur web pour déploiement local

## 📦 Assets et ressources

### Images
- `logo.jpg` : Logo Street Life dans le header
- `image.jpg`, `picture.jpg`, `cinema.jpg` : Photos d'articles
- Icônes sociales : `pinterest.png`, `google.png`, `facebook.png`, `twitter.png`, `linkedin.png`
- **Icons multi-plateformes** : 13 tailles différentes pour compatibilité maximale

### Fichiers de configuration
- `manifest.json` : Configuration PWA (nom, icônes, couleurs)
- `browserconfig.xml` : Configuration des tuiles Microsoft
- `CNAME` : Domaine personnalisé pour GitHub Pages

## 🎨 Design et UX

- **Palette de couleurs** : Bleu principal, textes gris, accents colorés
- **Typographie** : Système de classes pour tailles et poids
- **Espacements** : Système cohérent avec classes utilitaires
- **Hover effects** : Soulignement et changements de couleur sur les liens
- **Responsive** : Layout adaptatif via Flexbox

## 📊 Statistiques du projet

- **5 pages HTML** complètes et interconnectées
- **~200 lignes** par page HTML en moyenne
- **Système CSS** avec classes utilitaires Tailwind-inspired
- **13 icônes** pour support multi-plateformes
- **PWA-ready** avec manifest et meta tags

---

**Auteur** : Diogo/clairtyx  
**Projet** : HTML Avancé 1 - Exercice 2  
**Date** : Janvier 2026  
**Licence** : Voir fichier LICENSE
