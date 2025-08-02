HC1T8 - Tâche 8 : Fonctions d’ordre supérieur

---

## 💻 Code Haskell exécutable

```haskell
-- Définition d'une fonction d’ordre supérieur
applyTwice :: (a -> a) -> a -> a
applyTwice f x = f (f x)

-- Programme principal pour test
main :: IO ()
main = do
    let double x = x * 2
    let result = applyTwice double 3
    putStrLn ("Résultat de applyTwice double 3 : " ++ show result)
```

---

## 🔍 Explication détaillée

### ✅ Signature de type

```haskell
applyTwice :: (a -> a) -> a -> a
```

- `(a -> a)` : une fonction qui prend une valeur de type `a` et retourne une valeur de même type.
- `a` : la valeur d’entrée à laquelle la fonction sera appliquée deux fois.
- Le résultat est aussi de type `a`.

💡 **Polymorphisme** : le type `a` est générique, donc `applyTwice` peut fonctionner avec des nombres, des chaînes, des listes, etc., du moment que la fonction fournie respecte le type `(a -> a)`.

---

### ✅ Corps de la fonction

```haskell
applyTwice f x = f (f x)
```

- On applique `f` une première fois à `x`, ce qui donne `f x`.
- Puis on applique `f` encore une fois sur ce résultat.

---

### ✅ Exemple avec `double`

```haskell
double x = x * 2
applyTwice double 3
-- Étapes :
-- f x = double 3 = 6
-- f (f x) = double 6 = 12
```

Le terminal affichera :

```
Résultat de applyTwice double 3 : 12
```

---

