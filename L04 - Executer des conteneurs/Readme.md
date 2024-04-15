# L04 - Executer des conteneurs

Saisissez les commandes Docker suivantes :

## Créons une instance de l'image

    docker run -d -p 8080:80 --name hello myapp:v1

## Lister les conteneurs en cours d'exécution

    docker ps

## Affichez la page

À l'aide de curl (Mac ou linux)

    curl localhost:8080

ou utilisez votre navigateur. Aller vers http://localhost:8080

## Ouvrir une session sur le conteneur

    docker container exec -it  hello ash  

## Stopper le conteneur

    docker stop hello

## Arrêtez le conteneur

Actualisez le navigateur pour confirmer qu'il s'est arrêté

    docker stop hello

## Lister les conteneurs en cours d'exécution

Vous ne devriez plus voir l'instance hello-world:v1.

    docker ps

## Supprimer l'instance

    docker rm hello

## Confirmer que le conteneur n'est plus en cours d'exécution

    docker ps

## Enlever l'image

    docker rmi myapp:v1
