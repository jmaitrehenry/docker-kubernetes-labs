# L21 - Rolling Updates

![Hands-On Files](../images/checked-files-50px.png)

## Créer un déploiement V1

    kubectl apply -f hello-deployment.yaml

## Obtenir l'état du déploiement

    kubectl rollout status deployment/hello-dep

## Obtenir la liste des pods

    kubectl get pods -o wide

## Décrire le pod

    kubectl describe pod hello-dep-[replicaset-id]-[instance-id]

## Combien de ReplicaSets avons-nous ?

    kubectl get rs

Ne supprimez pas le déploiement !

---

## Créer un déploiement V2

Modifiez le fichier YAML et changez la version du conteneur de v1 à v2. Enregistrez le fichier.
 
## Créer le déploiement

    kubectl apply -f hello-deployment.yaml

## Obtenir l'état du déploiement

    kubectl rollout status deployment/hello-dep

## Obtenir la liste des pods

    kubectl get pods -o wide

## Combien de ReplicaSets avons-nous ?

    kubectl get rs

## Obtenir l'historique du déploiement

    kubectl rollout history deployment/hello-dep

---
 
## Rollback

## Annuler le dernier déploiement en utilisant soit

    kubectl rollout undo deployment/hello-dep

ou

    kubectl rollout undo deployment/hello-dep --to-revision 1

## Obtenir l'historique du déploiement

    kubectl rollout history deployment/hello-dep

## Combien de ReplicaSets avons-nous ?

    kubectl get rs

## Nettoyer

    kubectl delete -f hello-deployment.yaml
