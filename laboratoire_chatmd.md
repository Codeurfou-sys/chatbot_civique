---
titre: Laboratoire ChatMD V2 — Variables, conditions, formulaires, NLP et géolocalisation
variablesDynamiques: true
geolocation: true
obfuscate: false
gestionGrosMots: false
rechercheContenu: false
---

# Laboratoire ChatMD V2

Ce laboratoire utilise la syntaxe officielle fournie dans la documentation ChatMD.

1. [Commencer les tests](#LAB_MENU)

## LAB_MENU

### Tableau de bord

Effectuez les tests dans l’ordre.

1. [Test 1 — Navigation interne](#LAB_NAVIGATION)
2. [Test 2 — @INPUT et affichage d’une variable](#LAB_INPUT)
3. [Test 3 — Champ HTML `<input>`](#LAB_FORM_INPUT)
4. [Test 4 — Liste HTML `<select>`](#LAB_FORM_SELECT)
5. [Test 5 — Variable définie par un bouton](#LAB_BUTTON_VAR)
6. [Test 6 — Conditions](#LAB_CONDITIONS)
7. [Test 7 — Calcul et traitement séquentiel](#LAB_CALC)
8. [Test 8 — Fonctions sur une chaîne](#LAB_STRING)
9. [Test 9 — Détection de mots-clés avec `.includes()`](#LAB_KEYWORDS)
10. [Test 10 — Extraction avec `mainTopic()`](#LAB_MAIN_TOPIC)
11. [Test 11 — Paramètre URL `@GET...`](#LAB_GET)
12. [Test 12 — Géolocalisation](#LAB_GEO)
13. [Test 13 — Lien externe ordinaire](#LAB_EXTERNAL_LINK)
14. [Test 14 — URL dynamique expérimentale](#LAB_DYNAMIC_URL)
15. [Test 15 — Mémoire des variables](#LAB_MEMORY)
16. [Afficher le bilan](#LAB_REPORT)

## LAB_NAVIGATION

### Test 1 — Navigation interne

Si vous êtes arrivé ici depuis le menu, le lien interne Markdown fonctionne.

`@testNavigation = réussi`

1. [Retour au laboratoire](#LAB_MENU)

## LAB_INPUT

### Test 2 — Récupération de la dernière réponse avec `@INPUT`

Écrivez votre prénom dans la zone principale de saisie de ChatMD, puis envoyez.

!Next: LAB_INPUT_RESULT

1. [Retour au laboratoire](#LAB_MENU)

## LAB_INPUT_RESULT

`@prenom = calc(@INPUT)`

Bonjour **`@prenom`**.

La dernière réponse reçue par ChatMD était : **`@INPUT`**.

`if @prenom != undefined && @prenom.trim().length()>0`

✅ `@INPUT`, `calc(@INPUT)` et l’affichage avec les backticks fonctionnent.

`@testInput = réussi`

`endif`

`if !@prenom || @prenom.trim().length()==0`

❌ Aucune valeur n’a été enregistrée.

`@testInput = échoué`

`endif`

1. [Recommencer ce test](#LAB_INPUT)
2. [Retour au laboratoire](#LAB_MENU)

## LAB_FORM_INPUT

### Test 3 — Champ HTML `<input>`

Saisissez une commune, puis appuyez sur **Entrée** dans le champ.

<label for="commune">Commune recherchée :</label>

<input type="text" id="commune" name="commune" value="`@commune`" placeholder="Exemple : Strasbourg" />

`if @commune != undefined && @commune.trim().length()>0`

Valeur enregistrée : **`@commune`**

✅ Le champ HTML alimente directement la variable `@commune`.

`@testFormInput = réussi`

1. [Tester les mots-clés avec cette commune](#LAB_KEYWORDS)

`endif`

`if !@commune || @commune.trim().length()==0`

La variable n’est pas encore remplie. Saisissez une valeur et appuyez sur Entrée.

`endif`

1. [Retour au laboratoire](#LAB_MENU)

## LAB_FORM_SELECT

### Test 4 — Liste déroulante `<select>`

<label for="typeExamen">Vous préparez :</label>

<select name="typeExamen" id="typeExamen" data-selected="`@typeExamen`">
   <option value="">À sélectionner</option>
   <option value="CR">la carte de résident</option>
   <option value="CSP">la carte de séjour pluriannuelle</option>
   <option value="NAT">la naturalisation</option>
</select>

`if @typeExamen == "CR"`

Vous avez choisi : **carte de résident**.

`@testSelect = réussi`

`endif`

`if @typeExamen == "CSP"`

Vous avez choisi : **carte de séjour pluriannuelle**.

`@testSelect = réussi`

`endif`

`if @typeExamen == "NAT"`

Vous avez choisi : **naturalisation**.

`@testSelect = réussi`

`endif`

Valeur technique : **`@typeExamen`**

1. [Retour au laboratoire](#LAB_MENU)

## LAB_BUTTON_VAR

### Test 5 — Variable définie dans un bouton

1. [Grand Est @region=Grand Est](#LAB_BUTTON_RESULT)
2. [Bourgogne @region=Bourgogne](#LAB_BUTTON_RESULT)
3. [Auvergne @region=Auvergne](#LAB_BUTTON_RESULT)
4. [Retour au laboratoire](#LAB_MENU)

## LAB_BUTTON_RESULT

Région mémorisée : **`@region`**

`if @region != undefined`

✅ La variable du bouton est enregistrée et affichée.

`@testButton = réussi`

`endif`

1. [Modifier la région](#LAB_BUTTON_VAR)
2. [Retour au laboratoire](#LAB_MENU)

## LAB_CONDITIONS

### Test 6 — Blocs conditionnels

`if @typeExamen == "CR"`

✅ Condition CR validée.

`@testCondition = réussi`

`endif`

`if @typeExamen == "CSP"`

✅ Condition CSP validée.

`@testCondition = réussi`

`endif`

`if @typeExamen == "NAT"`

✅ Condition NAT validée.

`@testCondition = réussi`

`endif`

`if @typeExamen == undefined`

La variable `@typeExamen` n’est pas encore définie.

1. [Choisir un type d’examen](#LAB_FORM_SELECT)

`endif`

1. [Retour au laboratoire](#LAB_MENU)

## LAB_CALC

### Test 7 — Calcul et traitement séquentiel

`@score = 2`

Score initial : **`@score`**

`@score = calc(@score+3)`

Score après l’ajout de 3 points : **`@score`**

`if @score == 5`

✅ Le calcul et le traitement séquentiel fonctionnent.

`@testCalc = réussi`

`endif`

`if @score != 5`

❌ Le score attendu était 5.

`@testCalc = échoué`

`endif`

1. [Retour au laboratoire](#LAB_MENU)

## LAB_STRING

### Test 8 — Fonctions sur une chaîne

Saisissez une phrase dans la zone principale, par exemple :

**Prochaines dates à Strasbourg**

!Next: LAB_STRING_RESULT

1. [Retour au laboratoire](#LAB_MENU)

## LAB_STRING_RESULT

`@phrase = calc(@INPUT)`
`@phraseNettoyee = calc(@phrase.trim().toLowerCase())`
`@phraseEncodee = calc(encodeURI(@phrase.trim()))`

Phrase originale : **`@phrase`**

Phrase normalisée : **`@phraseNettoyee`**

Phrase encodée pour une URL : **`@phraseEncodee`**

Longueur : **`@phraseNettoyee.length()`**

`if @phraseNettoyee.length()>0`

✅ `trim()`, `toLowerCase()`, `length()` et `encodeURI()` sont exécutés.

`@testString = réussi`

`endif`

1. [Tester les mots-clés](#LAB_KEYWORDS_FROM_PHRASE)
2. [Tester le sujet principal](#LAB_MAIN_TOPIC_FROM_PHRASE)
3. [Retour au laboratoire](#LAB_MENU)

## LAB_KEYWORDS

### Test 9A — Détection de mots-clés depuis la commune

Commune actuelle : **`@commune`**

`if @commune != undefined && @commune.toLowerCase().includes("strasbourg")`

✅ Le mot-clé **Strasbourg** a été détecté.

`@ville = Strasbourg`
`@destinationTest = SCR_PASS_CITY_STRASBOURG`
`@testKeywords = réussi`

`endif`

`if @commune != undefined && @commune.toLowerCase().includes("dijon")`

✅ Le mot-clé **Dijon** a été détecté.

`@ville = Dijon`
`@destinationTest = SCR_PASS_CITY_DIJON`
`@testKeywords = réussi`

`endif`

Ville produite : **`@ville`**

Destination produite : **`@destinationTest`**

1. [Retour au laboratoire](#LAB_MENU)

## LAB_KEYWORDS_FROM_PHRASE

### Test 9B — Détection dans une phrase libre

Phrase analysée : **`@phraseNettoyee`**

`if @phraseNettoyee.includes("date") && @phraseNettoyee.includes("strasbourg")`

✅ Intention détectée : prochaines dates à Strasbourg.

`@intention = QL_DATE_VILLE`
`@ville = Strasbourg`
`@testKeywords = réussi`

`endif`

`if @phraseNettoyee.includes("centre") && @phraseNettoyee.includes("proche")`

✅ Intention détectée : centre le plus proche.

`@intention = QL_CENTRE_PROCHE`
`@testKeywords = réussi`

`endif`

Intention produite : **`@intention`**

Ville produite : **`@ville`**

1. [Retour au laboratoire](#LAB_MENU)

## LAB_MAIN_TOPIC

### Test 10 — `mainTopic()`

Saisissez une phrase courte dans la zone principale.

Exemples :

- prochaines dates à Strasbourg
- prix de l’examen
- définition de la laïcité

!Next: LAB_MAIN_TOPIC_RESULT

1. [Retour au laboratoire](#LAB_MENU)

## LAB_MAIN_TOPIC_RESULT

`@texteSujet = calc(@INPUT)`
`@sujetPrincipal = calc(mainTopic(@texteSujet))`

Phrase : **`@texteSujet`**

Sujet principal extrait : **`@sujetPrincipal`**

`if @sujetPrincipal != undefined`

✅ `mainTopic()` a retourné une valeur.

`@testMainTopic = réussi`

`endif`

1. [Retour au laboratoire](#LAB_MENU)

## LAB_MAIN_TOPIC_FROM_PHRASE

`@sujetPrincipal = calc(mainTopic(@phrase))`

Sujet extrait de la phrase précédente : **`@sujetPrincipal`**

1. [Retour au laboratoire](#LAB_MENU)

## LAB_GET

### Test 11 — Paramètre dans l’URL

Pour tester cette fonctionnalité, ajoutez manuellement à l’adresse du laboratoire :

`?departement=67`

ou, si l’URL contient déjà un `?`, ajoutez :

`&departement=67`

Valeur reçue : **`@GETdepartement`**

`if @GETdepartement == "67"`

✅ Le paramètre URL `departement=67` est reconnu.

`@testGet = réussi`

`endif`

`if @GETdepartement == undefined`

Aucun paramètre `departement` n’a été détecté.

`endif`

1. [Retour au laboratoire](#LAB_MENU)

## LAB_GEO

### Test 12 — Géolocalisation

Latitude : **`@LATITUDE`**

Longitude : **`@LONGITUDE`**

Précision : **`@POSITION_ACCURACY`** mètres

`if @LATITUDE != undefined && @LONGITUDE != undefined`

✅ Les coordonnées ont été obtenues.

`@testGeo = réussi`

`endif`

`if @LATITUDE>41.0 && @LATITUDE<51.5 && @LONGITUDE>-5.0 && @LONGITUDE<9.5`

La position semble se trouver en France métropolitaine.

`endif`

`if Math.abs(@LATITUDE - 48.5734)<0.5 && Math.abs(@LONGITUDE - 7.7521)<0.5`

La position semble proche de **Strasbourg**.

`endif`

`if @LATITUDE == undefined`

La géolocalisation n’a pas fonctionné ou n’a pas été autorisée.

`@testGeo = échoué ou refusé`

`endif`

1. [Recharger le test de géolocalisation](#LAB_GEO)
2. [Retour au laboratoire](#LAB_MENU)

## LAB_EXTERNAL_LINK

### Test 13 — Lien externe

Le bouton ci-dessous doit ouvrir la documentation ChatMD dans un nouvel onglet.

1. [Ouvrir la documentation ChatMD](link:https://chatmd.forge.apps.education.fr/docs/)
2. [Retour au laboratoire](#LAB_MENU)

## LAB_DYNAMIC_URL

### Test 14 — URL dynamique expérimentale

Ce test utilise une variable affichée dans une URL Markdown.

Commune disponible : **`@commune`**

Commune encodée : **`@communeEncodee`**

`if @commune != undefined`

`@communeEncodee = calc(encodeURI(@commune.trim()))`

[Tester l’API BAN avec la commune](link:https://api-adresse.data.gouv.fr/search/?q=`@communeEncodee`&limit=3)

`endif`

`if @commune == undefined`

Aucune commune n’est enregistrée.

1. [Saisir une commune](#LAB_FORM_INPUT)

`endif`

### Variante avec la dernière phrase

Phrase encodée : **`@phraseEncodee`**

`if @phraseEncodee != undefined`

[Tester l’API BAN avec la phrase](link:https://api-adresse.data.gouv.fr/search/?q=`@phraseEncodee`&limit=3)

`endif`

`@testDynamicUrl = à vérifier dans le navigateur`

1. [Retour au laboratoire](#LAB_MENU)

## LAB_MEMORY

### Test 15 — Conservation des variables

- Prénom : **`@prenom`**
- Commune : **`@commune`**
- Type d’examen : **`@typeExamen`**
- Région : **`@region`**
- Score : **`@score`**
- Phrase : **`@phrase`**
- Intention : **`@intention`**
- Ville : **`@ville`**
- Sujet principal : **`@sujetPrincipal`**
- Latitude : **`@LATITUDE`**
- Longitude : **`@LONGITUDE`**

`@testMemory = à vérifier`

1. [Retour au laboratoire](#LAB_MENU)

## LAB_REPORT

### Bilan des tests

| Fonction | Résultat |
|---|---|
| Navigation | `@testNavigation` |
| `@INPUT` et affichage | `@testInput` |
| Champ `<input>` | `@testFormInput` |
| Liste `<select>` | `@testSelect` |
| Variable dans un bouton | `@testButton` |
| Conditions | `@testCondition` |
| Calcul séquentiel | `@testCalc` |
| Fonctions sur chaînes | `@testString` |
| Détection `.includes()` | `@testKeywords` |
| NLP `mainTopic()` | `@testMainTopic` |
| Paramètre `@GET...` | `@testGet` |
| Géolocalisation | `@testGeo` |
| URL dynamique | `@testDynamicUrl` |
| Mémoire | `@testMemory` |

### Points décisifs pour le module 07

- Si `<input>` fonctionne, l’utilisateur pourra saisir directement une ville ou un code postal.
- Si `.includes()` fonctionne, la rubrique Question libre pourra détecter des mots dans une phrase.
- Si `encodeURI()` et l’URL dynamique fonctionnent, la saisie pourra être transmise à la BAN.
- Si la géolocalisation fonctionne, ChatMD pourra comparer la position de l’utilisateur aux coordonnées des centres.
- Si `mainTopic()` fonctionne, il pourra compléter le routage par mots-clés.
- Le plugin `readcsv` devra faire l’objet d’un laboratoire séparé dès que sa syntaxe complète aura été reproduite depuis un exemple officiel.

1. [Réinitialiser les indicateurs](#LAB_RESET)
2. [Retour au laboratoire](#LAB_MENU)

## LAB_RESET

`@testNavigation = undefined`
`@testInput = undefined`
`@testFormInput = undefined`
`@testSelect = undefined`
`@testButton = undefined`
`@testCondition = undefined`
`@testCalc = undefined`
`@testString = undefined`
`@testKeywords = undefined`
`@testMainTopic = undefined`
`@testGet = undefined`
`@testGeo = undefined`
`@testDynamicUrl = undefined`
`@testMemory = undefined`

Les indicateurs du laboratoire ont été réinitialisés.

1. [Retour au laboratoire](#LAB_MENU)
