# L29 - Volumes

![Hands-On Files](../images/checked-files-50px.png)

## Créer le volume persistant

    kubectl apply -f pv.yaml

## Lister les volumes persistants

    kubectl get pv

## Déployer le claim

    kubectl apply -f pvc.yaml

## Lister les pvc

    kubectl get pvc

## Déployer le pod

    kubectl apply -f pod.yaml

## Connectez-vous à l'instance Busybox

    kubectl exec mybox -it -- /bin/sh

## Créer un fichier

    cd demo
    echo Hello World > hello.txt
    ls
    exit

## Supprimer le pod

Supprimons le pod et déployons-le à nouveau pour valider la persistance du fichier.

    kubectl delete -f pod.yaml --force --grace-period=0

## Déployer à nouveau le pod

    kubectl apply -f pod.yaml

## Connectez-vous à l'instance Busybox

    kubectl exec mybox -it -- /bin/sh
    cd demo
    ls
    cat hello.txt
    exit

## Nettoyer

    kubectl delete -f pod.yaml  --force --grace-period=0
    kubectl delete -f pvc.yaml
    kubectl delete -f pv.yaml
