# 🗒️ Fiche : Chapitre 4.2 - Système de Gestion de Bases de Données (SGBD)

## Introduction
* **SGBD** : Interface entre l'utilisateur et les données. Permet de trouver, modifier, trier et transformer les données via des **requêtes**.
* **Langage SQL** (*Structured Query Language*) : Le langage standard utilisé pour interroger et manipuler les bases de données relationnelles.
* **Correspondance de vocabulaire** :
    * Modèle Relationnel $\rightarrow$ SGBD
    * Relation $\rightarrow$ **Table**
    * Attribut $\rightarrow$ **Colonne**
    * Enregistrement $\rightarrow$ **Ligne**

---

## 1. Rôle et fonctions d'un SGBD
* **Persistance** : Garantir que les données ne sont pas perdues (pannes, coupures).
* **Gestion des accès concurrents** : Gère les droits et privilèges des utilisateurs.
* **Efficacité** : Utilisation d'algorithmes puissants pour traiter les données rapidement.

---

## 2. Langage SQL pour la définition des données
* Permet d'implémenter les schémas relationnels en créant des tables réelles.
* On définit : le nom, les attributs, leurs types (domaines) et les contraintes.

---

## 3. Création de tables
* **Commande** : `CREATE TABLE nom_table (...);`.
* **Syntaxe** : Chaque attribut est suivi de son domaine et de ses contraintes.

### 3.1. Domaines : types de données en SQL
* **Entiers** : `INT` ou `INTEGER`.
* **Chaînes** : `VARCHAR(n)` (taille max $n$) ou `TEXT` (taille libre).
* **Temps** : `DATE` (AAAA-MM-JJ) ou `TIMESTAMP` (date + heure).
* **Divers** : `BOOLEAN`, `REAL` (flottant), `NULL` (vide).

### 3.2. Contraintes
* `PRIMARY KEY` : Identifiant unique de la ligne.
* `REFERENCES` : Clé étrangère pointant vers une autre table.
* `NOT NULL` : Valeur obligatoire.
* `UNIQUE` : Pas de doublons autorisés.
* `CHECK` : Condition personnalisée (ex: `CHECK (age >= 0)`).

### 3.3 Exemple
```sql
CREATE TABLE Film (
    idFilm INT PRIMARY KEY,
    nom VARCHAR(30) NOT NULL,
    idReal INT REFERENCES Realisateur(idReal)
);
