# L14 - Declaratif vs Imperatif

![Hands-On Files](../images/checked-files-50px.png)

Déployons un conteneur Nginx en utilisant les deux méthodes.

## Impératif

    kubectl create deployment mynginx1 --image=nginx

## Déclaratif

    kubectl create -f deploy-example.yaml

## Nettoyer

    kubectl delete deployment mynginx1
    kubectl delete deploy mynginx2
