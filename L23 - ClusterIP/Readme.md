# L23 - ClusterIP

![Hands-On Files](../images/checked-files-50px.png)

## Déployer le service

    kubectl apply -f clusterip.yaml

## Déployer l'application

    kubectl apply -f deploy-app.yaml

## Déployer Busybox

    kubectl apply -f pod.yaml

## Obtenir la liste des pods

    kubectl get pods -o wide

## Connectez-vous au conteneur BusyBox

    kubectl exec mybox -it -- /bin/sh

## Obtenez la page d'accueil de Nginx via le service ClusterIP

    wget -qO- http://svc-example:8080
    exit

## Nettoyer

    kubectl delete -f clusterip.yaml
    kubectl delete -f deploy-app.yaml
    kubectl delete -f pod.yaml --grace-period=0 --force
