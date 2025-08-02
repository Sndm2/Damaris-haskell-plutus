HC1T7 - Tâche 7 : Conversion Fahrenheit/Celsius

---

## 💻 Code Haskell exécutable

```haskell
-- Signature de type : fToC prend un Float et retourne un Float
fToC :: Float -> Float
fToC f = (f - 32) * 5 / 9

-- Programme principal
main :: IO ()
main = do
    let fahrenheit = 98.6
    let celsius = fToC fahrenheit
    putStrLn ("Température en Fahrenheit : " ++ show fahrenheit)
    putStrLn ("Convertie en Celsius : " ++ show celsius)
```

---

## 🔍 Explication détaillée

### ✅ Signature de type

```haskell
fToC :: Float -> Float
```

- Spécifie que `fToC` prend un **Float** (nombre à virgule) et retourne un **Float**.
- Le typage explicite permet de mieux **documenter** et **contrôler** le comportement.

---

### ✅ Corps de la fonction

```haskell
fToC f = (f - 32) * 5 / 9
```

- Formule mathématique standard :  
  $$\text{Celsius} = (\text{Fahrenheit} - 32) \times \frac{5}{9}$$
- L’expression est directe, claire et purement fonctionnelle.

---

### ✅ Bloc `main`

```haskell
main :: IO ()
```

- Lance le programme.
- `let` définit des constantes locales.
- `show` transforme les nombres en chaînes de caractères pour l’affichage.
- `putStrLn` affiche les résultats dans la console.

---

### 🧪 Résultat attendu

```
Température en Fahrenheit : 98.6
Convertie en Celsius : 37.0
```

---

