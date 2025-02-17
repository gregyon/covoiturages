# Covoiturage Écologique

## Description
Covoiturage Écologique est une application web développée avec **Symfony** qui permet aux utilisateurs de trouver et de proposer des trajets de covoiturage en mettant l'accent sur les véhicules électriques et les pratiques respectueuses de l'environnement.

##  Technologies
- **Symfony 6+**
- **Twig** (pour le rendu des vues)
- **Doctrine** (ORM pour la gestion de la base de données)
- **Bootstrap/Tailwind** (pour le design responsive)
- **API Google Maps** (pour la gestion des itinéraires)
- **Fly.io** (pour le déploiement)

---

## Installation & Configuration

###  1. Cloner le projet
```bash
git clone https://github.com/ton-repo/covoiturage-eco.git
cd covoiturage-eco
```

###  2. Installer les dépendances
```bash
composer install
npm install  # Si des assets front sont inclus
```

###  3. Configurer l'environnement
Créer un fichier `.env.local` et y ajouter les variables nécessaires :
```ini
DATABASE_URL="mysql://user:password@127.0.0.1:3306/covoiturage"
APP_ENV=dev
APP_SECRET=your_secret_key
```

###  4. Créer la base de données
```bash
php bin/console doctrine:database:create
php bin/console doctrine:migrations:migrate
```

###  5. Lancer le serveur local
```bash
symfony server:start
```
Ou avec PHP directement :
```bash
php -S 127.0.0.1:8000 -t public
```
Accéder à l'application sur `http://127.0.0.1:8000`

---

##  Fonctionnalités
-  **Recherche de trajets** (par ville et date)
-  **Filtres avancés** (prix, durée, note du conducteur, voyage écologique)
-  **Gestion des comptes** (création de compte, espace utilisateur)
-  **Publication de trajets** (ajout de trajets par les conducteurs)
-  **Gestion des crédits** (utilisation et mise à jour des crédits)
-  **Espace administrateur** (gestion des utilisateurs, validation des avis, suivi des performances)

---

##  Déploiement sur Fly.io

### 1️ Installer Fly.io CLI
```bash
curl -fsSL https://fly.io/install.sh | sh
fly auth login
```

### 2️ Initialiser le projet sur Fly.io
```bash
fly launch
```
Suivre les instructions pour configurer l'application.

### 3️ Déployer
```bash
fly deploy
```
L'application sera accessible à l'URL fournie par Fly.io.

---

##  Licence
Ce projet est sous licence **MIT**.

##  Contributeurs
- **José** (Product Owner)
- **Équipe de développement Symfony**

 Bon développement et bon covoiturage ! 


