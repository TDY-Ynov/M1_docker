# Elective Docker - YNOV 2023/2024
### DUPUY Tom

___

Ce projet vise à déployer une instance de WordPress à l'aide de Docker Compose, accessible via un reverse proxy, et où
les données sont persistées via MySQL.

___
## Réseaux

Deux réseaux Docker présents :

- **frontend**: Ce réseau est utilisé pour les services accessibles depuis l'extérieur, tels que NGINX.
- **backend**: Ce réseau est destiné aux services internes, tels que WordPress, la base de données et Redis.

## Démarrage

Copier le fichier .env afin d'avoir des variables d'environnement :

`cp .env.example .env`

Avoir docker d'installé (docker compose est inclus), puis lancer le docker compose :

`docker compose up`

Une fois les conteneurs démarrés, vous pouvez accéder à votre site WordPress à
l'adresse [http://localhost](http://localhost). 

Pour vous connecter à l'interface d'administration de WordPress ([http://localhost/wp-admin](http://localhost/wp-admin)),
utilisez les identifiants par défaut suivants :

- **Nom d'utilisateur**: user
- **Mot de passe**: bitnami

## Remarques

- Il peut y avoir un court délai après le démarrage pour que tous les services soient opérationnels.
- Le service Redis est inclus mais non connecté à WordPress pour l'instant.
