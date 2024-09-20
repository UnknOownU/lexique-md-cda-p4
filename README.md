
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
