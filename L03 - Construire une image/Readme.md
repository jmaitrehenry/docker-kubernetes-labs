# L03 - Construire une image

![Hands-On Files](../images/checked-files-50px.png)

Nous voulons conteneuriser une simple page HTML. Pour ce faire, vous devrez créer un fichier Dockerfile.

## Ajouter un fichier Dockerfile

Ajoutez un nouveau fichier et nommez-le **Dockerfile** (sans aucune extension de fichier).

Copiez et collez ce qui suit dans le fichier et enregistrez-le :

    FROM nginx:alpine
    COPY index.html /usr/share/nginx/html

## Construire l'image

    docker build -t hello-world:v1 .

## Lister les images

    docker images
    docker image ls

## Créer un nouveau tag pour l'image

    docker tag hello-world:v1 myapp:v1

## L'image est-elle toujours présente ?

    docker images

## Supprimer l'image

    docker rmi hello-world:v1
