# Street Life - Exercice 2

## Description

Site web "Street Life" présentant du contenu sur la culture urbaine et la vie de rue. Ce projet met en œuvre une architecture moderne avec HTML, CSS et un design responsive.

## Structure du projet

```
exercice-2/
├── apache.conf          # Configuration Apache
├── docker-compose.yaml  # Configuration Docker
└── site/
    ├── index.html       # Page d'accueil
    ├── about/           # Page À propos
    ├── archives/        # Page Archives
    ├── contact/         # Page Contact
    ├── panorama/        # Page Panorama
    ├── css/             # Feuilles de style
    └── img/             # Images et ressources
```

## Technologies utilisées

- HTML5
- CSS3 (avec classes utilitaires modernes)
- Design responsive
- Docker & Docker Compose
- Apache HTTP Server

## Démo en ligne

**[Voir le site en ligne](https://html-avancer-1-devoir-exercice-2.clairtyx.com)**

Le site est hébergé sur GitHub Pages avec un domaine personnalisé.

## Installation et démarrage

### Avec Docker (recommandé)

```bash
# Démarrer le conteneur
docker compose up -d

# Arrêter le conteneur
docker compose down
```

Le site sera accessible sur le port configuré dans `docker-compose.yaml`.

### Sans Docker

Servez le contenu du dossier `site/` avec n'importe quel serveur web (Apache, Nginx, etc.).

## Configuration GitHub Pages

Le site est configuré pour être déployé sur GitHub Pages :
- **Dossier source** : `/docs` (copie de `/site`)
- **Domaine personnalisé** : `html-avancer-1-devoir-exercice-2.clairtyx.com`
- **Fichier CNAME** : Configuré dans `/docs/CNAME`

Pour activer GitHub Pages, allez dans les paramètres du dépôt :
1. Settings → Pages
2. Source : Deploy from a branch
3. Branch : `main` / `docs`
4. Configurez votre DNS pour pointer vers GitHub Pages

## Fonctionnalités

- Navigation multi-pages
- Design responsive et moderne
- Architecture CSS modulaire
- Interface utilisateur intuitive
- Pages thématiques (Accueil, Archives, Panorama, À propos, Contact)

## Pages disponibles

- **Accueil** (`/`) - Page d'accueil du site
- **Archives** (`/archives`) - Archives du contenu
- **Panorama** (`/panorama`) - Vue panoramique
- **À propos** (`/about`) - Informations sur le projet
- **Contact** (`/contact`) - Page de contact

## Auteur

**entcorporg**

## Licence

Ce projet est sous licence MIT. Voir le fichier [LICENSE](LICENSE) pour plus de détails.
