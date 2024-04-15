# L34 - Helm

## S'il n'est pas déjà installé, installez Helm

Windows

    choco install kubernetes-helm

Mac

    brew install helm

Linux

Consultez la documentation

    https://helm.sh/docs/intro/install/

## Ajouter le référentiel

    helm repo add ingress-nginx https://kubernetes.github.io/ingress-nginx

Mettre à jour la cache local

    helm repo update

Valider que les référentiels ont été installés

    helm repo list

## Rechercher le référentiel pour Nginx

    helm search repo nginx

## Afficher le Chart Nginx

    helm show chart ingress-nginx/ingress-nginx

## Afficher les valeurs

    helm show values ingress-nginx/ingress-nginx

## Tirez le Chart Nginx

    helm pull --untar ingress-nginx/ingress-nginx

## Lister les versions disponibles

    helm search repo ingress-nginx -l

## Installer le Chart Nginx dans votre cluster

    helm install mynginx ingress-nginx/ingress-nginx --version 4.8.3

## Lancez K9s pour voir ce qui se passe

    k9s

## Lister le déploiement

    helm ls 

## Mise à niveau

    helm upgrade mynginx ingress-nginx/ingress-nginx

## Lister à nouveau le déploiement

    helm ls

## Obtenir l'historique du déploiement

    helm history mynginx

## Retour à la version précédente

    helm rollback mynginx

## Désinstaller le déploiement

    helm uninstall mynginx
