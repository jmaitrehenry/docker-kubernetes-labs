# L18 - Pods Multi Conteneurs

![Hands-On Files](../images/checked-files-50px.png)

Créons plusieurs conteneurs dans un pod à l'aide d'un fichier YAML. Nous utiliserons le conteneur Busybox pour obtenir la page par défaut servie par le conteneur Nginx.

## Créer le pod

    kubectl create -f two-containers.yaml

## Obtenir des informations

    kubectl get pods -o wide
    kubectl describe pod two-containers

## Connectez-vous au conteneur BusyBox

    kubectl exec -it two-containers --container mybox -- /bin/sh

## Récupérer la page HTML servie par le conteneur Nginx

Cela affichera le contenu de la page Web dans le terminal.

    wget -qO- localhost

## Fermer la session

    exit

## Nettoyer

    kubectl delete -f two-containers.yaml --force --grace-period=0
