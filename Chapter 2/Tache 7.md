HC2T7 - Tâche 7 : Expressions booléennes

---

## 🎯 Objectif pédagogique

Cette tâche vise à te familiariser avec :

- Le type **`Bool`**, qui ne contient que deux valeurs : `True` et `False`.
- Les **opérateurs logiques** : `&&`, `||`, `not`.
- Les **comparaisons** comme `<`, `>`, `==`, `>=`, etc.

Tu apprends à écrire des expressions qui retournent des valeurs booléennes selon la logique utilisée.

---

## 📚 Concepts tirés de la page environnante

- Le type `Bool` est utilisé pour représenter des **valeurs de vérité**.
- Les opérateurs logiques sont des **fonctions infixes** :
  - `&&` : ET logique
  - `||` : OU logique
  - `not` : négation logique (préfixe)
- Les comparaisons comme `5 /= 0`, `3 >= 0`, ou `7.2 < 6.1` retournent des `Bool`.

---

## 🧠 Implémentation des expressions demandées

### 1. ✅ Expression qui retourne `True` avec `&&`

```haskell
True && True
-- Résultat : True
```

### 2. ❌ Expression qui retourne `False` avec `||`

```haskell
False || False
-- Résultat : False
```

### 3. ✅ Expression qui retourne `True` avec `not`

```haskell
not False
-- Résultat : True
```

### 4. ❌ Comparaison qui retourne `False`

```haskell
5 > 10
-- Résultat : False
```

---

## 🧪 Tests dans GHCi

```haskell
True && True
False || False
not False
5 > 10
```

Observer les résultats affichés.

---

## ✅ Conclusion

Cette tâche t’aide à :

- Comprendre le fonctionnement des **opérateurs logiques**.
- Manipuler des **expressions conditionnelles**.
- Préparer le terrain pour des fonctions plus complexes, comme des filtres ou des conditions dans des listes.
