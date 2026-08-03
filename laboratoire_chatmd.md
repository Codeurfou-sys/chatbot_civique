---
titre: Laboratoire ChatMD V5 — readcsv, BAN et centres FRATE
variablesDynamiques: true
geolocation: true
plugins: readcsv
obfuscate: false
gestionGrosMots: false
rechercheContenu: false

# IMPORTANT
# Remplacez les deux URL ci-dessous dans tout le fichier avant le test :
# URL_BAN_RAW = URL Raw GitHub du CSV BAN réduit
# URL_CENTRES_RAW = URL Raw GitHub du CSV des centres FRATE
#
# Exemple :
# https://raw.githubusercontent.com/UTILISATEUR/DEPOT/main/data/ban_reduit.csv
# https://raw.githubusercontent.com/UTILISATEUR/DEPOT/main/data/centres_frate.csv

preload:
  - URL_BAN_RAW
  - URL_CENTRES_RAW
---

# Laboratoire ChatMD V5

Ce laboratoire vérifie si le plugin officiel `readcsv` peut alimenter le module **Passer mon examen** à partir de données externes.

1. [Commencer le laboratoire](V5_MENU)

## V5_MENU

### Tests disponibles

1. [Test 1 — Vérifier le chargement du CSV BAN](V5_BAN_LOAD)
2. [Test 2 — Rechercher une commune ou un lieu-dit](V5_BAN_INPUT)
3. [Test 3 — Rechercher un code postal](V5_CP_INPUT)
4. [Test 4 — Vérifier le CSV des centres FRATE](V5_CENTRES_LOAD)
5. [Test 5 — Afficher des centres autour d’une position](V5_GEO)
6. [Test 6 — Tentative de classement des trois centres](V5_NEAREST)
7. [Test 7 — Parcours complet simulé](V5_FULL_INPUT)
8. [Afficher le bilan](V5_REPORT)

---

## V5_BAN_LOAD

### Test 1 — Chargement du CSV BAN

Le bloc suivant doit afficher au maximum trois lignes du fichier BAN.

```readcsv URL_BAN_RAW
maxResults: 3

$i. **$5** — code postal : **$3**
Coordonnées : latitude **$11**, longitude **$10**
Lieu-dit : $2
```

`@testBanLoad = à vérifier`

1. [Retour au menu](V5_MENU)

---

## V5_BAN_INPUT

### Test 2 — Recherche d’une commune ou d’un lieu-dit

Écrivez une commune ou un lieu-dit dans la zone principale de ChatMD.

Exemples :

- Strasbourg
- Bourges
- Clermont-Ferrand
- Oberlin

!Next: V5_BAN_RESULTS

1. [Retour au menu](V5_MENU)

## V5_BAN_RESULTS

`@rechercheBan = calc(@INPUT.trim().toLowerCase())`
`@sujetBan = calc(mainTopic(@rechercheBan))`

Recherche normalisée : **`@rechercheBan`**

Sujet principal : **`@sujetBan`**

### Résultats trouvés

```readcsv URL_BAN_RAW
condition: $2.toLowerCase().includes(mainTopic("@INPUT").toLowerCase()) || $5.toLowerCase().includes(mainTopic("@INPUT").toLowerCase())
maxResults: 5

### $i. $5

- Lieu-dit : $2
- Code postal : $3
- Commune : $5
- Longitude : $10
- Latitude : $11
```

`@testBanSearch = à vérifier`

1. [Faire une autre recherche](V5_BAN_INPUT)
2. [Retour au menu](V5_MENU)

---

## V5_CP_INPUT

### Test 3 — Recherche par code postal

Saisissez exactement un code postal à cinq chiffres.

!Next: V5_CP_RESULTS

1. [Retour au menu](V5_MENU)

## V5_CP_RESULTS

`@codePostalBan = calc(@INPUT.trim())`

Code postal recherché : **`@codePostalBan`**

```readcsv URL_BAN_RAW
condition: $3 == "@codePostalBan"
sort: $5 asc alph
maxResults: 5

$i. **$5** — $3  
Lieu-dit : $2  
Coordonnées : $11, $10
```

`@testBanCP = à vérifier`

1. [Rechercher un autre code postal](V5_CP_INPUT)
2. [Retour au menu](V5_MENU)

---

## V5_CENTRES_LOAD

### Test 4 — Chargement du CSV des centres FRATE

Structure attendue du fichier `centres_frate.csv` :

```csv
centre_id;ville;departement;region;latitude;longitude;lien_inscription
STRASBOURG;Strasbourg;67;Grand Est;48.5734;7.7521;https://...
DIJON;Dijon;21;Bourgogne;47.3220;5.0415;https://...
CLERMONT_FERRAND;Clermont-Ferrand;63;Auvergne;45.7772;3.0870;https://...
```

Lecture du fichier :

```readcsv URL_CENTRES_RAW
sort: $2 asc alph
maxResults: 5

$i. **$2 ($3)**  
Région : $4  
Coordonnées : $5, $6  
[Inscription](link:$7)
```

`@testCentresLoad = à vérifier`

1. [Retour au menu](V5_MENU)

---

## V5_GEO

### Test 5 — Centres autour de la géolocalisation

Latitude de l’utilisateur : **`@LATITUDE`**

Longitude de l’utilisateur : **`@LONGITUDE`**

Précision : **`@POSITION_ACCURACY`** mètres

`if @LATITUDE != undefined && @LONGITUDE != undefined`

✅ La géolocalisation est disponible.

Le filtre ci-dessous conserve les centres situés dans un carré géographique d’environ deux degrés autour de la position.  
Il s’agit d’un **préfiltrage**, pas encore d’un classement exact par distance.

```readcsv URL_CENTRES_RAW
condition: Math.abs($5-@LATITUDE)<2 && Math.abs($6-@LONGITUDE)<2
maxResults: 10

$i. **$2 ($3)**  
Région : $4  
Latitude : $5 — Longitude : $6  
[Inscription](link:$7)
```

`@testGeoCentres = à vérifier`

`endif`

`if @LATITUDE == undefined || @LONGITUDE == undefined`

La géolocalisation n’est pas disponible. Autorisez-la dans le navigateur puis rechargez la page.

`@testGeoCentres = géolocalisation indisponible`

`endif`

1. [Retour au menu](V5_MENU)

---

## V5_NEAREST

### Test 6 — Tentative de classement des trois centres les plus proches

ChatMD documente le tri sur une **colonne** :

```text
sort: $5 asc num
```

La documentation ne confirme pas officiellement le tri sur une formule calculée.  
Les trois variantes suivantes permettent de déterminer ce que la version actuelle accepte.

`if @LATITUDE != undefined && @LONGITUDE != undefined`

### Variante A — Préfiltrage puis ordre du CSV

```readcsv URL_CENTRES_RAW
condition: Math.abs($5-@LATITUDE)<4 && Math.abs($6-@LONGITUDE)<4
maxResults: 3

$i. **$2** — $4  
Coordonnées : $5, $6
```

### Variante B — Tri expérimental par distance au carré

```readcsv URL_CENTRES_RAW
condition: Math.abs($5-@LATITUDE)<4 && Math.abs($6-@LONGITUDE)<4
sort: calc((($5-@LATITUDE)*($5-@LATITUDE))+(($6-@LONGITUDE)*($6-@LONGITUDE))) asc num
maxResults: 3

$i. **$2** — $4  
Coordonnées : $5, $6
```

### Variante C — Affichage expérimental de la distance au carré

```readcsv URL_CENTRES_RAW
condition: Math.abs($5-@LATITUDE)<4 && Math.abs($6-@LONGITUDE)<4
maxResults: 3

$i. **$2** — $4  
Distance expérimentale : calc((($5-@LATITUDE)*($5-@LATITUDE))+(($6-@LONGITUDE)*($6-@LONGITUDE)))
```

`@testNearest = à vérifier`

`endif`

`if @LATITUDE == undefined || @LONGITUDE == undefined`

Impossible de réaliser ce test sans géolocalisation.

`endif`

1. [Retour au menu](V5_MENU)

---

## V5_FULL_INPUT

### Test 7 — Parcours complet simulé

Saisissez une commune, un lieu-dit ou un code postal.

!Next: V5_FULL_BAN

1. [Retour au menu](V5_MENU)

## V5_FULL_BAN

`@adresseUtilisateur = calc(@INPUT.trim().toLowerCase())`
`@adresseSujet = calc(mainTopic(@adresseUtilisateur))`

Votre recherche : **`@adresseUtilisateur`**

### Étape 1 — Correspondances BAN

```readcsv URL_BAN_RAW
condition: $2.toLowerCase().includes(mainTopic("@INPUT").toLowerCase()) || $3 == "@adresseUtilisateur" || $5.toLowerCase().includes(mainTopic("@INPUT").toLowerCase())
maxResults: 3

$i. **$5 — $3**  
Lieu-dit : $2  
Coordonnées : $11, $10
```

### Étape 2 — Trois centres selon la géolocalisation du navigateur

`if @LATITUDE != undefined && @LONGITUDE != undefined`

```readcsv URL_CENTRES_RAW
condition: Math.abs($5-@LATITUDE)<4 && Math.abs($6-@LONGITUDE)<4
maxResults: 3

### $i. $2 ($3)

Région : $4  
Coordonnées : $5, $6  
[Ouvrir l’inscription](link:$7)
```

`endif`

`if @LATITUDE == undefined || @LONGITUDE == undefined`

La recherche BAN peut fonctionner, mais le classement des centres nécessite la géolocalisation.

`endif`

`@testFull = à vérifier`

1. [Nouvelle recherche](V5_FULL_INPUT)
2. [Retour au menu](V5_MENU)

---

## V5_REPORT

### Bilan du laboratoire V5

| Fonction | Résultat |
|---|---|
| Chargement BAN | `@testBanLoad` |
| Recherche par commune | `@testBanSearch` |
| Recherche par code postal | `@testBanCP` |
| Chargement centres FRATE | `@testCentresLoad` |
| Préfiltrage géographique | `@testGeoCentres` |
| Classement expérimental | `@testNearest` |
| Parcours complet | `@testFull` |

### Critères de décision

- Si le test 1 affiche des lignes, `readcsv` charge correctement le CSV BAN.
- Si les tests 2 et 3 filtrent les lignes, les variables ChatMD sont utilisables dans `condition:`.
- Si le test 4 affiche les centres, le second CSV est opérationnel.
- Si la variante B du test 6 fonctionne, ChatMD peut probablement calculer et trier les centres à la volée.
- Si seule la variante A fonctionne, Python devra pré-calculer ou fournir les centres déjà classés.
- Le fichier BAN national de grande taille ne devra être utilisé qu’après validation sur un fichier réduit.

1. [Réinitialiser les indicateurs](V5_RESET)
2. [Retour au menu](V5_MENU)

## V5_RESET

`@testBanLoad = undefined`
`@testBanSearch = undefined`
`@testBanCP = undefined`
`@testCentresLoad = undefined`
`@testGeoCentres = undefined`
`@testNearest = undefined`
`@testFull = undefined`

Les indicateurs ont été réinitialisés.

1. [Retour au menu](V5_MENU)
