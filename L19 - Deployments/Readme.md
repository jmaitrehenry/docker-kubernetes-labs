# L19 - Deployments

![Hands-On Files](../images/checked-files-50px.png)

Utilisons maintenant le modèle de déploiement au lieu du pod.

## Créer le déploiement

    kubectl apply -f deploy-example.yaml

## Obtenir la liste des pods

    kubectl get pods -o wide
    
## Décrire le pod

    kubectl describe pod deploy-example

## Obtenir les informations du déploiement

    kubectl get deploy
    kubectl describe deploy deploy-example

## Lister le ReplicaSet

    kubectl get rs

## Décrire le ReplicaSet

    kubectl describe rs

## Nettoyer

    kubectl delete -f deploy-example.yaml
