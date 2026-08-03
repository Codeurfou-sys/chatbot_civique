<!-- Module généré automatiquement : Bilan -->
<!-- Date : 2026-08-03T12:39:32+02:00 -->

## SCR_BIL_MENU

### Mon bilan

Choisissez le bilan qui correspond à votre situation. Le premier bilan vous aide à identifier votre niveau de départ. Le bilan de progression vous permet de comparer votre résultat actuel à votre dernier score obtenu.

1. [Mon 1er bilan](SCR_BIL_INIT_001)
2. [Mon bilan de progression](SCR_BIL_PROG_001)
3. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran d’entrée depuis le menu principal -->

## SCR_BIL_INIT_001

### Mon 1er bilan

Ce premier bilan vous permet d’évaluer votre niveau actuel avant de commencer ou d’organiser vos révisions. Il ne s’agit pas de l’examen officiel : son objectif est de repérer vos points forts et les notions à renforcer.

1. [Commencer](SCR_BIL_INIT_002)

## SCR_BIL_INIT_002

### Quelques questions avant de commencer

Avant de commencer, répondez à quelques questions rapides. Vos réponses nous aideront à sélectionner un niveau de difficulté adapté à votre situation.

1. [Continuer](SCR_BIL_INIT_003)

## SCR_BIL_INIT_003

### Depuis quand révisez-vous ?

<!-- Variables : {duree_revision} -->

<!-- Règle métier : Enregistrer la valeur technique de la réponse -->

**Réponse attendue :** Choix unique

<!-- Condition métier : Réponse sélectionnée | Valeur : DEBUT_AUJOURDHUI -->
1. [Je commence aujourd’hui](SCR_BIL_INIT_004)
<!-- Condition métier : Réponse sélectionnée | Valeur : QUELQUES_JOURS -->
2. [Depuis quelques jours](SCR_BIL_INIT_004)
<!-- Condition métier : Réponse sélectionnée | Valeur : QUELQUES_SEMAINES -->
3. [Depuis quelques semaines](SCR_BIL_INIT_004)
<!-- Condition métier : Réponse sélectionnée | Valeur : PLUS_UN_MOIS -->
4. [Depuis plus d’un mois](SCR_BIL_INIT_004)

## SCR_BIL_INIT_004

### Quand pensez-vous passer votre examen ?

<!-- Variables : {date_examen} -->

<!-- Règle métier : Enregistrer la valeur technique de la réponse -->

**Réponse attendue :** Choix unique

<!-- Condition métier : Réponse sélectionnée | Valeur : EXAMEN_7J -->
1. [Dans une semaine ou moins](SCR_BIL_INIT_005)
<!-- Condition métier : Réponse sélectionnée | Valeur : EXAMEN_15J -->
2. [Dans deux semaines](SCR_BIL_INIT_005)
<!-- Condition métier : Réponse sélectionnée | Valeur : EXAMEN_1M -->
3. [Dans un mois](SCR_BIL_INIT_005)
<!-- Condition métier : Réponse sélectionnée | Valeur : EXAMEN_PLUS_TARD -->
4. [Plus tard](SCR_BIL_INIT_005)

## SCR_BIL_INIT_005

### Avez-vous déjà réalisé un bilan ?

<!-- Variables : {deja_bilan} -->

<!-- Règle métier : Orienter vers le parcours adapté -->

**Réponse attendue :** Choix unique

<!-- Condition métier : Réponse sélectionnée | Valeur : PREMIER_BILAN -->
1. [Non, c’est mon premier bilan](SCR_BIL_INIT_006)
<!-- Condition métier : Réponse sélectionnée | Valeur : DEJA_BILAN -->
2. [Oui, j’ai déjà un score](SCR_BIL_PROG_001)

## SCR_BIL_INIT_006

### Sélection du scénario

<!-- Variables : {scenario} -->

<!-- Règle métier : Calculer le scénario à partir du contexte -->

<!-- Transition automatique NAV_BIL_INIT_006 : Calcul terminé → SCR_BIL_INIT_007 -->
1. [Sélectionner le scénario](SCR_BIL_INIT_007)

<!-- Écran logique non affiché -->

## SCR_BIL_INIT_007

### Avant de commencer

<!-- Règle métier : Présenter les 25 questions et le résultat final -->

1. [Je commence](SCR_BIL_INIT_008)

## SCR_BIL_INIT_008

### Question {numero_question} sur 25

<!-- Variables : {numero_question}; {theme_question}; {score} -->

<!-- Règle métier : Tirer 25 questions sans doublon selon le scénario -->

**Réponse attendue :** Choix unique par question

<!-- Transition automatique NAV_BIL_INIT_008A : Question 1 à 24 validée → SCR_BIL_INIT_008 -->
1. [Question suivante](SCR_BIL_INIT_008)
<!-- Condition métier : Question 25 validée -->
1. [Voir mes résultats](SCR_BIL_INIT_009)

<!-- Séquence dynamique de 25 questions -->

## SCR_BIL_INIT_009

### Votre résultat

<!-- Variables : {score}; {pourcentage}; {profil} -->

Vous avez obtenu {score}/25, soit {pourcentage} %. Votre profil actuel est : {profil}.

1. [Voir le détail](SCR_BIL_INIT_010)

## SCR_BIL_INIT_010

### Vos résultats par thématique

<!-- Variables : {score_T1}; {score_T2}; {score_T3}; {score_T4}; {score_T5} -->

<!-- Règle métier : Afficher un score sur 5 pour chaque thématique -->

1. [Analyser mes résultats](SCR_BIL_INIT_011)

## SCR_BIL_INIT_011

### Vos points forts et vos priorités

<!-- Variables : {theme_fort}; {theme_faible} -->

<!-- Règle métier : Choisir le message selon l’écart entre les scores -->

1. [Voir ma prochaine étape](SCR_BIL_INIT_012)

## SCR_BIL_INIT_012

### Votre prochaine étape

<!-- Variables : {profil} -->

<!-- Règle métier : Sélectionner la recommandation liée au profil -->

<!-- Condition métier : Au moins un thème sous le seuil -->
1. [Voir mes priorités de révision](SCR_BIL_INIT_013)
<!-- Condition métier : Aucun thème sous le seuil -->
2. [Terminer mon bilan](SCR_BIL_INIT_014)

## SCR_BIL_INIT_013

### Vos priorités de révision

<!-- Variables : {theme_faible}; {themes_sous_seuil} -->

<!-- Règle métier : Afficher les thèmes sous le seuil -->

1. [Terminer mon bilan](SCR_BIL_INIT_014)

## SCR_BIL_INIT_014

### Votre bilan est terminé

Votre premier bilan est terminé. Utilisez maintenant vos résultats pour organiser vos révisions et concentrez-vous en priorité sur les thèmes recommandés.

<!-- Condition métier : Profil 1 ou 2 | Valeur : PROFIL_1; PROFIL_2 -->
1. [Commencer mes révisions](SCR_REV_MENU)
<!-- Condition métier : Profil 3 | Valeur : PROFIL_3 -->
2. [M’entraîner](SCR_ENT_MENU)
<!-- Condition métier : Profil 4 | Valeur : PROFIL_4 -->
3. [Préparer mon examen](SCR_PREP_MENU)
4. [Retour au menu principal](MENU_PRINCIPAL)

## SCR_BIL_PROG_001

### Mon bilan de progression

Ce bilan vous permet de mesurer votre évolution depuis votre dernier test. Comme NovaFrate ne conserve pas encore automatiquement vos résultats entre deux connexions, indiquez votre dernier score avant de commencer.

1. [Commencer](SCR_BIL_PROG_002)

## SCR_BIL_PROG_002

### Mon dernier score

<!-- Variables : {score_precedent} -->

Quel était votre dernier score sur 25 ? Saisissez un nombre compris entre 0 et 25.

<!-- Condition métier : Score valide | Valeur : 0 à 25 -->
1. [Continuer](SCR_BIL_PROG_003)
<!-- Transition automatique NAV_BIL_PROG_002B : Score invalide → SCR_BIL_ERROR_SCORE -->
1. [Afficher une erreur](SCR_BIL_ERROR_SCORE)

## SCR_BIL_PROG_003

### Avant de commencer

<!-- Règle métier : Présenter le déroulement du test -->

1. [Je commence](SCR_BIL_PROG_004)

## SCR_BIL_PROG_004

### Question {numero_question} sur 25

<!-- Variables : {numero_question}; {score} -->

<!-- Règle métier : Tirer 25 questions sans doublon -->

**Réponse attendue :** Choix unique par question

<!-- Transition automatique NAV_BIL_PROG_004A : Question 1 à 24 validée → SCR_BIL_PROG_004 -->
1. [Question suivante](SCR_BIL_PROG_004)
<!-- Condition métier : Question 25 validée -->
1. [Voir mon résultat](SCR_BIL_PROG_005)

## SCR_BIL_PROG_005

### Votre résultat actuel

<!-- Variables : {score}; {pourcentage}; {profil} -->

Vous avez obtenu {score}/25, soit {pourcentage} %. Votre profil actuel est : {profil}.

1. [Comparer mes scores](SCR_BIL_PROG_006)

## SCR_BIL_PROG_006

### Votre progression

<!-- Variables : {score_precedent}; {score}; {progression}; {ecart_absolu} -->

<!-- Règle métier : Comparer les scores et choisir le message -->

1. [Voir le détail](SCR_BIL_PROG_007)

## SCR_BIL_PROG_007

### Vos résultats par thématique

<!-- Variables : {score_T1}; {score_T2}; {score_T3}; {score_T4}; {score_T5} -->

<!-- Règle métier : Afficher un score sur 5 par thématique -->

1. [Analyser mes résultats](SCR_BIL_PROG_008)

## SCR_BIL_PROG_008

### Vos points forts et vos priorités

<!-- Variables : {theme_fort}; {theme_faible} -->

<!-- Règle métier : Analyser les scores par thème -->

1. [Voir mes prochaines étapes](SCR_BIL_PROG_009)

## SCR_BIL_PROG_009

### Vos prochaines étapes

<!-- Variables : {profil}; {themes_sous_seuil} -->

<!-- Règle métier : Combiner profil et thèmes faibles -->

1. [Terminer mon bilan](SCR_BIL_PROG_010)

## SCR_BIL_PROG_010

### Bilan de progression terminé

Votre bilan de progression est terminé. Consultez vos priorités, révisez les notions recommandées, puis réalisez un nouvel entraînement lorsque vous vous sentez prêt.

<!-- Condition métier : Profil 1 ou 2 | Valeur : PROFIL_1; PROFIL_2 -->
1. [Poursuivre mes révisions](SCR_REV_MENU)
<!-- Condition métier : Profil 3 | Valeur : PROFIL_3 -->
2. [M’entraîner](SCR_ENT_MENU)
<!-- Condition métier : Profil 4 | Valeur : PROFIL_4 -->
3. [Préparer mon examen](SCR_PREP_MENU)
4. [Refaire un bilan](SCR_BIL_MENU)
5. [Retour au menu principal](MENU_PRINCIPAL)

## SCR_BIL_ERROR_SCORE

### Score incorrect

<!-- Variables : {score_precedent} -->

<!-- Règle métier : Afficher si la saisie est invalide -->

**Réponse attendue :** Nouvelle saisie

1. [Corriger mon score](SCR_BIL_PROG_002)

<!-- Écran de validation -->
