# L30 - Block Storage

![Hands-On Files](../images/checked-files-50px.png)

Montons un volume Block Storage.

## Valider que les StorageClass par défaut sont disponibles

    kubectl get sc

## Déployer le claim

    kubectl apply -f pvc.yaml

## Regarder le pvc

    kubectl get pvc


## Déployer le pod 1

    kubectl apply -f pod1.yaml

## Connectez-vous au Busybox 1

    kubectl exec mybox1 -it -- /bin/sh

## Créer un fichier

    ls
    cd demodisk
    echo Hello World > hello.txt
    ls
    exit

## Déployer le pod 2

    kubectl apply -f pod2.yaml

## Connectez-vous au Busybox 2

    kubectl exec mybox2 -it -- /bin/sh

    cd demodisk
    ls
    cat hello.txt
    exit

## Nettoyer

    kubectl delete -f pod1.yaml --grace-period=0 --force
    kubectl delete -f pod2.yaml --grace-period=0 --force
    kubectl delete -f pvc.yaml

Étant donné que nous avons utilisé la classe de stockage avec une stratégie de conservation définie sur Delete, le service Block Storage sera automatiquement supprimé.
