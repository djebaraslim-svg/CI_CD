# Demo01-Intro Github Action

# Mise place du projet
- Initialiser le repo git 
- Créer le projet et le mettre sur git
- Créer une action (fichier ou il y a les actions): 
    -pour ça on va créer un dossier github > worflows > first-action.yaml

## Syntaxe de base
Fichier yaml -> Fichier structuré par tabulation

yaml
    --> Nom du worflow (pipeline)
    name : exemple_syntaxe

    --> Triggers
    on : 
        worflow_dispatch:
        push : [main]

    --> Travaux à réaliser
    jobs:
        job_name :
        ...
        (toute la config)
yaml

### Triggers
Ensemble des events écoutés
- Manuellement -> Bouton pou lancer le traitement
- Push d'une branche
- Etc...

### Travaux à réaliser
L'ensemble des actions à faire.
-Runner -> machines virtuelles prêtées par github
- Actions à faire : script(syntaxe qui dépend du terminal), utilisation d'action