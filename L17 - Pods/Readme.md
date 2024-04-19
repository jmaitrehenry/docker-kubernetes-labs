# L17 - Pods

![Hands-On Files](../images/checked-files-50px.png)

Commençons par créer un nœud exécutant Nginx en utilisant la méthode impérative.

## Créer le pod

    kubectl run mynginx --image=nginx

## Obtenir une liste des pods en cours d'exécution

    kubectl get pods

## Obtenir plus d'informations

    kubectl get pods -o wide
    kubectl describe pod mynginx

## Supprimer le pod

    kubectl delete pod mynginx

## Créer un pod exécutant BusyBox

Créons maintenant un pod exécutant BusyBox, cette fois en attachant bash à notre terminal.

    kubectl run mybox --image=busybox -it -- /bin/sh

## Lister les dossiers et utiliser la commande base64

    ls
    echo -n 'A Secret' | base64
    exit

## Nettoyer

    kubectl delete pod mybox

## Créer un pod en utilisant la méthode déclarative

Créons maintenant un pod à l'aide d'un fichier YAML.

    kubectl apply -f myapp.yaml

## Obtenir plus d'informations

    kubectl get pods -o wide
    kubectl describe pod myapp-pod

## Ouvrir une session

    kubectl exec -it myapp-pod -- bash

Imprimez la variable d'environnement DBCON qui a été définie dans le fichier YAML.

    echo $DBCON

## Fermer la session

    exit

## Nettoyer

    kubectl delete -f myapp.yaml
