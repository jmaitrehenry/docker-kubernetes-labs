# L28 - LivenessProbe

![Hands-On Files](../images/checked-files-50px.png)

## Déployer le pod

    kubectl apply -f pod.yaml

## Regardez les événements du pod

    kubectl describe pod liveness-example

## Attendez 15 secondes et recommencez

    kubectl describe pod liveness-example

## Nettoyer

    kubectl delete -f pod.yaml --force --grace-period=0
