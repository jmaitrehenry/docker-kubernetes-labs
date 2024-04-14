# L22 - Deploiements Blue-Green

![Hands-On Files](../images/checked-files-50px.png)

## Créer un déploiement V1

    kubectl apply -f hello-dep-v1.yaml

## Créer le service ClusterIP

    kubectl apply -f clusterip.yaml

## Obtenir la liste des pods

    kubectl get pods -o wide

## Afficher l'application dans un navigateur

Tout d'abord, faire un port forward vers le ClusterIP :

    kubectl port-forward service/svc-front 3000:3000

Ouvrez un navigateur et accédez à http://localhost:3000

La version de l'application sera V1.

---

## Créer un déploiement V2

    kubectl apply -f hello-dep-v2.yaml

## Obtenir la liste des pods

    kubectl get pods -o wide

## Modifier le manifeste du ClusterIP

Modifiez le fichier clusterip.yaml et modifiez la dernière ligne afin que le service pointe vers notre déploiement V2.

    app: hello-v2

## Mettre à jour le service ClusterIP

    kubectl apply -f clusterip.yaml

## Afficher l'application dans un navigateur

Tout d'abord, aire un port forward vers le ClusterIP :

    kubectl port-forward service/svc-front 3000:3000

Ouvrez un navigateur et accédez à http://localhost:3000

La version de l'application sera V2.

## Nettoyer

    kubectl delete -f hello-dep-v1.yaml
    kubectl delete -f hello-dep-v2.yaml
    kubectl delete -f clusterip.yaml
