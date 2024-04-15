# L32 - K9s

![Hands-On Files](../images/checked-files-50px.png)

K9s est un excellent tableau de bord fonctionnant dans un terminal.

    https://k9scli.io/

## Installer K9s

Installez-le sur :

Windows (si vous avez installé Chocolatey):

    choco install k9s

macOS (si vous avez installé Brew):

    brew install k9s

Linux: voir https://k9scli.io/topics/install/

## Créez un déploiement et regardez ce qui se passe dans le tableau de bord

    kubectl create -f hello-deployment.yaml

## Dans un nouveau terminal, lancer K9s

    k9s

Regardez ce qui se passe dans K9s

## Supprimer un module

Sélectionnez l'un des pods et supprimez-le en tapant **Ctrl-k**. Vous remarquerez que le pod sera remplacé presque immédiatement.

## Nettoyer

    kubectl delete -f hello-deployment.yaml
