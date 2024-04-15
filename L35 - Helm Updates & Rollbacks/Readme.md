# L35 - Helm Updates & Rollbacks

Nous allons créer un chart simple en utilisant les valeurs par défaut fournies par Helm.

## Créer un chart

    helm create mynginx

## Installer le chart

    helm install mychart mynginx

## Lancez K9s pour voir ce qui se passe

    k9s

## Lister les déploiements

    helm ls 

## Editer le chart

    Modifiez le fichier values.yaml et changez le replicaCount de 1 à 3

## Changer la version du chart

    Modifiez le fichier Chart.yaml et changez la version de 0.1.0 à 0.2.0

## Installer le chart

    helm upgrade mychart ./mynginx

## Lister les déploiements et voir l'historique

    helm ls 
    helm history mychart

## Retour en arriere

    helm rollback mychart 1

## Voir l'historique

    helm history mychart

## Désinstaller le déploiement

    helm uninstall mychart
