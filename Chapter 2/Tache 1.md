HC2T1 - Tâche 1 : Vérification des types dans GHCi

---

## 🎯 Objectif de la tâche HC2T1

Cette tâche invite à explorer le **système de types de Haskell** à travers l’environnement interactif **GHCi**. Elle demande de :

1. **Prédire les types** des expressions données.
2. **Vérifier ces types** dans GHCi à l’aide de la commande `:type` ou `:t`.

Cela te permet de mieux comprendre comment Haskell attribue un type à chaque expression, ce qui est fondamental pour écrire du code sûr et cohérent.

---

## 📚 Concepts clés du cours

- Chaque expression en Haskell possède un **type**, indiqué par le symbole `::`.
- Les types **restreignent l’usage** d’une expression et permettent au compilateur de détecter les erreurs.
- La commande `:type` (ou `:t`) dans GHCi permet d’afficher le type d’une expression.
- Les **types de base** incluent :
  - `Int` et `Integer` pour les entiers
  - `Float` et `Double` pour les réels
  - `Bool` pour les valeurs logiques (`True`, `False`)
  - `Char` pour les caractères
  - `String` pour les chaînes de texte (`[Char]`)

---

## 🔍 Analyse des expressions

Voici les expressions à tester, avec les **types attendus** :

| Expression        | Type attendu       | Justification tirée du cours |
|-------------------|--------------------|------------------------------|
| `42`              | `Num a => a` (souvent `Int`) | Entier, interprété comme un nombre numérique générique. |
| `3.14`            | `Fractional a => a` (souvent `Double`) | Nombre à virgule flottante. |
| `"Haskell"`       | `String` ou `[Char]` | Chaîne de caractères, équivalente à une liste de `Char`. |
| `'Z'`             | `Char`              | Caractère unique entre apostrophes simples. |
| `True && False`   | `Bool`              | Expression logique avec l’opérateur `&&`. |

---

## 🧪 Vérification dans GHCi

code:

```haskell
:t 42
:t 3.14
:t "Haskell"
:t 'Z'
:t True && False
```

Résultats :

```haskell
42 :: Num a => a
3.14 :: Fractional a => a
"Haskell" :: [Char]
'Z' :: Char
True && False :: Bool
```

---

## ✅ Conclusion

Cette tâche permet de :

- se familiariser avec les **types fondamentaux** de Haskell.
- Comprendre la **notation de type** avec `::`.
- Utiliser GHCi comme un outil d’exploration et de vérification.
- Préparer les prochaines tâches du module, comme l’écriture de **signatures de fonctions** (HC2T2) ou la manipulation de **variables immuables** (HC2T3).
