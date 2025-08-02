HC1T6 - Tâche 6 : Utilisation de signatures de type

---

## 💻 Code Haskell exécutable

```haskell
-- Définition d'une fonction avec signature de type
addNumbers :: Int -> Int -> Int
addNumbers x y = x + y

-- Programme principal pour tester la fonction
main :: IO ()
main = do
    let a = 5
    let b = 7
    putStrLn ("a = " ++ show a)
    putStrLn ("b = " ++ show b)
    putStrLn ("Somme : " ++ show (addNumbers a b))
```

---

## 🔍 Explication détaillée

### ✅ Signature de type

```haskell
addNumbers :: Int -> Int -> Int
```

- Elle indique que `addNumbers` prend **deux entiers** (`Int`) et retourne **un entier** (`Int`).
- Le type est vérifié **avant l’exécution**, ce qui est une propriété clé des langages **statiquement typés** comme Haskell.

---

### ✅ Définition de la fonction

```haskell
addNumbers x y = x + y
```

- `x` et `y` sont les paramètres.
- L’expression `x + y` est le **corps de la fonction**, qui renvoie leur somme.
- Aucune dépendance extérieure → ✅ **fonction pure**

---

### ✅ Fonction `main`

```haskell
main :: IO ()
```

- Point d’entrée du programme Haskell.
- Utilise `putStrLn` pour afficher chaque étape.
- `show` convertit les entiers en chaînes de caractères pour l’affichage.

---

### 🧪 Exemple d’exécution

```haskell
a = 5
b = 7
addNumbers a b → 12
```

Le terminal affichera :

```
a = 5
b = 7
Somme : 12
```

---
