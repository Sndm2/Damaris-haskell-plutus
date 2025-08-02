HC1T2 - Tâche 2 : Exemple de fonction pure

### 💻 Code Haskell exécutable

```haskell
-- Définition d’une fonction pure qui calcule l’aire d’un cercle
circleArea :: Float -> Float
circleArea r = pi * r ^ 2

-- Exemple d’exécution
main :: IO ()
main = do
    let rayon = 3.0
    putStrLn ("Rayon : " ++ show rayon)
    putStrLn ("Aire du cercle : " ++ show (circleArea rayon))
```

---

### 🔍 Explication détaillée

#### 🧩 Définition de `circleArea`

- **Type** : `Float -> Float`  
  Elle prend un nombre décimal représentant le rayon (`r`) et retourne un nombre décimal représentant l’aire du cercle.
- **Calcul** : Utilise la formule mathématique classique :  
  $$\text{Aire} = \pi \times r^2$$
- **Constante `pi`** : fournie par Haskell, donc aucune dépendance externe.

✅ **Pureté garantie** :  
- `circleArea` dépend uniquement de son **paramètre**.
- Elle ne lit ni ne modifie d’état externe.
- Elle donne **toujours le même résultat** pour une valeur donnée.

---

#### 🖥️ Fonction `main`

- Crée un petit scénario d'exécution :
  - Initialise `rayon` à `3.0`.
  - Affiche la valeur du rayon.
  - Affiche le résultat de `circleArea 3.0`.

---

### 🎓 Lien avec ta leçon

Ta page sur la programmation fonctionnelle affirme que :
> "Une fonction pure renverra toujours le même résultat pour une même entrée, et ne dépend d’aucun état externe."

📌 `circleArea` illustre parfaitement ce principe :
- ✔️ Elle est **mathématiquement exacte**
- ✔️ Elle n’a **aucun effet de bord**
- ✔️ Elle est **testable**, **prévisible**, et **isolée**

---
