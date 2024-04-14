# L26 - Secrets

![Hands-On Files](../images/checked-files-50px.png)

Pour encoder/décoder rapidement des chaînes en base64

    https://www.base64encode.org/
    https://www.base64decode.org/

ou sous Windows, installez base64

    choco install base64

sous Linux/Mac

    echo [string] | base64
    echo [encodedString] | base64 -D

## Créer les secrets

    kubectl apply -f secrets.yaml
    kubectl apply -f secrets-string-data.yaml

## Regardez les secrets

    kubectl get secret
    kubectl describe secret secrets
    kubectl get secret secrets -o YAML

## Déployez le pod

    kubectl apply -f pod.yaml

## Connectez-vous au Busybox

    kubectl exec mybox -it -- /bin/sh

## Afficher les variables d'environnement USERNAME et PASSWORD

    echo $USERNAME
    echo $PASSWORD
    exit

## Déployer le deuxième pod

    kubectl apply -f pod-secret-as-file.yaml

## Connectez-vous au Busybox

    kubectl exec mybox2 -it -- /bin/sh

## Afficher les secrets

    cat /etc/myapp/.env

## Explorer la structure du dossier

    ls -al /etc/myapp/
    exit

## Mettez à jour le secret

Modifiez le fichier `secrets-string-data.yml` en modifiant le mot de passe et appliquez le changement:

    kubectl apply -f secrets-string-data.yaml

## Vérifiez l'état du volume

    cat /etc/myapp/.env
    ls -al /etc/myapp/
    exit

## Nettoyer

    kubectl delete -f secrets.yaml
    kubectl delete -f secrets-string-data.yaml 
    kubectl delete -f pod.yaml --force --grace-period=0
    kubectl delete -f pod-secret-as-file.yaml --force --grace-period=0
