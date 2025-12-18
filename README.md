# Teamsync 🚀

Une plateforme moderne de gestion de tâches collaboratives construite avec Laravel, conçue pour améliorer la productivité et la collaboration en équipe.

## 📋 Description

Teamsync est une application web complète qui permet aux équipes de gérer leurs projets, tâches et collaborations de manière efficace. La plateforme offre une interface intuitive pour organiser le travail, suivre les progrès et faciliter la communication entre les membres de l'équipe.

## ✨ Fonctionnalités principales

### Gestion de projets
- 📁 **Création de projets** :  Organisez votre travail en projets distincts
- 📊 **Tableaux de bord** : Visualisez l'avancement de vos projets en temps réel
- 🎯 **Suivi des objectifs** : Définissez et suivez les objectifs de chaque projet

### Gestion des tâches
- ✅ **Création de tâches** : Ajoutez des tâches avec descriptions, priorités et échéances
- 👥 **Attribution** : Assignez des tâches aux membres de l'équipe
- 🔄 **Statuts personnalisables** : À faire, En cours, Terminé, etc. 
- 📝 **Commentaires** : Discutez et collaborez sur chaque tâche

### Collaboration d'équipe
- 👤 **Gestion des utilisateurs** : Invitez et gérez les membres de votre équipe
- 🔐 **Rôles et permissions** : Admin, Chef de projet, Membre
- 💬 **Communication** : Échangez avec votre équipe directement dans l'application
- 🔔 **Notifications** : Restez informé des mises à jour importantes

### Interface utilisateur
- 🎨 **Design moderne** : Interface épurée avec Tailwind CSS
- 📱 **Responsive** : Fonctionne sur ordinateurs, tablettes et smartphones
- 🌙 **Mode sombre/clair** : Adaptez l'interface à vos préférences
- ⚡ **Performance optimisée** : Navigation rapide avec Vite

## 🛠️ Technologies utilisées

### Backend
- **Framework** : Laravel 11.x
- **Langage** : PHP >= 8.2
- **Base de données** : MySQL
- **ORM** : Eloquent
- **Authentification** : Laravel Sanctum
- **API** : RESTful API avec Laravel

### Frontend
- **Template Engine** : Blade
- **CSS Framework** : Tailwind CSS
- **Build Tool** : Vite
- **JavaScript** :  Vanilla JS / Alpine.js

### Outils de développement
- **Gestionnaire de dépendances PHP** : Composer
- **Gestionnaire de dépendances JS** : npm
- **Tests** : PHPUnit
- **Linter** : PHP CS Fixer

## 📋 Prérequis

Avant de commencer, assurez-vous d'avoir installé : 

- **PHP** >= 8.2
- **Composer** (dernière version)
- **Node.js** >= 16.x et npm
- **MySQL** >= 5.7 ou MariaDB >= 10.3
- **Git**

## 🚀 Installation

### 1. Cloner le dépôt

```bash
git clone https://github.com/18325/framework_2024_maurille-maxime.git
cd framework_2024_maurille-maxime
```

### 2. Installer les dépendances PHP

```bash
composer install
```

### 3. Installer les dépendances JavaScript

```bash
npm install
```

### 4. Configuration de l'environnement

```bash
# Copier le fichier d'environnement
cp .env.example .env

# Générer la clé de l'application
php artisan key: generate
```

### 5. Configurer la base de données

Éditez le fichier `.env` et configurez vos paramètres de base de données : 

```env
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=teamsync
DB_USERNAME=votre_utilisateur
DB_PASSWORD=votre_mot_de_passe
```

Créez la base de données : 

```sql
CREATE DATABASE teamsync CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci;
```

### 6. Exécuter les migrations

```bash
php artisan migrate
```

### 7. (Optionnel) Peupler la base de données

```bash
php artisan db:seed
```

### 8. Compiler les assets

```bash
# Mode développement
npm run dev

# Mode production
npm run build
```

## 💻 Utilisation

### Démarrer le serveur de développement

```bash
php artisan serve
```

L'application sera accessible à l'adresse : **http://127.0.0.1:8000**

### Connexion administrateur

Utilisez les identifiants suivants pour vous connecter en tant qu'administrateur :

- **Email** : maryse@example.com
- **Mot de passe** : password123

⚠️ **Important** : Changez ces identifiants en production !

## 📦 Structure du projet

```
framework_2024_maurille-maxime/
├── app/                    # Code de l'application
│   ├── Http/
│   │   ├── Controllers/   # Contrôleurs
│   │   └── Middleware/    # Middlewares
│   ├── Models/            # Modèles Eloquent
│   └── Providers/         # Service Providers
├── bootstrap/             # Fichiers de démarrage Laravel
├── config/                # Fichiers de configuration
├── database/
│   ├── migrations/        # Migrations de base de données
│   ├── seeders/           # Seeders
│   └── factories/         # Factories pour les tests
├── public/                # Point d'entrée web et assets publics
├── resources/
│   ├── views/             # Templates Blade
│   ├── css/               # Fichiers CSS
│   └── js/                # Fichiers JavaScript
├── routes/
│   ├── web.php            # Routes web
│   └── api. php            # Routes API
├── storage/               # Fichiers générés (logs, cache, uploads)
├── tests/                 # Tests automatisés
│   ├── Feature/           # Tests fonctionnels
│   └── Unit/              # Tests unitaires
├── .env. example           # Exemple de configuration
├── composer.json          # Dépendances PHP
├── package.json           # Dépendances JavaScript
├── tailwind.config.js     # Configuration Tailwind CSS
├── vite.config.js         # Configuration Vite
└── README.md
```

## 🎯 Fonctionnalités détaillées

### Pour les administrateurs
- Gestion complète des utilisateurs et des permissions
- Création et configuration des espaces de travail
- Accès aux statistiques et rapports
- Configuration des paramètres de l'application

### Pour les chefs de projet
- Création et gestion de projets
- Attribution des tâches aux membres
- Suivi de l'avancement des projets
- Génération de rapports

### Pour les membres de l'équipe
- Consultation des tâches assignées
- Mise à jour du statut des tâches
- Ajout de commentaires et collaboration
- Gestion du profil personnel

## 🔧 Commandes artisan utiles

```bash
# Créer un nouveau contrôleur
php artisan make:controller NomController

# Créer un nouveau modèle avec migration
php artisan make:model NomModele -m

# Créer une nouvelle migration
php artisan make:migration nom_de_la_migration

# Exécuter les migrations
php artisan migrate

# Annuler la dernière migration
php artisan migrate:rollback

# Vider le cache
php artisan cache:clear
php artisan config:clear
php artisan route:clear
php artisan view:clear

# Lancer les tests
php artisan test
```

## 🧪 Tests

```bash
# Exécuter tous les tests
php artisan test

# Exécuter les tests avec coverage
php artisan test --coverage

# Exécuter un test spécifique
php artisan test --filter NomDuTest

# Tests avec PHPUnit
vendor/bin/phpunit
```

## 🚀 Déploiement

### Préparation pour la production

```bash
# Optimiser l'autoloader
composer install --optimize-autoloader --no-dev

# Mettre en cache la configuration
php artisan config:cache

# Mettre en cache les routes
php artisan route:cache

# Mettre en cache les vues
php artisan view:cache

# Compiler les assets
npm run build
```

### Configuration de production

Dans votre fichier `.env` de production :

```env
APP_ENV=production
APP_DEBUG=false
APP_URL=https://votre-domaine.com

# Utilisez une clé forte
APP_KEY=base64:votre_cle_generee
```

## 🔐 Sécurité

- ✅ Protection CSRF activée
- ✅ Authentification sécurisée avec Laravel Sanctum
- ✅ Hashage des mots de passe avec bcrypt
- ✅ Validation des données côté serveur
- ✅ Protection contre les injections SQL (Eloquent ORM)
- ✅ Limitation du taux de requêtes (Rate Limiting)

## 📱 Responsive Design

L'application est entièrement responsive et optimisée pour : 
- 💻 Ordinateurs de bureau (1920px et plus)
- 💻 Laptops (1024px - 1919px)
- 📱 Tablettes (768px - 1023px)
- 📱 Smartphones (320px - 767px)

## 🤝 Contribution

Les contributions sont les bienvenues ! Pour contribuer :

1. Forkez le projet
2. Créez une branche pour votre fonctionnalité (`git checkout -b feature/NouvelleFonctionnalite`)
3. Committez vos changements (`git commit -m 'Ajout d'une nouvelle fonctionnalité'`)
4. Poussez vers la branche (`git push origin feature/NouvelleFonctionnalite`)
5. Ouvrez une Pull Request

## 📄 Licence

Ce projet est sous licence MIT. Voir le fichier [LICENSE](LICENSE) pour plus de détails.

## 👥 Auteurs

**Maurille KOMI et Maxime DASSI** 

GitHub:  [@18325](https://github.com/18325)

## 🙏 Remerciements

- Laravel pour le framework PHP exceptionnel
- Tailwind CSS pour le framework CSS utilitaire
- La communauté open source pour les packages utilisés

## 📞 Support

Pour toute question ou problème : 
- Ouvrez une [issue](https://github.com/18325/framework_2024_maurille-maxime/issues) sur GitHub
- Consultez la [documentation Laravel](https://laravel.com/docs)

---

🚀 **Boostez la productivité de votre équipe avec Teamsync !**
