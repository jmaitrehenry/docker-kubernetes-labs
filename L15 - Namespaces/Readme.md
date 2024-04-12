# L15 - Namespaces

## Obtenir les namespaces

Ouvrez un terminal et récupérez les espaces de noms actuellement configurés.

    kubectl get namespaces
    kubectl get ns

## Obtenir la liste des pods

Obtenez une liste de tous les pods en cours d'exécution.

    kubectl get pods

Vous obtenez les pods à partir du namespace par défaut. Essayez d'obtenir les pods à partir du namespace Docker. Vous obtiendrez une liste différente.

    kubectl get pods --namespace=kube-system
    kubectl get pods -n kube-system

## Changer de namespace

Retournez au namespace Docker et obtenez la liste des pods.

    kubectl config set-context --current --namespace=kube-system

## Lister les pods

    kubectl get pods

## Maintenant, revenez au namespace par défaut

    kubectl config set-context --current --namespace=default
    kubectl get pods

## Créer et supprimer un namespace

    kubectl create ns [name]
    kubectl get ns
    kubectl delete ns [name]

> **Attention:** Supprimer un namespace supprime aussi toutes les ressources associés! 
