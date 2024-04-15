# L05 - Utilisation de Docker Init

![Hands-On Files](../images/checked-files-50px.png)

Cette fois, nous allons conteneuriser une application Express. Pour ce faire, vous devrez créer un Dockerfile. Les fichiers de l'application Express se trouvent dans le dossier du laboratoire.

Saisissez la commandes Docker suivantes :

    docker init

Plusieurs questions seront posé pour configurer le projet:
- La plateforme utilisé: Node
- La version de Node: 20
- Le gestionnaire de dépendances: npm
- La commande pour partir l'application: npm start
- Le port utilisé: 3000

## Explorer les fichiers généré

Docker init vient de générer les fichiers suivants:
- .dockerignore
- Dockerfile
- compose.yaml
- README.Docker.md

On va se focaliser sur le `Dockerfile` ainsi que sur le fichier de documentation `README.Docker.md`, vous remarquerez que les fichiers possèdent plusieurs commentaires pour vous aider à comprendre chaque opération.

## Exécuter une instance à l'aide de la commande proposé

Dans le terminal, exécuté la commande:

    docker compose up --build

Pointez votre navigateur sur http://localhost:3000

## Arrêter l'instance

Faites `ctr + c` pour arrêter le container.

## Supprimer l'instance

Dans un terminal, exécuté la commande:

    docker compose down

## Supprimer l'image

Dans un terminal, exécuté la commande:

    docker image rm -f l05-utilisationdedockerinit-server:latest
