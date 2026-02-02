### 🔍 Arbres Binaires de Recherche (ABR) - Fiche de révision
=========================================================

Définition
----------

**Arbre Binaire de Recherche (ABR)** : arbre binaire dont les étiquettes vérifient :

-   Étiquette d'un nœud ≥ toutes les étiquettes de son **sous-arbre gauche**
-   Étiquette d'un nœud < toutes les étiquettes de son **sous-arbre droit**

**Remarque** : un ABR parcouru en **infixe** donne une suite **croissante**

**Arbre filiforme** : ABR où chaque nœud n'a qu'un seul fils (cas dégénéré)

## 1\. Déterminer si un arbre est un ABR
-------------------------------------

**Méthode** : effectuer un parcours infixe et vérifier que la liste obtenue est triée

python

```
def est_ABR(arbre, p = None):
    if p is None:
        p = []
    if arbre is None:
        return True

    gaucheABR = est_ABR(arbre.gauche, p)
    if not gaucheABR:
        return False
    p.append(arbre.etiquette)
    droiteABR = est_ABR(arbre.droite, p)
    if not droiteABR:
        return False
    return p == sorted(p)
```

## 2\. Rechercher une clé dans un ABR
----------------------------------

**Principe** : exploiter la structure ordonnée pour éliminer la moitié de l'arbre à chaque comparaison

python

```
def contient_valeur(arbre, valeur):
    if arbre is None:
        return False
    if arbre.etiquette == valeur:
        return True
    if valeur < arbre.etiquette:
        return contient_valeur(arbre.gauche, valeur)
    else:
        return contient_valeur(arbre.droite, valeur)
```

## 3\. Coût de la recherche dans un ABR équilibré
----------------------------------------------

-   **Complexité** : **O(log₂(n))** - logarithmique
-   Après chaque nœud, le nombre de nœuds restants est divisé par 2 (dichotomie)
-   Pour un arbre de **1000 valeurs** → seulement **10 étapes** maximum !
-   ⚡ **Très performant** comparé à une recherche linéaire O(n)

**Formule** : pour un arbre complet de hauteur h → taille n = 2^h - 1

## 4\. Insertion dans un ABR
-------------------------

**Algorithme** : insertion récursive au niveau d'une feuille

-   Si valeur ≤ nœud actuel → aller à gauche
-   Si valeur > nœud actuel → aller à droite
-   Créer une nouvelle feuille quand sous-arbre vide

python

```
def insertion(arbre, valeur):
    if valeur <= arbre.etiquette:
        if arbre.gauche is None:
            arbre.gauche = Arbre(valeur)
        else:
            insertion(arbre.gauche, valeur)
    else:
        if arbre.droite is None:
            arbre.droite = Arbre(valeur)
        else:
            insertion(arbre.droite, valeur)
```

* * * * *

💡 Points clés à retenir
------------------------

✅ ABR = structure **ordonnée** pour recherche **efficace**\
✅ Parcours infixe d'un ABR = **liste triée**\
✅ Recherche en **O(log n)** si arbre équilibré\
✅ Insertion toujours au niveau d'une **feuille**
