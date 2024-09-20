# lexique-md-cda-p4

### Les commandes de base de Git

- git init : initialise le versioning du repository
- git add monfichier : ajoute le fichier dans l’index
- git status : affiche le status de la branche active
- git commit : valide la sauvegarde de l’index
- git push : « pousse » la sauvegarde sur un serveur
- git pull : « tire » la dernière version du serveur
- git clone : clone un repo distant dans le dossier

Qu'est-ce qu'un `fork` ? : c'est une copie d’un repo depuis un compte GitHub vers un autre compte GitHub

### Pourquoi versionner son code ?

- Principe de sauvegarde
- Voyager dans le temps → on revient en arrière sur ce qu’on a fait
- Tester des features
- Qui a fait quoi ?
- Garder une version stable
- Avoir **des sauvegardes** de son code
- 2 modèles de versionning
    - Le modèle centralisé (SVN, CVS)
    - Le modèle distribué (Git)
- Git ne fait **qu’ajouter des données**
- Les 3 états :
    - **Modifié** (git status)
    - **Indexé** (git add)
    - **Validé** (git commit)
    


## Linux 
![Linux](https://blog.vtutor.com/wp-content/uploads/2019/12/Linux.jpg)
- **Découverte de Linux** :
  - **Savoir ce qu'est Linux**  
    Linux est un système d'exploitation open-source basé sur le noyau Linux. Il est utilisé dans divers environnements, allant des serveurs aux ordinateurs personnels, et est connu pour sa stabilité, sa sécurité et sa flexibilité.
  
  - **Savoir ce qu'est une distribution Linux**  
    Une distribution Linux (ou "distro") est une version de Linux qui inclut le noyau Linux ainsi qu'une sélection de logiciels et d'outils spécifiques pour former un système d'exploitation complet. Exemples populaires : Ubuntu, Fedora, Debian.

  - **Comprendre l'arborescence de Linux**  
    L'arborescence de Linux est l'organisation des fichiers et des répertoires du système. À la racine de cette arborescence se trouve `/` (racine) qui contient plusieurs dossiers tels que `/bin` (commandes de base), `/etc` (fichiers de configuration), `/home` (dossiers des utilisateurs), etc. Chaque répertoire a une fonction bien définie dans le système.

## Le Terminal

**Découverte du Terminal** : 
  - **Comprendre la différence entre une interface en ligne de commande et une interface graphique**  
    Une interface en ligne de commande (CLI) permet d'interagir avec l'ordinateur en saisissant des commandes sous forme de texte, tandis qu'une interface graphique (GUI) permet une interaction visuelle, généralement à l'aide de la souris et des icônes.
    Mais derrière le GUI se cache un CLI il y'a une couche entre les 2 qui est justement fais par les devs UX/UI.

  - **Savoir ce qu'est un Shell, quelle différence entre BASH et ZSH**  
    Un Shell est un interpréteur de commandes qui permet aux utilisateurs d'interagir avec le système d'exploitation. BASH (Bourne Again Shell) et ZSH (Z Shell) sont deux types de shells populaires. BASH est plus largement utilisé par défaut dans de nombreuses distributions Linux, tandis que ZSH offre des fonctionnalités supplémentaires telles que la correction automatique des commandes et une personnalisation plus poussée au niveau du Prompt (c'est toute la première ligne du shell).

  - **Comprendre comment fonctionne un shell**  
    Un shell fonctionne en lisant les commandes saisies par l'utilisateur, en les interprétant et en exécutant les programmes ou scripts associés. Il peut aussi utiliser des variables d'environnement pour configurer le comportement du système. En gros le shell c'est la couche situé entre l'utilisateur et le noyau (ex: Linux, WIndows, MacOs).

  - **Comprendre le fonctionnement des alias**  
    Un alias permet de définir un raccourci pour une commande plus longue ou plus complexe. Par exemple, `alias ll='ls -la'` crée un raccourci pour afficher les fichiers d'un répertoire avec des détails supplémentaires.

  - **Comprendre le fonctionnement et l'utilité des commandes de base (cd, ls, rm, rmdir, mv, cp, mkdir)**  
    - `cd` : Change de répertoire.
    - `ls` : Liste le contenu d'un répertoire.
    - `rm` : Supprime des fichiers.
    - `rmdir` : Supprime des répertoires vides.
    - `mv` : Déplace ou renomme des fichiers.
    - `cp` : Copie des fichiers.
    - `mkdir` : Crée un nouveau répertoire.

  - **Comprendre le principe des options dans les commandes**  
    Les options dans les commandes modifient leur comportement. Elles sont généralement précédées d'un tiret simple ou double. Par exemple, avec la commande `ls`, l'option `-l` affiche les fichiers en mode détaillé.

## Raccourci Clavier

**Comprendre l'intérêt des raccourcis clavier**  
Les raccourcis clavier permettent d'effectuer des actions plus rapidement sans avoir à utiliser la souris. Ils améliorent la productivité en réduisant le temps de navigation entre les menus et les fenêtres, facilitant ainsi l'interaction avec le système.

**Découverte des raccourcis clavier Linux** :
  - **Navigateur (fenêtres, onglets, navigation, etc.)**  
    Les raccourcis clavier dans les navigateurs permettent de gérer les fenêtres, les onglets et la navigation plus efficacement. Par exemple :
    - `Ctrl + T` : Ouvrir un nouvel onglet.
    - `Ctrl + W` : Fermer l'onglet actuel.
    - `Ctrl + Tab` : Passer à l'onglet suivant.
    - `Alt + Flèche gauche` : Revenir à la page précédente.

  - **Terminal (fenêtres, onglets, commandes)**  
    Les raccourcis dans le terminal permettent de gérer plusieurs fenêtres ou onglets et d'exécuter des commandes rapidement. Quelques exemples :
    - `Ctrl + Shift + T` : Ouvrir un nouvel onglet dans le terminal.
    - `Ctrl + Shift + W` : Fermer un onglet.
    - `Ctrl + C` : Arrêter une commande en cours d'exécution.
    - `Ctrl + L` : Effacer l'écran du terminal.

  - **Découverte et installation de Albert (Linux) / Alfred (Mac)**  
    Albert (pour Linux) et Alfred (pour Mac) sont des lanceurs d'applications qui permettent de rechercher et d'exécuter rapidement des programmes, des fichiers ou des commandes. Ils améliorent la productivité en offrant une interface rapide et simple d'accès via des raccourcis clavier. Pour installer Albert sur Linux, tu peux utiliser la commande suivante dans le terminal :  
    ```bash
    sudo apt install albert
    ```
    Pour Alfred sur Mac, tu peux le télécharger directement depuis le site officiel.


## GitFlow

GitFlow est une méthodologie de gestion de branches largement utilisée pour structurer les processus de développement dans des équipes travaillant avec Git. Elle permet d’organiser les branches de manière à rendre le flux de travail cohérent, tout en facilitant la collaboration et la livraison de fonctionnalités. Voici une explication détaillée des différentes branches et du processus GitFlow.

## Les Branches Principales de GitFlow

#### main (ou master) :

        Cette branche contient le code qui est déployé en production. Chaque modification apportée à main doit être validée et approuvée avec rigueur, car elle représente le produit final en cours d’exploitation.
        Les versions officielles sont créées à partir de cette branche. C'est pourquoi elle ne doit contenir que du code stable et bien testé.

#### develop :

        C’est la branche où l'intégration continue se fait. Toutes les nouvelles fonctionnalités et corrections de bugs sont fusionnées dans develop une fois prêtes, mais avant d’être envoyées en production.
        Elle contient le dernier code intégrant toutes les nouveautés, mais qui n'est pas encore considéré comme assez stable pour la production.

## Branches Temporaires et Spécifiques

 #### Branches de fonctionnalités (feature/) :

        Ces branches sont créées à partir de develop pour permettre le développement d'une nouvelle fonctionnalité spécifique. Chaque fonctionnalité aura sa propre branche (feature/nom_fonctionnalité), facilitant ainsi l'isolation du code.
        Une fois le développement terminé et la fonctionnalité validée, la branche est fusionnée dans develop.

 ####   Branches de release (release/) :
        Une fois qu'une série de fonctionnalités et de corrections de bugs est prête à être déployée en production, une branche release/ est créée à partir de develop.
        Cela permet de stabiliser le code, tester, corriger des bugs mineurs, et préparer les versions finales. Après validation, elle est fusionnée dans main et develop, et marquée avec un tag de version.

   #### Branches de hotfix (hotfix/) :
        Ces branches sont utilisées pour apporter des corrections d’urgence sur main, par exemple en cas de bug critique en production.
        Elles sont créées directement à partir de main, puis une fois la correction effectuée, la branche est fusionnée à la fois dans main et develop pour que la correction soit présente partout.

   #### Branches de correction de bugs (bugfix/) :
        Contrairement aux hotfix/, les branches bugfix/ sont créées à partir de develop pour corriger des bugs détectés pendant le développement. Elles ne sont pas urgentes comme les hotfix, mais permettent d'améliorer la stabilité du code avant une release.

## Les Commandes GitFlow

Voici quelques commandes GitFlow pour faciliter la gestion des branches et le respect du workflow :

#### Initialisation de GitFlow :
#### Lancer le processus GitFlow dans un projet déjà sous Git :

     
    git flow init

#### Fonctionnalités :

 ####    Démarrer une nouvelle fonctionnalité :


    git flow feature start nom_de_la_fonctionnalité

####  Terminer une fonctionnalité :



    git flow feature finish nom_de_la_fonctionnalité

####  Releases :

  ####   Démarrer une nouvelle release :

   
    git flow release start numéro_de_version

####  Terminer une release :


    git flow release finish numéro_de_version

####  Hotfixes :

   ####  Démarrer un hotfix (correction rapide) :



    git flow hotfix start nom_du_hotfix

####  Terminer un hotfix :


    git flow hotfix finish nom_du_hotfix

####  Bugfix :

####  Démarrer une correction de bug :



    git flow bugfix start nom_du_bugfix

####  Terminer une correction de bug :


    git flow bugfix finish nom_du_bugfix

---

#   Comprendre Github
---

> **Convention de commit :** [https://www.conventionalcommits.org/fr/v1.0.](https://www.conventionalcommits.org/fr/v1.0.0/)
> 

---

**LE MERGE COMMIT :**

Un **merge commit** se produit lorsque l’on fusionne une branche `feature` avec la branche `main`, mais que la branche `main` a continué d’avancer indépendamment de la `feature`.

**Exemple :**

Avant le merge :

```
main:     A---B---C---G---H
                \\
feature:         D---E---F

```

Lors du merge, Git va créer un **commit de merge** (`M`) pour combiner les deux branches. L'historique complet de la branche `feature` sera conservé dans l'historique de la branche `main`.

**Exemple :

Après le merge :**

```
main:     A---B---C---G---H---M
                \\           /
feature:         D---E---F

```

Le commit de merge `M` indique la convergence des deux branches tout en conservant leurs histoires respectives.

---

**LE COMMIT :**

Un **commit** est une sauvegarde d’un état spécifique de ton projet. Il enregistre des changements (modifications de fichiers, ajouts ou suppressions) et fait partie de l’historique de ta branche.

**Quand il est créé** :

- Un commit normal est créé chaque fois que tu exécutes la commande `git commit` après avoir ajouté des modifications avec `git add`.

**Objectif** :

- Sauvegarder un ensemble de changements à un moment donné.
- Chaque commit est lié à son parent ou à ses parents, ce qui permet à Git de garder un historique linéaire des modifications.

**Exemple :**

```
main:     A---B---C

```

Dans cet exemple, `A`, `B`, et `C` sont des **commits normaux**, chacun représentant un ensemble de modifications sur la branche `main`.

---

**LE FAST FORWARD :**
Un **fast-forward** se produit lorsque je travaille sur une branche `feature`, et que la branche `main` n’a pas évolué depuis la création de cette branche. Une fois la fonctionnalité terminée et que je fais un merge, Git va automatiquement effectuer un **fast-forward**.

Cela signifie que Git va simplement avancer la référence de la branche `main` pour inclure les commits de la branche `feature`, sans créer de commit de fusion. **L’historique restera linéaire**.

**Exemple :**

Avant le merge :

```
main:     A---B---C
                \\
feature:         D---E---F

```

Lors du merge, comme la branche `main` n'a pas avancé, Git fait un **fast-forward**, ce qui rend l'historique linéaire sans créer de commit supplémentaire.

**Exemple après le fast-forward :**

```
main:     A---B---C---D---E---F

```

Il n'y a pas de **commit de fusion** créé, et l’historique semble avoir évolué de manière continue et linéaire.

---
