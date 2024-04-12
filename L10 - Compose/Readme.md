
# L10 - Compose

![Hands-On Files](../images/checked-files-50px.png)

Utilisons Docker Compose.

## Déployer l'application

    docker compose up -d
    docker compose ls
    docker compose ps

## Déployer une deuxième version en utilisant un nom de projet différent

    docker compose -p test up -d

Cela échoue car le port localhost 8080 est déjà attribué.

## Supprimez la première application et modifiez le fichier Compose

    docker compose down

Modifiez la valeur des ports de

    - "8080:80"

a

    - "8081"

## Déployer à nouveau

    docker compose up -d
    docker compose -p test up -d
    docker compose ls

## Nettoyer

    docker compose down
    docker compose ls
    docker compose -p test down
    docker compose ls
