HC2T6 - Tâche 6 : Comprendre Int vs Integer

---

## 🎯 Objectif pédagogique

Cette tâche vise à faire comprendre :

- Les **limites de `Int`**, qui est un entier à taille fixe.
- Les **avantages de `Integer`**, qui est un entier à précision arbitraire.
- Les conséquences pratiques de cette différence, notamment en cas de dépassement de capacité.

---

## 📚 Concepts clés tirés de la page

La page environnante explique :

- **`Int`** est un entier **fixe**, généralement codé sur **64 bits** sur les systèmes modernes. Il est **plus rapide**, mais **limité** en taille.
- **`Integer`** est un entier **arbitraire**, sans limite de taille. Il est **plus lent**, mais **plus sûr** pour les grands calculs.
- Exemple donné :
  ```haskell
  2 ^ 62 :: Int     -- OK
  2 ^ 64 :: Int     -- Erreur !
  2 ^ 127 :: Integer -- OK
  ```

---

## 🧠 Implémentation demandée

### 1. Définir `smallNumber` avec `Int`

```haskell
smallNumber :: Int
smallNumber = 262
```

### 2. Définir `bigNumber` avec `Integer`

```haskell
bigNumber :: Integer
bigNumber = 2127
```

---

## 🧪 Test dans GHCi : `2^64 :: Int`

Lorsque tu tapes :

```haskell
2^64 :: Int
```

Tu obtiens une **erreur de dépassement** (overflow), car `2^64` dépasse la capacité maximale d’un `Int` sur 64 bits.

🔴 Résultat typique :
> *** Exception: arithmetic overflow

Mais si tu utilises `Integer` :

```haskell
2^64 :: Integer
```

✅ Résultat :
> 18446744073709551616

---

## ✅ Conclusion

Cette tâche illustre une règle fondamentale :

> 🔒 **Utilise `Integer` pour les grands calculs, et `Int` pour les performances sur des valeurs modestes.**
