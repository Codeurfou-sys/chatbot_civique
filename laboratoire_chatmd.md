---
titre: Laboratoire ChatMD — Variables, conditions et API
clavier: true
gestionGrosMots: false
rechercheContenu: false
variablesDynamiques: true
obfuscate: false
theme: light
messageParDéfaut:
  - Je n’ai pas reconnu cette réponse. Utilisez un bouton ou suivez précisément la consigne du test.
plugins: readcsv
---

# Laboratoire ChatMD

Ce laboratoire permet de vérifier, **fonction par fonction**, ce que ChatMD sait réellement exécuter.

1. [Commencer les tests](LAB_MENU)

## LAB_MENU

### Tableau de bord des tests

Effectuez les tests dans l’ordre et notez pour chacun : **réussi**, **partiel** ou **échoué**.

1. [Test 1 — Navigation](LAB_NAV_1)
2. [Test 2 — Saisie et variable](LAB_INPUT_NAME)
3. [Test 3 — Variable définie par un bouton](LAB_BUTTON_VAR)
4. [Test 4 — Conditions](LAB_CONDITIONS)
5. [Test 5 — Variable non définie](LAB_UNDEFINED)
6. [Test 6 — Calcul numérique](LAB_CALC)
7. [Test 7 — Code postal exact](LAB_CP_INPUT)
8. [Test 8 — URL dynamique BAN](LAB_BAN_INPUT)
9. [Test 9 — Conservation des variables](LAB_MEMORY_CHECK)
10. [Test 10 — Recherche par texte libre](LAB_TEXT_INPUT)
11. [Test 11 — Test expérimental CSV](LAB_CSV_INFO)
12. [Afficher le bilan des tests](LAB_REPORT)

## LAB_NAV_1

### Test 1A — Navigation simple

Cliquez sur le bouton.

1. [Continuer](LAB_NAV_2)
2. [Retour au laboratoire](LAB_MENU)

## LAB_NAV_2

### Test 1B — Navigation réussie

Si cet écran apparaît, la navigation entre sections fonctionne.

`@test_navigation="réussi"`

1. [Retour au laboratoire](LAB_MENU)

## LAB_INPUT_NAME

### Test 2 — Saisie dans une variable

Écrivez uniquement votre prénom dans la zone de saisie, puis envoyez-le.

!Next: LAB_CAPTURE_NAME

1. [Retour au laboratoire](LAB_MENU)

## LAB_CAPTURE_NAME

`@prenom = calc(@INPUT)`

### Résultat

La valeur saisie est :

**@prenom**

Si votre prénom apparaît ci-dessus, la récupération de `@INPUT` fonctionne.

`@test_saisie="réussi"`

1. [Modifier le prénom](LAB_INPUT_NAME)
2. [Retour au laboratoire](LAB_MENU)

## LAB_BUTTON_VAR

### Test 3 — Variable définie par un bouton

Choisissez un type d’examen.

1. [Carte de résident @type_examen=CR](LAB_BUTTON_RESULT)
2. [Carte de séjour pluriannuelle @type_examen=CSP](LAB_BUTTON_RESULT)
3. [Naturalisation @type_examen=NAT](LAB_BUTTON_RESULT)
4. [Retour au laboratoire](LAB_MENU)

## LAB_BUTTON_RESULT

### Résultat

Valeur de la variable :

**@type_examen**

`@test_bouton="réussi"`

1. [Tester les conditions avec cette valeur](LAB_CONDITIONS)
2. [Changer de type d’examen](LAB_BUTTON_VAR)
3. [Retour au laboratoire](LAB_MENU)

## LAB_CONDITIONS

### Test 4 — Conditions d’égalité

`if @type_examen == "CR"`

✅ La condition **CR** fonctionne.

Vous préparez la **carte de résident**.

`@test_condition="réussi"`

`endif`

`if @type_examen == "CSP"`

✅ La condition **CSP** fonctionne.

Vous préparez la **carte de séjour pluriannuelle**.

`@test_condition="réussi"`

`endif`

`if @type_examen == "NAT"`

✅ La condition **NAT** fonctionne.

Vous préparez la **naturalisation**.

`@test_condition="réussi"`

`endif`

`if @type_examen == undefined`

⚠️ La variable `@type_examen` n’est pas encore définie.

1. [Définir le type d’examen](LAB_BUTTON_VAR)

`endif`

1. [Retour au laboratoire](LAB_MENU)

## LAB_UNDEFINED

### Test 5 — Variable non définie

`if @variable_inexistante == undefined`

✅ ChatMD reconnaît qu’une variable est indéfinie.

`@test_undefined="réussi"`

`endif`

`if @variable_inexistante != undefined`

❌ Ce message ne devrait pas apparaître.

`endif`

1. [Retour au laboratoire](LAB_MENU)

## LAB_CALC

### Test 6 — Calcul numérique

`@resultat_calcul = calc(2+3)`

Le résultat attendu est **5**.

Résultat obtenu : **@resultat_calcul**

`if @resultat_calcul == 5`

✅ Le calcul et la comparaison numérique fonctionnent.

`@test_calcul="réussi"`

`endif`

`if @resultat_calcul != 5`

❌ Le calcul n’a pas donné le résultat attendu.

`@test_calcul="échoué"`

`endif`

1. [Retour au laboratoire](LAB_MENU)

## LAB_CP_INPUT

### Test 7 — Reconnaissance d’un code postal exact

Saisissez exactement **67000**, **68000** ou **21000**, puis envoyez.

!Next: LAB_CP_CAPTURE

1. [Retour au laboratoire](LAB_MENU)

## LAB_CP_CAPTURE

`@code_postal = calc(@INPUT)`

### Valeur reçue

**@code_postal**

`if @code_postal == "67000"`

✅ Code postal reconnu : **Strasbourg**.

`@ville="Strasbourg"`
`@test_cp="réussi"`

`endif`

`if @code_postal == "68000"`

✅ Code postal reconnu : **Colmar**.

`@ville="Colmar"`
`@test_cp="réussi"`

`endif`

`if @code_postal == "21000"`

✅ Code postal reconnu : **Dijon**.

`@ville="Dijon"`
`@test_cp="réussi"`

`endif`

`if @code_postal != "67000"`

`if @code_postal != "68000"`

`if @code_postal != "21000"`

⚠️ La valeur a bien été enregistrée, mais aucune règle exacte ne correspond à ce code postal.

`@test_cp="partiel"`

`endif`

`endif`

`endif`

1. [Tester cette valeur dans l’API BAN](LAB_BAN_FROM_CP)
2. [Essayer un autre code postal](LAB_CP_INPUT)
3. [Retour au laboratoire](LAB_MENU)

## LAB_BAN_INPUT

### Test 8 — URL dynamique avec l’API BAN

Saisissez une ville, une commune, un code postal ou une adresse.

Exemples : `Strasbourg`, `67000`, `Lons-le-Saunier`.

!Next: LAB_BAN_CAPTURE

1. [Retour au laboratoire](LAB_MENU)

## LAB_BAN_CAPTURE

`@localisation = calc(@INPUT)`

### Valeur injectée dans l’URL

**@localisation**

Cliquez sur le lien ci-dessous. Une page JSON doit s’ouvrir et contenir des résultats correspondant à votre saisie.

[Tester la recherche BAN pour « @localisation »](https://api-adresse.data.gouv.fr/search/?q=@{localisation}&limit=3)

Si la valeur apparaît correctement dans l’adresse du navigateur, les **variables dynamiques dans une URL** fonctionnent.

`@test_url="à vérifier dans le navigateur"`

1. [Tester une autre localisation](LAB_BAN_INPUT)
2. [Retour au laboratoire](LAB_MENU)

## LAB_BAN_FROM_CP

`@localisation = calc(@code_postal)`

### Test de l’API BAN avec le code postal mémorisé

Code postal utilisé : **@localisation**

[Ouvrir la recherche BAN](https://api-adresse.data.gouv.fr/search/?q=@{localisation}&limit=3)

1. [Retour au laboratoire](LAB_MENU)

## LAB_MEMORY_CHECK

### Test 9 — Conservation des variables

Valeurs actuellement mémorisées :

- Prénom : **@prenom**
- Type d’examen : **@type_examen**
- Code postal : **@code_postal**
- Ville détectée : **@ville**
- Localisation BAN : **@localisation**
- Résultat du calcul : **@resultat_calcul**

Si les valeurs saisies auparavant apparaissent encore, les variables sont conservées entre les écrans.

`@test_memoire="à vérifier"`

1. [Retour au laboratoire](LAB_MENU)

## LAB_TEXT_INPUT

### Test 10 — Saisie d’une phrase libre

Saisissez exactement :

**prochaines dates Strasbourg**

!Next: LAB_TEXT_CAPTURE

1. [Retour au laboratoire](LAB_MENU)

## LAB_TEXT_CAPTURE

`@phrase_libre = calc(@INPUT)`

### Phrase enregistrée

**@phrase_libre**

Ce test confirme d’abord que la phrase entière est stockée.

`if @phrase_libre == "prochaines dates Strasbourg"`

✅ Une phrase complète peut être comparée par **égalité exacte**.

`@intention="QL_DATE_VILLE"`
`@ville="Strasbourg"`
`@test_texte="réussi en égalité exacte"`

`endif`

`if @phrase_libre != "prochaines dates Strasbourg"`

⚠️ L’égalité exacte n’a pas reconnu la phrase. Vérifiez les majuscules, accents et espaces.

`@test_texte="échoué ou saisie différente"`

`endif`

### Limite évaluée

Ce test ne prouve pas encore que ChatMD sait rechercher un mot **à l’intérieur** d’une phrase. Il confirme seulement la comparaison exacte.

1. [Voir les variables produites](LAB_TEXT_RESULT)
2. [Retour au laboratoire](LAB_MENU)

## LAB_TEXT_RESULT

### Résultat du routage exact

- Intention : **@intention**
- Ville : **@ville**

`if @intention == "QL_DATE_VILLE"`

✅ Le routage déterministe exact fonctionne.

`endif`

1. [Retour au laboratoire](LAB_MENU)

## LAB_CSV_INFO

### Test 11 — Lecture CSV expérimentale

Ce test vérifie d’abord que le plugin `readcsv` déclaré dans l’en-tête ne bloque pas le chargement du chatbot.

✅ Si cet écran s’affiche, la déclaration `plugins: readcsv` ne bloque pas le document.

Pour tester réellement une recherche CSV, il faudra publier un petit fichier CSV sur GitHub et renseigner sa syntaxe exacte après validation dans la documentation ou dans un exemple opérationnel.

Le fichier de test recommandé sera :

```csv
code_postal,ville,ecran
67000,Strasbourg,SCR_PASS_CITY_STRASBOURG
68000,Colmar,SCR_PASS_INPUT_CITY
21000,Dijon,SCR_PASS_CITY_DIJON
```

`@test_csv="plugin chargé, requête à configurer"`

1. [Retour au laboratoire](LAB_MENU)

## LAB_REPORT

### Bilan des tests

| Fonction testée | Résultat enregistré |
|---|---|
| Navigation | @test_navigation |
| Saisie utilisateur | @test_saisie |
| Variable dans un bouton | @test_bouton |
| Conditions | @test_condition |
| Variable indéfinie | @test_undefined |
| Calcul | @test_calcul |
| Code postal exact | @test_cp |
| URL dynamique | @test_url |
| Mémoire des variables | @test_memoire |
| Phrase libre exacte | @test_texte |
| Plugin CSV | @test_csv |

### Interprétation

- Si les tests 1 à 9 fonctionnent, le module 07 peut déjà être reconstruit avec des parcours guidés et des conditions déterministes.
- Si le test d’URL dynamique fonctionne, la saisie peut être transmise à l’API BAN.
- Le test CSV nécessitera ensuite un fichier de données séparé et une syntaxe `readcsv` validée.
- La détection partielle de mots dans une phrase n’est pas supposée fonctionnelle tant qu’un test spécifique n’a pas été validé.

1. [Recommencer tous les tests](LAB_RESET)
2. [Retour au laboratoire](LAB_MENU)

## LAB_RESET

`@test_navigation=undefined`
`@test_saisie=undefined`
`@test_bouton=undefined`
`@test_condition=undefined`
`@test_undefined=undefined`
`@test_calcul=undefined`
`@test_cp=undefined`
`@test_url=undefined`
`@test_memoire=undefined`
`@test_texte=undefined`
`@test_csv=undefined`

Les indicateurs de test ont été réinitialisés.

1. [Retour au laboratoire](LAB_MENU)
