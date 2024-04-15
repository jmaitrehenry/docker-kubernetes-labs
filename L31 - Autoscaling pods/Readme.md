# L31 - Autoscaling pods

![Hands-On Files](../images/checked-files-50px.png)

Utilisons le Horizontal Pod Autoscaler pour redimensionner un pod.

## Metrics Server

Le Metrics Server est-il installé dans votre cluster ? Recherchez un pod appelé **metrics-server**

    kubectl get po -A 

Sinon, installez le Metrics Server à l'aide de la commande suivante:

    kubectl apply -f metric-server/components.yaml


## Créer le déploiement

    kubectl apply -f deploy.yaml

    kubectl get pods

## Définir les limites d'autoscaling

    kubectl autoscale deployment hpa-deployment --cpu-percent=50 --min=1 --max=10

Valider

    kubectl get hpa

## Déployer le Busybox

    kubectl apply -f pod.yaml

## Connectez-vous au conteneur BusyBox

    kubectl exec mybox -it -- /bin/sh

## Augmenter la charge

Tapez cette boucle sans fin :

    while true; do wget -q -O- http://php-apache; done

Valider dans un autre terminal :

    kubectl get hpa --watch


## Arrêtez la boucle sans fin

Appuyez sur **Ctrl-C** pour terminer la boucle et tapez **exit**.

## Supprimer l'autoscaler

    kubectl delete hpa hpa-deployment

## Nettoyer

    kubectl delete -f pod.yaml --grace-period=0 --force
    kubectl delete -f deploy.yaml
