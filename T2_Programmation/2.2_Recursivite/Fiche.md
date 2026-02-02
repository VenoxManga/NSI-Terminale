# Chapitre 6 – Récursivité (TNSI)

## 1. Première approche

### 1.1. Une fonction qui s’appelle elle-même
- Une fonction récursive est une fonction qui **s’appelle elle-même**.
- Elle permet de résoudre un problème en le **ramenant à une version plus simple** du même problème.

### 1.2. Définition
Une fonction récursive doit impérativement contenir :
- **un cas de base** (condition d’arrêt)
- **un ou plusieurs appels récursifs** vers un problème plus simple

Sans cas de base → **boucle infinie**.

---

## 2. Écriture d’une fonction récursive

### 2.1. Structure générale
- Tester le **cas de base**
- Sinon, appeler la fonction sur une version réduite du problème

Schéma :
- si condition simple → résultat
- sinon → appel récursif

### 2.2. Exemple : factorielle
- `factorielle(0) = 1` → cas de base
- `factorielle(n) = n × factorielle(n-1)` → appel récursif

### 2.3. Exemple : suite de Fibonacci
- `fib(0) = 0`, `fib(1) = 1`
- `fib(n) = fib(n-1) + fib(n-2)`
- Exemple simple mais **peu efficace** (beaucoup d’appels inutiles)

---

## 3. Exécution d’un programme récursif

### 3.1. Notion de pile (stack)
- Chaque appel de fonction est placé dans la **pile d’appels**
- Les appels sont empilés puis **dépilés** à la fin
- L’ordre d’exécution est **LIFO** (Last In, First Out)

### 3.2. Limitation de la taille de la pile
- La pile a une **taille limitée**
- Trop d’appels récursifs → **stack overflow**
- Python limite la profondeur de récursion

---

## 4. Erreurs classiques en récursivité

### 4.1. Oubli du cas de base
- Provoque une récursion infinie
- Erreur fréquente

### 4.2. Cas de base mal défini
- Résultat incorrect
- Fonction qui ne s’arrête pas au bon moment

### 4.3. Problème non réduit
- L’appel récursif doit toujours **se rapprocher du cas de base**

---

## 5. Récursif ou itératif ?

### 5.1. Avantages de la récursivité
- Code souvent **plus lisible**
- Adapté aux problèmes naturellement récursifs
  (arbres, diviser pour régner)

### 5.2. Inconvénients
- Plus coûteux en mémoire
- Risque de débordement de pile
- Souvent moins performant qu’une version itérative

---

## 6. À retenir absolument
- Une fonction récursive = **cas de base + appel récursif**
- Chaque appel utilise la **pile d’exécution**
- Attention à la **profondeur de récursion**
- Toujours vérifier que le problème **diminue à chaque appel**
