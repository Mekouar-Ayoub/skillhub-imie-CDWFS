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
