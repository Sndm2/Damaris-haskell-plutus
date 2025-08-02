HC1T3 - Tâche 3 : Vérifier si un nombre est supérieur à 18

---

### 💻 Code Haskell exécutable

```haskell
-- Définition d'une fonction pure qui teste si un nombre est supérieur à 18
greaterThan18 :: Int -> Bool
greaterThan18 x = x > 18

-- Exemple d’exécution
main :: IO ()
main = do
    let nombre = 20
    putStrLn ("Nombre : " ++ show nombre)
    putStrLn ("Est-il supérieur à 18 ? " ++ show (greaterThan18 nombre))
```

---

### 🔍 Explications détaillées

#### 🧩 Définition de la fonction

- **Nom** : `greaterThan18`
- **Type** : `Int -> Bool`  
  Elle prend un **entier** et retourne un **booléen** (`True` ou `False`)
- **Logique** : Elle utilise l’opérateur `>` pour vérifier si la valeur d’entrée est strictement supérieure à 18

✅ **Pureté** :
- Elle ne dépend que de son **argument**
- Elle donne **toujours** le même résultat pour la même entrée
- Elle n’interagit ni avec l’environnement ni avec un état externe

---

#### 🖥️ Partie `main`

- Initialise une variable `nombre` à `20`
- Affiche sa valeur avec `putStrLn`
- Utilise `greaterThan18 nombre` pour afficher le résultat du test

---

📚 Cette tâche illustre parfaitement le principe de la **programmation fonctionnelle pure**, tout comme l’expliquent tes cours sur Haskell.

