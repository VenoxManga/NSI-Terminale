# 🗒️ Fiche : Chapitre 4.3 - Le langage SQL (Requêtes)

## 1. Introduction
* **SQL** (*Structured Query Language*) : Langage standard pour interagir avec les bases de données.
* **Focus** : Ce chapitre traite de la manipulation des données (lecture, ajout, modification, suppression).

---

## 2. Extraction de données (SELECT)

### 2.1. Projection
* **But** : Choisir les colonnes (attributs) à afficher.
* **Syntaxe** : `SELECT nom_colonne1, nom_colonne2 FROM nom_table;`
* **Tout afficher** : `SELECT * FROM nom_table;`

### 2.2. Sélection (ou Restriction)
* **But** : Filtrer les lignes (n-uplets) selon une condition.
* **Syntaxe** : `SELECT ... FROM ... WHERE condition;`
* **Opérateurs** : `=`, `<>`, `<`, `>`, `AND`, `OR`, `NOT`, `IN`, `BETWEEN`.
* **Recherche de texte** : `WHERE attribut LIKE 'A%'` (tous ceux qui commencent par A).

### 2.3. Tri
* **Syntaxe** : `ORDER BY nom_colonne [ASC|DESC];`
* **Sens** : `ASC` (croissant, par défaut), `DESC` (décroissant).

### 2.4. Élimination des doublons
* **Syntaxe** : `SELECT DISTINCT nom_colonne FROM ...;`

---

## 3. Calculs et agrégats

### 3.1. Fonctions d'agrégation
* `COUNT(*)` : Compte le nombre de lignes.
* `SUM(colonne)` : Somme des valeurs.
* `AVG(colonne)` : Moyenne des valeurs.
* `MAX(colonne)` / `MIN(colonne)` : Valeur max ou min.

### 3.2. Groupement
* **But** : Regrouper des lignes pour appliquer une fonction d'agrégation par catégorie.
* **Syntaxe** : `SELECT categorie, COUNT(*) FROM table GROUP BY categorie;`

---

## 4. Requêtes portant sur plusieurs tables (Jointures)

### 4.1. Produit cartésien
* Associe chaque ligne de la première table à chaque ligne de la seconde. 
* Très lourd, rarement utilisé tel quel sans filtre.

### 4.2. Jointure
* **But** : Lier deux tables via une clé commune (souvent `CléPrimaire = CléÉtrangère`).
* **Syntaxe** :
