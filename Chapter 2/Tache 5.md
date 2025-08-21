HC2T5 - Tâche 5 : Définir et utiliser des fonctions

---

## 🎯 Objectif pédagogique

Cette tâche permet de mettre en pratique plusieurs compétences fondamentales :

- Définir des fonctions avec des **signatures explicites**.
- Utiliser des **types de base** comme `Float` et `Int`.
- Manipuler des **expressions mathématiques** et des **fonctions de comparaison**.
- Tester tes fonctions dans **GHCi** pour observer leur comportement.

---

## 📚 Concepts clés tirés de la page environnante

- Une **signature de fonction** utilise le symbole `::` pour indiquer les types des paramètres et du résultat :
  ```haskell
  nomFonction :: Type1 -> Type2 -> TypeRésultat
  ```

- Les **types de base** utilisés ici sont :
  - `Float` pour les nombres réels à précision simple.
  - `Int` pour les entiers.
  - `Double` est aussi mentionné comme plus précis, mais ici on utilise `Float` comme demandé.

- Une fonction peut prendre **plusieurs arguments**, séparés par des flèches `->`.

- Exemple donné dans le cours :
  ```haskell
  prod :: Int -> Int -> Int
  prod x y = x * y
  ```

---

## 🧠 Implémentation des fonctions demandées

### 1. Fonction `circleArea`

- **Signature** :
  ```haskell
  circleArea :: Float -> Float
  ```
- **Définition** :
  ```haskell
  circleArea r = pi * r ^ 2
  ```
- 🔎 Elle utilise la constante `pi` et l’opérateur `^` pour élever le rayon au carré.

---

### 2. Fonction `maxOfThree`

- **Signature** :
  ```haskell
  maxOfThree :: Int -> Int -> Int -> Int
  ```
- **Définition** :
  ```haskell
  maxOfThree x y z = max x (max y z)
  ```
- 🔎 Elle utilise la fonction standard `max` pour comparer les trois valeurs.

---

## 🧪 Tests dans GHCi

Tu peux tester les fonctions comme ceci :

```haskell
circleArea 3.0
-- Résultat : 28.274334

maxOfThree 7 12 5
-- Résultat : 12

maxOfThree (-3) 0 (-10)
-- Résultat : 0
```

---

## ✅ Conclusion

Cette tâche te permet de :

- Comprendre la **structure d’une fonction** en Haskell.
- Travailler avec des **opérations mathématiques** et des **fonctions intégrées**.
- Appliquer les notions de **types et signatures** vues dans les tâches précédentes.
