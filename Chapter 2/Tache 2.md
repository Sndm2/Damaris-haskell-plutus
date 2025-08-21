HC2T2 - Tâche 2 : Signatures de fonctions

---

## 🎯 Objectif pédagogique

Cette tâche vise à te familiariser avec deux compétences fondamentales en Haskell :
1. **Définir la signature d’une fonction** à l’aide du symbole `::`.
2. **Implémenter la fonction** en respectant les types spécifiés.

La signature est une sorte de contrat : elle indique clairement les types des paramètres et du résultat. Cela permet à Haskell de vérifier la cohérence du code et d’éviter les erreurs.

---

## 📚 Concepts tirés de la page environnante

La page explique que :
- Le symbole `::` signifie « est de type ».
- Une signature de fonction suit la forme :  
  ```haskell
  nomFonction :: Type1 -> Type2 -> ... -> TypeRésultat
  ```
- Les types courants incluent :
  - `Int` pour les entiers
  - `Bool` pour les valeurs logiques
  - `String` pour les chaînes de caractères
- Les fonctions peuvent prendre plusieurs arguments, séparés par des flèches `->`.

Exemple donné :
```haskell
prod :: Int -> Int -> Int
prod x y = x * y
```

---

## 🧠 Analyse des fonctions demandées

### 1. Fonction `add`

- **Signature attendue** :
  ```haskell
  add :: Int -> Int -> Int
  ```
- **Implémentation** :
  ```haskell
  add x y = x + y
  ```
- 🔎 Elle prend deux entiers et retourne leur somme. L’opérateur `+` est une fonction infixe.

---

### 2. Fonction `isEven`

- **Signature attendue** :
  ```haskell
  isEven :: Int -> Bool
  ```
- **Implémentation** :
  ```haskell
  isEven n = n `mod` 2 == 0
  ```
- 🔎 Elle utilise l’opérateur `mod` pour vérifier si le reste de la division par 2 est nul.

---

### 3. Fonction `concatStrings`

- **Signature attendue** :
  ```haskell
  concatStrings :: String -> String -> String
  ```
- **Implémentation** :
  ```haskell
  concatStrings s1 s2 = s1 ++ s2
  ```
- 🔎 Elle utilise l’opérateur `++` pour concaténer deux chaînes.

---

## ✅ Résumé du code complet

```haskell
add :: Int -> Int -> Int
add x y = x + y

isEven :: Int -> Bool
isEven n = n `mod` 2 == 0

concatStrings :: String -> String -> String
concatStrings s1 s2 = s1 ++ s2
```

---
