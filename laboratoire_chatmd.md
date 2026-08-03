---
titre: Laboratoire ChatMD V4
variablesDynamiques: true
geolocation: true
obfuscate: false
gestionGrosMots: false
rechercheContenu: false
---

# Laboratoire ChatMD V4

Ce laboratoire vérifie les fonctions encore décisives pour le module **Passer mon examen** et la rubrique **Pose-moi une question**.

1. [Commencer les tests](MENU)

## MENU

### Tests prioritaires

1. [Test 1 — Détection avec includes()](T1_INPUT)
2. [Test 2 — startsWith() et endsWith()](T2_INPUT)
3. [Test 3 — mainTopic()](T3_INPUT)
4. [Test 4 — URL dynamique vers la BAN](T4_INPUT)
5. [Test 5 — Géolocalisation](T5_GEO)
6. [Test 6 — Paramètre d’URL @GET](T6_GET)
7. [Test 7 — Navigation conditionnelle](T7_CHOICE)
8. [Test 8 — readcsv expérimental](T8_CSV)
9. [Test 9 — Mini-parcours Module 07](T9_START)
10. [Afficher le bilan](REPORT)

## T1_INPUT

### Test 1 — Détection avec `.includes()`

Saisissez exactement l’une des phrases suivantes :

- prochaines dates à Strasbourg
- centre proche de Dijon
- prix de l’examen

!Next: T1_RESULT

1. [Retour au menu](MENU)

## T1_RESULT

`@phrase = calc(@INPUT.trim().toLowerCase())`
`@contientDate = calc(@phrase.includes("date"))`
`@contientStrasbourg = calc(@phrase.includes("strasbourg"))`
`@contientCentre = calc(@phrase.includes("centre"))`
`@contientProche = calc(@phrase.includes("proche"))`
`@contientPrix = calc(@phrase.includes("prix"))`

Phrase normalisée : **`@phrase`**

- contient « date » : **`@contientDate`**
- contient « strasbourg » : **`@contientStrasbourg`**
- contient « centre » : **`@contientCentre`**
- contient « proche » : **`@contientProche`**
- contient « prix » : **`@contientPrix`**

`if @contientDate == true && @contientStrasbourg == true`

✅ Intention détectée : **prochaines dates à Strasbourg**.

`@intention = QL_DATE_VILLE`
`@villeDetectee = Strasbourg`
`@testIncludes = réussi`

`endif`

`if @contientCentre == true && @contientProche == true`

✅ Intention détectée : **centre le plus proche**.

`@intention = QL_CENTRE_PROCHE`
`@testIncludes = réussi`

`endif`

`if @contientPrix == true`

✅ Intention détectée : **prix de l’examen**.

`@intention = QL_PRIX`
`@testIncludes = réussi`

`endif`

Intention produite : **`@intention`**

1. [Recommencer](T1_INPUT)
2. [Retour au menu](MENU)

## T2_INPUT

### Test 2 — `startsWith()` et `endsWith()`

Saisissez exactement :

**je cherche une session à Strasbourg**

!Next: T2_RESULT

1. [Retour au menu](MENU)

## T2_RESULT

`@phrase2 = calc(@INPUT.trim().toLowerCase())`
`@commenceJe = calc(@phrase2.startsWith("je"))`
`@finitStrasbourg = calc(@phrase2.endsWith("strasbourg"))`

Phrase : **`@phrase2`**

- commence par « je » : **`@commenceJe`**
- finit par « strasbourg » : **`@finitStrasbourg`**

`if @commenceJe == true`

✅ `startsWith()` fonctionne.

`@testStartsWith = réussi`

`endif`

`if @finitStrasbourg == true`

✅ `endsWith()` fonctionne.

`@testEndsWith = réussi`

`endif`

1. [Retour au menu](MENU)

## T3_INPUT

### Test 3 — `mainTopic()`

Saisissez une phrase courte, par exemple :

**Je voudrais connaître les prochaines dates d’examen à Strasbourg**

!Next: T3_RESULT

1. [Retour au menu](MENU)

## T3_RESULT

`@phraseSujet = calc(@INPUT.trim())`
`@sujetPrincipal = calc(mainTopic(@phraseSujet))`

Phrase analysée : **`@phraseSujet`**

Sujet principal extrait : **`@sujetPrincipal`**

`if @sujetPrincipal != undefined && @sujetPrincipal.trim().length()>0`

✅ `mainTopic()` a renvoyé une valeur.

`@testMainTopic = réussi`

`endif`

`if !@sujetPrincipal || @sujetPrincipal.trim().length()==0`

❌ Aucun sujet principal n’a été extrait.

`@testMainTopic = échoué`

`endif`

1. [Retour au menu](MENU)

## T4_INPUT

### Test 4 — URL dynamique vers la BAN

Saisissez une commune ou un code postal dans le champ, puis appuyez sur **Entrée**.

<label for="localisation">Localisation :</label>

<input type="text" id="localisation" name="localisation" value="`@localisation`" placeholder="Exemple : Strasbourg ou 67000" />

`if @localisation != undefined && @localisation.trim().length()>0`

`@localisationEncodee = calc(encodeURI(@localisation.trim()))`

Valeur saisie : **`@localisation`**

Valeur encodée : **`@localisationEncodee`**

### Variante A — lien Markdown dynamique

[Tester la BAN — variante A](https://api-adresse.data.gouv.fr/search/?q=`@localisationEncodee`&limit=3)

### Variante B — bouton externe ChatMD

1. [Tester la BAN — variante B](link:https://api-adresse.data.gouv.fr/search/?q=`@localisationEncodee`&limit=3)

### Variante C — lien HTML

<a href="https://api-adresse.data.gouv.fr/search/?q=`@localisationEncodee`&limit=3" target="_blank" rel="noopener">Tester la BAN — variante C</a>

`@testUrlDynamique = à vérifier`

`endif`

`if !@localisation || @localisation.trim().length()==0`

Saisissez d’abord une commune ou un code postal.

`endif`

1. [Retour au menu](MENU)

## T5_GEO

### Test 5 — Géolocalisation

Le YAML contient :

- `variablesDynamiques: true`
- `geolocation: true`

Latitude : **`@LATITUDE`**

Longitude : **`@LONGITUDE`**

Précision : **`@POSITION_ACCURACY`** mètres

`if @LATITUDE != undefined && @LONGITUDE != undefined`

✅ La géolocalisation a fourni des coordonnées.

`@testGeo = réussi`

`endif`

`if @LATITUDE == undefined || @LONGITUDE == undefined`

⚠️ La géolocalisation n’a pas fourni de coordonnées. Vérifiez l’autorisation du navigateur, puis rechargez complètement la page.

`@testGeo = échoué ou refusé`

`endif`

`if @LATITUDE>41 && @LATITUDE<52 && @LONGITUDE>-6 && @LONGITUDE<10`

La position semble se trouver en France métropolitaine.

`endif`

`if Math.abs(@LATITUDE-48.5734)<0.5 && Math.abs(@LONGITUDE-7.7521)<0.5`

La position semble proche de Strasbourg.

`endif`

1. [Recharger ce test](T5_GEO)
2. [Retour au menu](MENU)

## T6_GET

### Test 6 — Paramètre d’URL `@GET`

Pour tester, ajoutez à l’URL du laboratoire :

```text
?departement=67
```

Si l’URL contient déjà un paramètre, ajoutez :

```text
&departement=67
```

Valeur de `@GETdepartement` : **`@GETdepartement`**

`if @GETdepartement == "67"`

✅ Le paramètre `departement=67` est reconnu.

`@testGET = réussi`

`endif`

`if @GETdepartement == undefined`

Aucun paramètre `departement` n’est actuellement présent dans l’URL.

`@testGET = non testé`

`endif`

1. [Retour au menu](MENU)

## T7_CHOICE

### Test 7 — Navigation conditionnelle

Choisissez une région.

1. [Grand Est @regionTest=GRAND_EST](T7_ROUTE)
2. [Bourgogne @regionTest=BOURGOGNE](T7_ROUTE)
3. [Auvergne @regionTest=AUVERGNE](T7_ROUTE)
4. [Retour au menu](MENU)

## T7_ROUTE

Région mémorisée : **`@regionTest`**

`if @regionTest == "GRAND_EST"`

✅ La condition Grand Est est satisfaite.

1. [Ouvrir l’écran Strasbourg](T7_STRASBOURG)

`endif`

`if @regionTest == "BOURGOGNE"`

✅ La condition Bourgogne est satisfaite.

1. [Ouvrir l’écran Dijon](T7_DIJON)

`endif`

`if @regionTest == "AUVERGNE"`

✅ La condition Auvergne est satisfaite.

1. [Ouvrir l’écran Clermont-Ferrand](T7_CLERMONT)

`endif`

`@testNavigationConditionnelle = réussi`

1. [Retour au menu](MENU)

## T7_STRASBOURG

### Strasbourg

La navigation conditionnelle vers Strasbourg fonctionne.

1. [Retour au menu](MENU)

## T7_DIJON

### Dijon

La navigation conditionnelle vers Dijon fonctionne.

1. [Retour au menu](MENU)

## T7_CLERMONT

### Clermont-Ferrand

La navigation conditionnelle vers Clermont-Ferrand fonctionne.

1. [Retour au menu](MENU)

## T8_CSV

### Test 8 — Plugin `readcsv` expérimental

Ce laboratoire n’invente pas de syntaxe non vérifiée.

Le test préparatoire consiste à publier sur GitHub un fichier nommé :

```text
laboratoire_centres.csv
```

avec ce contenu :

```csv
code_postal,ville,ecran,region
67000,Strasbourg,T8_STRASBOURG,Grand Est
21000,Dijon,T8_DIJON,Bourgogne
63000,Clermont-Ferrand,T8_CLERMONT,Auvergne
```

Objectifs du futur test `readcsv` :

1. charger le CSV depuis son URL Raw ;
2. rechercher une ligne à partir de `@localisation` ;
3. afficher la ville trouvée ;
4. récupérer l’identifiant d’écran ;
5. diriger l’utilisateur vers cet écran.

Statut actuel : **syntaxe d’appel à confirmer depuis un exemple ChatMD officiel opérationnel**.

`@testCSV = en attente de syntaxe officielle`

1. [Voir les écrans de contrôle](T8_CONTROL)
2. [Retour au menu](MENU)

## T8_CONTROL

1. [Écran Strasbourg](T8_STRASBOURG)
2. [Écran Dijon](T8_DIJON)
3. [Écran Clermont-Ferrand](T8_CLERMONT)
4. [Retour au menu](MENU)

## T8_STRASBOURG

Résultat CSV attendu : **Strasbourg — 67000 — Grand Est**

1. [Retour au menu](MENU)

## T8_DIJON

Résultat CSV attendu : **Dijon — 21000 — Bourgogne**

1. [Retour au menu](MENU)

## T8_CLERMONT

Résultat CSV attendu : **Clermont-Ferrand — 63000 — Auvergne**

1. [Retour au menu](MENU)

## T9_START

### Test 9 — Mini-parcours Module 07

Ce test reproduit un parcours simplifié du futur module.

<label for="typeExamenTest">Type d’examen :</label>

<select name="typeExamenTest" id="typeExamenTest" data-selected="`@typeExamenTest`">
  <option value="">À sélectionner</option>
  <option value="CR">Carte de résident</option>
  <option value="CSP">Carte de séjour pluriannuelle</option>
  <option value="NAT">Naturalisation</option>
</select>

<label for="villeTest">Ville ou code postal :</label>

<input type="text" id="villeTest" name="villeTest" value="`@villeTest`" placeholder="Exemple : Strasbourg ou 67000" />

`if @typeExamenTest != undefined && @typeExamenTest != "" && @villeTest != undefined && @villeTest.trim().length()>0`

`@villeTestNorm = calc(@villeTest.trim().toLowerCase())`
`@estStrasbourg = calc(@villeTestNorm.includes("strasbourg") || @villeTestNorm=="67000")`
`@estDijon = calc(@villeTestNorm.includes("dijon") || @villeTestNorm=="21000")`

1. [Analyser ma demande](T9_ROUTE)

`endif`

`if @typeExamenTest == undefined || @typeExamenTest == "" || @villeTest == undefined || @villeTest.trim().length()==0`

Sélectionnez un examen et saisissez une ville ou un code postal.

`endif`

1. [Retour au menu](MENU)

## T9_ROUTE

Type d’examen : **`@typeExamenTest`**

Localisation : **`@villeTest`**

`if @estStrasbourg == true`

✅ Strasbourg a été reconnu.

1. [Afficher les sessions de Strasbourg](T9_STRASBOURG)

`endif`

`if @estDijon == true`

✅ Dijon a été reconnu.

1. [Afficher les sessions de Dijon](T9_DIJON)

`endif`

`if @estStrasbourg != true && @estDijon != true`

La localisation n’est pas encore présente dans ce prototype.

1. [Modifier la recherche](T9_START)

`endif`

1. [Retour au menu](MENU)

## T9_STRASBOURG

### Sessions de Strasbourg

Type d’examen sélectionné : **`@typeExamenTest`**

Exemples de dates :

- 9 septembre 2026
- 30 septembre 2026
- 22 octobre 2026

1. [Ouvrir le formulaire d’inscription](link:https://forms.office.com/)
2. [Nouvelle recherche](T9_START)
3. [Retour au menu](MENU)

## T9_DIJON

### Sessions de Dijon

Type d’examen sélectionné : **`@typeExamenTest`**

Exemples de dates :

- 10 août 2026
- 7 septembre 2026
- 12 octobre 2026

1. [Ouvrir le formulaire d’inscription](link:https://forms.office.com/)
2. [Nouvelle recherche](T9_START)
3. [Retour au menu](MENU)

## REPORT

### Bilan de compatibilité

| Fonction | Résultat |
|---|---|
| `.includes()` | `@testIncludes` |
| `.startsWith()` | `@testStartsWith` |
| `.endsWith()` | `@testEndsWith` |
| `mainTopic()` | `@testMainTopic` |
| URL dynamique | `@testUrlDynamique` |
| Géolocalisation | `@testGeo` |
| Paramètre `@GET` | `@testGET` |
| Navigation conditionnelle | `@testNavigationConditionnelle` |
| `readcsv` | `@testCSV` |

### Décision pour le projet

- Si `.includes()` fonctionne, la question libre pourra détecter des expressions dans une phrase.
- Si l’une des variantes d’URL dynamique fonctionne, une saisie pourra être transmise à la BAN.
- Si la géolocalisation fonctionne, les coordonnées de l’utilisateur pourront alimenter un calcul de proximité.
- Si `readcsv` fonctionne, les centres et sessions pourront être lus depuis les fichiers générés par Python.
- Le mini-parcours doit permettre de vérifier l’architecture déterministe du module 07 sans dépendre d’une API.

1. [Recommencer les tests](RESET)
2. [Retour au menu](MENU)

## RESET

`@testIncludes = undefined`
`@testStartsWith = undefined`
`@testEndsWith = undefined`
`@testMainTopic = undefined`
`@testUrlDynamique = undefined`
`@testGeo = undefined`
`@testGET = undefined`
`@testNavigationConditionnelle = undefined`
`@testCSV = undefined`

Les indicateurs ont été réinitialisés.

1. [Retour au menu](MENU)
