---
titre: Laboratoire ChatMD V6 — syntaxe officielle readcsv
variablesDynamiques: true
geolocation: true
plugins: readcsv
obfuscate: false
preload:
  - https://raw.githubusercontent.com/Codeurfou-sys/chatbot_civique/refs/heads/main/lieux_dits_test.csv
  - https://raw.githubusercontent.com/Codeurfou-sys/chatbot_civique/refs/heads/main/centres_frate.csv
---

# Laboratoire ChatMD V6

Ce laboratoire reprend le modèle syntaxique du chatbot officiel de recherche d’établissements :

- saisie avec `@variable = @INPUT : écran cible` ;
- nettoyage avec `calc()` ;
- injection d’une variable dans `readcsv` avec les backticks ;
- filtrage avec `.toLowerCase().includes(...)`, `.startsWith(...)` et égalité ;
- liens construits avec les colonnes `$1`, `$2`, etc.

1. [Commencer](V6_MENU)

## V6_MENU

### Tests

1. [Recherche d’une ville dans le CSV BAN](V6_CITY)
2. [Recherche d’une adresse ou d’un mot-clé](V6_ADDRESS)
3. [Recherche par code postal](V6_CP)
4. [Recherche d’un centre FRATE par ville](V6_CENTRE_CITY)
5. [Recherche d’un centre FRATE par code postal](V6_CENTRE_CP)
6. [Lien cartographique dynamique depuis le CSV](V6_MAP)
7. [Filtre géographique avec les coordonnées du navigateur](V6_GEO)
8. [Parcours complet du module 07](V6_MODULE)
9. [Bilan](V6_REPORT)

---

## V6_CITY

`if !@citySearch`

D’accord, donne-moi le nom d’une ville.

Exemples : Strasbourg, Dijon, Colmar, Lyon.

`endif`

`if @citySearch`

`@citySearchPurified = calc(@citySearch.trim())`

Recherche nettoyée : **`@citySearchPurified`**

```readcsv https://raw.githubusercontent.com/Codeurfou-sys/chatbot_civique/refs/heads/main/lieux_dits_test.csv
condition: $2.toLowerCase().includes("`@citySearchPurified`".toLowerCase())
maxResults: 5

### $i. $2

Code postal : **$1**  
Adresse : $3  
Latitude : $4  
Longitude : $5
```

`@testCity = réussi si des lignes apparaissent`
`@citySearch = undefined`
`@citySearchPurified = undefined`

`endif`

`@citySearch = @INPUT : V6_CITY`

1. [Nouvelle recherche par ville](V6_CITY)
2. [Retour au menu](V6_MENU)

---

## V6_ADDRESS

`if !@addressSearch`

Donne-moi un mot présent dans une adresse.

Exemples : Jura, Kléber, Darcy, République.

`endif`

`if @addressSearch`

`@addressSearchPurified = calc(@addressSearch.trim())`

```readcsv https://raw.githubusercontent.com/Codeurfou-sys/chatbot_civique/refs/heads/main/lieux_dits_test.csv
condition: $3.toLowerCase().includes("`@addressSearchPurified`".toLowerCase())
maxResults: 5

### $i. $3

Ville : **$2**  
Code postal : $1  
Coordonnées : $4, $5
```

`@testAddress = réussi si des lignes apparaissent`
`@addressSearch = undefined`
`@addressSearchPurified = undefined`

`endif`

`@addressSearch = @INPUT : V6_ADDRESS`

1. [Nouvelle recherche par adresse](V6_ADDRESS)
2. [Retour au menu](V6_MENU)

---

## V6_CP

`if !@cpSearch`

Donne-moi un code postal à cinq chiffres.

Exemples : 67000, 21000, 63000.

`endif`

`if @cpSearch`

`@cpSearchPurified = calc(@cpSearch.trim())`

```readcsv https://raw.githubusercontent.com/Codeurfou-sys/chatbot_civique/refs/heads/main/lieux_dits_test.csv
condition: $1.startsWith("`@cpSearchPurified`")
sort: $2 asc alph
maxResults: 5

### $i. $2 — $1

Adresse : $3  
Coordonnées : $4, $5
```

`@testCP = réussi si des lignes apparaissent`
`@cpSearch = undefined`
`@cpSearchPurified = undefined`

`endif`

`@cpSearch = @INPUT : V6_CP`

1. [Nouvelle recherche par code postal](V6_CP)
2. [Retour au menu](V6_MENU)

---

## V6_CENTRE_CITY

`if !@centreCity`

Donne-moi la ville du centre FRATE recherché.

`endif`

`if @centreCity`

`@centreCityPurified = calc(@centreCity.trim())`

```readcsv https://raw.githubusercontent.com/Codeurfou-sys/chatbot_civique/refs/heads/main/centres_frate.csv
condition: $2.toLowerCase().includes("`@centreCityPurified`".toLowerCase())
maxResults: 5

### Centre de $2

Code postal : **$3**  
Région : $4  
Coordonnées : $5, $6  
[Ouvrir l’inscription](link:$7)
```

`@testCentreCity = réussi si le centre apparaît`
`@centreCity = undefined`
`@centreCityPurified = undefined`

`endif`

`@centreCity = @INPUT : V6_CENTRE_CITY`

1. [Nouvelle recherche](V6_CENTRE_CITY)
2. [Retour au menu](V6_MENU)

---

## V6_CENTRE_CP

`if !@centreCP`

Donne-moi le code postal du centre recherché.

`endif`

`if @centreCP`

`@centreCPPurified = calc(@centreCP.trim())`

```readcsv https://raw.githubusercontent.com/Codeurfou-sys/chatbot_civique/refs/heads/main/centres_frate.csv
condition: $3.startsWith("`@centreCPPurified`")
maxResults: 5

### Centre de $2

Code postal : **$3**  
Région : $4  
Coordonnées : $5, $6  
[Ouvrir l’inscription](link:$7)
```

`@testCentreCP = réussi si le centre apparaît`
`@centreCP = undefined`
`@centreCPPurified = undefined`

`endif`

`@centreCP = @INPUT : V6_CENTRE_CP`

1. [Nouvelle recherche](V6_CENTRE_CP)
2. [Retour au menu](V6_MENU)

---

## V6_MAP

### Liens cartographiques construits à partir des colonnes CSV

```readcsv https://raw.githubusercontent.com/Codeurfou-sys/chatbot_civique/refs/heads/main/centres_frate.csv
maxResults: 5

### $i. Centre de $2

Coordonnées : $5, $6  
[Voir le centre sur OpenStreetMap](https://www.openstreetmap.org/?#map=14/$5/$6)
```

`@testMap = réussi si les liens ouvrent la bonne position`

1. [Retour au menu](V6_MENU)

---

## V6_GEO

### Filtre géographique

Latitude utilisateur : **`@LATITUDE`**  
Longitude utilisateur : **`@LONGITUDE`**  
Précision : **`@POSITION_ACCURACY`** mètres

`if @LATITUDE != undefined && @LONGITUDE != undefined`

#### Variante A — injection numérique directe

```readcsv https://raw.githubusercontent.com/Codeurfou-sys/chatbot_civique/refs/heads/main/centres_frate.csv
condition: Math.abs($5-`@LATITUDE`)<4 && Math.abs($6-`@LONGITUDE`)<4
maxResults: 3

### $i. Centre de $2

Région : $4  
Coordonnées : $5, $6  
[Voir sur la carte](https://www.openstreetmap.org/?#map=12/$5/$6)
```

#### Variante B — comparaisons sans Math.abs

```readcsv https://raw.githubusercontent.com/Codeurfou-sys/chatbot_civique/refs/heads/main/centres_frate.csv
condition: $5>`@LATITUDE`-4 && $5<`@LATITUDE`+4 && $6>`@LONGITUDE`-4 && $6<`@LONGITUDE`+4
maxResults: 3

### $i. Centre de $2

Région : $4  
Coordonnées : $5, $6
```

`@testGeoFilter = réussi si au moins une variante affiche trois centres`

`endif`

`if @LATITUDE == undefined || @LONGITUDE == undefined`

La géolocalisation n’est pas disponible. Autorisez-la puis rechargez la page.

`@testGeoFilter = impossible sans géolocalisation`

`endif`

1. [Retour au menu](V6_MENU)

---

## V6_MODULE

### Parcours complet simplifié

1. [Rechercher par ville](V6_MODULE_CITY)
2. [Rechercher par code postal](V6_MODULE_CP)
3. [Utiliser ma géolocalisation](V6_MODULE_GEO)
4. [Retour au menu](V6_MENU)

## V6_MODULE_CITY

`if !@moduleCity`

Dans quelle ville souhaitez-vous passer l’examen ?

`endif`

`if @moduleCity`

`@moduleCityPurified = calc(@moduleCity.trim())`

### Lieux trouvés

```readcsv https://raw.githubusercontent.com/Codeurfou-sys/chatbot_civique/refs/heads/main/lieux_dits_test.csv
condition: $2.toLowerCase().includes("`@moduleCityPurified`".toLowerCase())
maxResults: 3

$i. **$2 — $1**  
$3
```

### Centre FRATE correspondant

```readcsv https://raw.githubusercontent.com/Codeurfou-sys/chatbot_civique/refs/heads/main/centres_frate.csv
condition: $2.toLowerCase().includes("`@moduleCityPurified`".toLowerCase())
maxResults: 3

### Centre de $2

Région : $4  
[Inscription](link:$7)  
[Carte](https://www.openstreetmap.org/?#map=14/$5/$6)
```

`@testModuleCity = réussi si les deux blocs affichent des données`
`@moduleCity = undefined`
`@moduleCityPurified = undefined`

`endif`

`@moduleCity = @INPUT : V6_MODULE_CITY`

1. [Nouvelle recherche](V6_MODULE_CITY)
2. [Retour au module](V6_MODULE)

## V6_MODULE_CP

`if !@moduleCP`

Quel est votre code postal ?

`endif`

`if @moduleCP`

`@moduleCPPurified = calc(@moduleCP.trim())`

### Lieux trouvés

```readcsv https://raw.githubusercontent.com/Codeurfou-sys/chatbot_civique/refs/heads/main/lieux_dits_test.csv
condition: $1.startsWith("`@moduleCPPurified`")
maxResults: 3

$i. **$2 — $1**  
$3
```

### Centre FRATE correspondant

```readcsv https://raw.githubusercontent.com/Codeurfou-sys/chatbot_civique/refs/heads/main/centres_frate.csv
condition: $3.startsWith("`@moduleCPPurified`")
maxResults: 3

### Centre de $2

Région : $4  
[Inscription](link:$7)  
[Carte](https://www.openstreetmap.org/?#map=14/$5/$6)
```

`@testModuleCP = réussi si les deux blocs affichent des données`
`@moduleCP = undefined`
`@moduleCPPurified = undefined`

`endif`

`@moduleCP = @INPUT : V6_MODULE_CP`

1. [Nouvelle recherche](V6_MODULE_CP)
2. [Retour au module](V6_MODULE)

## V6_MODULE_GEO

Latitude : **`@LATITUDE`**  
Longitude : **`@LONGITUDE`**

`if @LATITUDE != undefined && @LONGITUDE != undefined`

```readcsv https://raw.githubusercontent.com/Codeurfou-sys/chatbot_civique/refs/heads/main/centres_frate.csv
condition: $5>`@LATITUDE`-4 && $5<`@LATITUDE`+4 && $6>`@LONGITUDE`-4 && $6<`@LONGITUDE`+4
maxResults: 3

### $i. Centre de $2

Code postal : $3  
Région : $4  
[Inscription](link:$7)  
[Carte](https://www.openstreetmap.org/?#map=14/$5/$6)
```

`@testModuleGeo = réussi si trois centres apparaissent`

`endif`

`if @LATITUDE == undefined || @LONGITUDE == undefined`

La géolocalisation n’a pas été obtenue.

`endif`

1. [Retour au module](V6_MODULE)

---

## V6_REPORT

### Bilan du laboratoire V6

| Test | Résultat |
|---|---|
| Recherche de ville BAN | `@testCity` |
| Recherche d’adresse | `@testAddress` |
| Recherche par code postal | `@testCP` |
| Centre par ville | `@testCentreCity` |
| Centre par code postal | `@testCentreCP` |
| Liens cartographiques | `@testMap` |
| Filtre géographique | `@testGeoFilter` |
| Module par ville | `@testModuleCity` |
| Module par code postal | `@testModuleCP` |
| Module par géolocalisation | `@testModuleGeo` |

### Points à observer

1. Les variables doivent apparaître entre backticks dans les formules `readcsv`.
2. Les recherches texte utilisent le modèle officiel :
   `$2.toLowerCase().includes("`@variable`".toLowerCase())`.
3. Les recherches de codes utilisent :
   `$1.startsWith("`@variable`")`.
4. Les liens cartographiques sont construits directement avec les colonnes du CSV.
5. Les deux variantes du filtre géographique permettent de déterminer la syntaxe numérique acceptée.

1. [Retour au menu](V6_MENU)
