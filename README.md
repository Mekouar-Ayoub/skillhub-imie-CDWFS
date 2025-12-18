📦 SkillHub Starter Pack - Structure Complète
README.md
Copy# SkillHub - Symfony Starter Pack

Projet squelette Symfony pour SkillHub avec authentification et gestion des formateurs.

## 🚀 Installation Rapide

```bash
# Cloner le repository
git clone https://github.com/votre-organisation/skillhub-starter.git skillhub
cd skillhub

# Installer les dépendances
composer install

# Configurer la base de données
cp .env .env.local
# Éditer .env.local avec vos credentials MySQL

# Créer la base de données
php bin/console doctrine:database:create
php bin/console doctrine:migrations:migrate

# Charger les fixtures (données de test)
php bin/console doctrine:fixtures:load

# Lancer le serveur
symfony serve
🔑 Comptes de Test
Admin : admin@skillhub.fr / admin123
Formateur : trainer@skillhub.fr / trainer123
Étudiant : student@skillhub.fr / student123
📁 Structure du Projet
skillhub/
├── config/packages/security.yaml    # Configuration sécurité
├── src/
│   ├── Controller/
│   │   ├── LoginController.php      # Authentification
│   │   └── TrainerController.php    # Liste formateurs
│   ├── Entity/
│   │   └── User.php                 # Entité utilisateur avec rôles
│   └── Repository/
│       └── UserRepository.php       # Requêtes personnalisées
└── templates/
    ├── base.html.twig               # Layout de base
    ├── security/login.html.twig     # Page connexion
    └── trainer/index.html.twig      # Liste formateurs
🎯 Fonctionnalités Incluses
✅ Authentification Symfony Security
✅ Système de rôles (USER, TRAINER, ADMIN)
✅ Page de connexion stylée avec Tailwind CSS
✅ Liste des formateurs accessible à /trainers
✅ Fixtures pour données de test
✅ Configuration de base prête à l'emploi

📖 Routes Disponibles
GET / - Page d'accueil
GET /login - Connexion
POST /logout - Déconnexion
GET /trainers - Liste des formateurs
🛠️ Technologies
PHP 8.1+
Symfony 6.4
Doctrine ORM
Tailwind CSS (CDN)
MySQL 8.0
📝 Prochaines Étapes
Intégrer votre landing page HTML/CSS dans templates/
Créer l'entité Workshop avec relations
Implémenter le CRUD des workshops
Ajouter le système d'inscription aux ateliers
🤝 Contribution
Les étudiants du Bachelor CDWFS 2025-2026 peuvent contribuer via Pull Requests.

📄 Licence
MIT License - Formation SkillHub


---

### **Instructions de Déploiement sur GitHub**

```bash
# 1. Vous avez deja le repository Git
# Allez sur github.com et créez un nouveau repository nommé "skillhub-starter"

# 4. Créer un tag de version
git tag -a v1.0.0 -m "Version 1.0.0: Starter pack avec auth et liste formateurs"
git push origin v1.0.0
Fichiers Clés à Inclure (mettez les dans EC02)
1. .gitignore

###> symfony/framework-bundle ###
/.env.local
/.env.local.php
/.env.*.local
/config/secrets/prod/prod.decrypt.private.php
/public/bundles/
/var/
/vendor/
###> symfony/phpunit-bridge ###
.phpunit.result.cache
/phpunit.xml
###> phpunit/phpunit ###
/phpunit.xml
.phpunit.result.cache
2. composer.json (extrait)

Copy{
    "name": "skillhub/starter",
    "type": "project",
    "description": "SkillHub Symfony Starter Pack",
    "require": {
        "php": ">=8.1",
        "symfony/console": "6.4.*",
        "symfony/framework-bundle": "6.4.*",
        "symfony/security-bundle": "6.4.*",
        "symfony/twig-bundle": "6.4.*",
        "symfony/orm-pack": "^2.0",
        "doctrine/doctrine-bundle": "^2.10",
        "doctrine/doctrine-migrations-bundle": "^3.2"
    }
}
3. .env (exemple)

APP_ENV=dev
APP_SECRET=changeme

DATABASE_URL="mysql://root:password@127.0.0.1:3306/skillhub?serverVersion=8.0"
🚀 Pour push sur GitHub
Option A - Via GitHub Desktop :
Option B - Via Ligne de Commande : Utilisez les commandes fournies ci-dessus dans "Instructions de Déploiement"
