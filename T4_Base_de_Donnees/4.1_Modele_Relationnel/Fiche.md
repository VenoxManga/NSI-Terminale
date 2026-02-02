# 🗒️ Fiche : Chapitre 4.1 - Le Modèle Relationnel

## 1. Introduction
* **Objectif** : Organiser les données pour éviter les redondances (doublons), faciliter la recherche et garantir la cohérence des informations.
* **SGBD** : Système de Gestion de Bases de Données (ex: MySQL, PostgreSQL, SQLite). C'est le logiciel qui manipule les données.

---

## 2. Vocabulaire du modèle relationnel

### 2.1 Relation
* **Définition** : Une relation est ce qu'on appelle couramment une **table**. C'est un ensemble de données organisées en lignes et colonnes.

### 2.2 Attribut
* **Définition** : Correspond à une **colonne** de la table. Chaque attribut possède un nom et un domaine (type de donnée).

### 2.3 Domaine
* **Définition** : L'ensemble des valeurs possibles pour un attribut (ex: `Entier`, `Texte`, `Date`).

### 2.4 Enregistrement (ou n-uplet / tuple)
* **Définition** : Correspond à une **ligne** de la table. C'est une occurrence concrète des données.

[Image showing a database table with labels for attributes/columns and tuples/rows]

### 2.5 Schéma de relation
* **Définition** : C'est la signature de la table.
* **Notation** : `NOM_TABLE(Attribut1: Domaine, Attribut2: Domaine, ...)`

---

## 3. Clés et contraintes d'intégrité

### 3.1 Clé primaire
* **Définition** : Un attribut (ou groupe d'attributs) qui permet d'identifier de manière **unique** chaque ligne d'une table.
* **Règle** : Elle ne peut pas être vide (`NOT NULL`) et ne peut pas avoir de doublons.
* **Notation** : On souligne souvent la clé primaire dans le schéma.

### 3.2 Clé étrangère
* **Définition** : Un attribut dans une table qui fait référence à la clé primaire d'une **autre table**. Elle sert à lier les relations entre elles.

### 3.3 Contraintes d'intégrité
* **Intégrité de domaine** : La valeur doit respecter le type défini (ex: pas de texte dans un champ "Age").
* **Intégrité de relation** : La clé primaire doit être unique et non nulle.
* **Intégrité référentielle** : Une clé étrangère doit obligatoirement correspondre à une valeur existante dans la table d'origine.

---

## 4. Schéma relationnel d'une base de données
* **Définition** : C'est l'ensemble des schémas de toutes les tables de la base, incluant les liens (clés étrangères) entre elles.



---

## 🐍 Résumé visuel pour le Bac
| Concept Relationnel | Équivalent Simple |
| :--- | :--- |
| **Relation** | Table |
| **Attribut** | Colonne / Champ |
| **n-uplet** | Ligne / Enregistrement |
| **Clé Primaire** | Identifiant unique |
