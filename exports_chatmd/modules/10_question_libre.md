<!-- Module généré automatiquement : Question libre -->
<!-- Date : 2026-08-03T13:13:33+02:00 -->

## SCR_QL_CONFIRM

### J’ai compris votre demande

<!-- Variables : {message_confirmation}; {destination} -->

{message_confirmation}

1. [Afficher la réponse](SCR_QL_ROUTE)
2. [Modifier ma question](SCR_QL_INPUT)
3. [Retour au menu principal](MENU_PRINCIPAL)

## SCR_QL_CHECK

### Vérification des informations

<!-- Variables : {intention}; {destination}; {variable_obligatoire} -->

<!-- Règle métier : Si l’information obligatoire manque, ouvrir l’écran complémentaire prévu -->

<!-- Transition automatique NAV_QL_012 : Entité LOCALISATION ou VILLE obligatoire absente → SCR_QL_GEO_MISSING -->
1. [Demander une localisation](SCR_QL_GEO_MISSING)
<!-- Transition automatique NAV_QL_013 : Entité TERME obligatoire absente → SCR_QL_TERM_MISSING -->
1. [Demander le terme](SCR_QL_TERM_MISSING)
<!-- Transition automatique NAV_QL_014 : TYPE_EXAMEN obligatoire absent → SCR_QL_EXAM_MISSING -->
1. [Demander le type d’examen](SCR_QL_EXAM_MISSING)
<!-- Transition automatique NAV_QL_015 : THEME obligatoire absent → SCR_QL_THEME_MISSING -->
1. [Demander le thème](SCR_QL_THEME_MISSING)
<!-- Transition automatique NAV_QL_016 : Variables suffisantes → SCR_QL_CONFIRM -->
1. [Confirmer l’interprétation](SCR_QL_CONFIRM)

## SCR_QL_TERM_MISSING

### Quel mot souhaitez-vous comprendre ?

<!-- Variables : {mot_recherche} -->

Quel mot ou quelle notion souhaitez-vous comprendre ?

<!-- Transition automatique NAV_QL_022 : Saisie validée → SCR_GLO_SEARCH -->
1. [Ouvrir le Glossaire](SCR_GLO_SEARCH)
1. [Modifier ma question](SCR_QL_INPUT)

## SCR_QL_DETECT

### Détection de l’intention

<!-- Variables : {question_normalisee}; {intention}; {id_regle} -->

<!-- Contenu généré depuis BLOC 3. -->

<!-- Transition automatique NAV_QL_009 : Règle trouvée → SCR_QL_EXTRACT -->
1. [Extraire les informations](SCR_QL_EXTRACT)
<!-- Transition automatique NAV_QL_010 : Aucune correspondance → SCR_QL_NOT_FOUND -->
1. [Aucune règle trouvée](SCR_QL_NOT_FOUND)

<!-- Arrêt à la première règle applicable -->

## SCR_QL_EXAMPLES

### Exemples de questions reconnues

<!-- Variables : {question_exemple} -->

<!-- Contenu généré depuis BLOC 8. -->

1. [Prochaines dates à Strasbourg](SCR_QL_INPUT)
2. [Centre proche de chez moi](SCR_QL_INPUT)
3. [Définition de la laïcité](SCR_QL_INPUT)
4. [Passer un examen blanc](SCR_QL_INPUT)
5. [Écrire ma propre question](SCR_QL_INPUT)
6. [Retour au module](SCR_QL_MENU)

## SCR_QL_EXTRACT

### Extraction des informations utiles

<!-- Variables : {ville}; {region}; {code_postal}; {mot_recherche}; {type_examen}; {theme} -->

<!-- Règle métier : Comparer la question aux entités maîtrisées -->

<!-- Transition automatique NAV_QL_011 : Toujours → SCR_QL_CHECK -->
1. [Contrôler les variables](SCR_QL_CHECK)

<!-- Une commune libre est demandée dans un second temps -->

## SCR_QL_GEO_MISSING

### Précisez votre localisation

<!-- Variables : {saisie_localisation} -->

Indiquez une ville, une commune, un code postal ou une adresse.

<!-- Transition automatique NAV_QL_020 : Saisie validée → SCR_QL_EXTRACT -->
1. [Reprendre le traitement](SCR_QL_EXTRACT)
1. [Modifier ma question](SCR_QL_INPUT)

<!-- Utilisé pour dates, centre proche et inscription -->

## SCR_QL_MENU

### Pose-moi une question

Écrivez une question courte. Je détecterai une expression précise, puis les mots-clés et les informations utiles.

1. [Poser ma question](SCR_QL_INPUT)
2. [Voir des exemples](SCR_QL_EXAMPLES)
3. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran d’entrée -->

## SCR_QL_ROUTE

### Ouverture du résultat

<!-- Variables : {destination}; {variables_transmises} -->

`@{destination}`

<!-- Transition automatique NAV_QL_048 : ID règle détecté → SCR_PASS_RESULTS_NEAR -->
1. [QL_CENTRE_PROCHE](SCR_PASS_RESULTS_NEAR)
<!-- Transition automatique NAV_QL_050 : ID règle détecté → SCR_PASS_INPUT_CP -->
1. [QL_CODE_POSTAL](SCR_PASS_INPUT_CP)
<!-- Transition automatique NAV_QL_045 : ID règle détecté → @{ecran_centre} -->
1. [QL_DATE_VILLE](@{ecran_centre})
<!-- Transition automatique NAV_QL_046 : ID règle détecté → @{ecran_centre} -->
1. [QL_DATE_VILLE](@{ecran_centre})
<!-- Transition automatique NAV_QL_058 : ID règle détecté → SCR_GLO_SEARCH -->
1. [QL_DEFINITION](SCR_GLO_SEARCH)
<!-- Transition automatique NAV_QL_063 : ID règle détecté → SCR_PREP_MENU -->
1. [QL_EXAMEN_BLANC](SCR_PREP_MENU)
<!-- Transition automatique NAV_QL_055 : ID règle détecté → SCR_FAQ_004 -->
1. [QL_FORMAT](SCR_FAQ_004)
<!-- Transition automatique NAV_QL_052 : ID règle détecté → @{ecran_centre_ou_region} -->
1. [QL_INSCRIPTION](@{ecran_centre_ou_region})
<!-- Transition automatique NAV_QL_066 : ID règle détecté → SCR_BIL_MENU -->
1. [QL_BILAN](SCR_BIL_MENU)
<!-- Transition automatique NAV_QL_049 : ID règle détecté → SCR_PASS_RESULTS_NEAR -->
1. [QL_CENTRE_PROCHE](SCR_PASS_RESULTS_NEAR)
<!-- Transition automatique NAV_QL_047 : ID règle détecté → @{ecran_centre} -->
1. [QL_DATE_VILLE](@{ecran_centre})
<!-- Transition automatique NAV_QL_059 : ID règle détecté → SCR_GLO_SEARCH -->
1. [QL_DEFINITION](SCR_GLO_SEARCH)
<!-- Transition automatique NAV_QL_057 : ID règle détecté → SCR_FAQ_026 -->
1. [QL_ECHEC](SCR_FAQ_026)
<!-- Transition automatique NAV_QL_062 : ID règle détecté → SCR_ENT_MENU -->
1. [QL_ENTRAINEMENT](SCR_ENT_MENU)
<!-- Transition automatique NAV_QL_060 : ID règle détecté → SCR_GLO_SEARCH -->
1. [QL_LAICITE](SCR_GLO_SEARCH)
<!-- Transition automatique NAV_QL_064 : ID règle détecté → SCR_CONS_MEMOIRE_MENU -->
1. [QL_MEMOIRE](SCR_CONS_MEMOIRE_MENU)
<!-- Transition automatique NAV_QL_054 : ID règle détecté → SCR_FAQ_019 -->
1. [QL_PRIX](SCR_FAQ_019)
<!-- Transition automatique NAV_QL_051 : ID règle détecté → @{ecran_region} -->
1. [QL_REGION](@{ecran_region})
<!-- Transition automatique NAV_QL_056 : ID règle détecté → SCR_FAQ_009 -->
1. [QL_SCORE](SCR_FAQ_009)
<!-- Transition automatique NAV_QL_065 : ID règle détecté → SCR_CONS_ENTRETIEN_MENU -->
1. [QL_STRESS](SCR_CONS_ENTRETIEN_MENU)
<!-- Transition automatique NAV_QL_053 : ID règle détecté → @{ecran_centre_ou_region} -->
1. [QL_INSCRIPTION](@{ecran_centre_ou_region})
<!-- Transition automatique NAV_QL_061 : ID règle détecté → SCR_REV_MENU -->
1. [QL_REVISIONS](SCR_REV_MENU)
<!-- Transition automatique NAV_QL_067 : ID règle détecté → SCR_FAQ_SEARCH -->
1. [QL_FAQ](SCR_FAQ_SEARCH)

<!-- Écran logique non affiché -->

## SCR_QL_INPUT

### Écrivez votre question

<!-- Variables : {question_libre} -->

Exemples : « prochaines dates à Strasbourg », « quel centre est proche de Dole ? » ou « que signifie la laïcité ? ».

<!-- Transition automatique NAV_QL_005 : Saisie validée → SCR_QL_NORMALIZE -->
1. [Préparer la question](SCR_QL_NORMALIZE)
1. [Voir des exemples](SCR_QL_EXAMPLES)
2. [Retour au module](SCR_QL_MENU)

<!-- Variable principale -->

## SCR_QL_NOT_FOUND

### Je n’ai pas encore compris

<!-- Variables : {question_libre} -->

Reformulez avec une phrase plus courte ou choisissez une rubrique : FAQ, Glossaire, Révisions, Conseils ou Passer mon examen.

1. [Reformuler ma question](SCR_QL_INPUT)
2. [Consulter la FAQ](SCR_FAQ_SEARCH)
3. [Consulter le Glossaire](SCR_GLO_SEARCH)
4. [Voir les Révisions](SCR_REV_MENU)
5. [Voir les Conseils](SCR_CONS_MENU)
6. [Passer mon examen](SCR_PASS_MENU)
7. [Retour au menu principal](MENU_PRINCIPAL)

## SCR_QL_THEME_MISSING

### Quel thème souhaitez-vous travailler ?

<!-- Variables : {theme} -->

<!-- Contenu non renseigné. -->

<!-- Condition métier : Réponse sélectionnée | Valeur : T1 -->
1. [Principes et valeurs](SCR_QL_CHECK)
<!-- Condition métier : Réponse sélectionnée | Valeur : T2 -->
2. [Institutions](SCR_QL_CHECK)
<!-- Condition métier : Réponse sélectionnée | Valeur : T3 -->
3. [Droits et devoirs](SCR_QL_CHECK)
<!-- Condition métier : Réponse sélectionnée | Valeur : T4 -->
4. [Histoire, géographie et culture](SCR_QL_CHECK)
<!-- Condition métier : Réponse sélectionnée | Valeur : T5 -->
5. [Vie dans la société française](SCR_QL_CHECK)

<!-- Utilisé pour révisions et entraînement -->

## SCR_QL_NORMALIZE

### Préparation de la question

<!-- Variables : {question_libre}; {question_normalisee} -->

<!-- Règle métier : Normaliser les majuscules, accents, ponctuation et espaces -->

<!-- Transition automatique NAV_QL_008 : Toujours → SCR_QL_DETECT -->
1. [Détecter l’intention](SCR_QL_DETECT)

<!-- Aucun calcul de score -->

## SCR_QL_EXAM_MISSING

### Quel examen préparez-vous ?

<!-- Variables : {type_examen} -->

<!-- Contenu non renseigné. -->

<!-- Condition métier : Réponse sélectionnée | Valeur : CR -->
1. [Carte de résident](SCR_QL_CHECK)
<!-- Condition métier : Réponse sélectionnée | Valeur : CSP -->
2. [Carte de séjour pluriannuelle](SCR_QL_CHECK)
<!-- Condition métier : Réponse sélectionnée | Valeur : NAT -->
3. [Naturalisation](SCR_QL_CHECK)

<!-- Utilisé pour entraînement et examen blanc -->
