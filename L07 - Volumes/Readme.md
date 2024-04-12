# L07 - Volumes

## Ouvrir un terminal et créer un volume

    docker volume create myvol

## Listez les volumes

    docker volume ls

## Exécutez un conteneur nginx qui utilisera le volume

    docker run -d --name voltest -v myvol:/app nginx:latest

## Connectez-vous à l'instance

    docker exec -it voltest bash

## Let’s create a file in the volume

    cd /app
    echo Hello > test.txt

Détachez-vous de l'instance:

    exit

## Arrêter et retirer le conteneur

    docker stop voltest
    docker rm voltest

## Exécutez-le à nouveau et voyez si le fichier existe toujours

    docker run -d --name voltest -v myvol:/app nginx:latest
    docker exec -it voltest bash
    cd app
    cat test.txt
    exit

## Nettoyer

    docker stop voltest
    docker rm voltest
    docker volume rm myvol
