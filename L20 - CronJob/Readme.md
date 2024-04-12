# L20 - CronJob

![Hands-On Files](../images/checked-files-50px.png)

Utilisons maintenant un CronJob.

## Créer le CronJob

    kubectl apply -f cronjob.yaml

## Lister les Jobs

    kubectl get cronjobs

## Obtenir plus d'informations

    kubectl describe cronjob

## Obtenir le nom du pod

Obtenez le nom du pod. Quelque chose commençant par **hello-**

    kubectl get pods

## Obtenir la liste des Jobs

Obtenez le journal du conteneur. Vous devriez voir **Hello from the CronJob**.

    kubectl logs <podName>

## nettoyer

    kubectl delete -f cronjob.yaml
