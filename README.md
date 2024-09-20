
# lexique-md-cda-p4

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
