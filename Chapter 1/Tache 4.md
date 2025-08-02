HC1T4 - Tâche 4 : Composer une fonction pour traiter des données de joueurs

---

### 💻 Code Haskell

```haskell
import Data.List (sortBy)
import Data.Ord (comparing)

-- Type : Liste de tuples (nom, score)
type Player = (String, Int)

-- Trie les joueurs par score décroissant
sortByScore :: [Player] -> [Player]
sortByScore = sortBy (flip (comparing snd))

-- Extrait les noms des joueurs
extractPlayers :: [Player] -> [String]
extractPlayers players = [name | (name, _) <- players]

-- Retourne les 3 premiers éléments d'une liste
topThree :: [Player] -> [Player]
topThree = take 3

-- Fonction composée : trie, sélectionne les 3 meilleurs, puis extrait les noms
getTopThreePlayers :: [Player] -> [String]
getTopThreePlayers = extractPlayers . topThree . sortByScore

-- Programme principal
main :: IO ()
main = do
    let joueurs = [("Anna", 87), ("Liam", 92), ("Nina", 78), ("Jonas", 95), ("Emma", 88)]
    putStrLn "Liste des joueurs :"
    print joueurs

    putStrLn "\nTop 3 par score décroissant :"
    print (topThree (sortByScore joueurs))

    putStrLn "\nNoms des 3 meilleurs joueurs :"
    print (getTopThreePlayers joueurs)
```

---

### 🔎 Explication détaillée des fonctions

#### ✅ `sortByScore`
- Utilise `sortBy` avec `comparing snd` pour trier par le **second élément** du tuple (le score).
- `flip` inverse le tri pour que ce soit **décroissant**.

#### ✅ `topThree`
- Applique `take 3` sur la liste triée → garde les 3 premiers.

#### ✅ `extractPlayers`
- Parcourt les tuples `(nom, score)` et récupère le **nom** uniquement.
- Utilise une **liste en compréhension** (`[name | (name, _) <- ...]`) pour plus de lisibilité.

#### ✅ `getTopThreePlayers`
- Composition de fonctions :
  ```haskell
  getTopThreePlayers = extractPlayers . topThree . sortByScore
  ```
  - L’ordre d’exécution :  
    `sortByScore` ➝ `topThree` ➝ `extractPlayers`
  - Ce style de code correspond exactement à ce que ta leçon sur Haskell enseigne :
    > *Acheminer le résultat d'une fonction vers l'entrée d'une autre pour créer des chaînes de traitement de données.*

---

### 🧪 Exemple avec liste de joueurs

```haskell
[("Anna", 87), ("Liam", 92), ("Nina", 78), ("Jonas", 95), ("Emma", 88)]
```

📊 Tri décroissant →  
`[("Jonas",95),("Liam",92),("Emma",88)]`

🏆 Extraction des noms →  
`["Jonas","Liam","Emma"]`

---
