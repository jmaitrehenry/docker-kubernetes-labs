# L24 - Ingress

![Hands-On Files](../images/checked-files-50px.png)

## Déployer un contrôlleur Ingress NGINX

    kubectl apply -f https://raw.githubusercontent.com/kubernetes/ingress-nginx/controller-v1.10.0/deploy/static/provider/cloud/deploy.yaml

## Créer les applications

    kubectl apply -f helloworld-one.yaml
    kubectl apply -f helloworld-two.yaml

## Obtenir les informations sur les pods

    kubectl get pods

## Créer le contrôlleur Ingress

    kubectl apply -f ingress.yaml

## Obtenir l'adresse IP de l'équilibreur de charge

    kubectl get svc -n ingress-nginx

Lancer un navigateur

    http://localhost
    http://localhost/hello-world-one
    http://localhost/hello-world-two

## Nettoyer

    kubectl delete -f ingress.yaml
    kubectl delete -f helloworld-one.yaml
    kubectl delete -f helloworld-two.yaml
    kubectl delete -f https://raw.githubusercontent.com/kubernetes/ingress-nginx/controller-v1.10.0/deploy/static/provider/cloud/deploy.yaml

