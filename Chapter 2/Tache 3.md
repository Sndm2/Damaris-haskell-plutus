HC2T3 - Tâche 3 : Variables immuables

---

## 🎯 Objectif pédagogique

Cette tâche permet de comprendre que **Haskell est un langage purement fonctionnel**, ce qui signifie que **les variables sont immuables** : une fois qu’une valeur est assignée à un nom, elle ne peut plus être modifiée.

---

## 📚 Concepts clés tirés de la page

La page explique que :

- Une **variable** en Haskell est en réalité une **définition** :  
  ```haskell
  name = "Bob"
  ```
  Cela signifie que `name` est toujours égal à `"Bob"` — il ne peut pas être réassigné.

- Le symbole `::` est utilisé pour **annoter le type** d’une expression :
  ```haskell
  name :: String
  name = "Bob"
  ```

- Les **types de base** utilisés dans cette tâche sont :
  - `Int` pour les entiers
  - `Double` pour les réels à virgule flottante
  - `String` pour les chaînes de texte
  - `Bool` pour les valeurs logiques (`True`, `False`)

---

## 🧠 Implémentation attendue

Voici comment définir les variables demandées :

```haskell
myAge :: Int
myAge = 25

piValue :: Double
piValue = 3.14159

greeting :: String
greeting = "Bonjour, Haskell !"

isHaskellFun :: Bool
isHaskellFun = True
```

---

## ⚠️ Immutabilité en action

Essayons de **modifier une variable** dans GHCi ou dans un fichier `.hs`, comme ceci :

```haskell
myAge = 30
```

après l’avoir déjà définie, Haskell renverra une **erreur de redéfinition** :

> *Multiple declarations of ‘myAge’*

Cela confirme que **les noms ne peuvent pas être réassignés** — contrairement aux langages impératifs comme Python ou JavaScript.

---

## ✅ Conclusion

Cette tâche illustre un principe fondamental de Haskell :

> 🔒 **Une fois qu’un nom est défini, sa valeur est figée.**

Cela garantit la **prévisibilité** et la **sécurité** du code, en évitant les effets de bord liés à la mutation des variables.
