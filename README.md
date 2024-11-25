# **Figma Community Landing Page**

## **Description**
Ce projet est l'intégration d'une maquette de landing page issue de Figma, accessible via ce [lien](https://www.figma.com/design/PCgqHKvN3SNtggBlcZ5uUK/figmaland-business-landing-page-community?m=auto&t=ZBmlGyVhAqpR5NGW-6).

Il repose sur les technologies suivantes :
- **[Nuxt](https://nuxt.com)** : un framework puissant pour Vue.js, facilitant la création de sites web modernes et performants.
- **[Tailwind CSS](https://tailwindcss.com)** : un framework CSS utilitaire, conçu pour simplifier la gestion des styles.

Retrouvez les détails pour l'installation et l'utilisation dans le fichier [INSTALL.md](INSTALL.md).

---

## **Architecture des dossiers**
Voici la structure des dossiers du projet :

- **`/pages`** : Contient toutes les pages du site.
  - L'arborescence de ce dossier reflète l'arborescence des URL. Par exemple, le fichier `index.vue` situé à la racine correspond à l'URL `/`.

- **`/components`** : Regroupe tous les composants utilisés dans le projet, organisés comme suit :
  - **`Card`** : Composants sous forme de cartes (ex. : présentation des offres tarifaires).
  - **`Form`** : Composants liés aux formulaires, comme les champs de saisie (`Input`) et les zones de texte (`Textarea`).
  - **`Structure`** : Composants structurants, incluant les sections personnalisées, boutons d'action et liens de navigation.
  - **Racine** : Inclut des éléments globaux tels que l'en-tête et le pied de page.

- **`/assets`** : Contient les ressources complémentaires telles que les fichiers CSS et les polices personnalisées.

- **`/public`** : Regroupe les fichiers publics, y compris les images, logos et favicons. Les images sont organisées en sous-dossiers selon leur utilisation :
  - **`/contact`**, **`/features`**, **`/partners`**, **`/social`**, **`/testimonials`**.

- **`/server`** : Dossier utilisé pour la gestion côté serveur de Nuxt.

---

## **Fichiers importants**
Voici une liste des fichiers clés du projet :

- **`composer.json`** : Répertorie toutes les dépendances du projet.
- **`app.vue`** : Fichier de base qui charge toutes les pages et les composants de Nuxt.
- **`nuxt.config.ts`** : Fichier de configuration principal pour Nuxt.

---

Voici une section "Plugins" que vous pouvez ajouter à votre fichier README :

---

Voici une version enrichie de votre section **Modules et librairies** :

---

## **Modules et Librairies**
Ce projet s'appuie sur des modules Nuxt et des services tiers pour améliorer ses fonctionnalités, notamment la gestion des images, les interfaces utilisateur et la communication via formulaire de contact :

- **[@nuxt/image](https://nuxt.com/modules/image)** :  
  Un module performant pour la gestion des images, offrant des fonctionnalités telles que :
  - Chargement progressif.
  - Redimensionnement en temps réel.
  - Prise en charge de multiples fournisseurs.

- **[Web3Forms](https://web3forms.com/platforms/nuxt-contact-form)** :  
Un service fiable pour gérer l'envoi de messages via le formulaire de contact intégré.
  - Fonctionne sans configuration serveur complexe.
  - Compatible avec Nuxt pour une intégration rapide et sécurisée.

---

## **Installation**
Pour installer et démarrer ce projet, veuillez consulter le fichier [INSTALL.md](INSTALL.md). Ce document décrit :
- Les prérequis nécessaires.
- Les étapes détaillées d'installation.
- Les commandes pour exécuter le projet en environnement local.

---

## **Contributions**
Les contributions sont les bienvenues ! Si vous souhaitez participer, suivez ces étapes :
1. **Forkez** ce dépôt.
2. Créez une nouvelle branche pour vos modifications :
   ```bash
   git checkout -b feature/new-feature
   # Ou si vous avez git flow
   git flow feature start new-feature
   ```  
3. **Testez** vos modifications avant de soumettre une pull request.

---

## **Captures d'écran**
Vous trouverez ci-dessous une capture d'écran représentant la première page de la version HTML de l'application.

![Landing page](/assets/screenshot/landing_page.png?raw=true "Landing page")

---

## **Licences**
Ce projet est sous licence [MIT](https://opensource.org/license/mit). Vous êtes libre de l'utiliser, de le modifier et de le partager selon les termes de cette licence.

---

## **Contact**
Pour toute question ou suggestion, n'hésitez pas à nous contacter via [ghislaincarino@gmail.com](mailto:ghislaincarino@gmail.com).