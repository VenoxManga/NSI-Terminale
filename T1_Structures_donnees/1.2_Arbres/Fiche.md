### Arbres - Fiche de révision
==========================

## 1\. Terminologie
----------------

## 1.1 Vocabulaire de base

-   **Arbre** : structure hiérarchique de données, graphe non orienté, connexe, sans cycle
-   **Nœud racine** : seul nœud sans père (en haut de l'arbre)
-   **Nœud père/fils** : chaque nœud a exactement un père (sauf la racine) et peut avoir plusieurs fils
-   **Feuilles** : nœuds sans fils (nœuds externes)
-   **Nœuds internes** : nœuds qui ne sont pas des feuilles
-   **Étiquette** : nom du nœud

## 1.2 Exemples d'arbres

*Arbres généalogiques, DOM HTML, arborescence de fichiers Unix...*

## 1.3 Caractéristiques numériques

-   **Taille** : nombre total de nœuds
-   **Arité** : nombre de fils d'un nœud
-   **Profondeur d'un nœud** : nombre de nœuds sur le chemin vers la racine
-   **Hauteur de l'arbre** : profondeur du nœud le plus profond
    -   Arbre vide : hauteur = 0
    -   Arbre à 1 nœud : hauteur = 1

## 1.4 Arbres binaires

**Arbre binaire** : chaque nœud a **au plus 2 fils** (gauche et droit)

-   Chaque nœud possède un **sous-arbre gauche** et un **sous-arbre droit** (possiblement vides)
-   **Arbre binaire complet** : aucun fils manquant
    -   Taille = `2^h - 1` (où h = hauteur)
    -   Pour un arbre binaire quelconque : `h ≤ taille ≤ 2^h - 1`

## 2\. Parcours d'arbres
---------------------

## 2.1 Parcours en largeur (BFS)

**Breadth First Search** : parcours étage par étage, de gauche à droite

## 2.2 Parcours préfixe (DFS)

**Pré-ordre** : le père avant ses fils

-   Racine → Fils gauche → Fils droit
-   ⚡ Commence toujours par la racine

## 2.3 Parcours infixe (DFS)

**En ordre** : le père entre ses fils

-   Fils gauche → Racine → Fils droit
-   ⚡ La racine est "au milieu"

## 2.4 Parcours postfixe (DFS)

**Post-ordre** : le père après ses fils

-   Fils gauche → Fils droit → Racine
-   ⚡ Finit toujours par la racine

## 2.5 Mémo-technique

-   **Pré** = avant → père d'abord
-   **In** = au milieu → père entre les fils
-   **Post** = après → père en dernier

*Toujours traiter le fils gauche avant le fils droit !*
