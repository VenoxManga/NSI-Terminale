# 🗒️ Fiche : Chapitre 2 - Programmation Orientée Objet (POO)

## 1. Introduction
* **Paradigme** : Passage de la programmation procédurale (fonctions) à la **POO** (objets).
* **Objet** : Entité regroupant une structure interne (données) et un comportement (méthodes).

---

## 2. Vocabulaire de la P.O.O.

### 2.1 Les classes
* **Définition** : Le "moule" ou plan de construction qui définit la structure des futurs objets.

### 2.2 Les objets (ou instances)
* **Définition** : Un exemplaire concret créé à partir d'une classe.
* **Exemple** : La classe `Voiture` est le plan, `ma_voiture_bleue` est l'objet.

### 2.3 Les attributs
* **Définition** : Variables attachées à l'objet qui définissent son état (ex: couleur, vitesse).

### 2.4 Les méthodes
* **Définition** : Fonctions internes à la classe qui définissent ce que l'objet peut faire (ex: `accelerer()`).

---

## 3. Écrire une classe et créer des objets

### 3.1 Définir une classe
* Utilise le mot-clé `class` suivi du nom avec une majuscule.

### 3.2 Le constructeur `__init__`
* Méthode spéciale appelée à la création de l'objet pour initialiser ses attributs.

### 3.3 Le paramètre `self`
* Représente l'objet lui-même. Obligatoire comme premier argument des méthodes pour accéder aux attributs.

### 3.4 Instancier un objet
* Créer un objet en appelant la classe : `mon_objet = MaClasse(arguments)`.

---

## 4. Encapsulation (Interface et Implémentation)

### 4.1 Interface
* Ce que l'utilisateur voit et utilise (les méthodes publiques).

### 4.2 Implémentation
* Le code interne "caché". L'utilisateur n'a pas besoin de savoir *comment* c'est codé, seulement *comment* s'en servir.

---

## 🐍 Exemple de synthèse (Code)

```python
class Disque:
    def __init__(self, diametre):
        self.diametre = diametre  # Attribut
        
    def get_rayon(self):         # Méthode
        return self.diametre / 2

# Création d'une instance
disque1 = Disque(10)
print(disque1.get_rayon()) # Affiche 5.0
