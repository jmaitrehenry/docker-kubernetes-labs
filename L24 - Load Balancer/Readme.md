# L24 - Load Balancer

![Hands-On Files](../images/checked-files-50px.png)

## Déployer le service load balancer

    kubectl apply -f lb.yaml

## Déployer l'application

    kubectl apply -f deploy-app.yaml

## Obtenir la liste des pods

    kubectl get pods -o wide

## Opbetenir l'IP externe du load balancer

    kubectl get svc

## Obtenez la page d'accueil de Nginx via le service LoadBalancer

    http://localhost:8080

## Nettoyer

    kubectl delete -f lb.yaml
    kubectl delete -f deploy-app.yaml
