HC1T5 - Tâche 5 : Paresse en Haskell

---

## 💻 Code exécutable en Haskell

```haskell
-- Fonction qui génère une liste infinie de nombres naturels
infiniteNumbers :: [Int]
infiniteNumbers = [1..]  -- Commence à 1 et continue indéfiniment

-- Fonction qui extrait les n premiers éléments d'une liste
firstN :: Int -> [Int]
firstN n = take n infiniteNumbers

-- Fonction principale
main :: IO ()
main = do
    putStrLn "Voici les 15 premiers nombres naturels :"
    print (firstN 15)
```

---

## 📖 Explication étape par étape

### ✅ `infiniteNumbers :: [Int]`
- Créé avec la syntaxe `[1..]`, c’est une liste **infinie** de tous les entiers naturels à partir de 1.
- Grâce à Haskell et sa nature paresseuse, cette liste **n’est pas générée entièrement d’un seul coup**, mais **en partie, à la demande**.

### ✅ `firstN n = take n infiniteNumbers`
- Utilise `take` pour **extraire les n premiers** éléments de la liste.
- Même si la liste est infinie, `take` **ne va générer que ce qu’il faut**, rien de plus.
- Par exemple, `firstN 15` retourne : `[1,2,3,4,5,6,7,8,9,10,11,12,13,14,15]`.

### ✅ `main`
- Fonction d’entrée du programme.
- Appelle `firstN 15` et affiche le résultat dans le terminal.

---

## 🔬 Pourquoi ça fonctionne sans planter

- Haskell **évalue les expressions seulement quand elles sont nécessaires**.  
- Donc `[1..]` reste “suspendue” tant qu’on ne demande rien. Et dès qu’on appelle `take 15`, Haskell génère **juste 15 valeurs**, pas une de plus.

---

