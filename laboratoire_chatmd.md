# Test E --- condition fixe (sans variable)

Ce test permet de vérifier si **ChatMD applique réellement la directive
`condition:`**.

Le filtre est volontairement codé en dur sur le code postal **67000**.

👉 Si ce test retourne uniquement les lignes ayant le code postal
**67000**, alors le moteur `condition` fonctionne et le problème vient
de l'utilisation des variables (`ask()`).

👉 Si ce test ne retourne rien ou retourne toutes les lignes, alors le
problème vient du moteur `readcsv` lui-même.

------------------------------------------------------------------------

``` uai
button("Lancer le test E")
goto test_e_execution
```

``` uai
button("Retour au menu")
goto menu
```

------------------------------------------------------------------------

## test_e_execution

``` uai
readcsv https://raw.githubusercontent.com/Codeurfou-sys/chatbot_civique/refs/heads/main/lieux_dits_test.csv

condition: $1 == "67000"

maxResults: 10

### Résultats

$i. **$2 — $1**

Adresse : $3

Coordonnées : $4, $5
```

------------------------------------------------------------------------

### Variante 1

``` uai
condition: "67000" == $1
```

### Variante 2

``` uai
condition: $1 = "67000"
```

### Variante 3

``` uai
condition: $1 === "67000"
```

------------------------------------------------------------------------

``` uai
button("Recommencer le test E")
goto test_e_execution
```

``` uai
button("Retour au menu")
goto menu
```
