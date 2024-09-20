# lexique-md-cda-p4

## Linux 
![Linux](https://blog.vtutor.com/wp-content/uploads/2019/12/Linux.jpg)

- **Découverte de Linux** :
  - **Savoir ce qu'est Linux**  
    Linux est un système d'exploitation open-source basé sur le noyau Linux. Il est utilisé dans divers environnements, allant des serveurs aux ordinateurs personnels, et est connu pour sa stabilité, sa sécurité et sa flexibilité.
  
  - **Savoir ce qu'est une distribution Linux**  
    Une distribution Linux (ou "distro") est une version de Linux qui inclut le noyau Linux ainsi qu'une sélection de logiciels et d'outils spécifiques pour former un système d'exploitation complet. Exemples populaires : Ubuntu, Fedora, Debian.

  - **Comprendre l'arborescence de Linux**  
    L'arborescence de Linux est l'organisation des fichiers et des répertoires du système. À la racine de cette arborescence se trouve `/` (racine) qui contient plusieurs dossiers tels que `/bin` (commandes de base), `/etc` (fichiers de configuration), `/home` (dossiers des utilisateurs), etc. Chaque répertoire a une fonction bien définie dans le système.

## LeTerminale

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
