# Minimal API with Spring Framework and Docker

## Description
Il s'agit d'un petit projet conçu pour apprendre comment utiliser le Framework Spring avec Docker.
C'est une API simple qui utilise une base de données MySQL pour le stockage des données.

L'API fournit des endpoints pour effectuer des opérations CRUD (Create, Read, Update, Delete) sur une entité spécifique.

## Configuration de Docker
Pour exécuter ce projet à l'aide de Docker, vous pouvez suivre ces étapes :

1. Assurez-vous d'avoir Docker installé sur votre système.
2. Clonez ce dépôt sur votre machine locale.
3. Ouvrez un terminal et rendez-vous dans le répertoire racine du projet.
4. Exécutez la commande suivante pour construire le projet avec Maven : `mvn clean package -Dmaven.test.skip=true`
5. Ensuite, exécutez la commande suivante pour démarrer les conteneurs Docker : `docker-compose up -d`
6. L'API sera accessible à l'adresse : http://localhost:9000/employees
L'interface phpMyAdmin (pour la gestion de la base de données) sera accessible à l'adresse : http://localhost:8081

## Configuration
L'API utilise la base de données MySQL. La configuration de la base de données peut être modifiée dans le fichier `application.properties` situé dans le répertoire `src/main/resources`. Vous pouvez y configurer les propriétés de connexion à la base de données telles que l'URL, le nom d'utilisateur et le mot de passe.

## Données Initiales
Le projet est pré-configuré pour charger des données initiales dans la base de données à partir du fichier `data.sql` situé dans le répertoire `src/main/resources`.

## Utilisation
Une fois l'application démarrée, vous pouvez accéder à l'API en utilisant l'URL suivante :
http://localhost:9000/employees

### Endpoints

L'API expose les endpoints suivants :

- `GET /employees` : Récupère toutes les entités.
- `GET /employees/{id}` : Récupère une entité spécifique en utilisant son ID.
- `POST /employees/create` : Crée une nouvelle entité.
- `PUT /employees/update/{id}` : Met à jour une entité existante en utilisant son ID.
- `DELETE /employees/{id}` : Supprime une entité existante en utilisant son ID.