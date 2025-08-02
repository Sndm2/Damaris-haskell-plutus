HC1T1 - Tâche 1 : Composition de fonctions

---

### 💻 Code Haskell fourni

```haskell
-- Fonction qui multiplie un nombre par 2
double :: Int -> Int
double x = x * 2

-- Fonction qui augmente un nombre de 1
increment :: Int -> Int
increment x = x + 1

-- Composition : doubleThenIncrement applique d’abord double, puis increment
doubleThenIncrement :: Int -> Int
doubleThenIncrement = increment . double

-- Fonction principale : démonstration du comportement
main :: IO ()
main = do
    let x = 4
    print ("Résultat de double " ++ show x ++ ": " ++ show (double x))
    print ("Résultat de increment " ++ show (double x) ++ ": " ++ show (increment (double x)))
    print ("Résultat final (doubleThenIncrement): " ++ show (doubleThenIncrement x))
```

---

### 🔍 Explications détaillées

#### 🧠 Fonctions pures

Tu travailles ici avec des **fonctions pures**, ce qui est central en Haskell :
- `double` : calcule une transformation de données (`x * 2`)
- `increment` : ajoute 1 à une donnée
- Pas d’effet de bord, pas de dépendance à un état externe → elles sont **prévisibles et testables**

---

#### 🔗 Composition de fonctions : `doubleThenIncrement`

- Syntaxe : `increment . double`
- L’opérateur `.` signifie : *« Applique `double`, puis donne le résultat à `increment` »*
- Cela correspond à l’ordre **matériel** de traitement des données :
  1. `x = 4`
  2. `double 4 = 8`
  3. `increment 8 = 9`
  4. Résultat : `doubleThenIncrement 4 = 9`

---

### 🖥️ Fonction `main` et sortie console

Elle illustre chaque étape explicitement, ce qui est parfait pour bien comprendre :
- `print ("Résultat de double 4 : 8")`
- `print ("Résultat de increment 8 : 9")`
- `print ("Résultat final (doubleThenIncrement): 9")`

🔎 Tu mets en valeur le **flux logique de la transformation**, ce qui est au cœur de la programmation fonctionnelle : des **expressions chaînables, prévisibles, modulaires**.

---

### 📘 Lien avec ta leçon HC1T1

Ta leçon explique que :
> “La composition consiste à acheminer le résultat d'une fonction vers l'entrée d'une autre.”

Et c’est exactement ce que ton code fait, dans un style Haskell **élégant et paresseux**. Le système **évalue uniquement ce qui est nécessaire**, favorisant un code concis et efficace.

---
