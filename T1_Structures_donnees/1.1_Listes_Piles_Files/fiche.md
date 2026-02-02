# 📖 Chapitre 1 : Listes, Piles, Files (Interfaces)

## 1. Interfaces de structures de données
* **Définition** : L'**interface** définit ce que l'on peut faire sur un ensemble de données et avec quelle efficacité.
* **Implémentation** : C'est le code concret qui correspond à l'interface.
* **Exemple** : En Python, l'objet `list` est une implémentation d'un tableau.

---

## 2. Listes chaînées

### 2.1 Principe
* Une liste chaînée est une succession de **maillons**.
* Chaque maillon contient :
    1. Une **valeur** (la donnée).
    2. Un **pointeur** vers le maillon suivant.
* Elle se termine par une valeur spéciale (souvent `None`).



### 2.2 Interface
* `liste_vide()` : crée une liste vide.
* `est_vide(L)` : renvoie vrai si la liste est vide.
* `ajoute_tete(L, x)` : ajoute l'élément `x` au début.
* `renvoie_tete(L)` : renvoie la valeur du premier élément.
* `renvoie_queue(L)` : renvoie la liste sans son premier élément.

---

## 3. Piles (Stack)
* **Principe LIFO** (*Last In, First Out*) : Le dernier élément ajouté est le premier à sortir.
* **Analogie** : Une pile d'assiettes.



**Interface :**
* `pile_vide()` : crée une pile vide.
* `est_vide(P)` : renvoie vrai si la pile est vide.
* `empiler(P, x)` : ajoute `x` au sommet.
* `depiler(P)` : retire et renvoie l'élément au sommet.

---

## 4. Files (Queue)
* **Principe FIFO** (*First In, First Out*) : Le premier élément ajouté est le premier à sortir.
* **Analogie** : Une file d'attente à la caisse.



**Interface :**
* `file_vide()` : crée une file vide.
* `est_vide(F)` : renvoie vrai si la file est vide.
* `enfiler(F, x)` : ajoute `x` à la fin.
* `defiler(F)` : retire et renvoie l'élément au début.

---

## 🐍 Exemple de code (Python)
Exemple d'utilisation de l'interface des files :

```python
import file

ma_file = file.file_vide()
file.enfiler(ma_file, 3)
file.enfiler(ma_file, 2)
file.enfiler(ma_file, "bonjour")

file.afficher(ma_file)
file.defiler(ma_file) # Retire le 3
file.afficher(ma_file)
