<!-- Module généré automatiquement : M’entraîner -->
<!-- Date : 2026-08-03T13:13:33+02:00 -->

## SCR_ENT_CR_T1_QOFF_INTRO

### Questions officielles

<!-- Variables : {theme}=T1 -->

Vous allez répondre à 10 questions officielles de la thématique choisie. Une correction est affichée après chaque réponse.

1. [Commencer](SCR_ENT_CR_T1_QOFF_INIT)

## SCR_ENT_CR_T1_QOFF_INIT

### Préparation du tirage

<!-- Variables : {{session_id}}; {{deja_tires}} -->

<!-- Règle métier : Créer un tirage de 10 questions actives sans doublon -->

<!-- Condition métier : Tirage valide -->
1. [Lancer l’entraînement](SCR_ENT_CR_T1_QOFF_RUN)

<!-- Écran logique non affiché -->

## SCR_ENT_CR_T1_QOFF_RUN

### Question {numero} sur 10

<!-- Variables : {id_question}; {numero}; {score} -->

<!-- Règle métier : Afficher QUESTION et réponses A à D -->

**Réponse attendue :** Choix unique

<!-- Condition métier : Réponse sélectionnée -->
1. [Valider ma réponse](SCR_ENT_CR_T1_QOFF_CORR)

<!-- Écran dynamique -->

## SCR_ENT_CR_T1_QOFF_CORR

### Correction

<!-- Variables : {bonne_reponse}; {explication}; {score} -->

<!-- Règle métier : Afficher bonne réponse, explication et astuce mémoire -->

<!-- Condition métier : Question courante < 10 -->
1. [Question suivante](SCR_ENT_CR_T1_QOFF_RUN)
<!-- Condition métier : Question courante = 10 -->
2. [Voir mon résultat](SCR_ENT_CR_T1_QOFF_RESULT)

## SCR_ENT_CR_T1_QOFF_RESULT

### Votre résultat

<!-- Variables : {score}; {pourcentage} -->

Vous avez obtenu {score} bonne(s) réponse(s) sur 10, soit {pourcentage} %.

1. [🔄 Recommencer](SCR_ENT_CR_T1_QOFF_INTRO)
2. [⬅️ Retour au choix du mode](SCR_ENT_CR_T1_MODE)
3. [🏠 Retour au menu](MENU_PRINCIPAL)

## SCR_ENT_CR_T1_MIS_INTRO

### Mises en situation

<!-- Variables : {theme}=T1 -->

Vous allez répondre à 10 mises en situation de la thématique choisie. Une correction est affichée après chaque réponse.

1. [Commencer](SCR_ENT_CR_T1_MIS_INIT)

## SCR_ENT_CR_T1_MIS_INIT

### Préparation du tirage

<!-- Variables : {{session_id}}; {{deja_tires}} -->

<!-- Règle métier : Créer un tirage de 10 situations sans doublon -->

<!-- Condition métier : Tirage valide -->
1. [Lancer l’entraînement](SCR_ENT_CR_T1_MIS_RUN)

<!-- Écran logique non affiché -->

## SCR_ENT_CR_T1_MIS_RUN

### Situation {numero} sur 10

<!-- Variables : {id_situation}; {numero}; {score} -->

<!-- Règle métier : Afficher la situation, la question et les réponses A à D -->

**Réponse attendue :** Choix unique

<!-- Condition métier : Réponse sélectionnée -->
1. [Valider ma réponse](SCR_ENT_CR_T1_MIS_CORR)

<!-- Écran dynamique -->

## SCR_ENT_CR_T1_MIS_CORR

### Correction

<!-- Variables : {bonne_reponse}; {explication}; {score} -->

<!-- Règle métier : Afficher bonne réponse et feedback pédagogique -->

<!-- Condition métier : Situation courante < 10 -->
1. [Situation suivante](SCR_ENT_CR_T1_MIS_RUN)
<!-- Condition métier : Situation courante = 10 -->
2. [Voir mon résultat](SCR_ENT_CR_T1_MIS_RESULT)

## SCR_ENT_CR_T1_MIS_RESULT

### Votre résultat

<!-- Variables : {score}; {pourcentage} -->

Vous avez obtenu {score} bonne(s) réponse(s) sur 10, soit {pourcentage} %.

1. [🔄 Recommencer](SCR_ENT_CR_T1_MIS_INTRO)
2. [⬅️ Retour au choix du mode](SCR_ENT_CR_T1_MODE)
3. [🏠 Retour au menu](MENU_PRINCIPAL)

## SCR_ENT_CR_T2_QOFF_INTRO

### Questions officielles

<!-- Variables : {theme}=T2 -->

Vous allez répondre à 10 questions officielles de la thématique choisie. Une correction est affichée après chaque réponse.

1. [Commencer](SCR_ENT_CR_T2_QOFF_INIT)

## SCR_ENT_CR_T2_QOFF_INIT

### Préparation du tirage

<!-- Variables : {{session_id}}; {{deja_tires}} -->

<!-- Règle métier : Créer un tirage de 10 questions actives sans doublon -->

<!-- Condition métier : Tirage valide -->
1. [Lancer l’entraînement](SCR_ENT_CR_T2_QOFF_RUN)

<!-- Écran logique non affiché -->

## SCR_ENT_CR_T2_QOFF_RUN

### Question {numero} sur 10

<!-- Variables : {id_question}; {numero}; {score} -->

<!-- Règle métier : Afficher QUESTION et réponses A à D -->

**Réponse attendue :** Choix unique

<!-- Condition métier : Réponse sélectionnée -->
1. [Valider ma réponse](SCR_ENT_CR_T2_QOFF_CORR)

<!-- Écran dynamique -->

## SCR_ENT_CR_T2_QOFF_CORR

### Correction

<!-- Variables : {bonne_reponse}; {explication}; {score} -->

<!-- Règle métier : Afficher bonne réponse, explication et astuce mémoire -->

<!-- Condition métier : Question courante < 10 -->
1. [Question suivante](SCR_ENT_CR_T2_QOFF_RUN)
<!-- Condition métier : Question courante = 10 -->
2. [Voir mon résultat](SCR_ENT_CR_T2_QOFF_RESULT)

## SCR_ENT_CR_T2_QOFF_RESULT

### Votre résultat

<!-- Variables : {score}; {pourcentage} -->

Vous avez obtenu {score} bonne(s) réponse(s) sur 10, soit {pourcentage} %.

1. [🔄 Recommencer](SCR_ENT_CR_T2_QOFF_INTRO)
2. [⬅️ Retour au choix du mode](SCR_ENT_CR_T2_MODE)
3. [🏠 Retour au menu](MENU_PRINCIPAL)

## SCR_ENT_CR_T2_MIS_INTRO

### Mises en situation

<!-- Variables : {theme}=T2 -->

Vous allez répondre à 10 mises en situation de la thématique choisie. Une correction est affichée après chaque réponse.

1. [Commencer](SCR_ENT_CR_T2_MIS_INIT)

## SCR_ENT_CR_T2_MIS_INIT

### Préparation du tirage

<!-- Variables : {{session_id}}; {{deja_tires}} -->

<!-- Règle métier : Créer un tirage de 10 situations sans doublon -->

<!-- Condition métier : Tirage valide -->
1. [Lancer l’entraînement](SCR_ENT_CR_T2_MIS_RUN)

<!-- Écran logique non affiché -->

## SCR_ENT_CR_T2_MIS_RUN

### Situation {numero} sur 10

<!-- Variables : {id_situation}; {numero}; {score} -->

<!-- Règle métier : Afficher la situation, la question et les réponses A à D -->

**Réponse attendue :** Choix unique

<!-- Condition métier : Réponse sélectionnée -->
1. [Valider ma réponse](SCR_ENT_CR_T2_MIS_CORR)

<!-- Écran dynamique -->

## SCR_ENT_CR_T2_MIS_CORR

### Correction

<!-- Variables : {bonne_reponse}; {explication}; {score} -->

<!-- Règle métier : Afficher bonne réponse et feedback pédagogique -->

<!-- Condition métier : Situation courante < 10 -->
1. [Situation suivante](SCR_ENT_CR_T2_MIS_RUN)
<!-- Condition métier : Situation courante = 10 -->
2. [Voir mon résultat](SCR_ENT_CR_T2_MIS_RESULT)

## SCR_ENT_CR_T2_MIS_RESULT

### Votre résultat

<!-- Variables : {score}; {pourcentage} -->

Vous avez obtenu {score} bonne(s) réponse(s) sur 10, soit {pourcentage} %.

1. [🔄 Recommencer](SCR_ENT_CR_T2_MIS_INTRO)
2. [⬅️ Retour au choix du mode](SCR_ENT_CR_T2_MODE)
3. [🏠 Retour au menu](MENU_PRINCIPAL)

## SCR_ENT_CR_T3_QOFF_INTRO

### Questions officielles

<!-- Variables : {theme}=T3 -->

Vous allez répondre à 10 questions officielles de la thématique choisie. Une correction est affichée après chaque réponse.

1. [Commencer](SCR_ENT_CR_T3_QOFF_INIT)

## SCR_ENT_CR_T3_QOFF_INIT

### Préparation du tirage

<!-- Variables : {{session_id}}; {{deja_tires}} -->

<!-- Règle métier : Créer un tirage de 10 questions actives sans doublon -->

<!-- Condition métier : Tirage valide -->
1. [Lancer l’entraînement](SCR_ENT_CR_T3_QOFF_RUN)

<!-- Écran logique non affiché -->

## SCR_ENT_CR_T3_QOFF_RUN

### Question {numero} sur 10

<!-- Variables : {id_question}; {numero}; {score} -->

<!-- Règle métier : Afficher QUESTION et réponses A à D -->

**Réponse attendue :** Choix unique

<!-- Condition métier : Réponse sélectionnée -->
1. [Valider ma réponse](SCR_ENT_CR_T3_QOFF_CORR)

<!-- Écran dynamique -->

## SCR_ENT_CR_T3_QOFF_CORR

### Correction

<!-- Variables : {bonne_reponse}; {explication}; {score} -->

<!-- Règle métier : Afficher bonne réponse, explication et astuce mémoire -->

<!-- Condition métier : Question courante < 10 -->
1. [Question suivante](SCR_ENT_CR_T3_QOFF_RUN)
<!-- Condition métier : Question courante = 10 -->
2. [Voir mon résultat](SCR_ENT_CR_T3_QOFF_RESULT)

## SCR_ENT_CR_T3_QOFF_RESULT

### Votre résultat

<!-- Variables : {score}; {pourcentage} -->

Vous avez obtenu {score} bonne(s) réponse(s) sur 10, soit {pourcentage} %.

1. [🔄 Recommencer](SCR_ENT_CR_T3_QOFF_INTRO)
2. [⬅️ Retour au choix du mode](SCR_ENT_CR_T3_MODE)
3. [🏠 Retour au menu](MENU_PRINCIPAL)

## SCR_ENT_CR_T3_MIS_INTRO

### Mises en situation

<!-- Variables : {theme}=T3 -->

Vous allez répondre à 10 mises en situation de la thématique choisie. Une correction est affichée après chaque réponse.

1. [Commencer](SCR_ENT_CR_T3_MIS_INIT)

## SCR_ENT_CR_T3_MIS_INIT

### Préparation du tirage

<!-- Variables : {{session_id}}; {{deja_tires}} -->

<!-- Règle métier : Créer un tirage de 10 situations sans doublon -->

<!-- Condition métier : Tirage valide -->
1. [Lancer l’entraînement](SCR_ENT_CR_T3_MIS_RUN)

<!-- Écran logique non affiché -->

## SCR_ENT_CR_T3_MIS_RUN

### Situation {numero} sur 10

<!-- Variables : {id_situation}; {numero}; {score} -->

<!-- Règle métier : Afficher la situation, la question et les réponses A à D -->

**Réponse attendue :** Choix unique

<!-- Condition métier : Réponse sélectionnée -->
1. [Valider ma réponse](SCR_ENT_CR_T3_MIS_CORR)

<!-- Écran dynamique -->

## SCR_ENT_CR_T3_MIS_CORR

### Correction

<!-- Variables : {bonne_reponse}; {explication}; {score} -->

<!-- Règle métier : Afficher bonne réponse et feedback pédagogique -->

<!-- Condition métier : Situation courante < 10 -->
1. [Situation suivante](SCR_ENT_CR_T3_MIS_RUN)
<!-- Condition métier : Situation courante = 10 -->
2. [Voir mon résultat](SCR_ENT_CR_T3_MIS_RESULT)

## SCR_ENT_CR_T3_MIS_RESULT

### Votre résultat

<!-- Variables : {score}; {pourcentage} -->

Vous avez obtenu {score} bonne(s) réponse(s) sur 10, soit {pourcentage} %.

1. [🔄 Recommencer](SCR_ENT_CR_T3_MIS_INTRO)
2. [⬅️ Retour au choix du mode](SCR_ENT_CR_T3_MODE)
3. [🏠 Retour au menu](MENU_PRINCIPAL)

## SCR_ENT_CR_T4_QOFF_INTRO

### Questions officielles

<!-- Variables : {theme}=T4 -->

Vous allez répondre à 10 questions officielles de la thématique choisie. Une correction est affichée après chaque réponse.

1. [Commencer](SCR_ENT_CR_T4_QOFF_INIT)

## SCR_ENT_CR_T4_QOFF_INIT

### Préparation du tirage

<!-- Variables : {{session_id}}; {{deja_tires}} -->

<!-- Règle métier : Créer un tirage de 10 questions actives sans doublon -->

<!-- Condition métier : Tirage valide -->
1. [Lancer l’entraînement](SCR_ENT_CR_T4_QOFF_RUN)

<!-- Écran logique non affiché -->

## SCR_ENT_CR_T4_QOFF_RUN

### Question {numero} sur 10

<!-- Variables : {id_question}; {numero}; {score} -->

<!-- Règle métier : Afficher QUESTION et réponses A à D -->

**Réponse attendue :** Choix unique

<!-- Condition métier : Réponse sélectionnée -->
1. [Valider ma réponse](SCR_ENT_CR_T4_QOFF_CORR)

<!-- Écran dynamique -->

## SCR_ENT_CR_T4_QOFF_CORR

### Correction

<!-- Variables : {bonne_reponse}; {explication}; {score} -->

<!-- Règle métier : Afficher bonne réponse, explication et astuce mémoire -->

<!-- Condition métier : Question courante < 10 -->
1. [Question suivante](SCR_ENT_CR_T4_QOFF_RUN)
<!-- Condition métier : Question courante = 10 -->
2. [Voir mon résultat](SCR_ENT_CR_T4_QOFF_RESULT)

## SCR_ENT_CR_T4_QOFF_RESULT

### Votre résultat

<!-- Variables : {score}; {pourcentage} -->

Vous avez obtenu {score} bonne(s) réponse(s) sur 10, soit {pourcentage} %.

1. [🔄 Recommencer](SCR_ENT_CR_T4_QOFF_INTRO)
2. [⬅️ Retour au choix du mode](SCR_ENT_CR_T4_MODE)
3. [🏠 Retour au menu](MENU_PRINCIPAL)

## SCR_ENT_CR_T4_MIS_INTRO

### Mises en situation

<!-- Variables : {theme}=T4 -->

Vous allez répondre à 10 mises en situation de la thématique choisie. Une correction est affichée après chaque réponse.

1. [Commencer](SCR_ENT_CR_T4_MIS_INIT)

## SCR_ENT_CR_T4_MIS_INIT

### Préparation du tirage

<!-- Variables : {{session_id}}; {{deja_tires}} -->

<!-- Règle métier : Créer un tirage de 10 situations sans doublon -->

<!-- Condition métier : Tirage valide -->
1. [Lancer l’entraînement](SCR_ENT_CR_T4_MIS_RUN)

<!-- Écran logique non affiché -->

## SCR_ENT_CR_T4_MIS_RUN

### Situation {numero} sur 10

<!-- Variables : {id_situation}; {numero}; {score} -->

<!-- Règle métier : Afficher la situation, la question et les réponses A à D -->

**Réponse attendue :** Choix unique

<!-- Condition métier : Réponse sélectionnée -->
1. [Valider ma réponse](SCR_ENT_CR_T4_MIS_CORR)

<!-- Écran dynamique -->

## SCR_ENT_CR_T4_MIS_CORR

### Correction

<!-- Variables : {bonne_reponse}; {explication}; {score} -->

<!-- Règle métier : Afficher bonne réponse et feedback pédagogique -->

<!-- Condition métier : Situation courante < 10 -->
1. [Situation suivante](SCR_ENT_CR_T4_MIS_RUN)
<!-- Condition métier : Situation courante = 10 -->
2. [Voir mon résultat](SCR_ENT_CR_T4_MIS_RESULT)

## SCR_ENT_CR_T4_MIS_RESULT

### Votre résultat

<!-- Variables : {score}; {pourcentage} -->

Vous avez obtenu {score} bonne(s) réponse(s) sur 10, soit {pourcentage} %.

1. [🔄 Recommencer](SCR_ENT_CR_T4_MIS_INTRO)
2. [⬅️ Retour au choix du mode](SCR_ENT_CR_T4_MODE)
3. [🏠 Retour au menu](MENU_PRINCIPAL)

## SCR_ENT_CR_T5_QOFF_INTRO

### Questions officielles

<!-- Variables : {theme}=T5 -->

Vous allez répondre à 10 questions officielles de la thématique choisie. Une correction est affichée après chaque réponse.

1. [Commencer](SCR_ENT_CR_T5_QOFF_INIT)

## SCR_ENT_CR_T5_QOFF_INIT

### Préparation du tirage

<!-- Variables : {{session_id}}; {{deja_tires}} -->

<!-- Règle métier : Créer un tirage de 10 questions actives sans doublon -->

<!-- Condition métier : Tirage valide -->
1. [Lancer l’entraînement](SCR_ENT_CR_T5_QOFF_RUN)

<!-- Écran logique non affiché -->

## SCR_ENT_CR_T5_QOFF_RUN

### Question {numero} sur 10

<!-- Variables : {id_question}; {numero}; {score} -->

<!-- Règle métier : Afficher QUESTION et réponses A à D -->

**Réponse attendue :** Choix unique

<!-- Condition métier : Réponse sélectionnée -->
1. [Valider ma réponse](SCR_ENT_CR_T5_QOFF_CORR)

<!-- Écran dynamique -->

## SCR_ENT_CR_T5_QOFF_CORR

### Correction

<!-- Variables : {bonne_reponse}; {explication}; {score} -->

<!-- Règle métier : Afficher bonne réponse, explication et astuce mémoire -->

<!-- Condition métier : Question courante < 10 -->
1. [Question suivante](SCR_ENT_CR_T5_QOFF_RUN)
<!-- Condition métier : Question courante = 10 -->
2. [Voir mon résultat](SCR_ENT_CR_T5_QOFF_RESULT)

## SCR_ENT_CR_T5_QOFF_RESULT

### Votre résultat

<!-- Variables : {score}; {pourcentage} -->

Vous avez obtenu {score} bonne(s) réponse(s) sur 10, soit {pourcentage} %.

1. [🔄 Recommencer](SCR_ENT_CR_T5_QOFF_INTRO)
2. [⬅️ Retour au choix du mode](SCR_ENT_CR_T5_MODE)
3. [🏠 Retour au menu](MENU_PRINCIPAL)

## SCR_ENT_CR_T5_MIS_INTRO

### Mises en situation

<!-- Variables : {theme}=T5 -->

Vous allez répondre à 10 mises en situation de la thématique choisie. Une correction est affichée après chaque réponse.

1. [Commencer](SCR_ENT_CR_T5_MIS_INIT)

## SCR_ENT_CR_T5_MIS_INIT

### Préparation du tirage

<!-- Variables : {{session_id}}; {{deja_tires}} -->

<!-- Règle métier : Créer un tirage de 10 situations sans doublon -->

<!-- Condition métier : Tirage valide -->
1. [Lancer l’entraînement](SCR_ENT_CR_T5_MIS_RUN)

<!-- Écran logique non affiché -->

## SCR_ENT_CR_T5_MIS_RUN

### Situation {numero} sur 10

<!-- Variables : {id_situation}; {numero}; {score} -->

<!-- Règle métier : Afficher la situation, la question et les réponses A à D -->

**Réponse attendue :** Choix unique

<!-- Condition métier : Réponse sélectionnée -->
1. [Valider ma réponse](SCR_ENT_CR_T5_MIS_CORR)

<!-- Écran dynamique -->

## SCR_ENT_CR_T5_MIS_CORR

### Correction

<!-- Variables : {bonne_reponse}; {explication}; {score} -->

<!-- Règle métier : Afficher bonne réponse et feedback pédagogique -->

<!-- Condition métier : Situation courante < 10 -->
1. [Situation suivante](SCR_ENT_CR_T5_MIS_RUN)
<!-- Condition métier : Situation courante = 10 -->
2. [Voir mon résultat](SCR_ENT_CR_T5_MIS_RESULT)

## SCR_ENT_CR_T5_MIS_RESULT

### Votre résultat

<!-- Variables : {score}; {pourcentage} -->

Vous avez obtenu {score} bonne(s) réponse(s) sur 10, soit {pourcentage} %.

1. [🔄 Recommencer](SCR_ENT_CR_T5_MIS_INTRO)
2. [⬅️ Retour au choix du mode](SCR_ENT_CR_T5_MODE)
3. [🏠 Retour au menu](MENU_PRINCIPAL)

## SCR_ENT_CSP_INDISPONIBLE

### Entraînement bientôt disponible

<!-- Variables : {type_examen}=CSP -->

Cet entraînement n’est pas encore disponible. La banque de données correspondante doit être ajoutée au moteur.

1. [⬅️ Retour au choix de l’examen](SCR_ENT_MENU)

<!-- À remplacer après import de la banque CSP -->

## SCR_ENT_CR_THEMES

### Choisissez une thématique

<!-- Variables : {type_examen}=CR -->

Choisissez une thématique. Chaque entraînement comprend 10 éléments tirés aléatoirement.

1. [Thématique 1 — Principes et valeurs de la République](SCR_ENT_CR_T1_MODE)
2. [Thématique 2 — Système institutionnel et politique français](SCR_ENT_CR_T2_MODE)
3. [Thématique 3 — Droits et devoirs](SCR_ENT_CR_T3_MODE)
4. [Thématique 4 — Histoire, géographie, patrimoine et culture](SCR_ENT_CR_T4_MODE)
5. [Thématique 5 — Vivre dans la société française](SCR_ENT_CR_T5_MODE)
6. [⬅️ Retour au choix de l’examen](SCR_ENT_MENU)
7. [🏠 Retour au menu](MENU_PRINCIPAL)

## SCR_ENT_CR_T1_MODE

### Principes et valeurs

<!-- Variables : {type_examen}=CR; {theme}=T1 -->

Comment souhaitez-vous vous entraîner sur cette thématique ?

1. [📝 Questions officielles](SCR_ENT_CR_T1_QOFF_INTRO)
2. [🎭 Mises en situation](SCR_ENT_CR_T1_MIS_INTRO)
3. [⬅️ Retour aux thématiques](SCR_ENT_CR_THEMES)
4. [🏠 Retour au menu](MENU_PRINCIPAL)

## SCR_ENT_CR_T2_MODE

### Institutions

<!-- Variables : {type_examen}=CR; {theme}=T2 -->

Comment souhaitez-vous vous entraîner sur cette thématique ?

1. [📝 Questions officielles](SCR_ENT_CR_T2_QOFF_INTRO)
2. [🎭 Mises en situation](SCR_ENT_CR_T2_MIS_INTRO)
3. [⬅️ Retour aux thématiques](SCR_ENT_CR_THEMES)
4. [🏠 Retour au menu](MENU_PRINCIPAL)

## SCR_ENT_CR_T3_MODE

### Droits et devoirs

<!-- Variables : {type_examen}=CR; {theme}=T3 -->

Comment souhaitez-vous vous entraîner sur cette thématique ?

1. [📝 Questions officielles](SCR_ENT_CR_T3_QOFF_INTRO)
2. [🎭 Mises en situation](SCR_ENT_CR_T3_MIS_INTRO)
3. [⬅️ Retour aux thématiques](SCR_ENT_CR_THEMES)
4. [🏠 Retour au menu](MENU_PRINCIPAL)

## SCR_ENT_CR_T4_MODE

### Histoire et culture

<!-- Variables : {type_examen}=CR; {theme}=T4 -->

Comment souhaitez-vous vous entraîner sur cette thématique ?

1. [📝 Questions officielles](SCR_ENT_CR_T4_QOFF_INTRO)
2. [🎭 Mises en situation](SCR_ENT_CR_T4_MIS_INTRO)
3. [⬅️ Retour aux thématiques](SCR_ENT_CR_THEMES)
4. [🏠 Retour au menu](MENU_PRINCIPAL)

## SCR_ENT_CR_T5_MODE

### Vie dans la société

<!-- Variables : {type_examen}=CR; {theme}=T5 -->

Comment souhaitez-vous vous entraîner sur cette thématique ?

1. [📝 Questions officielles](SCR_ENT_CR_T5_QOFF_INTRO)
2. [🎭 Mises en situation](SCR_ENT_CR_T5_MIS_INTRO)
3. [⬅️ Retour aux thématiques](SCR_ENT_CR_THEMES)
4. [🏠 Retour au menu](MENU_PRINCIPAL)

## SCR_ENT_MENU

### M’entraîner

Choisissez le type d’examen pour lequel vous souhaitez vous entraîner.

<!-- Condition métier : Banque disponible | Valeur : CR -->
1. [Carte de résident](SCR_ENT_CR_THEMES)
<!-- Condition métier : Banque absente | Valeur : CSP -->
2. [Carte de séjour pluriannuelle](SCR_ENT_CSP_INDISPONIBLE)
<!-- Condition métier : Banque absente | Valeur : NAT -->
3. [Naturalisation](SCR_ENT_NAT_INDISPONIBLE)
4. [🏠 Retour au menu](MENU_PRINCIPAL)

<!-- Écran d’entrée -->

## SCR_ENT_NAT_INDISPONIBLE

### Entraînement bientôt disponible

<!-- Variables : {type_examen}=NAT -->

Cet entraînement n’est pas encore disponible. La banque de données correspondante doit être ajoutée au moteur.

1. [⬅️ Retour au choix de l’examen](SCR_ENT_MENU)

<!-- À remplacer après import de la banque Naturalisation -->
