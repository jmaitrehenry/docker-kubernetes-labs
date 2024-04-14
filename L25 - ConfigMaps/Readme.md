# L25 - ConfigMaps

![Hands-On Files](../images/checked-files-50px.png)

## Créer le ConfigMap

    kubectl apply -f cm.yaml

## Obtenir les informations du ConfigMap

    kubectl get cm
    kubectl describe configmap cm-example

Sortons les mêmes informations en format YAML

    kubectl get configmap cm-example -o YAML

## Déployez le pod

    kubectl apply -f pod.yaml

## Connectez-vous au Busybox

    kubectl exec mybox -it -- /bin/sh

## Affichez la variable d'environnement CITY

    echo $CITY
    exit

## Nettoyer

    kubectl delete -f cm.yaml
    kubectl delete -f pod.yaml --grace-period=0 --force
