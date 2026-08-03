---
titre: Laboratoire ChatMD V7 — modèle définitif du module 07
variablesDynamiques: true
geolocation: true
plugins: readcsv
obfuscate: false
preload:
  - https://raw.githubusercontent.com/Codeurfou-sys/chatbot_civique/refs/heads/main/lieux_dits_test.csv
  - https://raw.githubusercontent.com/Codeurfou-sys/chatbot_civique/refs/heads/main/centres_frate.csv
---

# Laboratoire ChatMD V7

Ce laboratoire reprend strictement le modèle fonctionnel du chatbot officiel de recherche d’établissements.

1. [Commencer](V7_MENU)

## V7_MENU

### Choisissez un test

1. [Rechercher un lieu par ville](V7_VILLE)
2. [Rechercher un lieu par adresse](V7_ADRESSE)
3. [Rechercher un lieu par code postal](V7_CP)
4. [Rechercher un centre FRATE par ville](V7_CENTRE_VILLE)
5. [Rechercher un centre FRATE par code postal](V7_CENTRE_CP)
6. [Afficher trois centres proches](V7_GEO)
7. [Tester le parcours complet du module 07](V7_MODULE)
8. [Afficher le bilan](V7_BILAN)

---

## V7_VILLE

`if !@ville`

D’accord, donne-moi le nom d’une ville.

Exemples : Strasbourg, Dijon, Colmar, Lyon.

`endif`

`if @ville`

`@villePurified = calc(@ville.trim())`

### Résultats

```readcsv https://raw.githubusercontent.com/Codeurfou-sys/chatbot_civique/refs/heads/main/lieux_dits_test.csv
condition: $2.toLowerCase().includes("`@villePurified`".toLowerCase())
maxResults: 5

### $i. $2

Code postal : **$1**  
Adresse : $3  
Latitude : $4  
Longitude : $5
```

`@testVille = réussi`
`@ville = undefined`
`@villePurified = undefined`

`endif`

`@ville = @INPUT : V7_VILLE`

1. [Nouvelle recherche par ville](V7_VILLE)
2. [Retour au menu](V7_MENU)

---

## V7_ADRESSE

`if !@adresse`

Donne-moi un mot présent dans une adresse.

Exemples : Jura, Kléber, Darcy, République.

`endif`

`if @adresse`

`@adressePurified = calc(@adresse.trim())`

### Résultats

```readcsv https://raw.githubusercontent.com/Codeurfou-sys/chatbot_civique/refs/heads/main/lieux_dits_test.csv
condition: $3.toLowerCase().includes("`@adressePurified`".toLowerCase())
maxResults: 5

### $i. $3

Ville : **$2**  
Code postal : $1  
Latitude : $4  
Longitude : $5
```

`@testAdresse = réussi`
`@adresse = undefined`
`@adressePurified = undefined`

`endif`

`@adresse = @INPUT : V7_ADRESSE`

1. [Nouvelle recherche par adresse](V7_ADRESSE)
2. [Retour au menu](V7_MENU)

---

## V7_CP

`if !@codePostal`

Donne-moi un code postal à cinq chiffres.

Exemples : 67000, 21000, 63000.

`endif`

`if @codePostal`

`@codePostalPurified = calc(@codePostal.trim())`

### Résultats BAN

```readcsv https://raw.githubusercontent.com/Codeurfou-sys/chatbot_civique/refs/heads/main/lieux_dits_test.csv
condition: $1.startsWith("`@codePostalPurified`")
sort: $2 asc alph
maxResults: 5

### $i. $2 — $1

Adresse : $3  
Latitude : $4  
Longitude : $5
```

`@testCP = réussi`
`@codePostal = undefined`
`@codePostalPurified = undefined`

`endif`

`@codePostal = @INPUT : V7_CP`

1. [Nouvelle recherche par code postal](V7_CP)
2. [Retour au menu](V7_MENU)

---

## V7_CENTRE_VILLE

`if !@centreVille`

Dans quelle ville recherchez-vous un centre FRATE ?

`endif`

`if @centreVille`

`@centreVillePurified = calc(@centreVille.trim())`

### Centre trouvé

```readcsv https://raw.githubusercontent.com/Codeurfou-sys/chatbot_civique/refs/heads/main/centres_frate.csv
condition: $2.toLowerCase().includes("`@centreVillePurified`".toLowerCase())
maxResults: 5

### Centre de $2

Code postal : **$3**  
Région : $4  
Coordonnées : $5, $6  

[Ouvrir l’inscription](link:$7)  
[Voir sur OpenStreetMap](https://www.openstreetmap.org/?#map=14/$5/$6)
```

`@testCentreVille = réussi`
`@centreVille = undefined`
`@centreVillePurified = undefined`

`endif`

`@centreVille = @INPUT : V7_CENTRE_VILLE`

1. [Nouvelle recherche par ville](V7_CENTRE_VILLE)
2. [Retour au menu](V7_MENU)

---

## V7_CENTRE_CP

`if !@centreCodePostal`

Quel est le code postal du centre recherché ?

`endif`

`if @centreCodePostal`

`@centreCodePostalPurified = calc(@centreCodePostal.trim())`

### Centre trouvé

```readcsv https://raw.githubusercontent.com/Codeurfou-sys/chatbot_civique/refs/heads/main/centres_frate.csv
condition: $3.startsWith("`@centreCodePostalPurified`")
maxResults: 5

### Centre de $2

Code postal : **$3**  
Région : $4  
Coordonnées : $5, $6  

[Ouvrir l’inscription](link:$7)  
[Voir sur OpenStreetMap](https://www.openstreetmap.org/?#map=14/$5/$6)
```

`@testCentreCP = réussi`
`@centreCodePostal = undefined`
`@centreCodePostalPurified = undefined`

`endif`

`@centreCodePostal = @INPUT : V7_CENTRE_CP`

1. [Nouvelle recherche par code postal](V7_CENTRE_CP)
2. [Retour au menu](V7_MENU)

---

## V7_GEO

### Trois centres proches de votre position

Latitude : **`@LATITUDE`**  
Longitude : **`@LONGITUDE`**  
Précision : **`@POSITION_ACCURACY`** mètres

`if @LATITUDE != undefined && @LONGITUDE != undefined`

```readcsv https://raw.githubusercontent.com/Codeurfou-sys/chatbot_civique/refs/heads/main/centres_frate.csv
condition: Math.abs($5-`@LATITUDE`)<4 && Math.abs($6-`@LONGITUDE`)<4
maxResults: 3

### $i. Centre de $2

Code postal : $3  
Région : $4  
Coordonnées : $5, $6  

[Ouvrir l’inscription](link:$7)  
[Voir sur OpenStreetMap](https://www.openstreetmap.org/?#map=14/$5/$6)
```

`@testGeo = réussi`

`endif`

`if @LATITUDE == undefined || @LONGITUDE == undefined`

La géolocalisation n’est pas disponible. Autorisez-la dans le navigateur, puis rechargez la page.

`@testGeo = indisponible`

`endif`

1. [Retour au menu](V7_MENU)

---

## V7_MODULE

# Passer mon examen

Comment souhaitez-vous effectuer votre recherche ?

1. [Par ville](V7_MODULE_VILLE)
2. [Par code postal](V7_MODULE_CP)
3. [Avec ma géolocalisation](V7_MODULE_GEO)
4. [Retour au menu du laboratoire](V7_MENU)

## V7_MODULE_VILLE

`if !@moduleVille`

Dans quelle ville souhaitez-vous passer l’examen ?

`endif`

`if @moduleVille`

`@moduleVillePurified = calc(@moduleVille.trim())`

### Localisation reconnue

```readcsv https://raw.githubusercontent.com/Codeurfou-sys/chatbot_civique/refs/heads/main/lieux_dits_test.csv
condition: $2.toLowerCase().includes("`@moduleVillePurified`".toLowerCase())
maxResults: 3

$i. **$2 — $1**  
$3
```

### Centre FRATE correspondant

```readcsv https://raw.githubusercontent.com/Codeurfou-sys/chatbot_civique/refs/heads/main/centres_frate.csv
condition: $2.toLowerCase().includes("`@moduleVillePurified`".toLowerCase())
maxResults: 3

### Centre de $2

Code postal : $3  
Région : $4  

[Ouvrir l’inscription](link:$7)  
[Voir sur OpenStreetMap](https://www.openstreetmap.org/?#map=14/$5/$6)
```

`@testModuleVille = réussi`
`@moduleVille = undefined`
`@moduleVillePurified = undefined`

`endif`

`@moduleVille = @INPUT : V7_MODULE_VILLE`

1. [Nouvelle recherche](V7_MODULE_VILLE)
2. [Retour au module](V7_MODULE)

## V7_MODULE_CP

`if !@moduleCodePostal`

Quel est votre code postal ?

`endif`

`if @moduleCodePostal`

`@moduleCodePostalPurified = calc(@moduleCodePostal.trim())`

### Localisation reconnue

```readcsv https://raw.githubusercontent.com/Codeurfou-sys/chatbot_civique/refs/heads/main/lieux_dits_test.csv
condition: $1.startsWith("`@moduleCodePostalPurified`")
maxResults: 3

$i. **$2 — $1**  
$3
```

### Centre FRATE correspondant

```readcsv https://raw.githubusercontent.com/Codeurfou-sys/chatbot_civique/refs/heads/main/centres_frate.csv
condition: $3.startsWith("`@moduleCodePostalPurified`")
maxResults: 3

### Centre de $2

Code postal : $3  
Région : $4  

[Ouvrir l’inscription](link:$7)  
[Voir sur OpenStreetMap](https://www.openstreetmap.org/?#map=14/$5/$6)
```

`@testModuleCP = réussi`
`@moduleCodePostal = undefined`
`@moduleCodePostalPurified = undefined`

`endif`

`@moduleCodePostal = @INPUT : V7_MODULE_CP`

1. [Nouvelle recherche](V7_MODULE_CP)
2. [Retour au module](V7_MODULE)

## V7_MODULE_GEO

### Centres proposés selon votre position

Latitude : **`@LATITUDE`**  
Longitude : **`@LONGITUDE`**

`if @LATITUDE != undefined && @LONGITUDE != undefined`

```readcsv https://raw.githubusercontent.com/Codeurfou-sys/chatbot_civique/refs/heads/main/centres_frate.csv
condition: Math.abs($5-`@LATITUDE`)<4 && Math.abs($6-`@LONGITUDE`)<4
maxResults: 3

### $i. Centre de $2

Code postal : $3  
Région : $4  

[Ouvrir l’inscription](link:$7)  
[Voir sur OpenStreetMap](https://www.openstreetmap.org/?#map=14/$5/$6)
```

`@testModuleGeo = réussi`

`endif`

`if @LATITUDE == undefined || @LONGITUDE == undefined`

La géolocalisation n’a pas pu être utilisée.

`endif`

1. [Retour au module](V7_MODULE)

---

## V7_BILAN

# Bilan du laboratoire V7

| Fonction | Résultat |
|---|---|
| Recherche BAN par ville | `@testVille` |
| Recherche BAN par adresse | `@testAdresse` |
| Recherche BAN par code postal | `@testCP` |
| Centre FRATE par ville | `@testCentreVille` |
| Centre FRATE par code postal | `@testCentreCP` |
| Géolocalisation | `@testGeo` |
| Module 07 par ville | `@testModuleVille` |
| Module 07 par code postal | `@testModuleCP` |
| Module 07 par géolocalisation | `@testModuleGeo` |

### Résultat attendu

La version V7 doit confirmer définitivement :

- la recherche par code postal ;
- la recherche par ville ;
- la recherche par adresse ;
- la récupération des centres FRATE ;
- les liens d’inscription et de cartographie ;
- l’exploitation de la géolocalisation ;
- le fonctionnement du futur module 07 avec la syntaxe officielle ChatMD.

1. [Retour au menu](V7_MENU)
