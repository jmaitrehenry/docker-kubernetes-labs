# L13 - Kubectl

## Contexte actuel

Obtenez le contexte actuel :

    kubectl config current-context

## Lister tous les contextes

    kubectl config get-contexts

## Changer de contexte

    kubectl config use-context [contextName]

## Utilisation de kubectx

Ce qui est génial avec Kubernetes, c'est la quantité incroyable d'outils créés par la communauté et disponibles gratuitement. Kubectx est un outil simple qui permet de répertorier et de modifier facilement le contexte.

Vous pouvez l'installer avec :

Windows (si vous avez Chocolatey):

    choco install kubectx-ps

macOS (si vous avez Brew):

    brew install kubectx

Ubuntu:

    sudo apt install kubectx

Pour lister les contextes, tapez simplement :

    kubectx

Pour changer de contexte :

    kubectx <contextName>

## Renommer le contexte

    kubectl config rename-context [old-name] [new-name]

## Supprimer le contexte

    kubectl config delete-context [contextName]
