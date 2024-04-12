# L11 - Compose dans une VM

![Hands-On Files](../images/checked-files-50px.png)

Déployons une application multi-conteneurs.

---

## Facultativement, construisez le reverse proxy et poussez-le vers un registre

    docker build -t [yourRegistry]/reverseproxy:latest .
    docker push [yourRegistry]/reverseproxy:latest

Modifiez le fichier Compose pour modifier l'emplacement de l'image du proxy inverse.

---

## Testez l'application localement

Utilisez docker compose pour créer et exécuter l'application localement.

    docker compose up -d

Ouvrez un navigateur et tapez http://localhost/hello

Dans un nouvel onglet du navigateur, tapez http://localhost/bonjour

Notez que le nom du serveur est différent.


## Nettoyer

    docker compose down
