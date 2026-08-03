---
titre: Laboratoire ChatMD V8 — quatre syntaxes code postal
variablesDynamiques: true
plugins: readcsv
obfuscate: false
preload:
  - https://raw.githubusercontent.com/Codeurfou-sys/chatbot_civique/refs/heads/main/lieux_dits_test.csv
  - https://raw.githubusercontent.com/Codeurfou-sys/chatbot_civique/refs/heads/main/centres_frate.csv
---

# Laboratoire ChatMD V8

Ce laboratoire compare quatre syntaxes de filtrage pour identifier celle qui fonctionne avec les codes postaux.

1. [Commencer le test](V8_MENU)

## V8_MENU

### Tests disponibles

1. [Test A — égalité exacte](V8_TEST_A)
2. [Test B — includes()](V8_TEST_B)
3. [Test C — conversion en chaîne avec concaténation](V8_TEST_C)
4. [Test D — startsWith() avec saisie directe](V8_TEST_D)
5. [Comparer les quatre résultats](V8_BILAN)

---

## V8_TEST_A

### Test A — égalité exacte

`if !@cpA`

Saisissez un code postal présent dans le CSV.

Exemples : `67000`, `21000`, `63000`.

`endif`

`if @cpA`

`@cpAPurified = calc(@cpA.trim())`

Valeur saisie : **`@cpA`**  
Valeur nettoyée : **`@cpAPurified`**

```readcsv https://raw.githubusercontent.com/Codeurfou-sys/chatbot_civique/refs/heads/main/lieux_dits_test.csv
condition: $1 == "`@cpAPurified`"
maxResults: 5

### $i. $2 — $1

Adresse : $3  
Coordonnées : $4, $5
```

`@resultatA = réussi si des lignes apparaissent`

`@cpA = undefined`
`@cpAPurified = undefined`

`endif`

`@cpA = @INPUT : V8_TEST_A`

1. [Recommencer le test A](V8_TEST_A)
2. [Retour au menu](V8_MENU)

---

## V8_TEST_B

### Test B — recherche avec `.includes()`

`if !@cpB`

Saisissez un code postal présent dans le CSV.

`endif`

`if @cpB`

`@cpBPurified = calc(@cpB.trim())`

Valeur saisie : **`@cpB`**  
Valeur nettoyée : **`@cpBPurified`**

```readcsv https://raw.githubusercontent.com/Codeurfou-sys/chatbot_civique/refs/heads/main/lieux_dits_test.csv
condition: $1.includes("`@cpBPurified`")
maxResults: 5

### $i. $2 — $1

Adresse : $3  
Coordonnées : $4, $5
```

`@resultatB = réussi si des lignes apparaissent`

`@cpB = undefined`
`@cpBPurified = undefined`

`endif`

`@cpB = @INPUT : V8_TEST_B`

1. [Recommencer le test B](V8_TEST_B)
2. [Retour au menu](V8_MENU)

---

## V8_TEST_C

### Test C — conversion en chaîne par concaténation

`if !@cpC`

Saisissez un code postal présent dans le CSV.

`endif`

`if @cpC`

`@cpCPurified = calc(@cpC.trim())`

Valeur saisie : **`@cpC`**  
Valeur nettoyée : **`@cpCPurified`**

```readcsv https://raw.githubusercontent.com/Codeurfou-sys/chatbot_civique/refs/heads/main/lieux_dits_test.csv
condition: ($1+"").startsWith("`@cpCPurified`")
maxResults: 5

### $i. $2 — $1

Adresse : $3  
Coordonnées : $4, $5
```

`@resultatC = réussi si des lignes apparaissent`

`@cpC = undefined`
`@cpCPurified = undefined`

`endif`

`@cpC = @INPUT : V8_TEST_C`

1. [Recommencer le test C](V8_TEST_C)
2. [Retour au menu](V8_MENU)

---

## V8_TEST_D

### Test D — `startsWith()` avec variable saisie directement

Ce test reprend au plus près le modèle officiel UAI, sans variable intermédiaire dans la condition.

`if !@cpD`

Saisissez un code postal présent dans le CSV.

`endif`

`if @cpD`

Valeur saisie : **`@cpD`**

```readcsv https://raw.githubusercontent.com/Codeurfou-sys/chatbot_civique/refs/heads/main/lieux_dits_test.csv
condition: $1.startsWith("`@cpD`")
maxResults: 5

### $i. $2 — $1

Adresse : $3  
Coordonnées : $4, $5
```

`@resultatD = réussi si des lignes apparaissent`

`@cpD = undefined`

`endif`

`@cpD = @INPUT : V8_TEST_D`

1. [Recommencer le test D](V8_TEST_D)
2. [Retour au menu](V8_MENU)

---

## V8_CENTRES

### Vérification complémentaire sur le CSV FRATE

Cette section permet de réutiliser la syntaxe gagnante sur la colonne `$3` du fichier des centres.

`if !@cpCentre`

Saisissez un code postal de centre : `67000`, `21000`, `63000`.

`endif`

`if @cpCentre`

`@cpCentrePurified = calc(@cpCentre.trim())`

#### Égalité exacte

```readcsv https://raw.githubusercontent.com/Codeurfou-sys/chatbot_civique/refs/heads/main/centres_frate.csv
condition: $3 == "`@cpCentrePurified`"
maxResults: 5

### Centre de $2

Code postal : $3  
Région : $4  
[Inscription](link:$7)
```

#### includes()

```readcsv https://raw.githubusercontent.com/Codeurfou-sys/chatbot_civique/refs/heads/main/centres_frate.csv
condition: $3.includes("`@cpCentrePurified`")
maxResults: 5

### Centre de $2

Code postal : $3  
Région : $4
```

#### Conversion puis startsWith()

```readcsv https://raw.githubusercontent.com/Codeurfou-sys/chatbot_civique/refs/heads/main/centres_frate.csv
condition: ($3+"").startsWith("`@cpCentrePurified`")
maxResults: 5

### Centre de $2

Code postal : $3  
Région : $4
```

`@cpCentre = undefined`
`@cpCentrePurified = undefined`

`endif`

`@cpCentre = @INPUT : V8_CENTRES`

1. [Recommencer la vérification FRATE](V8_CENTRES)
2. [Retour au menu](V8_MENU)

---

## V8_BILAN

# Comparaison des résultats

| Test | Syntaxe | Résultat |
|---|---|---|
| A | `$1 == "variable"` | `@resultatA` |
| B | `$1.includes("variable")` | `@resultatB` |
| C | `($1+"").startsWith("variable")` | `@resultatC` |
| D | `$1.startsWith("@cpD")` sans variable intermédiaire | `@resultatD` |

### Interprétation

- Si **A** fonctionne, retenir l’égalité exacte pour les codes postaux.
- Si **B** fonctionne, retenir `.includes()`.
- Si **C** fonctionne, cela confirme que la colonne est numérique et doit être convertie en chaîne.
- Si **D** fonctionne, le problème venait de la variable intermédiaire ou de son ordre d’évaluation.
- Si plusieurs tests fonctionnent, retenir **A**, car c’est la syntaxe la plus simple et la plus précise.

1. [Tester les mêmes syntaxes sur les centres FRATE](V8_CENTRES)
2. [Retour au menu](V8_MENU)
