---
titre: Laboratoire ChatMD V3
variablesDynamiques: true
geolocation: true
obfuscate: false
---

# Laboratoire ChatMD V3

Ce laboratoire est destiné à valider systématiquement les fonctionnalités de ChatMD avant leur intégration dans le chatbot Examen civique.

1. [Commencer les tests](MENU)

## MENU

1. [Variables et @INPUT](T1)
2. [Champ HTML input](T2)
3. [Liste déroulante select](T3)
4. [Variables par bouton](T4)
5. [Conditions if / endif](T5)
6. [calc() et calculs](T6)
7. [Fonctions trim / toLowerCase / toUpperCase](T7)
8. [includes()](T8)
9. [startsWith() / endsWith()](T9)
10. [encodeURI()](T10)
11. [mainTopic()](T11)
12. [Paramètres @GET](T12)
13. [Géolocalisation](T13)
14. [URL dynamique](T14)
15. [Plugin readcsv](T15)
16. [Navigation conditionnelle](T16)
17. [Mémoire des variables](T17)
18. [Quiz](T18)
19. [Plusieurs bots](T19)
20. [Bilan](REPORT)

## T1

Saisissez votre prénom.

!Next: T1_RESULT

## T1_RESULT

`@prenom = calc(@INPUT)`

Bonjour **`@prenom`**

Dernière saisie : **`@INPUT`**

1. [Retour](MENU)

## T2

<label>Ville :</label>
<input type="text" id="ville" name="ville" value="`@ville`"/>

Ville : **`@ville`**

1. [Retour](MENU)

## T3

<select name="type" data-selected="`@type`">
<option value="">Choisir</option>
<option value="CR">Carte résident</option>
<option value="CSP">Carte séjour</option>
<option value="NAT">Naturalisation</option>
</select>

Valeur : **`@type`**

1. [Retour](MENU)

## T4

1. [Grand Est @region=Grand Est](BTN)
2. [BFC @region=BFC](BTN)

## BTN

Région : **`@region`**

1. [Retour](MENU)

## T5

`if @region=="Grand Est"`

✅ Condition Grand Est

`endif`

`if @region=="BFC"`

✅ Condition BFC

`endif`

1. [Retour](MENU)

## T6

`@score=2`

Avant : **`@score`**

`@score=calc(@score+5)`

Après : **`@score`**

1. [Retour](MENU)

## T7

`@texte=calc(@INPUT)`
`@mini=calc(@texte.toLowerCase())`
`@maj=calc(@texte.toUpperCase())`
`@trim=calc(@texte.trim())`

Mini : **`@mini`**

Maj : **`@maj`**

Trim : **`@trim`**

1. [Retour](MENU)

## T8

`if @trim.toLowerCase().includes("strasbourg")`

Mot détecté : Strasbourg

`endif`

1. [Retour](MENU)

## T9

`if @trim.startsWith("prochaines")`

startsWith OK

`endif`

`if @trim.endsWith("strasbourg")`

endsWith OK

`endif`

1. [Retour](MENU)

## T10

`@url=calc(encodeURI(@trim))`

URL :

**`@url`**

1. [Retour](MENU)

## T11

`@topic=calc(mainTopic(@trim))`

Sujet :

**`@topic`**

1. [Retour](MENU)

## T12

Département :

**`@GETdepartement`**

1. [Retour](MENU)

## T13

Latitude :

**`@LATITUDE`**

Longitude :

**`@LONGITUDE`**

Précision :

**`@POSITION_ACCURACY`**

1. [Retour](MENU)

## T14

Lien test :

[Recherche BAN](link:https://api-adresse.data.gouv.fr/search/?q=`@url`&limit=3)

1. [Retour](MENU)

## T15

Objectif :

- charger readcsv
- lire un CSV GitHub
- rechercher une ville
- récupérer un écran

À compléter avec la syntaxe officielle issue d'un exemple opérationnel.

1. [Retour](MENU)

## T16

`if @region=="Grand Est"`

1. [Aller vers Strasbourg](STRAS)

`endif`

## STRAS

Navigation conditionnelle OK.

1. [Retour](MENU)

## T17

Variables mémorisées :

- `@prenom`
- `@ville`
- `@type`
- `@region`
- `@score`
- `@topic`

1. [Retour](MENU)

## T18

Question :

Quelle est la devise de la République ?

1. [Liberté, Égalité, Fraternité @scoreQuiz=1](QUIZ)
2. [Travail, Famille, Patrie @scoreQuiz=0](QUIZ)

## QUIZ

Score :

**`@scoreQuiz`**

1. [Retour](MENU)

## T19

Ce test servira à vérifier les appels entre plusieurs bots.

1. [Retour](MENU)

## REPORT

# Résultats attendus

| Fonction | Validation |
|---|---|
| @INPUT | ☐ |
| input HTML | ☐ |
| select HTML | ☐ |
| Variables | ☐ |
| Conditions | ☐ |
| calc() | ☐ |
| trim() | ☐ |
| includes() | ☐ |
| startsWith() | ☐ |
| endsWith() | ☐ |
| encodeURI() | ☐ |
| mainTopic() | ☐ |
| @GET | ☐ |
| Géolocalisation | ☐ |
| URL dynamique | ☐ |
| readcsv | ☐ |
| Navigation conditionnelle | ☐ |
| Mémoire | ☐ |
| Quiz | ☐ |
| Plusieurs bots | ☐ |

Une fois cette grille entièrement validée, le chatbot Examen civique pourra être adapté aux capacités réelles de ChatMD.
