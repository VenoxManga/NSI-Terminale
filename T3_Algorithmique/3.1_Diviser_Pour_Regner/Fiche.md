# Chapitre 7 – Diviser pour régner (TNSI)

## 1. Principe général

### 1.1. Définition
La méthode *diviser pour régner* consiste à :
- **diviser** un problème en sous-problèmes plus simples
- **résoudre** les sous-problèmes
- **combiner** leurs résultats pour résoudre le problème initial

### 1.2. Idée clé
Un problème difficile devient simple lorsqu’il est **suffisamment découpé**.

---

## 2. Les trois étapes fondamentales

### 2.1. Diviser
- Découper le problème en plusieurs sous-problèmes de même nature
- Les sous-problèmes doivent être **plus petits** que le problème initial

### 2.2. Régner
- Résoudre directement les sous-problèmes
- Souvent réalisé par **récursivité**
- Présence d’un **cas de base**

### 2.3. Combiner
- Fusionner les solutions partielles
- Cette étape peut être simple ou coûteuse selon l’algorithme

---

## 3. Exemples classiques

### 3.1. Recherche dichotomique
- Liste **triée**
- Découpe la liste en deux à chaque étape
- Complexité : **O(log n)**

### 3.2. Tri fusion
- Diviser la liste en deux
- Trier récursivement chaque moitié
- Fusionner les deux listes triées
- Complexité : **O(n log n)**

---

## 4. Lien avec la récursivité

### 4.1. Utilisation de fonctions récursives
- Chaque appel traite un sous-problème
- Le cas de base correspond au problème le plus simple

### 4.2. Pile d’appels
- Les appels récursifs utilisent la **pile**
- Profondeur liée au nombre de divisions

---

## 5. Avantages et limites

### 5.1. Avantages
- Algorithmes souvent **rapides**
- Structure claire
- Adapté aux grands jeux de données

### 5.2. Inconvénients
- Implémentation parfois complexe
- Utilisation de mémoire supplémentaire
- Pas toujours plus efficace que l’itératif

---

## 6. À retenir absolument
- Diviser pour régner = **diviser + résoudre + combiner**
- Souvent basé sur la **récursivité**
- Très efficace pour la recherche et le tri
- Réduction rapide de la taille du problème
