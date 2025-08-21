HC2T4 - Tâche 4 : Notation préfixe et infixe

---

## 🔄 Notation infixe vs préfixe : définitions

- **Notation infixe** : l’opérateur est **placé entre** ses deux arguments.  
  Exemple :  
  ```haskell
  5 + 3
  True && False
  ```

- **Notation préfixe** : la fonction est **placée avant** ses arguments, comme en mathématiques fonctionnelles.  
  Exemple :  
  ```haskell
  (+) 5 3
  (&&) True False
  ```

En Haskell, **les opérateurs sont des fonctions**. Tu peux donc les utiliser comme n’importe quelle fonction, en les entourant de **parenthèses** pour passer en mode préfixe.

---

## 🧪 Partie 1 : Convertir en notation préfixe

Expressions données :

- `5 + 3` devient :  
  ```haskell
  (+) 5 3
  ```

- `10 * 4` devient :  
  ```haskell
  (*) 10 4
  ```

- `True && False` devient :  
  ```haskell
  (&&) True False
  ```

👉 on remarque que chaque opérateur est placé **devant** ses deux arguments, entouré de parenthèses.

---

## 🔁 Partie 2 : Convertir en notation infixe

Fonctions données :

- `(+) 7 2` devient :  
  ```haskell
  7 + 2
  ```

- `(*) 6 5` devient :  
  ```haskell
  6 * 5
  ```

- `(&&) True False` devient :  
  ```haskell
  True && False
  ```

👉 Ici, on **retire les parenthèses** et on place l’opérateur **entre** les deux valeurs.

---

## 🧠 Pourquoi c’est utile ?

Cette flexibilité permet :

- D’utiliser les opérateurs comme **fonctions normales** (préfixe)
- D’écrire du code plus **lisible et naturel** (infixe)
- De manipuler des fonctions dans des expressions plus complexes, comme :
  ```haskell
  map (+3) [1,2,3]  -- ajoute 3 à chaque élément
  ```

---

## ✅ Résumé

| Expression originale | Notation préfixe       | Notation infixe       |
|----------------------|------------------------|------------------------|
| `5 + 3`              | `(+ ) 5 3`             | `5 + 3`                |
| `10 * 4`             | `(* ) 10 4`            | `10 * 4`               |
| `True && False`      | `(&&) True False`      | `True && False`        |
| `(+) 7 2`            | `(+ ) 7 2`             | `7 + 2`                |
| `(*) 6 5`            | `(* ) 6 5`             | `6 * 5`                |
| `(&&) True False`    | `(&&) True False`      | `True && False`        |

---
