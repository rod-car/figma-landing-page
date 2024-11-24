# Figma Community Landing Page

## Installation

### Prérequis

Avant d'installer les dépendances, assurez-vous d'avoir installé les prérequis suivants :
- **Node.js** : Version 18 ou supérieure ([Télécharger Node.js](https://nodejs.org))
- **Yarn** : Gestionnaire de dépendances ([Télécharger Yarn](https://yarnpkg.com/))
- **Git** : Outil de gestion de version ([Télécharger Git](https://git-scm.com/))
- **Git Flow** : Extension pour la gestion de l'architecture Git ([En savoir plus sur Git Flow](https://danielkummer.github.io/git-flow-cheatsheet/))

---

### Installation des dépendances

Le projet utilise Yarn comme gestionnaire de paquets, mais vous êtes libre d'utiliser un autre outil si vous le souhaitez.

```bash
# Installer les dépendances avec Yarn
yarn install
```

---

## Lancer le serveur de développement

Démarrez le serveur de développement à l'adresse `http://localhost:3000` :

```bash
# Lancer le serveur en mode développement
yarn dev
```

---

## Lancer le serveur en mode production

Construisez l'application en mode production. Notez que ce mode dépend de Node.js :

```bash
# Construire l'application en mode production
yarn build
```

Cette commande génère un dossier `.output` à la racine du projet.

Pour visualiser l'application en mode production sur votre environnement local à l'adresse `http://localhost:3000` :

```bash
# Prévisualiser la version production
yarn preview
```

---

## Générer une version statique

Générez une version statique de l'application qui n'a pas besoin de Node.js :

```bash
# Générer la version statique
yarn generate
```

Vous trouverez un fichier `index.html` dans le dossier `.output/public` à la racine du projet. Ce dossier contient une version statique de l'application, qui peut être déployée sur un serveur simple.

---

## Documentation complémentaire

Pour plus d'informations sur le fonctionnement de Nuxt, consultez la documentation officielle [ici](https://nuxt.com/)