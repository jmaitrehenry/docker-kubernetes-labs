# L05 - Utilisation de VS Code

![Hands-On Files](../images/checked-files-50px.png)

Cette fois, nous allons conteneuriser une application Express. Pour ce faire, vous devrez créer un Dockerfile. Les fichiers de l'application Express se trouvent dans le dossier du laboratoire.

## Ajouter un fichier Dockerfile

À l'aide des outils de Code, ajoutez un nouveau Dockerfile en ouvrant la palette de commandes dans le menu Affichage.

Tapez **Docker Add** et sélectionnez **Docker Add Docker Files to Workspace**, plusieurs questions seront posé pour configurer le projet:
- La plateforme utilisé: Node.js
- Le port utilisé: 3000
- Inclure les fichiers relié à Docker Compose?: Oui

## Construire l'image à l'aide de Code

Ouvrez à nouveau la palette de commandes et lancez une **Docker Build**. Le code utilisera le nom de l'application dans le package.json et ajoutera `latest`, par exemple, ici, cela donnera `myexpressapp:latest`. Si vous voulez changer le tag de l'image, vous pouvez utiliser la commande **Docker Tag**.

## Exécuter une instance à l'aide de Code

Ouvrez à nouveau la palette de commandes et lancez une **Docker Image: Run**.

Pointez votre navigateur sur http://localhost:3000

## Lister les conteneurs en cours d'exécution

Cliquez sur l'icône Docker dans le menu de gauche. Vous pourrez voir l'image que vous venez de créer et l'instance en cours d'exécution.

## Arrêter l'instance

Faites un clic droit sur le nom de l'instance et arrêtez-la.

## Supprimer l'image

Faites un clic droit sur le nom de l'image et supprimez-la.
