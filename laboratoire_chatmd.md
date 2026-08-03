---
titre: Laboratoire ChatMD V5 — BAN et centres FRATE
variablesDynamiques: true
geolocation: true
plugins: readcsv
obfuscate: false
preload:
  - https://raw.githubusercontent.com/Codeurfou-sys/chatbot_civique/refs/heads/main/lieux_dits_test.csv
  - https://raw.githubusercontent.com/Codeurfou-sys/chatbot_civique/refs/heads/main/centres_frate.csv
---

# Laboratoire ChatMD V5

Ce laboratoire utilise deux fichiers CSV réels publiés dans le dépôt GitHub :

- `lieux_dits_test.csv`
- `centres_frate.csv`

1. [Commencer les tests](V5_MENU)

## V5_MENU

### Tests proposés

1. [Vérifier la lecture du CSV des lieux](V5_BAN_LOAD)
2. [Rechercher une ville ou une adresse](V5_BAN_INPUT)
3. [Rechercher un code postal](V5_CP_INPUT)
4. [Vérifier la lecture des centres FRATE](V5_CENTRES_LOAD)
5. [Rechercher un centre par ville](V5_CENTRE_INPUT)
6. [Afficher les centres proches de ma position](V5_GEO)
7. [Tester un parcours simplifié du module 07](V5_MODULE_INPUT)
8. [Afficher le bilan](V5_REPORT)

## V5_BAN_LOAD

### Test 1 — Lecture du CSV des lieux

Les trois premières lignes du fichier doivent apparaître ci-dessous.

```readcsv https://raw.githubusercontent.com/Codeurfou-sys/chatbot_civique/refs/heads/main/lieux_dits_test.csv
maxResults: 3

### $i. $2

- Code postal : **$1**
- Adresse : $3
- Latitude : $4
- Longitude : $5
```

`@testBanLoad = réussi si trois résultats apparaissent`

1. [Retour au menu](V5_MENU)

## V5_BAN_INPUT

### Test 2 — Recherche d’une ville ou d’une adresse

Saisissez par exemple :

- Strasbourg
- Bourges
- rue du Jura
- place Darcy

!Next: V5_BAN_RESULTS

1. [Retour au menu](V5_MENU)

## V5_BAN_RESULTS

`@rechercheLieu = calc(@INPUT.trim().toLowerCase())`
`@sujetLieu = calc(mainTopic(@rechercheLieu))`

Recherche : **`@rechercheLieu`**

Sujet principal : **`@sujetLieu`**

```readcsv https://raw.githubusercontent.com/Codeurfou-sys/chatbot_civique/refs/heads/main/lieux_dits_test.csv
condition: $2.toLowerCase().includes(mainTopic("@INPUT").toLowerCase()) || $3.toLowerCase().includes(mainTopic("@INPUT").toLowerCase())
maxResults: 5

### $i. $2 — $1

Adresse : $3  
Latitude : $4  
Longitude : $5
```

`@testBanSearch = à vérifier`

1. [Nouvelle recherche](V5_BAN_INPUT)
2. [Retour au menu](V5_MENU)

## V5_CP_INPUT

### Test 3 — Recherche par code postal

Saisissez un code postal présent dans le fichier, par exemple `67000`, `21000` ou `63000`.

!Next: V5_CP_RESULTS

1. [Retour au menu](V5_MENU)

## V5_CP_RESULTS

`@rechercheCP = calc(@INPUT.trim())`

Code postal : **`@rechercheCP`**

```readcsv https://raw.githubusercontent.com/Codeurfou-sys/chatbot_civique/refs/heads/main/lieux_dits_test.csv
condition: $1 == "@rechercheCP"
sort: $2 asc alph
maxResults: 5

### $i. $2

Adresse : $3  
Code postal : $1  
Coordonnées : $4, $5
```

`@testBanCP = à vérifier`

1. [Nouvelle recherche](V5_CP_INPUT)
2. [Retour au menu](V5_MENU)

## V5_CENTRES_LOAD

### Test 4 — Lecture du CSV des centres FRATE

```readcsv https://raw.githubusercontent.com/Codeurfou-sys/chatbot_civique/refs/heads/main/centres_frate.csv
sort: $2 asc alph
maxResults: 8

### $i. $2 — $3

- Région : $4
- Latitude : $5
- Longitude : $6
- [Ouvrir le lien d’inscription](link:$7)
```

`@testCentresLoad = réussi si les centres apparaissent`

1. [Retour au menu](V5_MENU)

## V5_CENTRE_INPUT

### Test 5 — Recherche d’un centre par ville

Saisissez par exemple `Strasbourg`, `Dijon`, `Colmar` ou `Lyon`.

!Next: V5_CENTRE_RESULTS

1. [Retour au menu](V5_MENU)

## V5_CENTRE_RESULTS

`@rechercheCentre = calc(@INPUT.trim().toLowerCase())`

Ville recherchée : **`@rechercheCentre`**

```readcsv https://raw.githubusercontent.com/Codeurfou-sys/chatbot_civique/refs/heads/main/centres_frate.csv
condition: $2.toLowerCase().includes(mainTopic("@INPUT").toLowerCase()) || $3 == "@rechercheCentre"
maxResults: 5

### Centre de $2

Code postal : $3  
Région : $4  
Coordonnées : $5, $6  
[Inscription](link:$7)
```

`@testCentreSearch = à vérifier`

1. [Nouvelle recherche](V5_CENTRE_INPUT)
2. [Retour au menu](V5_MENU)

## V5_GEO

### Test 6 — Centres autour de la géolocalisation

Latitude : **`@LATITUDE`**

Longitude : **`@LONGITUDE`**

Précision : **`@POSITION_ACCURACY`** mètres

`if @LATITUDE != undefined && @LONGITUDE != undefined`

Le bloc conserve les centres situés dans une zone de quatre degrés autour de la position.

```readcsv https://raw.githubusercontent.com/Codeurfou-sys/chatbot_civique/refs/heads/main/centres_frate.csv
condition: Math.abs($5-@LATITUDE)<4 && Math.abs($6-@LONGITUDE)<4
maxResults: 3

### $i. Centre de $2

Code postal : $3  
Région : $4  
Coordonnées : $5, $6  
[Inscription](link:$7)
```

`@testGeo = réussi si trois centres apparaissent`

`endif`

`if @LATITUDE == undefined || @LONGITUDE == undefined`

La géolocalisation n’est pas disponible. Autorisez-la dans le navigateur puis rechargez ChatMD.

`@testGeo = géolocalisation indisponible`

`endif`

1. [Retour au menu](V5_MENU)

## V5_MODULE_INPUT

### Test 7 — Parcours simplifié du module 07

Saisissez une ville ou un code postal.

Exemples : `Strasbourg`, `67000`, `Dijon`, `21000`.

!Next: V5_MODULE_RESULTS

1. [Retour au menu](V5_MENU)

## V5_MODULE_RESULTS

`@demandeModule = calc(@INPUT.trim().toLowerCase())`
`@demandeSujet = calc(mainTopic(@demandeModule))`

Recherche saisie : **`@demandeModule`**

### Étape 1 — Lieux correspondants

```readcsv https://raw.githubusercontent.com/Codeurfou-sys/chatbot_civique/refs/heads/main/lieux_dits_test.csv
condition: $1 == "@demandeModule" || $2.toLowerCase().includes(mainTopic("@INPUT").toLowerCase()) || $3.toLowerCase().includes(mainTopic("@INPUT").toLowerCase())
maxResults: 3

$i. **$2 — $1**  
$3  
Coordonnées : $4, $5
```

### Étape 2 — Centre FRATE correspondant à la ville ou au code postal

```readcsv https://raw.githubusercontent.com/Codeurfou-sys/chatbot_civique/refs/heads/main/centres_frate.csv
condition: $2.toLowerCase().includes(mainTopic("@INPUT").toLowerCase()) || $3 == "@demandeModule"
maxResults: 3

### Centre de $2

Code postal : $3  
Région : $4  
Coordonnées : $5, $6  
[Ouvrir l’inscription](link:$7)
```

### Étape 3 — Centres autour de la position du navigateur

`if @LATITUDE != undefined && @LONGITUDE != undefined`

```readcsv https://raw.githubusercontent.com/Codeurfou-sys/chatbot_civique/refs/heads/main/centres_frate.csv
condition: Math.abs($5-@LATITUDE)<4 && Math.abs($6-@LONGITUDE)<4
maxResults: 3

$i. **$2 ($3)** — $4  
[Inscription](link:$7)
```

`endif`

`@testModule = à vérifier`

1. [Nouvelle recherche](V5_MODULE_INPUT)
2. [Retour au menu](V5_MENU)

## V5_REPORT

### Bilan

| Fonction | Résultat |
|---|---|
| Chargement du CSV des lieux | `@testBanLoad` |
| Recherche par texte | `@testBanSearch` |
| Recherche par code postal | `@testBanCP` |
| Chargement des centres | `@testCentresLoad` |
| Recherche d’un centre | `@testCentreSearch` |
| Filtre géographique | `@testGeo` |
| Parcours Module 07 | `@testModule` |

### Validation attendue

- Le test 1 confirme que `readcsv` charge réellement `lieux_dits_test.csv`.
- Les tests 2 et 3 confirment que les variables dynamiques fonctionnent dans `condition:`.
- Le test 4 confirme que `centres_frate.csv` est lisible.
- Le test 5 confirme qu’un centre peut être retrouvé à partir d’une ville.
- Le test 6 confirme que les coordonnées du navigateur peuvent filtrer les centres.
- Le test 7 valide un premier parcours fonctionnel du module 07.

1. [Recommencer](V5_RESET)
2. [Retour au menu](V5_MENU)

## V5_RESET

`@testBanLoad = undefined`
`@testBanSearch = undefined`
`@testBanCP = undefined`
`@testCentresLoad = undefined`
`@testCentreSearch = undefined`
`@testGeo = undefined`
`@testModule = undefined`

Les indicateurs ont été réinitialisés.

1. [Retour au menu](V5_MENU)
