<!-- Module généré automatiquement : Préparer examen -->
<!-- Date : 2026-08-03T12:39:32+02:00 -->

## SCR_PREP_RES_MENU

### Carte de résident

<!-- Variables : {type_examen} -->

Comment souhaitez-vous vous entraîner ?

1. [📝 Je réponds aux questions officielles](SCR_PREP_RES_QOFF_INTRO)
2. [🎭 Je réponds à des mises en situation](SCR_PREP_RES_MIS_INTRO)
3. [🎓 Je passe un examen blanc complet](SCR_PREP_RES_BLANC_INTRO)
4. [⬅️ Retour au choix de l’examen](SCR_PREP_MENU)
5. [🏠 Retour au menu principal](MENU_PRINCIPAL)

## SCR_PREP_RES_BLANC_INTRO

### Examen blanc complet

<!-- Variables : {type_examen} -->

L’examen blanc comprend 28 questions officielles et 12 mises en situation. Les corrections sont affichées seulement à la fin.

1. [Commencer l’examen blanc](SCR_PREP_RES_BLANC_INIT)

## SCR_PREP_RES_BLANC_INIT

### Préparation de l’examen blanc

<!-- Variables : {{session_id}}; {{deja_tires}} -->

<!-- Règle métier : Créer le tirage complet de 40 éléments -->

<!-- Condition métier : Tirage valide -->
1. [Lancer la première partie](SCR_PREP_RES_BLANC_QOFF)

<!-- Écran logique non affiché -->

## SCR_PREP_RES_BLANC_QOFF

### Question {numero_question} sur 28

<!-- Variables : {numero_question}; {id_question}; {reponses_examen} -->

<!-- Règle métier : Enregistrer la réponse sans afficher la correction -->

**Réponse attendue :** Choix unique

<!-- Condition métier : Question courante = 28 -->
1. [Terminer la première partie](SCR_PREP_RES_BLANC_TRANS)
<!-- Condition métier : Question courante < 28 -->
2. [Valider et continuer](SCR_PREP_RES_BLANC_QOFF)

<!-- Écran dynamique répété 28 fois -->

## SCR_PREP_RES_BLANC_TRANS

### Deuxième partie

<!-- Règle métier : Annoncer les 12 mises en situation -->

1. [Commencer les mises en situation](SCR_PREP_RES_BLANC_MIS)

## SCR_PREP_RES_BLANC_MIS

### Situation {numero_situation} sur 12

<!-- Variables : {numero_situation}; {id_situation}; {reponses_examen} -->

<!-- Règle métier : Tirer 6 situations T1 et 6 situations T3 sans doublon -->

**Réponse attendue :** Choix unique

<!-- Condition métier : Situation courante = 12 -->
1. [Calculer les résultats](SCR_PREP_RES_BLANC_CALC)
<!-- Condition métier : Situation courante < 12 -->
2. [Valider et continuer](SCR_PREP_RES_BLANC_MIS)

<!-- Écran dynamique répété 12 fois -->

## SCR_PREP_RES_BLANC_CALC

### Calcul des résultats

<!-- Variables : {score_total}; {score_qoff}; {score_mis}; {pourcentage} -->

<!-- Règle métier : Corriger les 40 réponses et calculer les scores -->

<!-- Condition métier : Calcul terminé -->
1. [Afficher le résultat](SCR_PREP_RES_BLANC_RESULT)

<!-- Écran logique non affiché -->

## SCR_PREP_RES_BLANC_RESULT

### Résultat de l’examen blanc

<!-- Variables : {score_total}; {score_qoff}; {score_mis}; {pourcentage} -->

Votre score total est de {score_total} sur 40. Questions officielles : {score_qoff}/28. Mises en situation : {score_mis}/12.

1. [Voir le détail des réponses](SCR_PREP_RES_BLANC_DETAIL)

## SCR_PREP_RES_BLANC_DETAIL

### Détail de vos réponses

<!-- Variables : {reponses_examen} -->

<!-- Règle métier : Afficher bonnes réponses et explications après la fin -->

1. [🔄 Recommencer](SCR_PREP_RES_BLANC_INTRO)
2. [⬅️ Retour à l’examen](SCR_PREP_RES_MENU)
3. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Prévoir pagination -->

## SCR_PREP_RES_MIS_INTRO

### Mises en situation

<!-- Variables : {type_examen} -->

Vous allez répondre à 10 mises en situation : 2 pour chacune des cinq thématiques. Une correction est proposée après chaque réponse.

1. [Commencer](SCR_PREP_RES_MIS_INIT)

## SCR_PREP_RES_MIS_INIT

### Préparation du tirage

<!-- Variables : {{session_id}}; {{deja_tires}} -->

<!-- Règle métier : Créer le tirage de 10 situations selon 2/2/2/2/2 -->

<!-- Condition métier : Tirage valide -->
1. [Lancer les situations](SCR_PREP_RES_MIS_RUN)

<!-- Écran logique non affiché -->

## SCR_PREP_RES_MIS_RUN

### Situation {numero_situation} sur 10

<!-- Variables : {numero_situation}; {id_situation}; {theme_situation}; {score} -->

<!-- Règle métier : Tirer sans doublon dans le thème attendu -->

**Réponse attendue :** Choix unique

<!-- Condition métier : Réponse sélectionnée -->
1. [Valider ma réponse](SCR_PREP_RES_MIS_CORR)

<!-- Écran dynamique répété 10 fois -->

## SCR_PREP_RES_MIS_CORR

### Correction

<!-- Variables : {bonne_reponse}; {explication}; {score} -->

<!-- Règle métier : Afficher résultat de la réponse et explication -->

<!-- Condition métier : Situation courante < 10 -->
1. [Situation suivante](SCR_PREP_RES_MIS_RUN)
<!-- Condition métier : Situation courante = 10 -->
2. [Voir mon résultat](SCR_PREP_RES_MIS_RESULT)

## SCR_PREP_RES_MIS_RESULT

### Votre résultat

<!-- Variables : {score}; {pourcentage} -->

Vous avez obtenu {score} bonne(s) réponse(s) sur 10, soit {pourcentage} %.

1. [🔄 Recommencer](SCR_PREP_RES_MIS_INTRO)
2. [⬅️ Retour à l’examen](SCR_PREP_RES_MENU)
3. [🏠 Retour au menu principal](MENU_PRINCIPAL)

## SCR_PREP_RES_QOFF_INTRO

### Questions officielles

<!-- Variables : {type_examen} -->

Vous allez répondre à 28 questions tirées aléatoirement selon la répartition officielle. Une correction est proposée après chaque réponse.

1. [Commencer](SCR_PREP_RES_QOFF_INIT)

## SCR_PREP_RES_QOFF_INIT

### Préparation du tirage

<!-- Variables : {{session_id}}; {{deja_tires}} -->

<!-- Règle métier : Créer le tirage de 28 questions selon 5/6/5/8/4 -->

<!-- Condition métier : Tirage valide -->
1. [Lancer le questionnaire](SCR_PREP_RES_QOFF_RUN)

<!-- Écran logique non affiché -->

## SCR_PREP_RES_QOFF_RUN

### Question {numero_question} sur 28

<!-- Variables : {numero_question}; {id_question}; {theme_question}; {score} -->

<!-- Règle métier : Tirer sans doublon dans le thème attendu -->

**Réponse attendue :** Choix unique

<!-- Condition métier : Réponse sélectionnée -->
1. [Valider ma réponse](SCR_PREP_RES_QOFF_CORR)

<!-- Écran dynamique répété 28 fois -->

## SCR_PREP_RES_QOFF_CORR

### Correction

<!-- Variables : {bonne_reponse}; {explication}; {score} -->

<!-- Règle métier : Afficher résultat de la réponse et explication -->

<!-- Condition métier : Question courante < 28 -->
1. [Question suivante](SCR_PREP_RES_QOFF_RUN)
<!-- Condition métier : Question courante = 28 -->
2. [Voir mon résultat](SCR_PREP_RES_QOFF_RESULT)

## SCR_PREP_RES_QOFF_RESULT

### Votre résultat

<!-- Variables : {score}; {pourcentage} -->

Vous avez obtenu {score} bonne(s) réponse(s) sur 28, soit {pourcentage} %.

1. [🔄 Recommencer](SCR_PREP_RES_QOFF_INTRO)
2. [⬅️ Retour à l’examen](SCR_PREP_RES_MENU)
3. [🏠 Retour au menu principal](MENU_PRINCIPAL)

## SCR_PREP_CSP_MENU

### Carte de séjour pluriannuelle

<!-- Variables : {type_examen} -->

Comment souhaitez-vous vous entraîner ?

1. [📝 Je réponds aux questions officielles](SCR_PREP_CSP_QOFF_INTRO)
2. [🎭 Je réponds à des mises en situation](SCR_PREP_CSP_MIS_INTRO)
3. [🎓 Je passe un examen blanc complet](SCR_PREP_CSP_BLANC_INTRO)
4. [⬅️ Retour au choix de l’examen](SCR_PREP_MENU)
5. [🏠 Retour au menu principal](MENU_PRINCIPAL)

## SCR_PREP_CSP_BLANC_INTRO

### Examen blanc complet

<!-- Variables : {type_examen} -->

L’examen blanc comprend 28 questions officielles et 12 mises en situation. Les corrections sont affichées seulement à la fin.

1. [Commencer l’examen blanc](SCR_PREP_CSP_BLANC_INIT)

## SCR_PREP_CSP_BLANC_INIT

### Préparation de l’examen blanc

<!-- Variables : {{session_id}}; {{deja_tires}} -->

<!-- Règle métier : Créer le tirage complet de 40 éléments -->

<!-- Condition métier : Tirage valide -->
1. [Lancer la première partie](SCR_PREP_CSP_BLANC_QOFF)

<!-- Écran logique non affiché -->

## SCR_PREP_CSP_BLANC_QOFF

### Question {numero_question} sur 28

<!-- Variables : {numero_question}; {id_question}; {reponses_examen} -->

<!-- Règle métier : Enregistrer la réponse sans afficher la correction -->

**Réponse attendue :** Choix unique

<!-- Condition métier : Question courante = 28 -->
1. [Terminer la première partie](SCR_PREP_CSP_BLANC_TRANS)
<!-- Condition métier : Question courante < 28 -->
2. [Valider et continuer](SCR_PREP_CSP_BLANC_QOFF)

<!-- Écran dynamique répété 28 fois -->

## SCR_PREP_CSP_BLANC_TRANS

### Deuxième partie

<!-- Règle métier : Annoncer les 12 mises en situation -->

1. [Commencer les mises en situation](SCR_PREP_CSP_BLANC_MIS)

## SCR_PREP_CSP_BLANC_MIS

### Situation {numero_situation} sur 12

<!-- Variables : {numero_situation}; {id_situation}; {reponses_examen} -->

<!-- Règle métier : Tirer 6 situations T1 et 6 situations T3 sans doublon -->

**Réponse attendue :** Choix unique

<!-- Condition métier : Situation courante = 12 -->
1. [Calculer les résultats](SCR_PREP_CSP_BLANC_CALC)
<!-- Condition métier : Situation courante < 12 -->
2. [Valider et continuer](SCR_PREP_CSP_BLANC_MIS)

<!-- Écran dynamique répété 12 fois -->

## SCR_PREP_CSP_BLANC_CALC

### Calcul des résultats

<!-- Variables : {score_total}; {score_qoff}; {score_mis}; {pourcentage} -->

<!-- Règle métier : Corriger les 40 réponses et calculer les scores -->

<!-- Condition métier : Calcul terminé -->
1. [Afficher le résultat](SCR_PREP_CSP_BLANC_RESULT)

<!-- Écran logique non affiché -->

## SCR_PREP_CSP_BLANC_RESULT

### Résultat de l’examen blanc

<!-- Variables : {score_total}; {score_qoff}; {score_mis}; {pourcentage} -->

Votre score total est de {score_total} sur 40. Questions officielles : {score_qoff}/28. Mises en situation : {score_mis}/12.

1. [Voir le détail des réponses](SCR_PREP_CSP_BLANC_DETAIL)

## SCR_PREP_CSP_BLANC_DETAIL

### Détail de vos réponses

<!-- Variables : {reponses_examen} -->

<!-- Règle métier : Afficher bonnes réponses et explications après la fin -->

1. [🔄 Recommencer](SCR_PREP_CSP_BLANC_INTRO)
2. [⬅️ Retour à l’examen](SCR_PREP_CSP_MENU)
3. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Prévoir pagination -->

## SCR_PREP_CSP_MIS_INTRO

### Mises en situation

<!-- Variables : {type_examen} -->

Vous allez répondre à 10 mises en situation : 2 pour chacune des cinq thématiques. Une correction est proposée après chaque réponse.

1. [Commencer](SCR_PREP_CSP_MIS_INIT)

## SCR_PREP_CSP_MIS_INIT

### Préparation du tirage

<!-- Variables : {{session_id}}; {{deja_tires}} -->

<!-- Règle métier : Créer le tirage de 10 situations selon 2/2/2/2/2 -->

<!-- Condition métier : Tirage valide -->
1. [Lancer les situations](SCR_PREP_CSP_MIS_RUN)

<!-- Écran logique non affiché -->

## SCR_PREP_CSP_MIS_RUN

### Situation {numero_situation} sur 10

<!-- Variables : {numero_situation}; {id_situation}; {theme_situation}; {score} -->

<!-- Règle métier : Tirer sans doublon dans le thème attendu -->

**Réponse attendue :** Choix unique

<!-- Condition métier : Réponse sélectionnée -->
1. [Valider ma réponse](SCR_PREP_CSP_MIS_CORR)

<!-- Écran dynamique répété 10 fois -->

## SCR_PREP_CSP_MIS_CORR

### Correction

<!-- Variables : {bonne_reponse}; {explication}; {score} -->

<!-- Règle métier : Afficher résultat de la réponse et explication -->

<!-- Condition métier : Situation courante < 10 -->
1. [Situation suivante](SCR_PREP_CSP_MIS_RUN)
<!-- Condition métier : Situation courante = 10 -->
2. [Voir mon résultat](SCR_PREP_CSP_MIS_RESULT)

## SCR_PREP_CSP_MIS_RESULT

### Votre résultat

<!-- Variables : {score}; {pourcentage} -->

Vous avez obtenu {score} bonne(s) réponse(s) sur 10, soit {pourcentage} %.

1. [🔄 Recommencer](SCR_PREP_CSP_MIS_INTRO)
2. [⬅️ Retour à l’examen](SCR_PREP_CSP_MENU)
3. [🏠 Retour au menu principal](MENU_PRINCIPAL)

## SCR_PREP_CSP_QOFF_INTRO

### Questions officielles

<!-- Variables : {type_examen} -->

Vous allez répondre à 28 questions tirées aléatoirement selon la répartition officielle. Une correction est proposée après chaque réponse.

1. [Commencer](SCR_PREP_CSP_QOFF_INIT)

## SCR_PREP_CSP_QOFF_INIT

### Préparation du tirage

<!-- Variables : {{session_id}}; {{deja_tires}} -->

<!-- Règle métier : Créer le tirage de 28 questions selon 5/6/5/8/4 -->

<!-- Condition métier : Tirage valide -->
1. [Lancer le questionnaire](SCR_PREP_CSP_QOFF_RUN)

<!-- Écran logique non affiché -->

## SCR_PREP_CSP_QOFF_RUN

### Question {numero_question} sur 28

<!-- Variables : {numero_question}; {id_question}; {theme_question}; {score} -->

<!-- Règle métier : Tirer sans doublon dans le thème attendu -->

**Réponse attendue :** Choix unique

<!-- Condition métier : Réponse sélectionnée -->
1. [Valider ma réponse](SCR_PREP_CSP_QOFF_CORR)

<!-- Écran dynamique répété 28 fois -->

## SCR_PREP_CSP_QOFF_CORR

### Correction

<!-- Variables : {bonne_reponse}; {explication}; {score} -->

<!-- Règle métier : Afficher résultat de la réponse et explication -->

<!-- Condition métier : Question courante < 28 -->
1. [Question suivante](SCR_PREP_CSP_QOFF_RUN)
<!-- Condition métier : Question courante = 28 -->
2. [Voir mon résultat](SCR_PREP_CSP_QOFF_RESULT)

## SCR_PREP_CSP_QOFF_RESULT

### Votre résultat

<!-- Variables : {score}; {pourcentage} -->

Vous avez obtenu {score} bonne(s) réponse(s) sur 28, soit {pourcentage} %.

1. [🔄 Recommencer](SCR_PREP_CSP_QOFF_INTRO)
2. [⬅️ Retour à l’examen](SCR_PREP_CSP_MENU)
3. [🏠 Retour au menu principal](MENU_PRINCIPAL)

## SCR_PREP_MENU

### Préparer mon examen

Choisissez l’examen que vous souhaitez préparer.

1. [Carte de résident](SCR_PREP_RES_MENU)
2. [Carte de séjour pluriannuelle](SCR_PREP_CSP_MENU)
3. [Naturalisation](SCR_PREP_NAT_MENU)
4. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran d’entrée depuis le menu principal -->

## SCR_PREP_NAT_MENU

### Naturalisation

<!-- Variables : {type_examen} -->

Comment souhaitez-vous vous entraîner ?

1. [📝 Je réponds aux questions officielles](SCR_PREP_NAT_QOFF_INTRO)
2. [🎭 Je réponds à des mises en situation](SCR_PREP_NAT_MIS_INTRO)
3. [🎓 Je passe un examen blanc complet](SCR_PREP_NAT_BLANC_INTRO)
4. [⬅️ Retour au choix de l’examen](SCR_PREP_MENU)
5. [🏠 Retour au menu principal](MENU_PRINCIPAL)

## SCR_PREP_NAT_BLANC_INTRO

### Examen blanc complet

<!-- Variables : {type_examen} -->

L’examen blanc comprend 28 questions officielles et 12 mises en situation. Les corrections sont affichées seulement à la fin.

1. [Commencer l’examen blanc](SCR_PREP_NAT_BLANC_INIT)

## SCR_PREP_NAT_BLANC_INIT

### Préparation de l’examen blanc

<!-- Variables : {{session_id}}; {{deja_tires}} -->

<!-- Règle métier : Créer le tirage complet de 40 éléments -->

<!-- Condition métier : Tirage valide -->
1. [Lancer la première partie](SCR_PREP_NAT_BLANC_QOFF)

<!-- Écran logique non affiché -->

## SCR_PREP_NAT_BLANC_QOFF

### Question {numero_question} sur 28

<!-- Variables : {numero_question}; {id_question}; {reponses_examen} -->

<!-- Règle métier : Enregistrer la réponse sans afficher la correction -->

**Réponse attendue :** Choix unique

<!-- Condition métier : Question courante = 28 -->
1. [Terminer la première partie](SCR_PREP_NAT_BLANC_TRANS)
<!-- Condition métier : Question courante < 28 -->
2. [Valider et continuer](SCR_PREP_NAT_BLANC_QOFF)

<!-- Écran dynamique répété 28 fois -->

## SCR_PREP_NAT_BLANC_TRANS

### Deuxième partie

<!-- Règle métier : Annoncer les 12 mises en situation -->

1. [Commencer les mises en situation](SCR_PREP_NAT_BLANC_MIS)

## SCR_PREP_NAT_BLANC_MIS

### Situation {numero_situation} sur 12

<!-- Variables : {numero_situation}; {id_situation}; {reponses_examen} -->

<!-- Règle métier : Tirer 6 situations T1 et 6 situations T3 sans doublon -->

**Réponse attendue :** Choix unique

<!-- Condition métier : Situation courante = 12 -->
1. [Calculer les résultats](SCR_PREP_NAT_BLANC_CALC)
<!-- Condition métier : Situation courante < 12 -->
2. [Valider et continuer](SCR_PREP_NAT_BLANC_MIS)

<!-- Écran dynamique répété 12 fois -->

## SCR_PREP_NAT_BLANC_CALC

### Calcul des résultats

<!-- Variables : {score_total}; {score_qoff}; {score_mis}; {pourcentage} -->

<!-- Règle métier : Corriger les 40 réponses et calculer les scores -->

<!-- Condition métier : Calcul terminé -->
1. [Afficher le résultat](SCR_PREP_NAT_BLANC_RESULT)

<!-- Écran logique non affiché -->

## SCR_PREP_NAT_BLANC_RESULT

### Résultat de l’examen blanc

<!-- Variables : {score_total}; {score_qoff}; {score_mis}; {pourcentage} -->

Votre score total est de {score_total} sur 40. Questions officielles : {score_qoff}/28. Mises en situation : {score_mis}/12.

1. [Voir le détail des réponses](SCR_PREP_NAT_BLANC_DETAIL)

## SCR_PREP_NAT_BLANC_DETAIL

### Détail de vos réponses

<!-- Variables : {reponses_examen} -->

<!-- Règle métier : Afficher bonnes réponses et explications après la fin -->

1. [🔄 Recommencer](SCR_PREP_NAT_BLANC_INTRO)
2. [⬅️ Retour à l’examen](SCR_PREP_NAT_MENU)
3. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Prévoir pagination -->

## SCR_PREP_NAT_MIS_INTRO

### Mises en situation

<!-- Variables : {type_examen} -->

Vous allez répondre à 10 mises en situation : 2 pour chacune des cinq thématiques. Une correction est proposée après chaque réponse.

1. [Commencer](SCR_PREP_NAT_MIS_INIT)

## SCR_PREP_NAT_MIS_INIT

### Préparation du tirage

<!-- Variables : {{session_id}}; {{deja_tires}} -->

<!-- Règle métier : Créer le tirage de 10 situations selon 2/2/2/2/2 -->

<!-- Condition métier : Tirage valide -->
1. [Lancer les situations](SCR_PREP_NAT_MIS_RUN)

<!-- Écran logique non affiché -->

## SCR_PREP_NAT_MIS_RUN

### Situation {numero_situation} sur 10

<!-- Variables : {numero_situation}; {id_situation}; {theme_situation}; {score} -->

<!-- Règle métier : Tirer sans doublon dans le thème attendu -->

**Réponse attendue :** Choix unique

<!-- Condition métier : Réponse sélectionnée -->
1. [Valider ma réponse](SCR_PREP_NAT_MIS_CORR)

<!-- Écran dynamique répété 10 fois -->

## SCR_PREP_NAT_MIS_CORR

### Correction

<!-- Variables : {bonne_reponse}; {explication}; {score} -->

<!-- Règle métier : Afficher résultat de la réponse et explication -->

<!-- Condition métier : Situation courante < 10 -->
1. [Situation suivante](SCR_PREP_NAT_MIS_RUN)
<!-- Condition métier : Situation courante = 10 -->
2. [Voir mon résultat](SCR_PREP_NAT_MIS_RESULT)

## SCR_PREP_NAT_MIS_RESULT

### Votre résultat

<!-- Variables : {score}; {pourcentage} -->

Vous avez obtenu {score} bonne(s) réponse(s) sur 10, soit {pourcentage} %.

1. [🔄 Recommencer](SCR_PREP_NAT_MIS_INTRO)
2. [⬅️ Retour à l’examen](SCR_PREP_NAT_MENU)
3. [🏠 Retour au menu principal](MENU_PRINCIPAL)

## SCR_PREP_NAT_QOFF_INTRO

### Questions officielles

<!-- Variables : {type_examen} -->

Vous allez répondre à 28 questions tirées aléatoirement selon la répartition officielle. Une correction est proposée après chaque réponse.

1. [Commencer](SCR_PREP_NAT_QOFF_INIT)

## SCR_PREP_NAT_QOFF_INIT

### Préparation du tirage

<!-- Variables : {{session_id}}; {{deja_tires}} -->

<!-- Règle métier : Créer le tirage de 28 questions selon 5/6/5/8/4 -->

<!-- Condition métier : Tirage valide -->
1. [Lancer le questionnaire](SCR_PREP_NAT_QOFF_RUN)

<!-- Écran logique non affiché -->

## SCR_PREP_NAT_QOFF_RUN

### Question {numero_question} sur 28

<!-- Variables : {numero_question}; {id_question}; {theme_question}; {score} -->

<!-- Règle métier : Tirer sans doublon dans le thème attendu -->

**Réponse attendue :** Choix unique

<!-- Condition métier : Réponse sélectionnée -->
1. [Valider ma réponse](SCR_PREP_NAT_QOFF_CORR)

<!-- Écran dynamique répété 28 fois -->

## SCR_PREP_NAT_QOFF_CORR

### Correction

<!-- Variables : {bonne_reponse}; {explication}; {score} -->

<!-- Règle métier : Afficher résultat de la réponse et explication -->

<!-- Condition métier : Question courante < 28 -->
1. [Question suivante](SCR_PREP_NAT_QOFF_RUN)
<!-- Condition métier : Question courante = 28 -->
2. [Voir mon résultat](SCR_PREP_NAT_QOFF_RESULT)

## SCR_PREP_NAT_QOFF_RESULT

### Votre résultat

<!-- Variables : {score}; {pourcentage} -->

Vous avez obtenu {score} bonne(s) réponse(s) sur 28, soit {pourcentage} %.

1. [🔄 Recommencer](SCR_PREP_NAT_QOFF_INTRO)
2. [⬅️ Retour à l’examen](SCR_PREP_NAT_MENU)
3. [🏠 Retour au menu principal](MENU_PRINCIPAL)
