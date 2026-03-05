# Demo01-Intro Github Action

## Part 1 : syntaxe 
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

## Part 2 : variables
### Mise en place
- Nouveau fichier worflow
- Push sur github
- Définir des variables et secrets : 
    -définir une zone env dans le worflow (attention c'est public! pas de password epar exemple)
    -définir dans les paramètres du repo github
    -manipuler les variables d'event du worflow (lié au déclenchement du trigger)

### Syntaxe d'utilisation
### Variable d'env local : 
Utilisation
-"$VAR_NAME" (écriture sous linux) ET "$env:VAR_NAME" (écriture sous windows)

### Variables et secrets dans github
Aller à setting>secrets ans variables>action pour configurer les variables.

Deux types d'éléments configurables : 
- Repository : variables toujours accessible dans le repo
- Environnement : Accessible si le job utilise environnement : env-name 

Utilisation
- variables : ${{vars.VAR_NAME}}
- secrets : ${{secrets.VAR_NAME}}