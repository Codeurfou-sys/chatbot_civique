---
obfuscate: true
variablesDynamiques: true
---

# Coach Civique NovaFrate

1. [Commencer](START)

<!-- Début du fichier source : modules\start.md -->

## START

<!-- Initialisation globale -->
1. [Ouvrir le Coach](MENU_PRINCIPAL)

## MENU_PRINCIPAL

### Coach Civique NovaFrate

Bienvenue dans le Coach Civique NovaFrate.

Je vous accompagne pour comprendre l’examen civique, organiser vos révisions, vous entraîner, préparer un examen blanc, trouver une session et répondre à vos questions.

Choisissez une rubrique ci-dessous ou utilisez « Pose-moi une question ».

1. [Bilan](SCR_BIL_MENU)
2. [Conseils pour réussir](SCR_CONS_MENU)
3. [FAQ](SCR_FAQ_MENU)
4. [M’entraîner](SCR_ENT_MENU)
5. [Passer mon examen](SCR_PASS_MENU)
6. [Pose-moi une question](SCR_QL_MENU)
7. [Préparer mon examen](SCR_PREP_MENU)
8. [Révisions](SCR_REV_MENU)
9. [Consulter le glossaire](SCR_GLO_MENU)
10. [Aide](SCR_ACC_AIDE)

<!-- Fin du fichier source : modules\start.md -->

<!-- Début du fichier source : modules\00_accueil_complements.md -->

<!-- Module généré automatiquement : Accueil -->
<!-- Date : 2026-08-03T13:13:33+02:00 -->

## SCR_ACC_AIDE

### Comment utiliser le Coach ?

Choisissez une rubrique selon votre besoin. Utilisez les boutons de retour pour changer d’activité. Pour une demande précise, écrivez votre question dans « Pose-moi une question ».

1. [À propos du Coach](SCR_ACC_APROPOS)
2. [Poser une question](SCR_QL_INPUT)
3. [Retour au menu principal](MENU_PRINCIPAL)

## SCR_ACC_RESTART

### Recommencer la conversation ?

Vos réponses de cette session seront réinitialisées. Souhaitez-vous continuer ?

<!-- Condition métier : Réponse sélectionnée | Valeur : RESTART_YES -->
1. [Oui, recommencer](START)
<!-- Condition métier : Réponse sélectionnée | Valeur : RESTART_NO -->
2. [Non, revenir au menu](MENU_PRINCIPAL)

## SCR_ACC_APROPOS

### À propos du Coach Civique

Le Coach Civique est un assistant pédagogique déterministe construit à partir de ressources validées. Il vous oriente, explique et propose des activités, mais ne remplace pas les informations officielles ni les consignes de votre centre d’examen.

1. [Retour à l’aide](SCR_ACC_AIDE)
2. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Fin du fichier source : modules\00_accueil_complements.md -->

<!-- Début du fichier source : modules\02_bilan.md -->

<!-- Module généré automatiquement : Bilan -->
<!-- Date : 2026-08-03T13:13:33+02:00 -->

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

<!-- Fin du fichier source : modules\02_bilan.md -->

<!-- Début du fichier source : modules\08_conseils.md -->

<!-- Module généré automatiquement : Conseils -->
<!-- Date : 2026-08-03T13:13:33+02:00 -->

## SCR_CONS_MENU

### Conseils pour réussir

Choisissez le conseil dont vous avez besoin. Vous pouvez consulter le guide dans l’ordre ou accéder directement à une rubrique.

1. [🌟 Bien démarrer](SCR_CONS_GUIDE_MENU)
2. [📅 Construire mon parcours](SCR_CONS_PARCOURS_MENU)
3. [🧠 Mémoriser efficacement](SCR_CONS_MEMOIRE_MENU)
4. [🧩 Utiliser des moyens mnémotechniques](SCR_CONS_MNEMO_MENU)
5. [✅ Réussir les QCM](SCR_CONS_QCM_MENU)
6. [🎭 Réussir les mises en situation](SCR_CONS_SITUATIONS_MENU)
7. [⚠️ Éviter les erreurs fréquentes](SCR_CONS_ERREURS_MENU)
8. [👤 Préparer l’entretien de naturalisation](SCR_CONS_ENTRETIEN_MENU)
9. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran d’entrée -->

## SCR_CONS_ERREURS_01

### ⚠️ Les erreurs les plus fréquentes

<!-- Variables : {rubrique}=ERREURS; {ordre}=1 -->

### Resume

Les candidats commettent souvent les mêmes erreurs : ❌ Lire la question trop rapidement. ❌ Choisir la première réponse qui semble correcte. ❌ Modifier sa réponse sans véritable justification. ❌ Chercher à répondre le...

Les candidats commettent souvent les mêmes erreurs :

❌ Lire la question trop rapidement.

❌ Choisir la première réponse qui semble correcte.

❌ Modifier sa réponse sans véritable justification.

❌ Chercher à répondre le plus vite possible.

❌ Ne pas relire les explications après une erreur.

---

1. [Conseil suivant](SCR_CONS_ERREURS_02)
2. [Retour à la rubrique](SCR_CONS_ERREURS_MENU)
3. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : GUIDE_REUSSITE.md — niveau H1 -->

## SCR_CONS_ERREURS_02

### 🎯 La méthode Frate Formation

<!-- Variables : {rubrique}=ERREURS; {ordre}=2 -->

### Resume

Pour chaque question : 1. Lire attentivement la question. 2. Lire toutes les réponses proposées. 3. Éliminer les réponses manifestement fausses. 4. Choisir la réponse la plus juste. 5. Lire l'explication, même si votr...

Pour chaque question :

1. Lire attentivement la question.
2. Lire toutes les réponses proposées.
3. Éliminer les réponses manifestement fausses.
4. Choisir la réponse la plus juste.
5. Lire l'explication, même si votre réponse est correcte (lors des entraînements).

Cette dernière étape est essentielle pour consolider vos connaissances.

---

> ## 💡 Le conseil du Coach
>
> Une bonne réponse vous permet de gagner un point.
>
> Une bonne explication vous permet de réussir les prochaines questions.
>
> Prenez toujours le temps de lire les explications proposées après chaque question.

---

1. [Conseil précédent](SCR_CONS_ERREURS_01)
2. [Conseil suivant](SCR_CONS_ERREURS_03)
3. [Retour à la rubrique](SCR_CONS_ERREURS_MENU)
4. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : GUIDE_REUSSITE.md — niveau H1 -->

## SCR_CONS_ERREURS_03

### 📌 À retenir

<!-- Variables : {rubrique}=ERREURS; {ordre}=3 -->

### Resume

Réussir un QCM ne dépend pas uniquement de vos connaissances. Il faut également : ✔ Lire attentivement chaque question. ✔ Prendre son temps. ✔ Comprendre ses erreurs. ✔ S'entraîner régulièrement. ✔ Lire les explicatio...

Réussir un QCM ne dépend pas uniquement de vos connaissances.

Il faut également :

✔ Lire attentivement chaque question.

✔ Prendre son temps.

✔ Comprendre ses erreurs.

✔ S'entraîner régulièrement.

✔ Lire les explications après chaque réponse.

En appliquant cette méthode à chaque entraînement, vous progresserez rapidement et gagnerez en confiance avant le jour de l'examen.

---

1. [Conseil précédent](SCR_CONS_ERREURS_02)
2. [Conseil suivant](SCR_CONS_ERREURS_04)
3. [Retour à la rubrique](SCR_CONS_ERREURS_MENU)
4. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : GUIDE_REUSSITE.md — niveau H1 -->

## SCR_CONS_ERREURS_04

### ⚠️ Les erreurs les plus fréquentes

<!-- Variables : {rubrique}=ERREURS; {ordre}=4 -->

### Resume

Évitez de : ❌ Apprendre des réponses par cœur. ❌ Répondre trop rapidement. ❌ Vous énerver si vous ne connaissez pas une réponse. ❌ Interrompre votre interlocuteur. ❌ Penser qu'une seule erreur signifie un échec.

Évitez de :

❌ Apprendre des réponses par cœur.

❌ Répondre trop rapidement.

❌ Vous énerver si vous ne connaissez pas une réponse.

❌ Interrompre votre interlocuteur.

❌ Penser qu'une seule erreur signifie un échec.

---

1. [Conseil précédent](SCR_CONS_ERREURS_03)
2. [Conseil suivant](SCR_CONS_ERREURS_05)
3. [Retour à la rubrique](SCR_CONS_ERREURS_MENU)
4. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : GUIDE_REUSSITE.md — niveau H1 -->

## SCR_CONS_ERREURS_05

### 📌 À retenir

<!-- Variables : {rubrique}=ERREURS; {ordre}=5 -->

### Resume

L'entretien est avant tout un échange. Une bonne préparation, une attitude calme et une bonne compréhension des valeurs de la République sont les meilleurs atouts pour réussir. Restez naturel, prenez le temps de réflé...

L'entretien est avant tout un échange.

Une bonne préparation, une attitude calme et une bonne compréhension des valeurs de la République sont les meilleurs atouts pour réussir.

Restez naturel, prenez le temps de réfléchir et faites confiance au travail réalisé pendant vos révisions.

---

> ## 💡 Le conseil du Coach
>
> N'essayez pas d'impressionner votre interlocuteur.
>
> Soyez simplement capable d'expliquer, avec vos propres mots, ce que vous avez compris de la République française, de ses valeurs et de votre parcours.
>
> Une réponse sincère et bien construite est toujours préférable à une réponse récitée.

1. [Conseil précédent](SCR_CONS_ERREURS_04)
2. [Retour à la rubrique](SCR_CONS_ERREURS_MENU)
3. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : GUIDE_REUSSITE.md — niveau H1 -->

## SCR_CONS_ERREURS_MENU

### ⚠️ Éviter les erreurs fréquentes

<!-- Variables : {rubrique}=ERREURS -->

<!-- Liste dynamique : LISTE_ERREURS. Les choix sont générés depuis 99_NAVIGATION. -->

1. [⚠️ Les erreurs les plus fréquentes](SCR_CONS_ERREURS_01)
2. [🎯 La méthode Frate Formation](SCR_CONS_ERREURS_02)
3. [📌 À retenir](SCR_CONS_ERREURS_03)
4. [⚠️ Les erreurs les plus fréquentes](SCR_CONS_ERREURS_04)
5. [📌 À retenir](SCR_CONS_ERREURS_05)
6. [Réviser mes points faibles](SCR_REV_MENU)
7. [M’entraîner](SCR_ENT_MENU)
8. [Retour aux conseils](SCR_CONS_MENU)
9. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Repérer les confusions par thématique et corriger sa méthode. -->

## SCR_CONS_QCM_01

### ✅ Réussir les QCM

<!-- Variables : {rubrique}=QCM; {ordre}=1 -->

✅ Réussir les QCM

1. [Conseil suivant](SCR_CONS_QCM_02)
2. [Retour à la rubrique](SCR_CONS_QCM_MENU)
3. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : GUIDE_REUSSITE.md — niveau H1 -->

## SCR_CONS_QCM_02

### Pourquoi les QCM posent-ils parfois des difficultés ?

<!-- Variables : {rubrique}=QCM; {ordre}=2 -->

### Resume

Beaucoup de candidats pensent qu'un QCM est simple. Pourtant, de nombreuses erreurs sont dues non pas à un manque de connaissances, mais à un manque d'attention. Quelques bonnes habitudes permettent d'éviter ces erreu...

Beaucoup de candidats pensent qu'un QCM est simple.

Pourtant, de nombreuses erreurs sont dues non pas à un manque de connaissances, mais à un manque d'attention.

Quelques bonnes habitudes permettent d'éviter ces erreurs et d'améliorer rapidement son score.

---

1. [Conseil précédent](SCR_CONS_QCM_01)
2. [Conseil suivant](SCR_CONS_QCM_03)
3. [Retour à la rubrique](SCR_CONS_QCM_MENU)
4. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : GUIDE_REUSSITE.md — niveau H2 -->

## SCR_CONS_QCM_03

### 📍 Conseil n°1 : Lire toute la question

<!-- Variables : {rubrique}=QCM; {ordre}=3 -->

### Resume

Ne vous précipitez jamais sur les réponses. Prenez le temps de lire la question jusqu'au dernier mot. Certains mots changent complètement son sens. Par exemple : Laquelle de ces propositions est fausse ? Laquelle de c...

Ne vous précipitez jamais sur les réponses.

Prenez le temps de lire la question jusqu'au dernier mot.

Certains mots changent complètement son sens.

Par exemple :

- **Laquelle de ces propositions est fausse ?**
- **Laquelle de ces propositions est correcte ?**
- **Lequel de ces droits est garanti par la Constitution ?**

Une lecture trop rapide peut conduire à choisir une mauvaise réponse alors que vous connaissiez pourtant la bonne.

---

1. [Conseil précédent](SCR_CONS_QCM_02)
2. [Conseil suivant](SCR_CONS_QCM_04)
3. [Retour à la rubrique](SCR_CONS_QCM_MENU)
4. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : GUIDE_REUSSITE.md — niveau H1 -->

## SCR_CONS_QCM_04

### 📍 Conseil n°2 : Lire toutes les réponses proposées

<!-- Variables : {rubrique}=QCM; {ordre}=4 -->

### Resume

Même si une réponse vous paraît immédiatement correcte, prenez le temps de lire les autres propositions. Vous éviterez ainsi de sélectionner une réponse incomplète ou de passer à côté de la meilleure réponse.

Même si une réponse vous paraît immédiatement correcte, prenez le temps de lire les autres propositions.

Vous éviterez ainsi de sélectionner une réponse incomplète ou de passer à côté de la meilleure réponse.

---

1. [Conseil précédent](SCR_CONS_QCM_03)
2. [Conseil suivant](SCR_CONS_QCM_05)
3. [Retour à la rubrique](SCR_CONS_QCM_MENU)
4. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : GUIDE_REUSSITE.md — niveau H1 -->

## SCR_CONS_QCM_05

### 📍 Conseil n°3 : Éliminer les réponses manifestement fausses

<!-- Variables : {rubrique}=QCM; {ordre}=5 -->

### Resume

Lorsque vous hésitez entre plusieurs réponses, commencez par éliminer celles qui sont clairement incorrectes. Cette méthode vous permet de réduire le nombre de possibilités et d'augmenter vos chances de trouver la bon...

Lorsque vous hésitez entre plusieurs réponses, commencez par éliminer celles qui sont clairement incorrectes.

Cette méthode vous permet de réduire le nombre de possibilités et d'augmenter vos chances de trouver la bonne réponse.

---

1. [Conseil précédent](SCR_CONS_QCM_04)
2. [Conseil suivant](SCR_CONS_QCM_06)
3. [Retour à la rubrique](SCR_CONS_QCM_MENU)
4. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : GUIDE_REUSSITE.md — niveau H1 -->

## SCR_CONS_QCM_MENU

### ✅ Réussir les QCM

<!-- Variables : {rubrique}=QCM -->

<!-- Liste dynamique : LISTE_QCM. Les choix sont générés depuis 99_NAVIGATION. -->

1. [✅ Réussir les QCM](SCR_CONS_QCM_01)
2. [Pourquoi les QCM posent-ils parfois des difficultés ?](SCR_CONS_QCM_02)
3. [📍 Conseil n°1 : Lire toute la question](SCR_CONS_QCM_03)
4. [📍 Conseil n°2 : Lire toutes les réponses proposées](SCR_CONS_QCM_04)
5. [📍 Conseil n°3 : Éliminer les réponses manifestement fausses](SCR_CONS_QCM_05)
6. [📍 Conseil n°4 : Repérer les mots importants](SCR_CONS_QCM_06)
7. [📍 Conseil n°5 : Ne répondez pas trop vite](SCR_CONS_QCM_07)
8. [📍 Conseil n°6 : Analysez vos erreurs](SCR_CONS_QCM_08)
9. [📍 Conseil n°7 : Faites confiance à votre préparation](SCR_CONS_QCM_09)
10. [M’entraîner](SCR_ENT_MENU)
11. [Préparer un examen blanc](SCR_PREP_MENU)
12. [Retour aux conseils](SCR_CONS_MENU)
13. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Lire, éliminer les pièges, analyser les erreurs et gagner des points. -->

## SCR_CONS_QCM_06

### 📍 Conseil n°4 : Repérer les mots importants

<!-- Variables : {rubrique}=QCM; {ordre}=6 -->

### Resume

Certains mots méritent une attention particulière : toujours ; jamais ; obligatoire ; interdit ; autorisé ; uniquement ; principalement. Ils donnent souvent un indice sur la réponse attendue.

Certains mots méritent une attention particulière :

- toujours ;
- jamais ;
- obligatoire ;
- interdit ;
- autorisé ;
- uniquement ;
- principalement.

Ils donnent souvent un indice sur la réponse attendue.

---

1. [Conseil précédent](SCR_CONS_QCM_05)
2. [Conseil suivant](SCR_CONS_QCM_07)
3. [Retour à la rubrique](SCR_CONS_QCM_MENU)
4. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : GUIDE_REUSSITE.md — niveau H1 -->

## SCR_CONS_QCM_07

### 📍 Conseil n°5 : Ne répondez pas trop vite

<!-- Variables : {rubrique}=QCM; {ordre}=7 -->

### Resume

Il est inutile de vouloir terminer un quiz le plus rapidement possible. Prenez quelques secondes pour réfléchir avant de valider votre réponse. Un candidat attentif obtient généralement de meilleurs résultats qu'un ca...

Il est inutile de vouloir terminer un quiz le plus rapidement possible.

Prenez quelques secondes pour réfléchir avant de valider votre réponse.

Un candidat attentif obtient généralement de meilleurs résultats qu'un candidat pressé.

---

1. [Conseil précédent](SCR_CONS_QCM_06)
2. [Conseil suivant](SCR_CONS_QCM_08)
3. [Retour à la rubrique](SCR_CONS_QCM_MENU)
4. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : GUIDE_REUSSITE.md — niveau H1 -->

## SCR_CONS_QCM_08

### 📍 Conseil n°6 : Analysez vos erreurs

<!-- Variables : {rubrique}=QCM; {ordre}=8 -->

### Resume

Le véritable apprentissage commence après votre réponse. Lorsque vous vous trompez : relisez l'explication proposée ; demandez au Coach pédagogique pourquoi votre réponse est incorrecte ; consultez le glossaire si un...

Le véritable apprentissage commence après votre réponse.

Lorsque vous vous trompez :

- relisez l'explication proposée ;
- demandez au Coach pédagogique pourquoi votre réponse est incorrecte ;
- consultez le glossaire si un terme vous est inconnu ;
- refaites quelques questions sur le même thème.

Une erreur comprise est rarement une erreur que l'on reproduit.

---

1. [Conseil précédent](SCR_CONS_QCM_07)
2. [Conseil suivant](SCR_CONS_QCM_09)
3. [Retour à la rubrique](SCR_CONS_QCM_MENU)
4. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : GUIDE_REUSSITE.md — niveau H1 -->

## SCR_CONS_QCM_09

### 📍 Conseil n°7 : Faites confiance à votre préparation

<!-- Variables : {rubrique}=QCM; {ordre}=9 -->

### Resume

Il est normal d'hésiter sur certaines questions. Si vous avez travaillé régulièrement, faites confiance à vos connaissances. Évitez de changer votre réponse au dernier moment sans raison particulière.

Il est normal d'hésiter sur certaines questions.

Si vous avez travaillé régulièrement, faites confiance à vos connaissances.

Évitez de changer votre réponse au dernier moment sans raison particulière.

---

1. [Conseil précédent](SCR_CONS_QCM_08)
2. [Retour à la rubrique](SCR_CONS_QCM_MENU)
3. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : GUIDE_REUSSITE.md — niveau H1 -->

## SCR_CONS_GUIDE_01

### 🌟 Guide de réussite

<!-- Variables : {rubrique}=GUIDE; {ordre}=1 -->

🌟 Guide de réussite

1. [Conseil suivant](SCR_CONS_GUIDE_02)
2. [Retour à la rubrique](SCR_CONS_GUIDE_MENU)
3. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : GUIDE_REUSSITE.md — niveau H1 -->

## SCR_CONS_GUIDE_MENU

### 🌟 Bien démarrer

<!-- Variables : {rubrique}=GUIDE -->

<!-- Liste dynamique : LISTE_GUIDE. Les choix sont générés depuis 99_NAVIGATION. -->

1. [🌟 Guide de réussite](SCR_CONS_GUIDE_01)
2. [Bienvenue !](SCR_CONS_GUIDE_02)
3. [Pourquoi ce guide ?](SCR_CONS_GUIDE_03)
4. [Comment utiliser ce guide ?](SCR_CONS_GUIDE_04)
5. [Notre conseil](SCR_CONS_GUIDE_05)
6. [Notre conseil](SCR_CONS_GUIDE_06)
7. [🏛️ Thématique 2 - Système institutionnel français](SCR_CONS_GUIDE_07)
8. [Notre conseil](SCR_CONS_GUIDE_08)
9. [⚖️ Thématique 3 - Droits et devoirs](SCR_CONS_GUIDE_09)
10. [Notre conseil](SCR_CONS_GUIDE_10)
11. [🗺️ Thématique 4 - Histoire, géographie et culture](SCR_CONS_GUIDE_11)
12. [Notre conseil](SCR_CONS_GUIDE_12)
13. [🏡 Thématique 5 - Vivre dans la société française](SCR_CONS_GUIDE_13)
14. [Notre conseil](SCR_CONS_GUIDE_14)
15. [🎯 Les erreurs de méthode](SCR_CONS_GUIDE_15)
16. [📌 À retenir](SCR_CONS_GUIDE_16)
17. [Commencer mes révisions](SCR_REV_MENU)
18. [Retour aux conseils](SCR_CONS_MENU)
19. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Comprendre l’objectif du guide et choisir une méthode de travail. -->

## SCR_CONS_GUIDE_02

### Bienvenue !

<!-- Variables : {rubrique}=GUIDE; {ordre}=2 -->

### Resume

Vous préparez un examen civique dans le cadre d'une demande de carte de séjour pluriannuelle, de carte de résident ou de naturalisation. Peut être vous posez vous certaines questions : Par où commencer mes révisions ?...

Vous préparez un examen civique dans le cadre d'une demande de carte de séjour pluriannuelle, de carte de résident ou de naturalisation.

Peut-être vous posez-vous certaines questions :

- Par où commencer mes révisions ?
- Comment retenir toutes les informations importantes ?
- Combien de temps faut-il réviser ?
- Comment éviter les erreurs les plus fréquentes ?
- Comment être prêt le jour de l'examen ?

Si c'est le cas, ce guide est fait pour vous.

---

1. [Conseil précédent](SCR_CONS_GUIDE_01)
2. [Conseil suivant](SCR_CONS_GUIDE_03)
3. [Retour à la rubrique](SCR_CONS_GUIDE_MENU)
4. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : GUIDE_REUSSITE.md — niveau H2 -->

## SCR_CONS_GUIDE_03

### Pourquoi ce guide ?

<!-- Variables : {rubrique}=GUIDE; {ordre}=3 -->

### Resume

Réussir un examen civique ne consiste pas à apprendre des centaines de réponses par cœur. L'objectif est avant tout de comprendre les notions essentielles, de les mémoriser durablement et de savoir les reconnaître lor...

Réussir un examen civique ne consiste pas à apprendre des centaines de réponses par cœur.

L'objectif est avant tout de comprendre les notions essentielles, de les mémoriser durablement et de savoir les reconnaître lorsqu'elles sont présentées sous différentes formes.

Une bonne méthode de travail est souvent plus efficace que de longues heures de révision.

Ce guide a été conçu pour vous accompagner tout au long de votre préparation.

Vous y découvrirez :

- comment organiser efficacement vos révisions ;
- comment construire un planning réaliste ;
- comment mémoriser les dates, les symboles et les notions importantes ;
- comment éviter les erreurs les plus fréquentes ;
- comment gagner en confiance avant votre examen ou votre entretien.

---

1. [Conseil précédent](SCR_CONS_GUIDE_02)
2. [Conseil suivant](SCR_CONS_GUIDE_04)
3. [Retour à la rubrique](SCR_CONS_GUIDE_MENU)
4. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : GUIDE_REUSSITE.md — niveau H2 -->

## SCR_CONS_GUIDE_04

### Comment utiliser ce guide ?

<!-- Variables : {rubrique}=GUIDE; {ordre}=4 -->

### Resume

Vous pouvez le lire dans l'ordre, du premier au dernier chapitre, ou consulter directement le thème qui vous intéresse. Chaque chapitre contient : des conseils pratiques ; des méthodes de mémorisation ; des exemples c...

Vous pouvez le lire dans l'ordre, du premier au dernier chapitre, ou consulter directement le thème qui vous intéresse.

Chaque chapitre contient :

- des conseils pratiques ;
- des méthodes de mémorisation ;
- des exemples concrets ;
- des astuces faciles à appliquer ;
- des encadrés « À retenir » et « Le conseil du Coach ».

L'objectif est de vous aider à apprendre plus facilement, tout en gagnant du temps.

---

1. [Conseil précédent](SCR_CONS_GUIDE_03)
2. [Conseil suivant](SCR_CONS_GUIDE_05)
3. [Retour à la rubrique](SCR_CONS_GUIDE_MENU)
4. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : GUIDE_REUSSITE.md — niveau H2 -->

## SCR_CONS_GUIDE_05

### Notre conseil

<!-- Variables : {rubrique}=GUIDE; {ordre}=5 -->

### Resume

Il n'est pas nécessaire d'être un spécialiste de l'histoire ou des institutions françaises pour réussir. Une préparation régulière, une bonne méthode et un peu de persévérance permettent à la grande majorité des candi...

Il n'est pas nécessaire d'être un spécialiste de l'histoire ou des institutions françaises pour réussir.

Une préparation régulière, une bonne méthode et un peu de persévérance permettent à la grande majorité des candidats d'atteindre leur objectif.

Avancez étape par étape.

Prenez le temps de comprendre les notions.

Et surtout…

Faites-vous confiance.

---

> **💡 Le conseil du Coach**
>
> Révisez un peu chaque jour plutôt que plusieurs heures d'affilée une seule fois par semaine.
>
> Le cerveau mémorise beaucoup mieux les apprentissages répartis dans le temps.

1. [Conseil précédent](SCR_CONS_GUIDE_04)
2. [Conseil suivant](SCR_CONS_GUIDE_06)
3. [Retour à la rubrique](SCR_CONS_GUIDE_MENU)
4. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : GUIDE_REUSSITE.md — niveau H2 -->

## SCR_CONS_GUIDE_06

### Notre conseil

<!-- Variables : {rubrique}=GUIDE; {ordre}=6 -->

### Resume

Ne cherchez pas uniquement à retenir les symboles. Comprenez ce qu'ils représentent et pourquoi ils sont importants.

Ne cherchez pas uniquement à retenir les symboles.

Comprenez ce qu'ils représentent et pourquoi ils sont importants.

---

1. [Conseil précédent](SCR_CONS_GUIDE_05)
2. [Conseil suivant](SCR_CONS_GUIDE_07)
3. [Retour à la rubrique](SCR_CONS_GUIDE_MENU)
4. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : GUIDE_REUSSITE.md — niveau H3 -->

## SCR_CONS_GUIDE_07

### 🏛️ Thématique 2 - Système institutionnel français

<!-- Variables : {rubrique}=GUIDE; {ordre}=7 -->

### Resume

Les erreurs les plus fréquentes concernent : ❌ Le rôle du Président de la République. ❌ Le rôle du Premier ministre. ❌ La différence entre le Gouvernement et le Parlement. ❌ Le rôle des maires, des départements et des...

Les erreurs les plus fréquentes concernent :

❌ Le rôle du Président de la République.

❌ Le rôle du Premier ministre.

❌ La différence entre le Gouvernement et le Parlement.

❌ Le rôle des maires, des départements et des régions.

1. [Conseil précédent](SCR_CONS_GUIDE_06)
2. [Conseil suivant](SCR_CONS_GUIDE_08)
3. [Retour à la rubrique](SCR_CONS_GUIDE_MENU)
4. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : GUIDE_REUSSITE.md — niveau H1 -->

## SCR_CONS_GUIDE_08

### Notre conseil

<!-- Variables : {rubrique}=GUIDE; {ordre}=8 -->

### Resume

Posez vous toujours la question : "Qui prend cette décision ?" Cette simple réflexion permet souvent de retrouver la bonne réponse.

Posez-vous toujours la question :

**"Qui prend cette décision ?"**

Cette simple réflexion permet souvent de retrouver la bonne réponse.

---

1. [Conseil précédent](SCR_CONS_GUIDE_07)
2. [Conseil suivant](SCR_CONS_GUIDE_09)
3. [Retour à la rubrique](SCR_CONS_GUIDE_MENU)
4. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : GUIDE_REUSSITE.md — niveau H3 -->

## SCR_CONS_GUIDE_09

### ⚖️ Thématique 3 - Droits et devoirs

<!-- Variables : {rubrique}=GUIDE; {ordre}=9 -->

### Resume

Les candidats hésitent souvent sur : ❌ Les libertés fondamentales. ❌ Les limites de la liberté d'expression. ❌ Les droits et les obligations du citoyen. ❌ Les principales règles de la vie en société.

Les candidats hésitent souvent sur :

❌ Les libertés fondamentales.

❌ Les limites de la liberté d'expression.

❌ Les droits et les obligations du citoyen.

❌ Les principales règles de la vie en société.

1. [Conseil précédent](SCR_CONS_GUIDE_08)
2. [Conseil suivant](SCR_CONS_GUIDE_10)
3. [Retour à la rubrique](SCR_CONS_GUIDE_MENU)
4. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : GUIDE_REUSSITE.md — niveau H1 -->

## SCR_CONS_GUIDE_10

### Notre conseil

<!-- Variables : {rubrique}=GUIDE; {ordre}=10 -->

### Resume

Lorsque vous rencontrez une mise en situation, demandez vous toujours : "Quelle règle ou quel principe s'applique ici ?"

Lorsque vous rencontrez une mise en situation, demandez-vous toujours :

**"Quelle règle ou quel principe s'applique ici ?"**

---

1. [Conseil précédent](SCR_CONS_GUIDE_09)
2. [Conseil suivant](SCR_CONS_GUIDE_11)
3. [Retour à la rubrique](SCR_CONS_GUIDE_MENU)
4. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : GUIDE_REUSSITE.md — niveau H3 -->

## SCR_CONS_GUIDE_11

### 🗺️ Thématique 4 - Histoire, géographie et culture

<!-- Variables : {rubrique}=GUIDE; {ordre}=11 -->

### Resume

C'est généralement la thématique qui demande le plus de mémorisation. Les erreurs portent souvent sur : ❌ Les grandes dates de l'histoire. ❌ Les personnages célèbres. ❌ Les régions françaises. ❌ Les fleuves et les mon...

C'est généralement la thématique qui demande le plus de mémorisation.

Les erreurs portent souvent sur :

❌ Les grandes dates de l'histoire.

❌ Les personnages célèbres.

❌ Les régions françaises.

❌ Les fleuves et les montagnes.

❌ Les institutions européennes.

1. [Conseil précédent](SCR_CONS_GUIDE_10)
2. [Conseil suivant](SCR_CONS_GUIDE_12)
3. [Retour à la rubrique](SCR_CONS_GUIDE_MENU)
4. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : GUIDE_REUSSITE.md — niveau H1 -->

## SCR_CONS_GUIDE_12

### Notre conseil

<!-- Variables : {rubrique}=GUIDE; {ordre}=12 -->

### Resume

N'apprenez jamais une simple liste. Classez les informations : par époque ; par catégorie ; ou par thème. Votre mémoire retiendra beaucoup plus facilement ces informations.

N'apprenez jamais une simple liste.

Classez les informations :

- par époque ;
- par catégorie ;
- ou par thème.

Votre mémoire retiendra beaucoup plus facilement ces informations.

---

1. [Conseil précédent](SCR_CONS_GUIDE_11)
2. [Conseil suivant](SCR_CONS_GUIDE_13)
3. [Retour à la rubrique](SCR_CONS_GUIDE_MENU)
4. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : GUIDE_REUSSITE.md — niveau H3 -->

## SCR_CONS_GUIDE_13

### 🏡 Thématique 5 - Vivre dans la société française

<!-- Variables : {rubrique}=GUIDE; {ordre}=13 -->

### Resume

Les erreurs concernent souvent : ❌ Les démarches administratives. ❌ Le système de santé. ❌ Les droits des salariés. ❌ Les règles relatives à la scolarité. ❌ Les administrations françaises.

Les erreurs concernent souvent :

❌ Les démarches administratives.

❌ Le système de santé.

❌ Les droits des salariés.

❌ Les règles relatives à la scolarité.

❌ Les administrations françaises.

1. [Conseil précédent](SCR_CONS_GUIDE_12)
2. [Conseil suivant](SCR_CONS_GUIDE_14)
3. [Retour à la rubrique](SCR_CONS_GUIDE_MENU)
4. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : GUIDE_REUSSITE.md — niveau H1 -->

## SCR_CONS_GUIDE_14

### Notre conseil

<!-- Variables : {rubrique}=GUIDE; {ordre}=14 -->

### Resume

Essayez d'imaginer des situations de la vie quotidienne. Plus vous visualisez une situation concrète, plus il sera facile de retrouver la bonne réponse.

Essayez d'imaginer des situations de la vie quotidienne.

Plus vous visualisez une situation concrète, plus il sera facile de retrouver la bonne réponse.

---

1. [Conseil précédent](SCR_CONS_GUIDE_13)
2. [Conseil suivant](SCR_CONS_GUIDE_15)
3. [Retour à la rubrique](SCR_CONS_GUIDE_MENU)
4. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : GUIDE_REUSSITE.md — niveau H3 -->

## SCR_CONS_GUIDE_15

### 🎯 Les erreurs de méthode

<!-- Variables : {rubrique}=GUIDE; {ordre}=15 -->

### Resume

Au delà des connaissances, certains comportements expliquent de nombreux échecs. Évitez de : ❌ Apprendre les réponses par cœur. ❌ Réviser uniquement la veille de l'examen. ❌ Négliger les explications proposées après u...

Au-delà des connaissances, certains comportements expliquent de nombreux échecs.

Évitez de :

❌ Apprendre les réponses par cœur.

❌ Réviser uniquement la veille de l'examen.

❌ Négliger les explications proposées après une erreur.

❌ Oublier de refaire les questions sur lesquelles vous vous êtes trompé.

❌ Vouloir aller trop vite.

---

1. [Conseil précédent](SCR_CONS_GUIDE_14)
2. [Conseil suivant](SCR_CONS_GUIDE_16)
3. [Retour à la rubrique](SCR_CONS_GUIDE_MENU)
4. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : GUIDE_REUSSITE.md — niveau H1 -->

## SCR_CONS_GUIDE_16

### 📌 À retenir

<!-- Variables : {rubrique}=GUIDE; {ordre}=16 -->

### Resume

Les erreurs sont normales. Elles permettent d'identifier les notions qui doivent être retravaillées. Chaque erreur est une occasion de progresser. L'important n'est pas de ne jamais se tromper. L'important est de comp...

Les erreurs sont normales.

Elles permettent d'identifier les notions qui doivent être retravaillées.

Chaque erreur est une occasion de progresser.

L'important n'est pas de ne jamais se tromper.

L'important est de comprendre pourquoi une réponse est correcte afin de ne plus refaire la même erreur.

---

> ## 💡 Le conseil du Coach
>
> Ne vous découragez jamais après un mauvais résultat.
>
> Les candidats qui progressent le plus ne sont pas ceux qui font le moins d'erreurs.
>
> Ce sont ceux qui prennent le temps de les comprendre.

---

1. [Conseil précédent](SCR_CONS_GUIDE_15)
2. [Retour à la rubrique](SCR_CONS_GUIDE_MENU)
3. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : GUIDE_REUSSITE.md — niveau H1 -->

## SCR_CONS_SITUATIONS_01

### 🎭 Réussir les mises en situation

<!-- Variables : {rubrique}=SITUATIONS; {ordre}=1 -->

🎭 Réussir les mises en situation

1. [Conseil suivant](SCR_CONS_SITUATIONS_02)
2. [Retour à la rubrique](SCR_CONS_SITUATIONS_MENU)
3. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : GUIDE_REUSSITE.md — niveau H1 -->

## SCR_CONS_SITUATIONS_02

### Pourquoi les mises en situation sont-elles importantes ?

<!-- Variables : {rubrique}=SITUATIONS; {ordre}=2 -->

### Resume

Les mises en situation permettent de vérifier que vous savez appliquer vos connaissances à une situation concrète. Elles ne cherchent pas uniquement à tester votre mémoire. Elles évaluent votre capacité à identifier l...

Les mises en situation permettent de vérifier que vous savez appliquer vos connaissances à une situation concrète.

Elles ne cherchent pas uniquement à tester votre mémoire.

Elles évaluent votre capacité à identifier la bonne attitude face à une situation de la vie quotidienne.

Par exemple :

- un comportement dans un lieu public ;
- une démarche administrative ;
- une situation de travail ;
- un droit ou un devoir du citoyen.

L'objectif est de réfléchir avant de répondre.

---

1. [Conseil précédent](SCR_CONS_SITUATIONS_01)
2. [Conseil suivant](SCR_CONS_SITUATIONS_03)
3. [Retour à la rubrique](SCR_CONS_SITUATIONS_MENU)
4. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : GUIDE_REUSSITE.md — niveau H2 -->

## SCR_CONS_SITUATIONS_03

### 📍 Conseil n°1 : Lire toute la situation

<!-- Variables : {rubrique}=SITUATIONS; {ordre}=3 -->

### Resume

Avant de regarder les réponses, prenez le temps de lire toute la situation. Chaque détail peut être important. Ne vous arrêtez pas aux premières lignes. Essayez de comprendre : Qui est concerné ? Que se passe t il ? Q...

Avant de regarder les réponses, prenez le temps de lire toute la situation.

Chaque détail peut être important.

Ne vous arrêtez pas aux premières lignes.

Essayez de comprendre :

- Qui est concerné ?
- Que se passe-t-il ?
- Quel est le problème posé ?

---

1. [Conseil précédent](SCR_CONS_SITUATIONS_02)
2. [Conseil suivant](SCR_CONS_SITUATIONS_04)
3. [Retour à la rubrique](SCR_CONS_SITUATIONS_MENU)
4. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : GUIDE_REUSSITE.md — niveau H1 -->

## SCR_CONS_SITUATIONS_04

### 📍 Conseil n°2 : Identifier le thème

<!-- Variables : {rubrique}=SITUATIONS; {ordre}=4 -->

### Resume

Demandez vous toujours : À quelle thématique cette situation fait elle référence ? Par exemple : Les valeurs de la République ? Les institutions ? Les droits et devoirs ? La vie en société ? L'histoire, la géographie...

Demandez-vous toujours :

> À quelle thématique cette situation fait-elle référence ?

Par exemple :

- Les valeurs de la République ?
- Les institutions ?
- Les droits et devoirs ?
- La vie en société ?
- L'histoire, la géographie ou la culture ?

Cette première étape vous aide souvent à retrouver la bonne réponse.

---

1. [Conseil précédent](SCR_CONS_SITUATIONS_03)
2. [Conseil suivant](SCR_CONS_SITUATIONS_05)
3. [Retour à la rubrique](SCR_CONS_SITUATIONS_MENU)
4. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : GUIDE_REUSSITE.md — niveau H1 -->

## SCR_CONS_SITUATIONS_05

### 📍 Conseil n°3 : Chercher la règle

<!-- Variables : {rubrique}=SITUATIONS; {ordre}=5 -->

### Resume

Chaque mise en situation repose sur une règle ou un principe. Posez vous cette question : Quelle règle française s'applique dans cette situation ? Quelques exemples : Respect de la loi. Liberté d'expression. Obligatio...

Chaque mise en situation repose sur une règle ou un principe.

Posez-vous cette question :

> Quelle règle française s'applique dans cette situation ?

Quelques exemples :

- Respect de la loi.
- Liberté d'expression.
- Obligation scolaire.
- Égalité entre les femmes et les hommes.
- Respect de la laïcité...

Si vous identifiez la règle, la réponse devient souvent évidente.

---

1. [Conseil précédent](SCR_CONS_SITUATIONS_04)
2. [Conseil suivant](SCR_CONS_SITUATIONS_06)
3. [Retour à la rubrique](SCR_CONS_SITUATIONS_MENU)
4. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : GUIDE_REUSSITE.md — niveau H1 -->

## SCR_CONS_SITUATIONS_06

### 📍 Conseil n°4 : Ne répondez pas selon votre opinion

<!-- Variables : {rubrique}=SITUATIONS; {ordre}=6 -->

### Resume

Une erreur fréquente consiste à répondre selon ce que l'on ferait personnellement. À l'examen, ce n'est pas votre opinion qui est évaluée. C'est votre connaissance des règles et des valeurs de la République française....

Une erreur fréquente consiste à répondre selon ce que l'on ferait personnellement.

À l'examen, ce n'est pas votre opinion qui est évaluée.

C'est votre connaissance des règles et des valeurs de la République française.

Basez toujours votre réponse sur ces principes.

---

1. [Conseil précédent](SCR_CONS_SITUATIONS_05)
2. [Conseil suivant](SCR_CONS_SITUATIONS_07)
3. [Retour à la rubrique](SCR_CONS_SITUATIONS_MENU)
4. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : GUIDE_REUSSITE.md — niveau H1 -->

## SCR_CONS_SITUATIONS_MENU

### 🎭 Réussir les mises en situation

<!-- Variables : {rubrique}=SITUATIONS -->

<!-- Liste dynamique : LISTE_SITUATIONS. Les choix sont générés depuis 99_NAVIGATION. -->

1. [🎭 Réussir les mises en situation](SCR_CONS_SITUATIONS_01)
2. [Pourquoi les mises en situation sont-elles importantes ?](SCR_CONS_SITUATIONS_02)
3. [📍 Conseil n°1 : Lire toute la situation](SCR_CONS_SITUATIONS_03)
4. [📍 Conseil n°2 : Identifier le thème](SCR_CONS_SITUATIONS_04)
5. [📍 Conseil n°3 : Chercher la règle](SCR_CONS_SITUATIONS_05)
6. [📍 Conseil n°4 : Ne répondez pas selon votre opinion](SCR_CONS_SITUATIONS_06)
7. [📍 Conseil n°5 : Utilisez vos connaissances](SCR_CONS_SITUATIONS_07)
8. [📍 Conseil n°6 : Analysez les explications](SCR_CONS_SITUATIONS_08)
9. [⚠️ Les erreurs les plus fréquentes](SCR_CONS_SITUATIONS_09)
10. [📌 À retenir](SCR_CONS_SITUATIONS_10)
11. [⚠️ Les erreurs les plus fréquentes](SCR_CONS_SITUATIONS_11)
12. [Pourquoi connaître les erreurs fréquentes ?](SCR_CONS_SITUATIONS_12)
13. [🇫🇷 Thématique 1 - Principes et valeurs de la République](SCR_CONS_SITUATIONS_13)
14. [M’entraîner aux situations](SCR_ENT_MENU)
15. [Préparer un examen blanc](SCR_PREP_MENU)
16. [Retour aux conseils](SCR_CONS_MENU)
17. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Identifier le thème, la règle et la réponse conforme aux principes français. -->

## SCR_CONS_SITUATIONS_07

### 📍 Conseil n°5 : Utilisez vos connaissances

<!-- Variables : {rubrique}=SITUATIONS; {ordre}=7 -->

### Resume

Les mises en situation ne demandent pas de nouvelles connaissances. Elles utilisent les mêmes notions que celles vues dans les questions de connaissances. Chaque fois que vous apprenez une règle, demandez vous : Dans...

Les mises en situation ne demandent pas de nouvelles connaissances.

Elles utilisent les mêmes notions que celles vues dans les questions de connaissances.

Chaque fois que vous apprenez une règle, demandez-vous :

> Dans quelle situation pourrait-elle s'appliquer ?

Vous serez ainsi mieux préparé.

---

1. [Conseil précédent](SCR_CONS_SITUATIONS_06)
2. [Conseil suivant](SCR_CONS_SITUATIONS_08)
3. [Retour à la rubrique](SCR_CONS_SITUATIONS_MENU)
4. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : GUIDE_REUSSITE.md — niveau H1 -->

## SCR_CONS_SITUATIONS_08

### 📍 Conseil n°6 : Analysez les explications

<!-- Variables : {rubrique}=SITUATIONS; {ordre}=8 -->

### Resume

Après chaque mise en situation : relisez l'explication proposée (en mode entraînement); identifiez la règle utilisée ; demandez des précisions au Coach si nécessaire. Comprendre le raisonnement est plus important que...

Après chaque mise en situation :

- relisez l'explication proposée (en mode entraînement);
- identifiez la règle utilisée ;
- demandez des précisions au Coach si nécessaire.

Comprendre le raisonnement est plus important que retenir la réponse.

---

1. [Conseil précédent](SCR_CONS_SITUATIONS_07)
2. [Conseil suivant](SCR_CONS_SITUATIONS_09)
3. [Retour à la rubrique](SCR_CONS_SITUATIONS_MENU)
4. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : GUIDE_REUSSITE.md — niveau H1 -->

## SCR_CONS_SITUATIONS_09

### ⚠️ Les erreurs les plus fréquentes

<!-- Variables : {rubrique}=SITUATIONS; {ordre}=9 -->

### Resume

Les candidats ont tendance à : ❌ Répondre selon leur expérience personnelle. ❌ Lire trop rapidement la situation. ❌ Oublier la règle de droit ou le principe concerné. ❌ Choisir une réponse qui paraît "logique" mais qu...

Les candidats ont tendance à :

❌ Répondre selon leur expérience personnelle.

❌ Lire trop rapidement la situation.

❌ Oublier la règle de droit ou le principe concerné.

❌ Choisir une réponse qui paraît "logique" mais qui ne respecte pas la réglementation française.

---

1. [Conseil précédent](SCR_CONS_SITUATIONS_08)
2. [Conseil suivant](SCR_CONS_SITUATIONS_10)
3. [Retour à la rubrique](SCR_CONS_SITUATIONS_MENU)
4. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : GUIDE_REUSSITE.md — niveau H1 -->

## SCR_CONS_SITUATIONS_10

### 📌 À retenir

<!-- Variables : {rubrique}=SITUATIONS; {ordre}=10 -->

### Resume

Pour réussir une mise en situation : ✔ Lisez toute la situation. ✔ Identifiez le thème concerné. ✔ Recherchez la règle applicable. ✔ Appuyez vous sur les valeurs et les lois françaises. ✔ Analysez toujours l'explicati...

Pour réussir une mise en situation :

✔ Lisez toute la situation.

✔ Identifiez le thème concerné.

✔ Recherchez la règle applicable.

✔ Appuyez-vous sur les valeurs et les lois françaises.

✔ Analysez toujours l'explication après votre réponse.

---

> ## 💡 Le conseil du Coach
>
> Lorsque vous réalisez une mise en situation, ne cherchez pas immédiatement la bonne réponse.
>
> Cherchez d'abord **la règle** qui s'applique.
>
> Une fois la règle trouvée, la réponse apparaît généralement beaucoup plus facilement.

---

1. [Conseil précédent](SCR_CONS_SITUATIONS_09)
2. [Conseil suivant](SCR_CONS_SITUATIONS_11)
3. [Retour à la rubrique](SCR_CONS_SITUATIONS_MENU)
4. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : GUIDE_REUSSITE.md — niveau H1 -->

## SCR_CONS_SITUATIONS_11

### ⚠️ Les erreurs les plus fréquentes

<!-- Variables : {rubrique}=SITUATIONS; {ordre}=11 -->

⚠️ Les erreurs les plus fréquentes

1. [Conseil précédent](SCR_CONS_SITUATIONS_10)
2. [Conseil suivant](SCR_CONS_SITUATIONS_12)
3. [Retour à la rubrique](SCR_CONS_SITUATIONS_MENU)
4. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : GUIDE_REUSSITE.md — niveau H1 -->

## SCR_CONS_SITUATIONS_12

### Pourquoi connaître les erreurs fréquentes ?

<!-- Variables : {rubrique}=SITUATIONS; {ordre}=12 -->

### Resume

Lors de leurs révisions, beaucoup de candidats commettent les mêmes erreurs. Le plus souvent, ces erreurs ne sont pas dues à un manque de travail, mais à une mauvaise compréhension de certaines notions. Les connaître...

Lors de leurs révisions, beaucoup de candidats commettent les mêmes erreurs.

Le plus souvent, ces erreurs ne sont pas dues à un manque de travail, mais à une mauvaise compréhension de certaines notions.

Les connaître à l'avance vous permettra d'être plus vigilant et d'éviter les pièges les plus courants.

---

1. [Conseil précédent](SCR_CONS_SITUATIONS_11)
2. [Conseil suivant](SCR_CONS_SITUATIONS_13)
3. [Retour à la rubrique](SCR_CONS_SITUATIONS_MENU)
4. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : GUIDE_REUSSITE.md — niveau H2 -->

## SCR_CONS_SITUATIONS_13

### 🇫🇷 Thématique 1 - Principes et valeurs de la République

<!-- Variables : {rubrique}=SITUATIONS; {ordre}=13 -->

### Resume

Les candidats confondent souvent : ❌ La République et la démocratie. ❌ La laïcité et la liberté de religion. ❌ Les symboles de la République (Marianne, drapeau, devise, hymne). ❌ Les valeurs de la République et les dr...

Les candidats confondent souvent :

❌ La République et la démocratie.

❌ La laïcité et la liberté de religion.

❌ Les symboles de la République (Marianne, drapeau, devise, hymne).

❌ Les valeurs de la République et les droits fondamentaux.

1. [Conseil précédent](SCR_CONS_SITUATIONS_12)
2. [Retour à la rubrique](SCR_CONS_SITUATIONS_MENU)
3. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : GUIDE_REUSSITE.md — niveau H1 -->

## SCR_CONS_ENTRETIEN_01

### 👤 Chapitre 7 - Préparer son entretien de naturalisation

<!-- Variables : {rubrique}=ENTRETIEN; {ordre}=1 -->

👤 Chapitre 7 - Préparer son entretien de naturalisation

1. [Conseil suivant](SCR_CONS_ENTRETIEN_02)
2. [Retour à la rubrique](SCR_CONS_ENTRETIEN_MENU)
3. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : GUIDE_REUSSITE.md — niveau H1 -->

## SCR_CONS_ENTRETIEN_02

### Pourquoi préparer son entretien ?

<!-- Variables : {rubrique}=ENTRETIEN; {ordre}=2 -->

### Resume

L'entretien de naturalisation est une étape importante de votre demande. Il ne s'agit pas d'un examen scolaire. L'objectif de cet entretien est de permettre à l'administration de vérifier que vous connaissez les princ...

L'entretien de naturalisation est une étape importante de votre demande.

Il ne s'agit pas d'un examen scolaire.

L'objectif de cet entretien est de permettre à l'administration de vérifier que vous connaissez les principaux repères de la République française et que vous comprenez les droits, les devoirs et les valeurs qui fondent la citoyenneté française.

Une bonne préparation vous permettra d'aborder cet échange avec davantage de confiance.

---

1. [Conseil précédent](SCR_CONS_ENTRETIEN_01)
2. [Conseil suivant](SCR_CONS_ENTRETIEN_03)
3. [Retour à la rubrique](SCR_CONS_ENTRETIEN_MENU)
4. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : GUIDE_REUSSITE.md — niveau H2 -->

## SCR_CONS_ENTRETIEN_03

### 📍 Conseil n°1 : Soyez vous-même

<!-- Variables : {rubrique}=ENTRETIEN; {ordre}=3 -->

### Resume

L'entretien n'a pas pour objectif de vous piéger. Répondez simplement, avec vos propres mots. L'agent évalue avant tout votre compréhension des notions essentielles. Il n'est pas nécessaire de réciter des réponses app...

L'entretien n'a pas pour objectif de vous piéger.

Répondez simplement, avec vos propres mots.

L'agent évalue avant tout votre compréhension des notions essentielles.

Il n'est pas nécessaire de réciter des réponses apprises par cœur.

---

1. [Conseil précédent](SCR_CONS_ENTRETIEN_02)
2. [Conseil suivant](SCR_CONS_ENTRETIEN_04)
3. [Retour à la rubrique](SCR_CONS_ENTRETIEN_MENU)
4. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : GUIDE_REUSSITE.md — niveau H1 -->

## SCR_CONS_ENTRETIEN_04

### 📍 Conseil n°2 : Connaître les thèmes essentiels

<!-- Variables : {rubrique}=ENTRETIEN; {ordre}=4 -->

### Resume

Avant votre entretien, assurez vous de maîtriser les principales connaissances portant sur : les valeurs de la République ; les symboles de la République ; les institutions françaises ; les droits et devoirs du citoye...

Avant votre entretien, assurez-vous de maîtriser les principales connaissances portant sur :

- les valeurs de la République ;
- les symboles de la République ;
- les institutions françaises ;
- les droits et devoirs du citoyen ;
- l'histoire de France ;
- la géographie française ;
- les grandes figures historiques et culturelles.

Ces thèmes reviennent très régulièrement lors des entretiens.

---

1. [Conseil précédent](SCR_CONS_ENTRETIEN_03)
2. [Conseil suivant](SCR_CONS_ENTRETIEN_05)
3. [Retour à la rubrique](SCR_CONS_ENTRETIEN_MENU)
4. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : GUIDE_REUSSITE.md — niveau H1 -->

## SCR_CONS_ENTRETIEN_05

### 📍 Conseil n°3 : Préparez votre parcours personnel

<!-- Variables : {rubrique}=ENTRETIEN; {ordre}=5 -->

### Resume

L'agent pourra également vous poser quelques questions sur votre parcours. Par exemple : Depuis quand vivez vous en France ? Pourquoi souhaitez vous devenir français ? Que faites vous actuellement ? Comment participez...

L'agent pourra également vous poser quelques questions sur votre parcours.

Par exemple :

- Depuis quand vivez-vous en France ?
- Pourquoi souhaitez-vous devenir français ?
- Que faites-vous actuellement ?
- Comment participez-vous à la vie de la société française ?

Répondez avec sincérité et simplicité.

Il ne s'agit pas de trouver la réponse parfaite, mais d'expliquer votre parcours.

---

1. [Conseil précédent](SCR_CONS_ENTRETIEN_04)
2. [Conseil suivant](SCR_CONS_ENTRETIEN_06)
3. [Retour à la rubrique](SCR_CONS_ENTRETIEN_MENU)
4. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : GUIDE_REUSSITE.md — niveau H1 -->

## SCR_CONS_ENTRETIEN_06

### 📍 Conseil n°4 : Prenez le temps de répondre

<!-- Variables : {rubrique}=ENTRETIEN; {ordre}=6 -->

### Resume

Écoutez attentivement chaque question. Si vous ne comprenez pas une question, n'hésitez pas à demander qu'elle soit reformulée. Il vaut mieux demander une précision que répondre à côté du sujet. Prenez quelques second...

Écoutez attentivement chaque question.

Si vous ne comprenez pas une question, n'hésitez pas à demander qu'elle soit reformulée.

Il vaut mieux demander une précision que répondre à côté du sujet.

Prenez quelques secondes pour réfléchir avant de répondre.

---

1. [Conseil précédent](SCR_CONS_ENTRETIEN_05)
2. [Conseil suivant](SCR_CONS_ENTRETIEN_07)
3. [Retour à la rubrique](SCR_CONS_ENTRETIEN_MENU)
4. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : GUIDE_REUSSITE.md — niveau H1 -->

## SCR_CONS_ENTRETIEN_07

### 📍 Conseil n°5 : Valorisez ce que vous connaissez

<!-- Variables : {rubrique}=ENTRETIEN; {ordre}=7 -->

### Resume

Il est normal de ne pas connaître toutes les réponses. Si vous hésitez, expliquez ce que vous savez déjà. Une réponse partielle est souvent préférable à une absence de réponse.

Il est normal de ne pas connaître toutes les réponses.

Si vous hésitez, expliquez ce que vous savez déjà.

Une réponse partielle est souvent préférable à une absence de réponse.

---

1. [Conseil précédent](SCR_CONS_ENTRETIEN_06)
2. [Conseil suivant](SCR_CONS_ENTRETIEN_08)
3. [Retour à la rubrique](SCR_CONS_ENTRETIEN_MENU)
4. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : GUIDE_REUSSITE.md — niveau H1 -->

## SCR_CONS_ENTRETIEN_08

### 📍 Conseil n°6 : Adoptez une attitude sereine

<!-- Variables : {rubrique}=ENTRETIEN; {ordre}=8 -->

### Resume

Le jour de l'entretien : arrivez en avance ; apportez les documents demandés ; adoptez une tenue correcte ; restez poli et respectueux ; gardez votre calme tout au long de l'entretien. Une attitude sereine favorise un...

Le jour de l'entretien :

- arrivez en avance ;
- apportez les documents demandés ;
- adoptez une tenue correcte ;
- restez poli et respectueux ;
- gardez votre calme tout au long de l'entretien.

Une attitude sereine favorise un échange de qualité.

---

1. [Conseil précédent](SCR_CONS_ENTRETIEN_07)
2. [Conseil suivant](SCR_CONS_ENTRETIEN_09)
3. [Retour à la rubrique](SCR_CONS_ENTRETIEN_MENU)
4. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : GUIDE_REUSSITE.md — niveau H1 -->

## SCR_CONS_ENTRETIEN_MENU

### 👤 Préparer l’entretien de naturalisation

<!-- Variables : {rubrique}=ENTRETIEN -->

<!-- Liste dynamique : LISTE_ENTRETIEN. Les choix sont générés depuis 99_NAVIGATION. -->

1. [👤 Chapitre 7 - Préparer son entretien de naturalisation](SCR_CONS_ENTRETIEN_01)
2. [Pourquoi préparer son entretien ?](SCR_CONS_ENTRETIEN_02)
3. [📍 Conseil n°1 : Soyez vous-même](SCR_CONS_ENTRETIEN_03)
4. [📍 Conseil n°2 : Connaître les thèmes essentiels](SCR_CONS_ENTRETIEN_04)
5. [📍 Conseil n°3 : Préparez votre parcours personnel](SCR_CONS_ENTRETIEN_05)
6. [📍 Conseil n°4 : Prenez le temps de répondre](SCR_CONS_ENTRETIEN_06)
7. [📍 Conseil n°5 : Valorisez ce que vous connaissez](SCR_CONS_ENTRETIEN_07)
8. [📍 Conseil n°6 : Adoptez une attitude sereine](SCR_CONS_ENTRETIEN_08)
9. [📍 Conseil n°7 : Continuez à réviser jusqu'au dernier moment](SCR_CONS_ENTRETIEN_09)
10. [🎯 Les questions qui reviennent souvent](SCR_CONS_ENTRETIEN_10)
11. [Préparer mon examen](SCR_PREP_MENU)
12. [Consulter le glossaire](SCR_GLO_MENU)
13. [Retour aux conseils](SCR_CONS_MENU)
14. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Préparer ses connaissances, son parcours personnel et son attitude. -->

## SCR_CONS_ENTRETIEN_09

### 📍 Conseil n°7 : Continuez à réviser jusqu'au dernier moment

<!-- Variables : {rubrique}=ENTRETIEN; {ordre}=9 -->

### Resume

Dans les jours qui précèdent l'entretien, privilégiez : les examens blancs ; les mises en situation ; les fiches de synthèse ; les ressources de révision ; le Coach pédagogique pour revoir les notions qui vous posent...

Dans les jours qui précèdent l'entretien, privilégiez :

- les examens blancs ;
- les mises en situation ;
- les fiches de synthèse ;
- les ressources de révision ;
- le Coach pédagogique pour revoir les notions qui vous posent encore des difficultés.

Il est préférable de consolider vos connaissances plutôt que d'essayer d'apprendre de nouveaux contenus à la dernière minute.

---

1. [Conseil précédent](SCR_CONS_ENTRETIEN_08)
2. [Conseil suivant](SCR_CONS_ENTRETIEN_10)
3. [Retour à la rubrique](SCR_CONS_ENTRETIEN_MENU)
4. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : GUIDE_REUSSITE.md — niveau H1 -->

## SCR_CONS_ENTRETIEN_10

### 🎯 Les questions qui reviennent souvent

<!-- Variables : {rubrique}=ENTRETIEN; {ordre}=10 -->

### Resume

Lors de votre préparation, entraînez vous à répondre simplement à des questions telles que : Que signifie la devise de la République ? Pourquoi souhaitez vous devenir français ? Quels sont les symboles de la Républiqu...

Lors de votre préparation, entraînez-vous à répondre simplement à des questions telles que :

- Que signifie la devise de la République ?
- Pourquoi souhaitez-vous devenir français ?
- Quels sont les symboles de la République ?
- Quel est le rôle du Président de la République ?
- Quels sont les principaux droits et devoirs du citoyen ?
- Que représente la laïcité ?

L'objectif n'est pas de réciter une réponse, mais de montrer que vous comprenez ces notions.

---

1. [Conseil précédent](SCR_CONS_ENTRETIEN_09)
2. [Retour à la rubrique](SCR_CONS_ENTRETIEN_MENU)
3. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : GUIDE_REUSSITE.md — niveau H1 -->

## SCR_CONS_PARCOURS_01

### 📅 Construire son parcours de révision

<!-- Variables : {rubrique}=PARCOURS; {ordre}=1 -->

📅 Construire son parcours de révision

1. [Conseil suivant](SCR_CONS_PARCOURS_02)
2. [Retour à la rubrique](SCR_CONS_PARCOURS_MENU)
3. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : GUIDE_REUSSITE.md — niveau H1 -->

## SCR_CONS_PARCOURS_02

### Pourquoi suivre un parcours de révision ?

<!-- Variables : {rubrique}=PARCOURS; {ordre}=2 -->

### Resume

Préparer un examen civique ne consiste pas à apprendre toutes les réponses par cœur. Pour réussir, il est préférable d'avancer progressivement, de comprendre les notions essentielles et de revenir régulièrement sur le...

Préparer un examen civique ne consiste pas à apprendre toutes les réponses par cœur.

Pour réussir, il est préférable d'avancer progressivement, de comprendre les notions essentielles et de revenir régulièrement sur les connaissances déjà étudiées.

NovaFrate a été conçu autour de cette logique d'apprentissage.

Le parcours proposé ci-dessous vous permet de tirer pleinement parti des différents outils disponibles sur la plateforme.

---

1. [Conseil précédent](SCR_CONS_PARCOURS_01)
2. [Conseil suivant](SCR_CONS_PARCOURS_03)
3. [Retour à la rubrique](SCR_CONS_PARCOURS_MENU)
4. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : GUIDE_REUSSITE.md — niveau H2 -->

## SCR_CONS_PARCOURS_MENU

### 📅 Construire mon parcours

<!-- Variables : {rubrique}=PARCOURS -->

<!-- Liste dynamique : LISTE_PARCOURS. Les choix sont générés depuis 99_NAVIGATION. -->

1. [📅 Construire son parcours de révision](SCR_CONS_PARCOURS_01)
2. [Pourquoi suivre un parcours de révision ?](SCR_CONS_PARCOURS_02)
3. [📍 Étape 1 : Réaliser les entraînements thématiques](SCR_CONS_PARCOURS_03)
4. [📍 Étape 2 : Consolider les connaissances](SCR_CONS_PARCOURS_04)
5. [📍 Étape 3 : Utiliser les ressources de révision](SCR_CONS_PARCOURS_05)
6. [🗺️ La géographie de la France](SCR_CONS_PARCOURS_06)
7. [📅 Les grandes dates de l'histoire](SCR_CONS_PARCOURS_07)
8. [👤 Les grandes figures françaises](SCR_CONS_PARCOURS_08)
9. [📍 Étape 4 : Refaire les mises en situation](SCR_CONS_PARCOURS_09)
10. [📍 Étape 5 : Passer un examen blanc](SCR_CONS_PARCOURS_10)
11. [📍 Étape 6 : Analyser ses erreurs](SCR_CONS_PARCOURS_11)
12. [📍 Étape 7 : Repasser un examen blanc](SCR_CONS_PARCOURS_12)
13. [🧠 Le parcours recommandé](SCR_CONS_PARCOURS_13)
14. [📌 À retenir](SCR_CONS_PARCOURS_14)
15. [M’entraîner](SCR_ENT_MENU)
16. [Réviser](SCR_REV_MENU)
17. [Préparer un examen blanc](SCR_PREP_MENU)
18. [Retour aux conseils](SCR_CONS_MENU)
19. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Suivre une progression logique, des entraînements à l’examen blanc. -->

## SCR_CONS_PARCOURS_03

### 📍 Étape 1 : Réaliser les entraînements thématiques

<!-- Variables : {rubrique}=PARCOURS; {ordre}=3 -->

### Resume

Commencez par travailler les cinq thématiques de l'examen, dans l'ordre qui vous convient. Chaque entraînement comprend : des questions de connaissances ; des mises en situation ; des explications détaillées après cha...

Commencez par travailler les cinq thématiques de l'examen, dans l'ordre qui vous convient.

Chaque entraînement comprend :

- des questions de connaissances ;
- des mises en situation ;
- des explications détaillées après chaque réponse.

L'objectif n'est pas d'obtenir un score parfait dès la première tentative, mais de comprendre les notions abordées.

Après chaque entraînement :

✅ relisez les explications ;

✅ notez les notions difficiles ;

✅ demandez au Coach pédagogique de vous expliquer les points que vous ne comprenez pas.

---

1. [Conseil précédent](SCR_CONS_PARCOURS_02)
2. [Conseil suivant](SCR_CONS_PARCOURS_04)
3. [Retour à la rubrique](SCR_CONS_PARCOURS_MENU)
4. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : GUIDE_REUSSITE.md — niveau H1 -->

## SCR_CONS_PARCOURS_04

### 📍 Étape 2 : Consolider les connaissances

<!-- Variables : {rubrique}=PARCOURS; {ordre}=4 -->

### Resume

Une fois les cinq entraînements terminés, prenez le temps de revoir les questions auxquelles vous avez répondu de manière incorrecte. Pour chaque erreur : relisez l'explication ; consultez le glossaire si un terme vou...

Une fois les cinq entraînements terminés, prenez le temps de revoir les questions auxquelles vous avez répondu de manière incorrecte.

Pour chaque erreur :

- relisez l'explication ;
- consultez le glossaire si un terme vous semble difficile ;
- posez vos questions au Coach pédagogique.

L'objectif est de comprendre vos erreurs avant de poursuivre.

---

1. [Conseil précédent](SCR_CONS_PARCOURS_03)
2. [Conseil suivant](SCR_CONS_PARCOURS_05)
3. [Retour à la rubrique](SCR_CONS_PARCOURS_MENU)
4. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : GUIDE_REUSSITE.md — niveau H1 -->

## SCR_CONS_PARCOURS_05

### 📍 Étape 3 : Utiliser les ressources de révision

<!-- Variables : {rubrique}=PARCOURS; {ordre}=5 -->

### Resume

NovaFrate met à votre disposition plusieurs activités complémentaires pour faciliter la mémorisation. Nous vous conseillons notamment de travailler :

NovaFrate met à votre disposition plusieurs activités complémentaires pour faciliter la mémorisation.

Nous vous conseillons notamment de travailler :

1. [Conseil précédent](SCR_CONS_PARCOURS_04)
2. [Conseil suivant](SCR_CONS_PARCOURS_06)
3. [Retour à la rubrique](SCR_CONS_PARCOURS_MENU)
4. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : GUIDE_REUSSITE.md — niveau H1 -->

## SCR_CONS_PARCOURS_06

### 🗺️ La géographie de la France

<!-- Variables : {rubrique}=PARCOURS; {ordre}=6 -->

### Resume

Retrouvez les régions, les principaux fleuves et les repères géographiques.

Retrouvez les régions, les principaux fleuves et les repères géographiques.

---

1. [Conseil précédent](SCR_CONS_PARCOURS_05)
2. [Conseil suivant](SCR_CONS_PARCOURS_07)
3. [Retour à la rubrique](SCR_CONS_PARCOURS_MENU)
4. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : GUIDE_REUSSITE.md — niveau H3 -->

## SCR_CONS_PARCOURS_07

### 📅 Les grandes dates de l'histoire

<!-- Variables : {rubrique}=PARCOURS; {ordre}=7 -->

### Resume

Retenez les événements les plus importants grâce à des activités spécialement conçues pour faciliter leur mémorisation.

Retenez les événements les plus importants grâce à des activités spécialement conçues pour faciliter leur mémorisation.

---

1. [Conseil précédent](SCR_CONS_PARCOURS_06)
2. [Conseil suivant](SCR_CONS_PARCOURS_08)
3. [Retour à la rubrique](SCR_CONS_PARCOURS_MENU)
4. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : GUIDE_REUSSITE.md — niveau H3 -->

## SCR_CONS_PARCOURS_08

### 👤 Les grandes figures françaises

<!-- Variables : {rubrique}=PARCOURS; {ordre}=8 -->

### Resume

Découvrez les principaux personnages historiques, politiques, scientifiques, artistes et écrivains qui reviennent régulièrement dans les questions d'examen. Ces ressources sont particulièrement utiles avant de passer...

Découvrez les principaux personnages historiques, politiques, scientifiques, artistes et écrivains qui reviennent régulièrement dans les questions d'examen.

Ces ressources sont particulièrement utiles avant de passer un examen blanc.

---

1. [Conseil précédent](SCR_CONS_PARCOURS_07)
2. [Conseil suivant](SCR_CONS_PARCOURS_09)
3. [Retour à la rubrique](SCR_CONS_PARCOURS_MENU)
4. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : GUIDE_REUSSITE.md — niveau H3 -->

## SCR_CONS_PARCOURS_09

### 📍 Étape 4 : Refaire les mises en situation

<!-- Variables : {rubrique}=PARCOURS; {ordre}=9 -->

### Resume

Les mises en situation permettent de vérifier votre capacité à appliquer vos connaissances dans des situations concrètes. Avant de passer un examen blanc, nous vous conseillons de refaire plusieurs mises en situation...

Les mises en situation permettent de vérifier votre capacité à appliquer vos connaissances dans des situations concrètes.

Avant de passer un examen blanc, nous vous conseillons de refaire plusieurs mises en situation afin de consolider vos acquis.

Cette étape est souvent déterminante pour gagner en confiance.

---

1. [Conseil précédent](SCR_CONS_PARCOURS_08)
2. [Conseil suivant](SCR_CONS_PARCOURS_10)
3. [Retour à la rubrique](SCR_CONS_PARCOURS_MENU)
4. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : GUIDE_REUSSITE.md — niveau H1 -->

## SCR_CONS_PARCOURS_10

### 📍 Étape 5 : Passer un examen blanc

<!-- Variables : {rubrique}=PARCOURS; {ordre}=10 -->

### Resume

Lorsque vous vous sentez prêt, réalisez un examen blanc correspondant à votre objectif : Carte de Séjour Pluriannuelle ; Carte de Résident ; Naturalisation. Essayez de reproduire les conditions de l'examen : installez...

Lorsque vous vous sentez prêt, réalisez un examen blanc correspondant à votre objectif :

- Carte de Séjour Pluriannuelle ;
- Carte de Résident ;
- Naturalisation.

Essayez de reproduire les conditions de l'examen :

- installez-vous dans un endroit calme ;
- évitez toute interruption ;
- répondez sans consulter vos notes.

Votre score vous permettra d'identifier les derniers points à renforcer.

---

1. [Conseil précédent](SCR_CONS_PARCOURS_09)
2. [Conseil suivant](SCR_CONS_PARCOURS_11)
3. [Retour à la rubrique](SCR_CONS_PARCOURS_MENU)
4. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : GUIDE_REUSSITE.md — niveau H1 -->

## SCR_CONS_PARCOURS_11

### 📍 Étape 6 : Analyser ses erreurs

<!-- Variables : {rubrique}=PARCOURS; {ordre}=11 -->

### Resume

L'examen blanc est avant tout un outil de progression. Après chaque évaluation : analysez vos erreurs ; identifiez les thèmes les moins bien maîtrisés ; demandez au Coach pédagogique des explications complémentaires ;...

L'examen blanc est avant tout un outil de progression.

Après chaque évaluation :

- analysez vos erreurs ;
- identifiez les thèmes les moins bien maîtrisés ;
- demandez au Coach pédagogique des explications complémentaires ;
- consultez les ressources correspondantes.

Ce travail d'analyse est souvent plus utile que l'examen lui-même.

---

1. [Conseil précédent](SCR_CONS_PARCOURS_10)
2. [Conseil suivant](SCR_CONS_PARCOURS_12)
3. [Retour à la rubrique](SCR_CONS_PARCOURS_MENU)
4. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : GUIDE_REUSSITE.md — niveau H1 -->

## SCR_CONS_PARCOURS_12

### 📍 Étape 7 : Repasser un examen blanc

<!-- Variables : {rubrique}=PARCOURS; {ordre}=12 -->

### Resume

Après avoir retravaillé vos points faibles, réalisez un nouvel examen blanc. L'objectif n'est pas uniquement d'obtenir un meilleur score. Il s'agit surtout de vérifier que les notions précédemment mal comprises sont d...

Après avoir retravaillé vos points faibles, réalisez un nouvel examen blanc.

L'objectif n'est pas uniquement d'obtenir un meilleur score.

Il s'agit surtout de vérifier que les notions précédemment mal comprises sont désormais acquises.

Vous pouvez répéter ce cycle autant de fois que nécessaire jusqu'à vous sentir pleinement prêt.

---

1. [Conseil précédent](SCR_CONS_PARCOURS_11)
2. [Conseil suivant](SCR_CONS_PARCOURS_13)
3. [Retour à la rubrique](SCR_CONS_PARCOURS_MENU)
4. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : GUIDE_REUSSITE.md — niveau H1 -->

## SCR_CONS_PARCOURS_13

### 🧠 Le parcours recommandé

<!-- Variables : {rubrique}=PARCOURS; {ordre}=13 -->

### Resume

text 📚 Entraînements thématiques │ ▼ 📝 Comprendre les explications │ ▼ 📖 Glossaire + Coach pédagogique │ ▼ 🎯 Ressources de révision │ ▼ 🎭 Mises en situation │ ▼ 📝 Examen blanc │ ▼ 📊 Analyse des erreurs │ ▼ 🔁 Révision...

```text
📚 Entraînements thématiques
            │
            ▼
📝 Comprendre les explications
            │
            ▼
📖 Glossaire + Coach pédagogique
            │
            ▼
🎯 Ressources de révision
            │
            ▼
🎭 Mises en situation
            │
            ▼
📝 Examen blanc
            │
            ▼
📊 Analyse des erreurs
            │
            ▼
🔁 Révision ciblée
            │
            ▼
🏆 Nouvel examen blanc
```

---

> ## 💡 Le conseil du Coach
>
> N'essayez pas de réussir parfaitement votre premier entraînement.
>
> Les erreurs font partie de l'apprentissage.
>
> Ce qui compte réellement est de comprendre pourquoi une réponse est correcte ou incorrecte.
>
> Plus vous analysez vos erreurs, plus vous progressez rapidement.

---

1. [Conseil précédent](SCR_CONS_PARCOURS_12)
2. [Conseil suivant](SCR_CONS_PARCOURS_14)
3. [Retour à la rubrique](SCR_CONS_PARCOURS_MENU)
4. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : GUIDE_REUSSITE.md — niveau H1 -->

## SCR_CONS_PARCOURS_14

### 📌 À retenir

<!-- Variables : {rubrique}=PARCOURS; {ordre}=14 -->

### Resume

Une bonne préparation repose sur une progression logique : découvrir ; comprendre ; mémoriser ; s'entraîner ; corriger ses erreurs ; recommencer. C'est cette progression qui vous permettra d'aborder votre examen avec...

Une bonne préparation repose sur une progression logique :

- découvrir ;
- comprendre ;
- mémoriser ;
- s'entraîner ;
- corriger ses erreurs ;
- recommencer.

C'est cette progression qui vous permettra d'aborder votre examen avec confiance.

---

1. [Conseil précédent](SCR_CONS_PARCOURS_13)
2. [Retour à la rubrique](SCR_CONS_PARCOURS_MENU)
3. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : GUIDE_REUSSITE.md — niveau H1 -->

## SCR_CONS_MEMOIRE_01

### 🧠 Les secrets de la mémoire

<!-- Variables : {rubrique}=MEMOIRE; {ordre}=1 -->

🧠 Les secrets de la mémoire

1. [Conseil suivant](SCR_CONS_MEMOIRE_02)
2. [Retour à la rubrique](SCR_CONS_MEMOIRE_MENU)
3. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : GUIDE_REUSSITE.md — niveau H1 -->

## SCR_CONS_MEMOIRE_02

### Pourquoi oublie-t-on ?

<!-- Variables : {rubrique}=MEMOIRE; {ordre}=2 -->

### Resume

Avez vous déjà eu l'impression de connaître une réponse... puis de l'oublier quelques minutes plus tard ? C'est tout à fait normal. Notre cerveau ne peut pas retenir durablement toutes les informations qu'il rencontre...

Avez-vous déjà eu l'impression de connaître une réponse... puis de l'oublier quelques minutes plus tard ?

C'est tout à fait normal.

Notre cerveau ne peut pas retenir durablement toutes les informations qu'il rencontre.

Pour mémoriser efficacement, il a besoin :

- de revoir plusieurs fois une information ;
- de la comprendre ;
- de la réutiliser régulièrement.

L'objectif n'est donc pas de tout apprendre en une seule fois, mais de consolider progressivement vos connaissances.

---

1. [Conseil précédent](SCR_CONS_MEMOIRE_01)
2. [Conseil suivant](SCR_CONS_MEMOIRE_03)
3. [Retour à la rubrique](SCR_CONS_MEMOIRE_MENU)
4. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : GUIDE_REUSSITE.md — niveau H2 -->

## SCR_CONS_MEMOIRE_03

### 🧠 Secret n°1 : Comprendre avant de mémoriser

<!-- Variables : {rubrique}=MEMOIRE; {ordre}=3 -->

### Resume

Apprendre une réponse sans la comprendre fonctionne rarement sur le long terme. Par exemple, il est plus facile de retenir que : La devise de la République est Liberté, Égalité, Fraternité lorsque vous comprenez ce qu...

Apprendre une réponse sans la comprendre fonctionne rarement sur le long terme.

Par exemple, il est plus facile de retenir que :

> La devise de la République est **Liberté, Égalité, Fraternité**

lorsque vous comprenez ce que représentent ces trois valeurs.

Lorsque vous comprenez une notion, votre cerveau crée davantage de liens avec ce que vous connaissez déjà.

La mémorisation devient alors beaucoup plus facile.

---

> 💡 **Le conseil du Coach**
>
> Si vous n'arrivez pas à retenir une réponse, demandez-vous d'abord si vous en comprenez réellement le sens.

---

1. [Conseil précédent](SCR_CONS_MEMOIRE_02)
2. [Conseil suivant](SCR_CONS_MEMOIRE_04)
3. [Retour à la rubrique](SCR_CONS_MEMOIRE_MENU)
4. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : GUIDE_REUSSITE.md — niveau H1 -->

## SCR_CONS_MEMOIRE_MENU

### 🧠 Mémoriser efficacement

<!-- Variables : {rubrique}=MEMOIRE -->

<!-- Liste dynamique : LISTE_MEMOIRE. Les choix sont générés depuis 99_NAVIGATION. -->

1. [🧠 Les secrets de la mémoire](SCR_CONS_MEMOIRE_01)
2. [Pourquoi oublie-t-on ?](SCR_CONS_MEMOIRE_02)
3. [🧠 Secret n°1 : Comprendre avant de mémoriser](SCR_CONS_MEMOIRE_03)
4. [🧠 Secret n°2 : Réviser plusieurs fois](SCR_CONS_MEMOIRE_04)
5. [🧠 Secret n°3 : Se tester régulièrement](SCR_CONS_MEMOIRE_05)
6. [🧠 Secret n°4 : Faire des liens](SCR_CONS_MEMOIRE_06)
7. [🧠 Secret n°5 : Apprendre par petites séances](SCR_CONS_MEMOIRE_07)
8. [🧠 Secret n°6 : Dormir](SCR_CONS_MEMOIRE_08)
9. [📌 À retenir](SCR_CONS_MEMOIRE_09)
10. [Réviser](SCR_REV_MENU)
11. [Consulter le glossaire](SCR_GLO_MENU)
12. [Retour aux conseils](SCR_CONS_MENU)
13. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Comprendre le fonctionnement de la mémoire et réviser durablement. -->

## SCR_CONS_MEMOIRE_04

### 🧠 Secret n°2 : Réviser plusieurs fois

<!-- Variables : {rubrique}=MEMOIRE; {ordre}=4 -->

### Resume

Relire une information une seule fois ne suffit généralement pas. Le cerveau retient beaucoup mieux lorsqu'il retrouve régulièrement la même notion. Par exemple : une première révision le jour même ; une deuxième quel...

Relire une information une seule fois ne suffit généralement pas.

Le cerveau retient beaucoup mieux lorsqu'il retrouve régulièrement la même notion.

Par exemple :

- une première révision le jour même ;
- une deuxième quelques jours plus tard ;
- une troisième la semaine suivante.

Chaque révision renforce progressivement votre mémoire.

---

1. [Conseil précédent](SCR_CONS_MEMOIRE_03)
2. [Conseil suivant](SCR_CONS_MEMOIRE_05)
3. [Retour à la rubrique](SCR_CONS_MEMOIRE_MENU)
4. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : GUIDE_REUSSITE.md — niveau H1 -->

## SCR_CONS_MEMOIRE_05

### 🧠 Secret n°3 : Se tester régulièrement

<!-- Variables : {rubrique}=MEMOIRE; {ordre}=5 -->

### Resume

Lire une fiche est utile. Essayer de retrouver la réponse sans regarder est encore plus efficace. C'est ce que l'on appelle le rappel actif . Lorsque vous cherchez une réponse dans votre mémoire, votre cerveau renforc...

Lire une fiche est utile.

Essayer de retrouver la réponse sans regarder est encore plus efficace.

C'est ce que l'on appelle le **rappel actif**.

Lorsque vous cherchez une réponse dans votre mémoire, votre cerveau renforce les connexions qui lui permettront de la retrouver plus facilement la prochaine fois.

C'est exactement le principe des entraînements proposés dans NovaFrate.

---

> 🎯 **Petit exercice**
>
> Sans regarder vos notes, essayez de citer les trois couleurs du drapeau français.
>
> Puis vérifiez votre réponse.
>
> Ce simple exercice est plus efficace qu'une nouvelle lecture.

---

1. [Conseil précédent](SCR_CONS_MEMOIRE_04)
2. [Conseil suivant](SCR_CONS_MEMOIRE_06)
3. [Retour à la rubrique](SCR_CONS_MEMOIRE_MENU)
4. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : GUIDE_REUSSITE.md — niveau H1 -->

## SCR_CONS_MEMOIRE_06

### 🧠 Secret n°4 : Faire des liens

<!-- Variables : {rubrique}=MEMOIRE; {ordre}=6 -->

### Resume

Notre mémoire adore les associations. Plus une information est reliée à une autre, plus elle devient facile à retrouver. Par exemple : 1789 ↓ Révolution française ↓ Déclaration des droits de l'homme et du citoyen ↓ Fi...

Notre mémoire adore les associations.

Plus une information est reliée à une autre, plus elle devient facile à retrouver.

Par exemple :

1789

↓

Révolution française

↓

Déclaration des droits de l'homme et du citoyen

↓

Fin de la monarchie absolue

Au lieu de retenir une simple date, vous mémorisez une histoire.

---

1. [Conseil précédent](SCR_CONS_MEMOIRE_05)
2. [Conseil suivant](SCR_CONS_MEMOIRE_07)
3. [Retour à la rubrique](SCR_CONS_MEMOIRE_MENU)
4. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : GUIDE_REUSSITE.md — niveau H1 -->

## SCR_CONS_MEMOIRE_07

### 🧠 Secret n°5 : Apprendre par petites séances

<!-- Variables : {rubrique}=MEMOIRE; {ordre}=7 -->

### Resume

Le cerveau apprend mieux pendant plusieurs séances courtes que pendant une très longue séance. Nous vous conseillons de privilégier : 20 à 30 minutes de travail ; une courte pause ; puis une nouvelle séance si nécessa...

Le cerveau apprend mieux pendant plusieurs séances courtes que pendant une très longue séance.

Nous vous conseillons de privilégier :

- 20 à 30 minutes de travail ;
- une courte pause ;
- puis une nouvelle séance si nécessaire.

Cette méthode améliore la concentration et limite la fatigue.

---

1. [Conseil précédent](SCR_CONS_MEMOIRE_06)
2. [Conseil suivant](SCR_CONS_MEMOIRE_08)
3. [Retour à la rubrique](SCR_CONS_MEMOIRE_MENU)
4. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : GUIDE_REUSSITE.md — niveau H1 -->

## SCR_CONS_MEMOIRE_08

### 🧠 Secret n°6 : Dormir

<!-- Variables : {rubrique}=MEMOIRE; {ordre}=8 -->

### Resume

Le sommeil joue un rôle essentiel dans la mémorisation. Pendant que vous dormez, votre cerveau consolide une partie des connaissances apprises dans la journée. Une bonne nuit de sommeil est souvent plus bénéfique qu'u...

Le sommeil joue un rôle essentiel dans la mémorisation.

Pendant que vous dormez, votre cerveau consolide une partie des connaissances apprises dans la journée.

Une bonne nuit de sommeil est souvent plus bénéfique qu'une longue révision tard dans la nuit.

---

1. [Conseil précédent](SCR_CONS_MEMOIRE_07)
2. [Conseil suivant](SCR_CONS_MEMOIRE_09)
3. [Retour à la rubrique](SCR_CONS_MEMOIRE_MENU)
4. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : GUIDE_REUSSITE.md — niveau H1 -->

## SCR_CONS_MEMOIRE_09

### 📌 À retenir

<!-- Variables : {rubrique}=MEMOIRE; {ordre}=9 -->

### Resume

Pour mieux mémoriser : ✔ Comprenez avant d'apprendre. ✔ Révisez régulièrement. ✔ Testez vous souvent. ✔ Faites des liens entre les notions. ✔ Travaillez par petites séances. ✔ Dormez suffisamment. 💡 Le conseil du Coac...

Pour mieux mémoriser :

✔ Comprenez avant d'apprendre.

✔ Révisez régulièrement.

✔ Testez-vous souvent.

✔ Faites des liens entre les notions.

✔ Travaillez par petites séances.

✔ Dormez suffisamment.

---

> 💡 **Le conseil du Coach**
>
> La mémoire n'est pas une question de chance.
>
> C'est une méthode.
>
> En appliquant ces quelques principes, vous retiendrez beaucoup plus facilement les connaissances nécessaires pour réussir votre examen.

---

1. [Conseil précédent](SCR_CONS_MEMOIRE_08)
2. [Retour à la rubrique](SCR_CONS_MEMOIRE_MENU)
3. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : GUIDE_REUSSITE.md — niveau H1 -->

## SCR_CONS_MNEMO_01

### 🧩 Les moyens mnémotechniques pour réussir l'examen civique

<!-- Variables : {rubrique}=MNEMO; {ordre}=1 -->

🧩 Les moyens mnémotechniques pour réussir l'examen civique

1. [Conseil suivant](SCR_CONS_MNEMO_02)
2. [Retour à la rubrique](SCR_CONS_MNEMO_MENU)
3. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : GUIDE_REUSSITE.md — niveau H1 -->

## SCR_CONS_MNEMO_02

### Pourquoi utiliser des moyens mnémotechniques ?

<!-- Variables : {rubrique}=MNEMO; {ordre}=2 -->

### Resume

Notre cerveau retient beaucoup plus facilement : une histoire ; une image ; une émotion ; une association d'idées. À l'inverse, il retient difficilement une simple liste de dates ou de noms. Les techniques proposées d...

Notre cerveau retient beaucoup plus facilement :

- une histoire ;
- une image ;
- une émotion ;
- une association d'idées.

À l'inverse, il retient difficilement une simple liste de dates ou de noms.

Les techniques proposées dans ce chapitre ont pour objectif de faciliter vos révisions.

Elles ne remplacent pas la compréhension des notions, mais elles peuvent vous aider à mémoriser plus rapidement les informations importantes.

---

1. [Conseil précédent](SCR_CONS_MNEMO_01)
2. [Conseil suivant](SCR_CONS_MNEMO_03)
3. [Retour à la rubrique](SCR_CONS_MNEMO_MENU)
4. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : GUIDE_REUSSITE.md — niveau H2 -->

## SCR_CONS_MNEMO_03

### 📅 Mémoriser les grandes dates de l'histoire de France

<!-- Variables : {rubrique}=MNEMO; {ordre}=3 -->

### Resume

Les dates sont souvent celles que les candidats redoutent le plus. Pourtant, il n'est pas nécessaire d'apprendre une longue liste de chiffres. Essayez plutôt d'associer chaque date à une image mentale.

Les dates sont souvent celles que les candidats redoutent le plus.

Pourtant, il n'est pas nécessaire d'apprendre une longue liste de chiffres.

Essayez plutôt d'associer chaque date à une image mentale.

1. [Conseil précédent](SCR_CONS_MNEMO_02)
2. [Conseil suivant](SCR_CONS_MNEMO_04)
3. [Retour à la rubrique](SCR_CONS_MNEMO_MENU)
4. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : GUIDE_REUSSITE.md — niveau H1 -->

## SCR_CONS_MNEMO_04

### Exemple

<!-- Variables : {rubrique}=MNEMO; {ordre}=4 -->

Exemple

1. [Conseil précédent](SCR_CONS_MNEMO_03)
2. [Conseil suivant](SCR_CONS_MNEMO_05)
3. [Retour à la rubrique](SCR_CONS_MNEMO_MENU)
4. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : GUIDE_REUSSITE.md — niveau H2 -->

## SCR_CONS_MNEMO_MENU

### 🧩 Utiliser des moyens mnémotechniques

<!-- Variables : {rubrique}=MNEMO -->

<!-- Liste dynamique : LISTE_MNEMO. Les choix sont générés depuis 99_NAVIGATION. -->

1. [🧩 Les moyens mnémotechniques pour réussir l'examen civique](SCR_CONS_MNEMO_01)
2. [Pourquoi utiliser des moyens mnémotechniques ?](SCR_CONS_MNEMO_02)
3. [📅 Mémoriser les grandes dates de l'histoire de France](SCR_CONS_MNEMO_03)
4. [Exemple](SCR_CONS_MNEMO_04)
5. [1789](SCR_CONS_MNEMO_05)
6. [1905](SCR_CONS_MNEMO_06)
7. [1958](SCR_CONS_MNEMO_07)
8. [🇫🇷 Mémoriser les symboles de la République](SCR_CONS_MNEMO_08)
9. [🗺️ Mémoriser les régions françaises](SCR_CONS_MNEMO_09)
10. [🌊 Mémoriser les principaux fleuves](SCR_CONS_MNEMO_10)
11. [👤 Mémoriser les personnages importants](SCR_CONS_MNEMO_11)
12. [Écrivains](SCR_CONS_MNEMO_12)
13. [Peintres](SCR_CONS_MNEMO_13)
14. [Scientifiques](SCR_CONS_MNEMO_14)
15. [Hommes et femmes politiques](SCR_CONS_MNEMO_15)
16. [🏛️ Mémoriser les institutions](SCR_CONS_MNEMO_16)
17. [🧠 Utiliser le rappel actif](SCR_CONS_MNEMO_17)
18. [📌 À retenir](SCR_CONS_MNEMO_18)
19. [Réviser](SCR_REV_MENU)
20. [Consulter le glossaire](SCR_GLO_MENU)
21. [Retour aux conseils](SCR_CONS_MENU)
22. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Mémoriser dates, symboles, géographie, personnages et institutions. -->

## SCR_CONS_MNEMO_05

### 1789

<!-- Variables : {rubrique}=MNEMO; {ordre}=5 -->

### Resume

Imaginez une immense porte qui s'ouvre. Cette porte représente le début d'une nouvelle France. ➡️ Révolution française

Imaginez une immense porte qui s'ouvre.

Cette porte représente le début d'une nouvelle France.

➡️ Révolution française

---

1. [Conseil précédent](SCR_CONS_MNEMO_04)
2. [Conseil suivant](SCR_CONS_MNEMO_06)
3. [Retour à la rubrique](SCR_CONS_MNEMO_MENU)
4. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : GUIDE_REUSSITE.md — niveau H3 -->

## SCR_CONS_MNEMO_06

### 1905

<!-- Variables : {rubrique}=MNEMO; {ordre}=6 -->

### Resume

Imaginez une église et une mairie qui prennent chacune un chemin différent. ➡️ Séparation des Églises et de l'État.

Imaginez une église et une mairie qui prennent chacune un chemin différent.

➡️ Séparation des Églises et de l'État.

---

1. [Conseil précédent](SCR_CONS_MNEMO_05)
2. [Conseil suivant](SCR_CONS_MNEMO_07)
3. [Retour à la rubrique](SCR_CONS_MNEMO_MENU)
4. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : GUIDE_REUSSITE.md — niveau H3 -->

## SCR_CONS_MNEMO_07

### 1958

<!-- Variables : {rubrique}=MNEMO; {ordre}=7 -->

### Resume

Imaginez une maison toute neuve. Cette maison représente la nouvelle Constitution. ➡️ Naissance de la Ve République. 💡 Le conseil du Coach Ne mémorisez jamais une date seule. Associez toujours : une date + un événemen...

Imaginez une maison toute neuve.

Cette maison représente la nouvelle Constitution.

➡️ Naissance de la Ve République.

---

> 💡 Le conseil du Coach
>
> Ne mémorisez jamais une date seule.
>
> Associez toujours :
>
> **une date + un événement + une image.**

---

1. [Conseil précédent](SCR_CONS_MNEMO_06)
2. [Conseil suivant](SCR_CONS_MNEMO_08)
3. [Retour à la rubrique](SCR_CONS_MNEMO_MENU)
4. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : GUIDE_REUSSITE.md — niveau H3 -->

## SCR_CONS_MNEMO_08

### 🇫🇷 Mémoriser les symboles de la République

<!-- Variables : {rubrique}=MNEMO; {ordre}=8 -->

### Resume

Les symboles sont beaucoup plus faciles à retenir lorsqu'on les associe à leur rôle. Symbole À quoi penser ? 🇫🇷 Drapeau La France 🎵 Marseillaise Hymne national 👩 Marianne République 🏛 Devise Liberté • Égalité • Frater...

Les symboles sont beaucoup plus faciles à retenir lorsqu'on les associe à leur rôle.

| Symbole | À quoi penser ? |
|----------|-----------------|
| 🇫🇷 Drapeau | La France |
| 🎵 Marseillaise | Hymne national |
| 👩 Marianne | République |
| 🏛 Devise | Liberté • Égalité • Fraternité |
| 📜 14 juillet | Fête nationale |

Cherchez toujours à comprendre ce que représente chaque symbole plutôt que d'apprendre une simple liste.

---

1. [Conseil précédent](SCR_CONS_MNEMO_07)
2. [Conseil suivant](SCR_CONS_MNEMO_09)
3. [Retour à la rubrique](SCR_CONS_MNEMO_MENU)
4. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : GUIDE_REUSSITE.md — niveau H1 -->

## SCR_CONS_MNEMO_09

### 🗺️ Mémoriser les régions françaises

<!-- Variables : {rubrique}=MNEMO; {ordre}=9 -->

### Resume

Les régions sont souvent difficiles à retenir lorsqu'on essaie de les apprendre dans le désordre. Nous vous conseillons : d'utiliser une carte de France ; de placer progressivement les régions ; de les revoir régulièr...

Les régions sont souvent difficiles à retenir lorsqu'on essaie de les apprendre dans le désordre.

Nous vous conseillons :

- d'utiliser une carte de France ;
- de placer progressivement les régions ;
- de les revoir régulièrement.

L'activité **Géographie de la France** disponible dans NovaFrate est spécialement conçue pour faciliter cette mémorisation.

---

1. [Conseil précédent](SCR_CONS_MNEMO_08)
2. [Conseil suivant](SCR_CONS_MNEMO_10)
3. [Retour à la rubrique](SCR_CONS_MNEMO_MENU)
4. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : GUIDE_REUSSITE.md — niveau H1 -->

## SCR_CONS_MNEMO_10

### 🌊 Mémoriser les principaux fleuves

<!-- Variables : {rubrique}=MNEMO; {ordre}=10 -->

### Resume

Essayez de visualiser leur parcours sur une carte. Plus vous les verrez, plus ils deviendront faciles à retenir. Ne cherchez pas à apprendre leur nom par cœur sans les situer.

Essayez de visualiser leur parcours sur une carte.

Plus vous les verrez, plus ils deviendront faciles à retenir.

Ne cherchez pas à apprendre leur nom par cœur sans les situer.

---

1. [Conseil précédent](SCR_CONS_MNEMO_09)
2. [Conseil suivant](SCR_CONS_MNEMO_11)
3. [Retour à la rubrique](SCR_CONS_MNEMO_MENU)
4. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : GUIDE_REUSSITE.md — niveau H1 -->

## SCR_CONS_MNEMO_11

### 👤 Mémoriser les personnages importants

<!-- Variables : {rubrique}=MNEMO; {ordre}=11 -->

### Resume

Il est beaucoup plus simple de retenir les personnages lorsqu'ils sont regroupés par famille. Par exemple :

Il est beaucoup plus simple de retenir les personnages lorsqu'ils sont regroupés par famille.

Par exemple :

1. [Conseil précédent](SCR_CONS_MNEMO_10)
2. [Conseil suivant](SCR_CONS_MNEMO_12)
3. [Retour à la rubrique](SCR_CONS_MNEMO_MENU)
4. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : GUIDE_REUSSITE.md — niveau H1 -->

## SCR_CONS_MNEMO_12

### Écrivains

<!-- Variables : {rubrique}=MNEMO; {ordre}=12 -->

### Resume

Victor Hugo Molière Albert Camus George Sand

- Victor Hugo
- Molière
- Albert Camus
- George Sand

---

1. [Conseil précédent](SCR_CONS_MNEMO_11)
2. [Conseil suivant](SCR_CONS_MNEMO_13)
3. [Retour à la rubrique](SCR_CONS_MNEMO_MENU)
4. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : GUIDE_REUSSITE.md — niveau H3 -->

## SCR_CONS_MNEMO_13

### Peintres

<!-- Variables : {rubrique}=MNEMO; {ordre}=13 -->

### Resume

Claude Monet Paul Cézanne Auguste Renoir

- Claude Monet
- Paul Cézanne
- Auguste Renoir

---

1. [Conseil précédent](SCR_CONS_MNEMO_12)
2. [Conseil suivant](SCR_CONS_MNEMO_14)
3. [Retour à la rubrique](SCR_CONS_MNEMO_MENU)
4. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : GUIDE_REUSSITE.md — niveau H3 -->

## SCR_CONS_MNEMO_14

### Scientifiques

<!-- Variables : {rubrique}=MNEMO; {ordre}=14 -->

### Resume

Marie Curie

- Marie Curie

---

1. [Conseil précédent](SCR_CONS_MNEMO_13)
2. [Conseil suivant](SCR_CONS_MNEMO_15)
3. [Retour à la rubrique](SCR_CONS_MNEMO_MENU)
4. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : GUIDE_REUSSITE.md — niveau H3 -->

## SCR_CONS_MNEMO_15

### Hommes et femmes politiques

<!-- Variables : {rubrique}=MNEMO; {ordre}=15 -->

### Resume

Charles de Gaulle Simone Veil Votre cerveau retiendra plus facilement ces catégories qu'une liste de noms mélangés.

- Charles de Gaulle
- Simone Veil

Votre cerveau retiendra plus facilement ces catégories qu'une liste de noms mélangés.

---

1. [Conseil précédent](SCR_CONS_MNEMO_14)
2. [Conseil suivant](SCR_CONS_MNEMO_16)
3. [Retour à la rubrique](SCR_CONS_MNEMO_MENU)
4. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : GUIDE_REUSSITE.md — niveau H3 -->

## SCR_CONS_MNEMO_16

### 🏛️ Mémoriser les institutions

<!-- Variables : {rubrique}=MNEMO; {ordre}=16 -->

### Resume

Ne cherchez pas à retenir immédiatement toutes leurs missions. Commencez par répondre à une question simple : Qui fait quoi ? Par exemple : Président de la République ↓ Chef de l'État Premier ministre ↓ Dirige le Gouv...

Ne cherchez pas à retenir immédiatement toutes leurs missions.

Commencez par répondre à une question simple :

**Qui fait quoi ?**

Par exemple :

Président de la République

↓

Chef de l'État

---

Premier ministre

↓

Dirige le Gouvernement

---

Parlement

↓

Vote les lois

---

Petit à petit, ajoutez de nouveaux détails.

---

1. [Conseil précédent](SCR_CONS_MNEMO_15)
2. [Conseil suivant](SCR_CONS_MNEMO_17)
3. [Retour à la rubrique](SCR_CONS_MNEMO_MENU)
4. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : GUIDE_REUSSITE.md — niveau H1 -->

## SCR_CONS_MNEMO_17

### 🧠 Utiliser le rappel actif

<!-- Variables : {rubrique}=MNEMO; {ordre}=17 -->

### Resume

Une fois votre séance terminée : Fermez votre cahier. Essayez de retrouver : les trois couleurs du drapeau ; la devise de la République ; les cinq thématiques de l'examen ; trois grandes dates ; trois personnages célè...

Une fois votre séance terminée :

Fermez votre cahier.

Essayez de retrouver :

- les trois couleurs du drapeau ;
- la devise de la République ;
- les cinq thématiques de l'examen ;
- trois grandes dates ;
- trois personnages célèbres.

Puis vérifiez vos réponses.

Cet exercice est beaucoup plus efficace qu'une simple relecture.

---

1. [Conseil précédent](SCR_CONS_MNEMO_16)
2. [Conseil suivant](SCR_CONS_MNEMO_18)
3. [Retour à la rubrique](SCR_CONS_MNEMO_MENU)
4. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : GUIDE_REUSSITE.md — niveau H1 -->

## SCR_CONS_MNEMO_18

### 📌 À retenir

<!-- Variables : {rubrique}=MNEMO; {ordre}=18 -->

### Resume

Pour mieux mémoriser : ✔ Associez les dates à des images. ✔ Classez les personnages par catégorie. ✔ Utilisez une carte pour apprendre la géographie. ✔ Comprenez le rôle des institutions. ✔ Testez vous régulièrement s...

Pour mieux mémoriser :

✔ Associez les dates à des images.

✔ Classez les personnages par catégorie.

✔ Utilisez une carte pour apprendre la géographie.

✔ Comprenez le rôle des institutions.

✔ Testez-vous régulièrement sans regarder vos notes.

---

> ## 💡 Le conseil du Coach
>
> N'essayez pas de tout retenir en une seule fois.
>
> Votre mémoire fonctionne comme un muscle :
>
> plus vous la sollicitez régulièrement, plus elle devient efficace.

1. [Conseil précédent](SCR_CONS_MNEMO_17)
2. [Retour à la rubrique](SCR_CONS_MNEMO_MENU)
3. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : GUIDE_REUSSITE.md — niveau H1 -->

<!-- Fin du fichier source : modules\08_conseils.md -->

<!-- Début du fichier source : modules\09_faq.md -->

<!-- Module généré automatiquement : FAQ -->
<!-- Date : 2026-08-03T13:13:33+02:00 -->

## SCR_FAQ_CATEGORIES

### Parcourir la FAQ

<!-- Liste dynamique : LISTE_CATEGORIES. Les choix sont générés depuis 99_NAVIGATION. -->

1. [📘 Examen civique](SCR_FAQ_EXAMEN_MENU)
2. [📝 Inscription, prix et organisation](SCR_FAQ_INSCRIPTION_MENU)
3. [📊 Résultats](SCR_FAQ_RESULTATS_MENU)
4. [🏛️ OFII et formation civique](SCR_FAQ_OFII_MENU)
5. [👤 Entretien de naturalisation](SCR_FAQ_ENTRETIEN_MENU)
6. [💻 NovaFrate](SCR_FAQ_NOVAFRATE_MENU)
7. [ℹ️ Conseils de réussite](SCR_FAQ_CONSEILS_MENU)
8. [Retour à la FAQ](SCR_FAQ_MENU)
9. [Retour au menu principal](MENU_PRINCIPAL)

## SCR_FAQ_MENU

### FAQ du Coach

Recherchez une question ou parcourez les catégories de la FAQ.

1. [Rechercher une question](SCR_FAQ_SEARCH)
2. [Parcourir par catégorie](SCR_FAQ_CATEGORIES)
3. [Questions fréquentes](SCR_FAQ_POPULAR)
4. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran d’entrée -->

## SCR_FAQ_POPULAR

### Questions les plus fréquentes

<!-- Liste dynamique : LISTE_POPULAR. Les choix sont générés depuis 99_NAVIGATION. -->

1. [Qu'est-ce que l'examen civique ?](SCR_FAQ_001)
2. [Combien de questions comporte l'examen civique ?](SCR_FAQ_004)
3. [Quel score doit-on obtenir pour réussir l'examen civique ?](SCR_FAQ_009)
4. [Comment s'inscrire à l'examen civique ?](SCR_FAQ_018)
5. [Combien coûte l'examen civique ?](SCR_FAQ_019)
6. [Quel score faut-il obtenir pour réussir l'examen ?](SCR_FAQ_025)
7. [Quand reçoit-on les résultats ?](SCR_FAQ_028)
8. [Quelle est la différence entre la formation civique et l'examen civique ?](SCR_FAQ_033)
9. [Qu'est-ce que l'entretien de naturalisation ?](SCR_FAQ_037)
10. [Les questions proposées sur NovaFrate sont-elles officielles ?](SCR_FAQ_053)
11. [Que vais-je trouver sur NovaFrate ?](SCR_FAQ_054)
12. [Comment bien préparer l'examen civique ?](SCR_FAQ_063)
13. [Retour à la FAQ](SCR_FAQ_MENU)
14. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Sélection éditoriale -->

## SCR_FAQ_SEARCH

### Rechercher dans la FAQ

<!-- Variables : {requete_faq} -->

Saisissez un mot-clé ou une question courte. Le moteur compare la saisie aux questions et aux mots-clés.

<!-- Transition automatique NAV_FAQ_006 : Saisie validée → SCR_FAQ_RESULT -->
1. [Rechercher](SCR_FAQ_RESULT)
1. [Parcourir les catégories](SCR_FAQ_CATEGORIES)
2. [Retour à la FAQ](SCR_FAQ_MENU)

<!-- Accepte un mot ou une question courte -->

## SCR_FAQ_RESULT

### Résultat de recherche

<!-- Variables : {requete_faq}; {faq_id} -->

Normaliser la saisie puis rechercher dans Question et Mots-clés. Ouvrir la réponse la plus pertinente.

<!-- Transition automatique NAV_FAQ_009 : Correspondance trouvée → @{screen_id_faq} -->
1. [Ouvrir la meilleure réponse](@{screen_id_faq})
<!-- Transition automatique NAV_FAQ_010 : Aucune correspondance → SCR_FAQ_NOT_FOUND -->
1. [Aucune réponse trouvée](SCR_FAQ_NOT_FOUND)

<!-- Écran logique non affiché -->

## SCR_FAQ_NOT_FOUND

### Réponse non trouvée

<!-- Variables : {requete_faq} -->

Aucune réponse exacte n’a été trouvée. Consultez le glossaire, les révisions ou les conseils de réussite.

1. [Nouvelle recherche](SCR_FAQ_SEARCH)
2. [Consulter le glossaire](SCR_GLO_MENU)
3. [Consulter les révisions](SCR_REV_MENU)
4. [Voir les conseils de réussite](SCR_CONS_MENU)
5. [Retour au menu principal](MENU_PRINCIPAL)

## SCR_FAQ_063

### Comment bien préparer l'examen civique ?

<!-- Variables : {categorie}=CONSEILS; {ordre}=1; {faq_id}=FAQ-063 -->

### Reponse markdown

Une bonne préparation repose avant tout sur la régularité.

Nous vous conseillons de :

- réviser un peu chaque jour ;
- comprendre les notions plutôt que les apprendre par cœur ;
- refaire les questions sur lesquelles vous avez échoué ;
- réaliser plusieurs examens blancs avant le jour de l'épreuve.

Le Coach pédagogique adapte vos révisions en fonction de vos résultats.

1. [Question suivante](SCR_FAQ_064)
2. [Nouvelle recherche](SCR_FAQ_SEARCH)
3. [Retour à la catégorie](SCR_FAQ_CONSEILS_MENU)
4. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : FAQ_COACH_CIVIQUE.md -->

## SCR_FAQ_064

### Combien de temps faut-il réviser ?

<!-- Variables : {categorie}=CONSEILS; {ordre}=2; {faq_id}=FAQ-064 -->

### Reponse markdown

Il n'existe pas de durée idéale.

Cela dépend de votre niveau de départ et de vos connaissances.

Quelques séances régulières de 15 à 30 minutes sont généralement plus efficaces qu'une longue révision réalisée la veille de l'examen.

1. [Question précédente](SCR_FAQ_063)
2. [Question suivante](SCR_FAQ_065)
3. [Nouvelle recherche](SCR_FAQ_SEARCH)
4. [Retour à la catégorie](SCR_FAQ_CONSEILS_MENU)
5. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : FAQ_COACH_CIVIQUE.md -->

## SCR_FAQ_065

### Dois-je apprendre toutes les réponses par cœur ?

<!-- Variables : {categorie}=CONSEILS; {ordre}=3; {faq_id}=FAQ-065 -->

### Reponse markdown

Non.

L'objectif est de comprendre les notions.

Les questions peuvent être formulées différemment le jour de l'examen.

Une bonne compréhension vous permettra de répondre correctement même si la formulation change.

1. [Question précédente](SCR_FAQ_064)
2. [Question suivante](SCR_FAQ_066)
3. [Nouvelle recherche](SCR_FAQ_SEARCH)
4. [Retour à la catégorie](SCR_FAQ_CONSEILS_MENU)
5. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : FAQ_COACH_CIVIQUE.md -->

## SCR_FAQ_066

### Comment retenir les dates importantes ?

<!-- Variables : {categorie}=CONSEILS; {ordre}=4; {faq_id}=FAQ-066 -->

### Reponse markdown

Il est conseillé d'associer chaque date à un événement important.

Par exemple :

- 1789 → Révolution française
- 1905 → Loi de séparation des Églises et de l'État
- 1958 → Constitution de la Ve République

Le Coach propose des rappels réguliers afin de faciliter la mémorisation.

1. [Question précédente](SCR_FAQ_065)
2. [Question suivante](SCR_FAQ_067)
3. [Nouvelle recherche](SCR_FAQ_SEARCH)
4. [Retour à la catégorie](SCR_FAQ_CONSEILS_MENU)
5. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : FAQ_COACH_CIVIQUE.md -->

## SCR_FAQ_067

### Que faire si je me trompe souvent sur un même thème ?

<!-- Variables : {categorie}=CONSEILS; {ordre}=5; {faq_id}=FAQ-067 -->

### Reponse markdown

Il est préférable de retravailler le thème concerné avant de poursuivre vos révisions.

Le Coach pédagogique identifie automatiquement vos difficultés et peut vous proposer :

- de revoir le cours ;
- de consulter le glossaire ;
- de refaire des questions similaires.

1. [Question précédente](SCR_FAQ_066)
2. [Question suivante](SCR_FAQ_068)
3. [Nouvelle recherche](SCR_FAQ_SEARCH)
4. [Retour à la catégorie](SCR_FAQ_CONSEILS_MENU)
5. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : FAQ_COACH_CIVIQUE.md -->

## SCR_FAQ_068

### Comment répondre aux questions ouvertes ?

<!-- Variables : {categorie}=CONSEILS; {ordre}=6; {faq_id}=FAQ-068 -->

### Reponse markdown

Prenez le temps de lire attentivement la question.

Répondez avec des mots simples et précis.

Lorsque plusieurs éléments sont attendus, essayez de tous les citer.

Le Coach vous indique toujours les éléments essentiels attendus dans la réponse.

1. [Question précédente](SCR_FAQ_067)
2. [Question suivante](SCR_FAQ_069)
3. [Nouvelle recherche](SCR_FAQ_SEARCH)
4. [Retour à la catégorie](SCR_FAQ_CONSEILS_MENU)
5. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : FAQ_COACH_CIVIQUE.md -->

## SCR_FAQ_069

### Que faire si je ne connais pas une réponse ?

<!-- Variables : {categorie}=CONSEILS; {ordre}=7; {faq_id}=FAQ-069 -->

### Reponse markdown

Ne cherchez pas à mémoriser immédiatement la bonne réponse.

Prenez le temps de comprendre l'explication proposée par le Coach.

Il vous reposera ensuite une question similaire afin de vérifier que la notion est acquise.

1. [Question précédente](SCR_FAQ_068)
2. [Question suivante](SCR_FAQ_070)
3. [Nouvelle recherche](SCR_FAQ_SEARCH)
4. [Retour à la catégorie](SCR_FAQ_CONSEILS_MENU)
5. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : FAQ_COACH_CIVIQUE.md -->

## SCR_FAQ_CONSEILS_MENU

### ℹ️ Conseils de réussite

<!-- Variables : {categorie}=CONSEILS -->

<!-- Liste dynamique : LISTE_CONSEILS. Les choix sont générés depuis 99_NAVIGATION. -->

1. [Comment bien préparer l'examen civique ?](SCR_FAQ_063)
2. [Combien de temps faut-il réviser ?](SCR_FAQ_064)
3. [Dois-je apprendre toutes les réponses par cœur ?](SCR_FAQ_065)
4. [Comment retenir les dates importantes ?](SCR_FAQ_066)
5. [Que faire si je me trompe souvent sur un même thème ?](SCR_FAQ_067)
6. [Comment répondre aux questions ouvertes ?](SCR_FAQ_068)
7. [Que faire si je ne connais pas une réponse ?](SCR_FAQ_069)
8. [Comment gérer le stress avant l'examen ?](SCR_FAQ_070)
9. [Comment savoir si je suis prêt pour l'examen ?](SCR_FAQ_071)
10. [Rechercher dans la FAQ](SCR_FAQ_SEARCH)
11. [Retour aux catégories](SCR_FAQ_CATEGORIES)
12. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Réviser efficacement, mémoriser, gérer le stress et savoir si l’on est prêt. -->

## SCR_FAQ_070

### Comment gérer le stress avant l'examen ?

<!-- Variables : {categorie}=CONSEILS; {ordre}=8; {faq_id}=FAQ-070 -->

### Reponse markdown

Le stress est normal.

Une bonne préparation permet de gagner en confiance.

Avant l'examen :

- dormez suffisamment ;
- arrivez en avance ;
- prenez le temps de lire chaque question ;
- répondez calmement.

Le Coach vous aide à vous entraîner dans des conditions proches de l'examen afin de réduire le stress le jour J.

1. [Question précédente](SCR_FAQ_069)
2. [Question suivante](SCR_FAQ_071)
3. [Nouvelle recherche](SCR_FAQ_SEARCH)
4. [Retour à la catégorie](SCR_FAQ_CONSEILS_MENU)
5. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : FAQ_COACH_CIVIQUE.md -->

## SCR_FAQ_071

### Comment savoir si je suis prêt pour l'examen ?

<!-- Variables : {categorie}=CONSEILS; {ordre}=9; {faq_id}=FAQ-071 -->

### Reponse markdown

Lorsque vous obtenez régulièrement de bons résultats aux entraînements et aux examens blancs, vous êtes probablement prêt à passer l'examen.

Le Coach suit votre progression et vous indique les thèmes qu'il est encore conseillé de revoir.

1. [Question précédente](SCR_FAQ_070)
2. [Nouvelle recherche](SCR_FAQ_SEARCH)
3. [Retour à la catégorie](SCR_FAQ_CONSEILS_MENU)
4. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : FAQ_COACH_CIVIQUE.md -->

## SCR_FAQ_029

### Qu'est-ce que l'OFII ?

<!-- Variables : {categorie}=OFII; {ordre}=1; {faq_id}=FAQ-029 -->

### Reponse markdown

L'OFII (Office français de l'immigration et de l'intégration) est un établissement public chargé d'accompagner les personnes étrangères dans leur parcours d'intégration en France.

Il intervient notamment dans :

- l'accueil des nouveaux arrivants ;
- le Contrat d'Intégration Républicaine (CIR) ;
- les formations civiques ;
- les formations linguistiques lorsque cela est nécessaire.

1. [Question suivante](SCR_FAQ_030)
2. [Nouvelle recherche](SCR_FAQ_SEARCH)
3. [Retour à la catégorie](SCR_FAQ_OFII_MENU)
4. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : FAQ_COACH_CIVIQUE.md -->

## SCR_FAQ_030

### Qu'est-ce que la formation civique de l'OFII ?

<!-- Variables : {categorie}=OFII; {ordre}=2; {faq_id}=FAQ-030 -->

### Reponse markdown

La formation civique est une formation de 4 jours obligatoire dans le cadre du Contrat d'Intégration Républicaine (CIR).

Elle permet de découvrir :

- les valeurs de la République française ;
- les droits et les devoirs en France ;
- le fonctionnement des institutions ;
- les principales règles de la vie en société.

Cette formation favorise l'intégration des nouveaux arrivants et prépare à l'examen civique, mais ne le remplace pas.

1. [Question précédente](SCR_FAQ_029)
2. [Question suivante](SCR_FAQ_031)
3. [Nouvelle recherche](SCR_FAQ_SEARCH)
4. [Retour à la catégorie](SCR_FAQ_OFII_MENU)
5. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : FAQ_COACH_CIVIQUE.md -->

## SCR_FAQ_031

### Combien de temps dure la formation civique ?

<!-- Variables : {categorie}=OFII; {ordre}=3; {faq_id}=FAQ-031 -->

### Reponse markdown

La formation civique de l'OFII dure 4 jours (soit 24 heures au total). Elle se déroule généralement sur 4 journées consécutives ou réparties sur plusieurs semaines.

1. [Question précédente](SCR_FAQ_030)
2. [Question suivante](SCR_FAQ_032)
3. [Nouvelle recherche](SCR_FAQ_SEARCH)
4. [Retour à la catégorie](SCR_FAQ_OFII_MENU)
5. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : FAQ_COACH_CIVIQUE.md -->

## SCR_FAQ_032

### Qu'est-ce que le Contrat d'Intégration Républicaine (CIR) ?

<!-- Variables : {categorie}=OFII; {ordre}=4; {faq_id}=FAQ-032 -->

### Reponse markdown

Le Contrat d'Intégration Républicaine (CIR) est un engagement entre l'État français et les primo-arrivants

Il prévoit notamment :

- une formation civique ;
- un accompagnement vers l'intégration ;
- et, lorsque cela est nécessaire, une formation en langue française.

L'objectif est de favoriser une bonne intégration dans la société française. Le CIR est obligatoire pour obtenir une carte de séjour pluriannuelle.

1. [Question précédente](SCR_FAQ_031)
2. [Question suivante](SCR_FAQ_033)
3. [Nouvelle recherche](SCR_FAQ_SEARCH)
4. [Retour à la catégorie](SCR_FAQ_OFII_MENU)
5. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : FAQ_COACH_CIVIQUE.md -->

## SCR_FAQ_OFII_MENU

### 🏛️ OFII et formation civique

<!-- Variables : {categorie}=OFII -->

<!-- Liste dynamique : LISTE_OFII. Les choix sont générés depuis 99_NAVIGATION. -->

1. [Qu'est-ce que l'OFII ?](SCR_FAQ_029)
2. [Qu'est-ce que la formation civique de l'OFII ?](SCR_FAQ_030)
3. [Combien de temps dure la formation civique ?](SCR_FAQ_031)
4. [Qu'est-ce que le Contrat d'Intégration Républicaine (CIR) ?](SCR_FAQ_032)
5. [Quelle est la différence entre la formation civique et l'examen civique ?](SCR_FAQ_033)
6. [La formation civique suffit-elle pour réussir l'examen civique ?](SCR_FAQ_034)
7. [L'OFII organise-t-il l'examen civique ?](SCR_FAQ_035)
8. [Que se passe-t-il après la formation civique ?](SCR_FAQ_036)
9. [Rechercher dans la FAQ](SCR_FAQ_SEARCH)
10. [Retour aux catégories](SCR_FAQ_CATEGORIES)
11. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Distinguer l’OFII, le CIR, la formation civique et l’examen. -->

## SCR_FAQ_033

### Quelle est la différence entre la formation civique et l'examen civique ?

<!-- Variables : {categorie}=OFII; {ordre}=5; {faq_id}=FAQ-033 -->

### Reponse markdown

La formation civique et l'examen civique sont deux dispositifs différents.

La **formation civique** est une formation de 4 jours permettant d'acquérir les connaissances nécessaires sur la France et les valeurs de la République. Elle est gratuite et obligatoire pour les signataires du contrat d'intégration Républicaine (CIR). 

L'**examen civique** permet ensuite de vérifier que ces connaissances sont acquises. Le test est payant et comprend 40 questions. 

La formation prépare donc à l'examen, mais ne le remplace pas.

1. [Question précédente](SCR_FAQ_032)
2. [Question suivante](SCR_FAQ_034)
3. [Nouvelle recherche](SCR_FAQ_SEARCH)
4. [Retour à la catégorie](SCR_FAQ_OFII_MENU)
5. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : FAQ_COACH_CIVIQUE.md -->

## SCR_FAQ_034

### La formation civique suffit-elle pour réussir l'examen civique ?

<!-- Variables : {categorie}=OFII; {ordre}=6; {faq_id}=FAQ-034 -->

### Reponse markdown

La formation civique constitue une excellente base, mais elle ne couvre pas toujours l'ensemble des connaissances évaluées lors de l'examen.

Pour augmenter vos chances de réussite, il est conseillé de compléter cette formation par un entraînement régulier avec des questions similaires à celles de l'examen.

Le Coach pédagogique est conçu pour vous accompagner dans cette préparation.

1. [Question précédente](SCR_FAQ_033)
2. [Question suivante](SCR_FAQ_035)
3. [Nouvelle recherche](SCR_FAQ_SEARCH)
4. [Retour à la catégorie](SCR_FAQ_OFII_MENU)
5. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : FAQ_COACH_CIVIQUE.md -->

## SCR_FAQ_035

### L'OFII organise-t-il l'examen civique ?

<!-- Variables : {categorie}=OFII; {ordre}=7; {faq_id}=FAQ-035 -->

### Reponse markdown

Non.

L'OFII organise la formation civique dans le cadre du Contrat d'Intégration Républicaine.

L'examen civique est organisé par des centres agréés selon les modalités prévues par la réglementation.

Si vous souhaitez passer l'examen, utilisez la rubrique **« Je passe mon examen »** du Coach ou consultez le site de **FRATE Formation** pour trouver un centre et vous inscrire.

1. [Question précédente](SCR_FAQ_034)
2. [Question suivante](SCR_FAQ_036)
3. [Nouvelle recherche](SCR_FAQ_SEARCH)
4. [Retour à la catégorie](SCR_FAQ_OFII_MENU)
5. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : FAQ_COACH_CIVIQUE.md -->

## SCR_FAQ_036

### Que se passe-t-il après la formation civique ?

<!-- Variables : {categorie}=OFII; {ordre}=8; {faq_id}=FAQ-036 -->

### Reponse markdown

À l'issue de la formation, vous poursuivez votre parcours administratif selon votre situation.

Si votre démarche nécessite la réussite de l'examen civique, vous devrez vous inscrire auprès d'un centre agréé afin de passer l'épreuve.

Le Coach pédagogique peut ensuite vous accompagner dans vos révisions jusqu'au jour de l'examen.

1. [Question précédente](SCR_FAQ_035)
2. [Nouvelle recherche](SCR_FAQ_SEARCH)
3. [Retour à la catégorie](SCR_FAQ_OFII_MENU)
4. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : FAQ_COACH_CIVIQUE.md -->

## SCR_FAQ_037

### Qu'est-ce que l'entretien de naturalisation ?

<!-- Variables : {categorie}=ENTRETIEN; {ordre}=1; {faq_id}=FAQ-037 -->

### Reponse markdown

L'entretien de naturalisation est un rendez-vous organisé par l'administration afin de vérifier que vous remplissez les conditions pour devenir français.

L'agent échange avec vous sur votre parcours, votre intégration, votre connaissance de la langue française ainsi que des valeurs et des principes de la République. Il dure généralement entre 15 et 30 minutes.

1. [Question suivante](SCR_FAQ_038)
2. [Nouvelle recherche](SCR_FAQ_SEARCH)
3. [Retour à la catégorie](SCR_FAQ_ENTRETIEN_MENU)
4. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : FAQ_COACH_CIVIQUE.md -->

## SCR_FAQ_038

### Quelles questions sont posées pendant l'entretien de naturalisation ?

<!-- Variables : {categorie}=ENTRETIEN; {ordre}=2; {faq_id}=FAQ-038 -->

### Reponse markdown

Les questions peuvent porter notamment sur :

- votre parcours personnel et professionnel en France ;
- vos motivations pour devenir français ;
- vos droits et devoirs ;
- les valeurs de la République (liberté, égalité, fraternité, laïcité...) ;
- les institutions françaises et leur fonctionnement ;
- votre vie quotidienne et votre intégration en France ;
- l'histoire, la culture et la société françaises.

Le contenu peut varier d'un entretien à l'autre.

1. [Question précédente](SCR_FAQ_037)
2. [Question suivante](SCR_FAQ_039)
3. [Nouvelle recherche](SCR_FAQ_SEARCH)
4. [Retour à la catégorie](SCR_FAQ_ENTRETIEN_MENU)
5. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : FAQ_COACH_CIVIQUE.md -->

## SCR_FAQ_039

### Comment répondre à la question : "Pourquoi souhaitez-vous devenir français ?"

<!-- Variables : {categorie}=ENTRETIEN; {ordre}=3; {faq_id}=FAQ-039 -->

### Reponse markdown

Il n'existe pas de réponse unique.

L'important est de répondre de manière personnelle, sincère et cohérente avec votre parcours.

Expliquez ce qui motive votre demande (intégration, projet de vie, attachement à la France, etc.) sans chercher à réciter une réponse apprise par cœur. Evitez les réponses trop génériques comme "mes enfants sont nés ici alors je souhaite devenir français".

1. [Question précédente](SCR_FAQ_038)
2. [Question suivante](SCR_FAQ_040)
3. [Nouvelle recherche](SCR_FAQ_SEARCH)
4. [Retour à la catégorie](SCR_FAQ_ENTRETIEN_MENU)
5. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : FAQ_COACH_CIVIQUE.md -->

## SCR_FAQ_040

### Combien de temps dure l'entretien de naturalisation ?

<!-- Variables : {categorie}=ENTRETIEN; {ordre}=4; {faq_id}=FAQ-040 -->

### Reponse markdown

La durée peut varier selon les situations.

En général, un entretien dure entre **15 et 30 minutes**, mais il peut être plus court ou plus long selon votre dossier et les questions complémentaires posées par l'agent. Si vous avez une parfaite maîtrise de la langue française alors l'entretien peut être court. Dans tous les cas ne vous inquiétez pas du temps passé en entretien, celui-ci n'est pas un indicateur de réussite !

1. [Question précédente](SCR_FAQ_039)
2. [Question suivante](SCR_FAQ_041)
3. [Nouvelle recherche](SCR_FAQ_SEARCH)
4. [Retour à la catégorie](SCR_FAQ_ENTRETIEN_MENU)
5. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : FAQ_COACH_CIVIQUE.md -->

## SCR_FAQ_041

### Quelle est la différence entre l'entretien de naturalisation et l'examen civique ?

<!-- Variables : {categorie}=ENTRETIEN; {ordre}=5; {faq_id}=FAQ-041 -->

### Reponse markdown

L'examen civique évalue vos connaissances à l'aide d'un QCM (40 questions).

L'entretien de naturalisation permet à un agent d'échanger directement avec vous afin d'apprécier votre intégration, votre niveau de français et votre connaissance des valeurs de la République.

Les deux sont complémentaires mais répondent à des objectifs différents.L'examen teste vos connaissances, alors que l'entretien teste votre assimilation à la culture française.

1. [Question précédente](SCR_FAQ_040)
2. [Question suivante](SCR_FAQ_042)
3. [Nouvelle recherche](SCR_FAQ_SEARCH)
4. [Retour à la catégorie](SCR_FAQ_ENTRETIEN_MENU)
5. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : FAQ_COACH_CIVIQUE.md -->

## SCR_FAQ_ENTRETIEN_MENU

### 👤 Entretien de naturalisation

<!-- Variables : {categorie}=ENTRETIEN -->

<!-- Liste dynamique : LISTE_ENTRETIEN. Les choix sont générés depuis 99_NAVIGATION. -->

1. [Qu'est-ce que l'entretien de naturalisation ?](SCR_FAQ_037)
2. [Quelles questions sont posées pendant l'entretien de naturalisation ?](SCR_FAQ_038)
3. [Comment répondre à la question : "Pourquoi souhaitez-vous devenir français ?"](SCR_FAQ_039)
4. [Combien de temps dure l'entretien de naturalisation ?](SCR_FAQ_040)
5. [Quelle est la différence entre l'entretien de naturalisation et l'examen civique ?](SCR_FAQ_041)
6. [L'examen civique est-il obligatoire pour obtenir la naturalisation ?](SCR_FAQ_042)
7. [Comment bien préparer son entretien de naturalisation ?](SCR_FAQ_043)
8. [Dois-je parler parfaitement français pour réussir l'entretien de naturalisation ?](SCR_FAQ_044)
9. [Puis-je demander à l'agent de répéter ou de reformuler une question ?](SCR_FAQ_045)
10. [Quels documents dois-je apporter le jour de l'entretien ?](SCR_FAQ_046)
11. [Comment dois-je m'habiller pour l'entretien de naturalisation ?](SCR_FAQ_047)
12. [Que faire si je ne comprends pas une question pendant l'entretien ?](SCR_FAQ_048)
13. [L'entretien de naturalisation est-il éliminatoire ?](SCR_FAQ_049)
14. [Puis-je préparer les réponses à l'avance ?](SCR_FAQ_050)
15. [Que faire si je suis stressé le jour de l'entretien ?](SCR_FAQ_051)
16. [Faut-il apprendre des réponses par cœur pour réussir l'entretien ?](SCR_FAQ_052)
17. [Rechercher dans la FAQ](SCR_FAQ_SEARCH)
18. [Retour aux catégories](SCR_FAQ_CATEGORIES)
19. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Préparer les questions, les documents, l’attitude et le stress. -->

## SCR_FAQ_042

### L'examen civique est-il obligatoire pour obtenir la naturalisation ?

<!-- Variables : {categorie}=ENTRETIEN; {ordre}=6; {faq_id}=FAQ-042 -->

### Reponse markdown

Oui, l'examen civique fait partie des étapes à prévoir pour une demande de naturalisation, sauf cas de dispense prévus par les textes applicables. Il ne remplace pas l'entretien d'assimilation : l'examen vérifie vos connaissances par QCM, tandis que l'entretien évalue votre parcours, votre intégration et votre expression orale.

1. [Question précédente](SCR_FAQ_041)
2. [Question suivante](SCR_FAQ_043)
3. [Nouvelle recherche](SCR_FAQ_SEARCH)
4. [Retour à la catégorie](SCR_FAQ_ENTRETIEN_MENU)
5. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : FAQ_COACH_CIVIQUE.md -->

## SCR_FAQ_043

### Comment bien préparer son entretien de naturalisation ?

<!-- Variables : {categorie}=ENTRETIEN; {ordre}=7; {faq_id}=FAQ-043 -->

### Reponse markdown

Pour préparer votre entretien, il est conseillé de :

- connaître les valeurs de la République ;
- maîtriser les principales institutions françaises ;
- revoir les grandes dates de l'histoire de France ;
- être capable de présenter votre parcours personnel ;
- s'entraîner à l'oral en français ; 
- Relisez le livret du Citoyen disponible sur le site du gouvernement.📝 **[Lire le livret](https://www.immigration.interieur.gouv.fr/documentation/guides-textes-et-brochures/livret-du-citoyen.html)**

- répondre naturellement aux questions, sans réciter un texte appris par cœur.

Le Coach pédagogique vous aide à travailler chacun de ces points progressivement.

1. [Question précédente](SCR_FAQ_042)
2. [Question suivante](SCR_FAQ_044)
3. [Nouvelle recherche](SCR_FAQ_SEARCH)
4. [Retour à la catégorie](SCR_FAQ_ENTRETIEN_MENU)
5. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : FAQ_COACH_CIVIQUE.md -->

## SCR_FAQ_044

### Dois-je parler parfaitement français pour réussir l'entretien de naturalisation ?

<!-- Variables : {categorie}=ENTRETIEN; {ordre}=8; {faq_id}=FAQ-044 -->

### Reponse markdown

Non.

L'objectif n'est pas de parler parfaitement français, mais de démontrer que vous possédez le niveau de langue exigé par la réglementation et que vous êtes capable de comprendre les questions et d'y répondre de manière claire.

N'hésitez pas à demander à l'agent de reformuler une question si vous ne l'avez pas comprise.

1. [Question précédente](SCR_FAQ_043)
2. [Question suivante](SCR_FAQ_045)
3. [Nouvelle recherche](SCR_FAQ_SEARCH)
4. [Retour à la catégorie](SCR_FAQ_ENTRETIEN_MENU)
5. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : FAQ_COACH_CIVIQUE.md -->

## SCR_FAQ_045

### Puis-je demander à l'agent de répéter ou de reformuler une question ?

<!-- Variables : {categorie}=ENTRETIEN; {ordre}=9; {faq_id}=FAQ-045 -->

### Reponse markdown

Oui.

Si vous ne comprenez pas une question, vous pouvez demander poliment à l'agent de la répéter ou de la reformuler.

Il est préférable de demander une explication plutôt que de répondre au hasard.

1. [Question précédente](SCR_FAQ_044)
2. [Question suivante](SCR_FAQ_046)
3. [Nouvelle recherche](SCR_FAQ_SEARCH)
4. [Retour à la catégorie](SCR_FAQ_ENTRETIEN_MENU)
5. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : FAQ_COACH_CIVIQUE.md -->

## SCR_FAQ_046

### Quels documents dois-je apporter le jour de l'entretien ?

<!-- Variables : {categorie}=ENTRETIEN; {ordre}=10; {faq_id}=FAQ-046 -->

### Reponse markdown

Vous devez apporter les documents demandés dans votre convocation.

Selon votre situation, il peut s'agir notamment :

- d'une pièce d'identité ;
- de votre titre de séjour ;
- de votre convocation ;
- et des autres justificatifs demandés par l'administration.

Vérifiez toujours votre convocation avant le rendez-vous.

1. [Question précédente](SCR_FAQ_045)
2. [Question suivante](SCR_FAQ_047)
3. [Nouvelle recherche](SCR_FAQ_SEARCH)
4. [Retour à la catégorie](SCR_FAQ_ENTRETIEN_MENU)
5. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : FAQ_COACH_CIVIQUE.md -->

## SCR_FAQ_047

### Comment dois-je m'habiller pour l'entretien de naturalisation ?

<!-- Variables : {categorie}=ENTRETIEN; {ordre}=11; {faq_id}=FAQ-047 -->

### Reponse markdown

Il n'existe pas de tenue obligatoire.

Une tenue propre, soignée et adaptée à un entretien administratif est recommandée.

L'essentiel est de vous présenter avec sérieux et de rester naturel.

1. [Question précédente](SCR_FAQ_046)
2. [Question suivante](SCR_FAQ_048)
3. [Nouvelle recherche](SCR_FAQ_SEARCH)
4. [Retour à la catégorie](SCR_FAQ_ENTRETIEN_MENU)
5. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : FAQ_COACH_CIVIQUE.md -->

## SCR_FAQ_048

### Que faire si je ne comprends pas une question pendant l'entretien ?

<!-- Variables : {categorie}=ENTRETIEN; {ordre}=12; {faq_id}=FAQ-048 -->

### Reponse markdown

Ne répondez pas au hasard.

Demandez calmement à l'agent de répéter ou de reformuler la question.

L'entretien est un échange. Il est préférable de demander une précision plutôt que de donner une réponse incorrecte.

1. [Question précédente](SCR_FAQ_047)
2. [Question suivante](SCR_FAQ_049)
3. [Nouvelle recherche](SCR_FAQ_SEARCH)
4. [Retour à la catégorie](SCR_FAQ_ENTRETIEN_MENU)
5. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : FAQ_COACH_CIVIQUE.md -->

## SCR_FAQ_049

### L'entretien de naturalisation est-il éliminatoire ?

<!-- Variables : {categorie}=ENTRETIEN; {ordre}=13; {faq_id}=FAQ-049 -->

### Reponse markdown

L'entretien constitue une étape importante de la procédure de naturalisation.

Il permet notamment d'évaluer votre niveau de français, votre connaissance des valeurs de la République et votre intégration dans la société française.

L'administration prend ensuite sa décision en tenant compte de l'ensemble de votre dossier, et non de l'entretien uniquement.

1. [Question précédente](SCR_FAQ_048)
2. [Question suivante](SCR_FAQ_050)
3. [Nouvelle recherche](SCR_FAQ_SEARCH)
4. [Retour à la catégorie](SCR_FAQ_ENTRETIEN_MENU)
5. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : FAQ_COACH_CIVIQUE.md -->

## SCR_FAQ_050

### Puis-je préparer les réponses à l'avance ?

<!-- Variables : {categorie}=ENTRETIEN; {ordre}=14; {faq_id}=FAQ-050 -->

### Reponse markdown

Oui, mais il est déconseillé d'apprendre des réponses par cœur.

L'agent recherche avant tout des réponses personnelles, cohérentes et sincères.

Le Coach pédagogique vous aide à comprendre les notions et à vous entraîner à répondre naturellement.

1. [Question précédente](SCR_FAQ_049)
2. [Question suivante](SCR_FAQ_051)
3. [Nouvelle recherche](SCR_FAQ_SEARCH)
4. [Retour à la catégorie](SCR_FAQ_ENTRETIEN_MENU)
5. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : FAQ_COACH_CIVIQUE.md -->

## SCR_FAQ_051

### Que faire si je suis stressé le jour de l'entretien ?

<!-- Variables : {categorie}=ENTRETIEN; {ordre}=15; {faq_id}=FAQ-051 -->

### Reponse markdown

Le stress est normal.

Prenez le temps d'écouter les questions, répondez calmement et n'hésitez pas à demander qu'une question soit répétée si nécessaire.

Une bonne préparation est le meilleur moyen de gagner en confiance.

1. [Question précédente](SCR_FAQ_050)
2. [Question suivante](SCR_FAQ_052)
3. [Nouvelle recherche](SCR_FAQ_SEARCH)
4. [Retour à la catégorie](SCR_FAQ_ENTRETIEN_MENU)
5. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : FAQ_COACH_CIVIQUE.md -->

## SCR_FAQ_052

### Faut-il apprendre des réponses par cœur pour réussir l'entretien ?

<!-- Variables : {categorie}=ENTRETIEN; {ordre}=16; {faq_id}=FAQ-052 -->

### Reponse markdown

Non.

L'entretien de naturalisation n'est pas un exercice de récitation.

L'agent cherche avant tout à vérifier que vous comprenez les valeurs de la République, que vous êtes intégré dans la société française et que vous êtes capable de répondre avec vos propres mots.

1. [Question précédente](SCR_FAQ_051)
2. [Nouvelle recherche](SCR_FAQ_SEARCH)
3. [Retour à la catégorie](SCR_FAQ_ENTRETIEN_MENU)
4. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : FAQ_COACH_CIVIQUE.md -->

## SCR_FAQ_NOVAFRATE_MENU

### 💻 NovaFrate

<!-- Variables : {categorie}=NOVAFRATE -->

<!-- Liste dynamique : LISTE_NOVAFRATE. Les choix sont générés depuis 99_NAVIGATION. -->

1. [Les questions proposées sur NovaFrate sont-elles officielles ?](SCR_FAQ_053)
2. [Que vais-je trouver sur NovaFrate ?](SCR_FAQ_054)
3. [Quand vais-je recevoir mes accès à NovaFrate ?](SCR_FAQ_055)
4. [Comment accéder à NovaFrate ?](SCR_FAQ_056)
5. [Combien de temps faut-il pour préparer l'examen civique ?](SCR_FAQ_057)
6. [Le contenu est-il régulièrement mis à jour ?](SCR_FAQ_058)
7. [Dois-je installer une application pour utiliser NovaFrate ?](SCR_FAQ_059)
8. [Le Coach pédagogique peut-il vraiment m'aider à réussir ?](SCR_FAQ_060)
9. [Comment contacter le support de FRATE Formation ?](SCR_FAQ_061)
10. [Je n'ai pas trouvé la réponse à ma question. Que puis-je faire ?](SCR_FAQ_062)
11. [Rechercher dans la FAQ](SCR_FAQ_SEARCH)
12. [Retour aux catégories](SCR_FAQ_CATEGORIES)
13. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Utiliser la plateforme, le Coach, les accès et le support. -->

## SCR_FAQ_053

### Les questions proposées sur NovaFrate sont-elles officielles ?

<!-- Variables : {categorie}=NOVAFRATE; {ordre}=1; {faq_id}=FAQ-053 -->

### Reponse markdown

Oui.

Les contenus proposés sur NovaFrate sont élaborés à partir des référentiels officiels de l'examen civique publiés par les autorités françaises.

Vous retrouverez :

- les connaissances attendues à l'examen ;
- des entraînements inspirés des questions officielles ;
- des examens blancs ;
- des explications pédagogiques pour mieux comprendre les notions.

L'objectif est de vous préparer efficacement aux différentes mentions de l'examen civique.

1. [Question suivante](SCR_FAQ_054)
2. [Nouvelle recherche](SCR_FAQ_SEARCH)
3. [Retour à la catégorie](SCR_FAQ_NOVAFRATE_MENU)
4. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : FAQ_COACH_CIVIQUE.md -->

## SCR_FAQ_054

### Que vais-je trouver sur NovaFrate ?

<!-- Variables : {categorie}=NOVAFRATE; {ordre}=2; {faq_id}=FAQ-054 -->

### Reponse markdown

NovaFrate est une plateforme de préparation à l'examen civique.

Vous y trouverez notamment :

- le Coach pédagogique intelligent ;
- des entraînements par thématique ;
- des examens blancs ;
- des explications détaillées après chaque réponse ;
- des ressources de révision ;
- des fiches de synthèse ;
- un suivi de votre progression.

La plateforme est conçue pour vous accompagner jusqu'au jour de votre examen.

1. [Question précédente](SCR_FAQ_053)
2. [Question suivante](SCR_FAQ_055)
3. [Nouvelle recherche](SCR_FAQ_SEARCH)
4. [Retour à la catégorie](SCR_FAQ_NOVAFRATE_MENU)
5. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : FAQ_COACH_CIVIQUE.md -->

## SCR_FAQ_055

### Quand vais-je recevoir mes accès à NovaFrate ?

<!-- Variables : {categorie}=NOVAFRATE; {ordre}=3; {faq_id}=FAQ-055 -->

### Reponse markdown

Après validation de votre inscription à l'examen auprès de FRATE Formation, vos identifiants NovaFrate sont généralement envoyés dans un délai de **24 heures ouvrées**.

Pensez également à vérifier votre dossier « Courriers indésirables » ou « Spam » si vous ne recevez pas votre e-mail.

1. [Question précédente](SCR_FAQ_054)
2. [Question suivante](SCR_FAQ_056)
3. [Nouvelle recherche](SCR_FAQ_SEARCH)
4. [Retour à la catégorie](SCR_FAQ_NOVAFRATE_MENU)
5. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : FAQ_COACH_CIVIQUE.md -->

## SCR_FAQ_056

### Comment accéder à NovaFrate ?

<!-- Variables : {categorie}=NOVAFRATE; {ordre}=4; {faq_id}=FAQ-056 -->

### Reponse markdown

Dès réception de vos identifiants, il vous suffit de vous connecter à la plateforme NovaFrate avec les informations qui vous ont été communiquées par e-mail.

En cas de difficulté de connexion, vous pouvez contacter le support de FRATE Formation.

1. [Question précédente](SCR_FAQ_055)
2. [Question suivante](SCR_FAQ_057)
3. [Nouvelle recherche](SCR_FAQ_SEARCH)
4. [Retour à la catégorie](SCR_FAQ_NOVAFRATE_MENU)
5. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : FAQ_COACH_CIVIQUE.md -->

## SCR_FAQ_057

### Combien de temps faut-il pour préparer l'examen civique ?

<!-- Variables : {categorie}=NOVAFRATE; {ordre}=5; {faq_id}=FAQ-057 -->

### Reponse markdown

La durée de préparation dépend de votre niveau de départ.

Une révision régulière, même de courte durée, est généralement plus efficace que de longues séances espacées.

Le Coach pédagogique adapte progressivement les questions afin de vous aider à progresser à votre rythme.

1. [Question précédente](SCR_FAQ_056)
2. [Question suivante](SCR_FAQ_058)
3. [Nouvelle recherche](SCR_FAQ_SEARCH)
4. [Retour à la catégorie](SCR_FAQ_NOVAFRATE_MENU)
5. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : FAQ_COACH_CIVIQUE.md -->

## SCR_FAQ_058

### Le contenu est-il régulièrement mis à jour ?

<!-- Variables : {categorie}=NOVAFRATE; {ordre}=6; {faq_id}=FAQ-058 -->

### Reponse markdown

Oui.

Les contenus pédagogiques sont mis à jour afin de rester conformes aux évolutions de la réglementation, des référentiels officiels et des modalités de l'examen civique.

1. [Question précédente](SCR_FAQ_057)
2. [Question suivante](SCR_FAQ_059)
3. [Nouvelle recherche](SCR_FAQ_SEARCH)
4. [Retour à la catégorie](SCR_FAQ_NOVAFRATE_MENU)
5. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : FAQ_COACH_CIVIQUE.md -->

## SCR_FAQ_059

### Dois-je installer une application pour utiliser NovaFrate ?

<!-- Variables : {categorie}=NOVAFRATE; {ordre}=7; {faq_id}=FAQ-059 -->

### Reponse markdown

Non.

NovaFrate est accessible directement en ligne depuis un ordinateur, une tablette ou un smartphone disposant d'une connexion Internet.

Aucune installation particulière n'est nécessaire.

1. [Question précédente](SCR_FAQ_058)
2. [Question suivante](SCR_FAQ_060)
3. [Nouvelle recherche](SCR_FAQ_SEARCH)
4. [Retour à la catégorie](SCR_FAQ_NOVAFRATE_MENU)
5. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : FAQ_COACH_CIVIQUE.md -->

## SCR_FAQ_060

### Le Coach pédagogique peut-il vraiment m'aider à réussir ?

<!-- Variables : {categorie}=NOVAFRATE; {ordre}=8; {faq_id}=FAQ-060 -->

### Reponse markdown

Le Coach pédagogique a été conçu pour vous accompagner tout au long de votre préparation.

Il vous aide à :

- comprendre les notions importantes ;
- identifier vos points faibles ;
- réviser les thèmes à renforcer ;
- vous entraîner dans des conditions proches de l'examen.

Son objectif est de rendre vos révisions plus simples, plus efficaces et plus personnalisées.

1. [Question précédente](SCR_FAQ_059)
2. [Question suivante](SCR_FAQ_061)
3. [Nouvelle recherche](SCR_FAQ_SEARCH)
4. [Retour à la catégorie](SCR_FAQ_NOVAFRATE_MENU)
5. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : FAQ_COACH_CIVIQUE.md -->

## SCR_FAQ_061

### Comment contacter le support de FRATE Formation ?

<!-- Variables : {categorie}=NOVAFRATE; {ordre}=9; {faq_id}=FAQ-061 -->

### Reponse markdown

Si vous avez une question concernant votre inscription, votre accès à NovaFrate ou le déroulement de votre préparation, vous pouvez utiliser le formulaire de contact disponible sur le site de FRATE Formation.

L'équipe vous répondra dans les meilleurs délais.

👉 Rendez-vous sur la page **Examen civique** puis dans la rubrique **« Un problème ? Des questions ? Contactez-nous ! »** pour accéder au formulaire de contact.

1. [Question précédente](SCR_FAQ_060)
2. [Question suivante](SCR_FAQ_062)
3. [Nouvelle recherche](SCR_FAQ_SEARCH)
4. [Retour à la catégorie](SCR_FAQ_NOVAFRATE_MENU)
5. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : FAQ_COACH_CIVIQUE.md -->

## SCR_FAQ_062

### Je n'ai pas trouvé la réponse à ma question. Que puis-je faire ?

<!-- Variables : {categorie}=NOVAFRATE; {ordre}=10; {faq_id}=FAQ-062 -->

### Reponse markdown

Si votre question ne figure pas dans cette FAQ :

- utilisez le Coach conversationnel de NovaFrate ;
- consultez les ressources pédagogiques disponibles sur la plateforme ;
- ou contactez directement l'équipe de FRATE Formation via le formulaire de contact.

Nous vous accompagnerons pour trouver la réponse la plus adaptée à votre situation.

1. [Question précédente](SCR_FAQ_061)
2. [Nouvelle recherche](SCR_FAQ_SEARCH)
3. [Retour à la catégorie](SCR_FAQ_NOVAFRATE_MENU)
4. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : FAQ_COACH_CIVIQUE.md -->

## SCR_FAQ_025

### Quel score faut-il obtenir pour réussir l'examen ?

<!-- Variables : {categorie}=RESULTATS; {ordre}=1; {faq_id}=FAQ-025 -->

### Reponse markdown

Le score minimum à obtenir est de 32 bonnes réponses sur 40 (soit 80 % de réussite). Il n'y pas de repassage possible, en cas de score non atteint, il faut repasser l'examen. 

Le Coach vous aide à identifier les thèmes à renforcer.

1. [Question suivante](SCR_FAQ_026)
2. [Nouvelle recherche](SCR_FAQ_SEARCH)
3. [Retour à la catégorie](SCR_FAQ_RESULTATS_MENU)
4. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : FAQ_COACH_CIVIQUE.md -->

## SCR_FAQ_026

### Que se passe-t-il si j'échoue à l'examen ?

<!-- Variables : {categorie}=RESULTATS; {ordre}=2; {faq_id}=FAQ-026 -->

### Reponse markdown

Pas de panique, cela n'annule pas votre demande de visa. Mais vous devez : (1) Vous réinscrire à une nouvelle session, (2) Repayer les frais d'inscription, (3) Attendre la prochaine date disponible. C'est pourquoi il est plus économique de bien se préparer dès la première fois.

1. [Question précédente](SCR_FAQ_025)
2. [Question suivante](SCR_FAQ_027)
3. [Nouvelle recherche](SCR_FAQ_SEARCH)
4. [Retour à la catégorie](SCR_FAQ_RESULTATS_MENU)
5. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : FAQ_COACH_CIVIQUE.md -->

## SCR_FAQ_027

### L'attestation de réussite a-t-elle une date de fin de validité ?

<!-- Variables : {categorie}=RESULTATS; {ordre}=3; {faq_id}=FAQ-027 -->

### Reponse markdown

Non. Une fois l'examen réussi, cela est définitif. Vous pourrez réutiliser votre attestation pour effectuer d'autres démarches administratives.

1. [Question précédente](SCR_FAQ_026)
2. [Question suivante](SCR_FAQ_028)
3. [Nouvelle recherche](SCR_FAQ_SEARCH)
4. [Retour à la catégorie](SCR_FAQ_RESULTATS_MENU)
5. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : FAQ_COACH_CIVIQUE.md -->

## SCR_FAQ_RESULTATS_MENU

### 📊 Résultats

<!-- Variables : {categorie}=RESULTATS -->

<!-- Liste dynamique : LISTE_RESULTATS. Les choix sont générés depuis 99_NAVIGATION. -->

1. [Quel score faut-il obtenir pour réussir l'examen ?](SCR_FAQ_025)
2. [Que se passe-t-il si j'échoue à l'examen ?](SCR_FAQ_026)
3. [L'attestation de réussite a-t-elle une date de fin de validité ?](SCR_FAQ_027)
4. [Quand reçoit-on les résultats ?](SCR_FAQ_028)
5. [Rechercher dans la FAQ](SCR_FAQ_SEARCH)
6. [Retour aux catégories](SCR_FAQ_CATEGORIES)
7. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Comprendre le score, l’échec, les délais et l’attestation. -->

## SCR_FAQ_028

### Quand reçoit-on les résultats ?

<!-- Variables : {categorie}=RESULTATS; {ordre}=4; {faq_id}=FAQ-028 -->

### Reponse markdown

Généralement, vous obtenez le résultat sous 48 h de la part de Frate Formation. L'attestation vous sera envoyé quelques jours après la passation de l'examen.

1. [Question précédente](SCR_FAQ_027)
2. [Nouvelle recherche](SCR_FAQ_SEARCH)
3. [Retour à la catégorie](SCR_FAQ_RESULTATS_MENU)
4. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : FAQ_COACH_CIVIQUE.md -->

## SCR_FAQ_001

### Qu'est-ce que l'examen civique ?

<!-- Variables : {categorie}=EXAMEN; {ordre}=1; {faq_id}=FAQ-001 -->

### Reponse markdown

L'examen civique est un test obligatoire pour obtenir certains titres de séjour (carte de séjour pluriannuelle ou carte de résident) mais aussi la nationalité française (naturalisation). Il 
permet d'évaluer vos connaissances sur les valeurs de la République, les institutions françaises, les droits et devoirs, l'histoire, la géographie, la culture française ainsi que la vie en société.

Le contenu varie selon que vous préparez :

- La carte de séjour ;
- La carte de résident ;
- Ou La Naturalisation.

1. [Question suivante](SCR_FAQ_002)
2. [Nouvelle recherche](SCR_FAQ_SEARCH)
3. [Retour à la catégorie](SCR_FAQ_EXAMEN_MENU)
4. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : FAQ_COACH_CIVIQUE.md -->

## SCR_FAQ_EXAMEN_MENU

### 📘 Examen civique

<!-- Variables : {categorie}=EXAMEN -->

<!-- Liste dynamique : LISTE_EXAMEN. Les choix sont générés depuis 99_NAVIGATION. -->

1. [Qu'est-ce que l'examen civique ?](SCR_FAQ_001)
2. [Qui est concerné par l'examen civique ?](SCR_FAQ_002)
3. [Quelles sont les thématiques officielles de l'examen civique ?](SCR_FAQ_003)
4. [Combien de questions comporte l'examen civique ?](SCR_FAQ_004)
5. [Quelles sont les diffénces entre les examens Carte de séjour, Carte de résident et Naturalisation ?](SCR_FAQ_005)
6. [A quoi correspond l'examen civique pour la naturalisation ?](SCR_FAQ_006)
7. [A quoi correspond l'examen civique pour la carte de résident ?](SCR_FAQ_007)
8. [A quoi correspond l'examen civique pour la carte de séjour pluriannuelle ?](SCR_FAQ_008)
9. [Quel score doit-on obtenir pour réussir l'examen civique ?](SCR_FAQ_009)
10. [Que se passe-t-il si on triche à l'examen ?](SCR_FAQ_010)
11. [L'examen est-il difficile ?](SCR_FAQ_011)
12. [Quel est le niveau de français requis pour passer l'examen ?](SCR_FAQ_012)
13. [Existe-t-il des questions pièges dans cet examen ?](SCR_FAQ_013)
14. [Qui peut être dispensé de passer l'examen civique ?](SCR_FAQ_014)
15. [Peut-on repasser l'examen si on échoue ?](SCR_FAQ_015)
16. [Rechercher dans la FAQ](SCR_FAQ_SEARCH)
17. [Retour aux catégories](SCR_FAQ_CATEGORIES)
18. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Comprendre le format, les thèmes, les niveaux et les règles de l’examen. -->

## SCR_FAQ_002

### Qui est concerné par l'examen civique ?

<!-- Variables : {categorie}=EXAMEN; {ordre}=2; {faq_id}=FAQ-002 -->

### Reponse markdown

L'examen civique concerne toutes les personnes réalisant une première demande de carte de résident, de carte de séjour pluriannuelle ou une demande de naturalisation. Il vise à vérifier vos connaissances concernant la France (fonctionnement des institutions, droits et devoirs du citoyen français, histoire et géographie de la France, culture française...)

1. [Question précédente](SCR_FAQ_001)
2. [Question suivante](SCR_FAQ_003)
3. [Nouvelle recherche](SCR_FAQ_SEARCH)
4. [Retour à la catégorie](SCR_FAQ_EXAMEN_MENU)
5. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : FAQ_COACH_CIVIQUE.md -->

## SCR_FAQ_003

### Quelles sont les thématiques officielles de l'examen civique ?

<!-- Variables : {categorie}=EXAMEN; {ordre}=3; {faq_id}=FAQ-003 -->

### Reponse markdown

Les questions portent sur cinq grandes thématiques :

- Les valeurs et principes de la République française ;
- Le système institutionnel et politique français ;
- Les droits et devoirs du citoyen ;
- L'histoire, la géographie et la culture françaises ;
- La vie dans la société française.

Ces thèmes correspondent au référentiel officiel publié par les autorités françaises.

1. [Question précédente](SCR_FAQ_002)
2. [Question suivante](SCR_FAQ_004)
3. [Nouvelle recherche](SCR_FAQ_SEARCH)
4. [Retour à la catégorie](SCR_FAQ_EXAMEN_MENU)
5. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : FAQ_COACH_CIVIQUE.md -->

## SCR_FAQ_004

### Combien de questions comporte l'examen civique ?

<!-- Variables : {categorie}=EXAMEN; {ordre}=4; {faq_id}=FAQ-004 -->

### Reponse markdown

L'examen comporte 40 questions QCM : 28 questions de connaissances et 12 mises en situation. Vous avez 45 minutes pour répondre. Vous devez obtenir 32 bonnes réponses sur 40 pour valider le test.

1. [Question précédente](SCR_FAQ_003)
2. [Question suivante](SCR_FAQ_005)
3. [Nouvelle recherche](SCR_FAQ_SEARCH)
4. [Retour à la catégorie](SCR_FAQ_EXAMEN_MENU)
5. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : FAQ_COACH_CIVIQUE.md -->

## SCR_FAQ_005

### Quelles sont les diffénces entre les examens Carte de séjour, Carte de résident et Naturalisation ?

<!-- Variables : {categorie}=EXAMEN; {ordre}=5; {faq_id}=FAQ-005 -->

### Reponse markdown

Les trois examens civiques ont des niveaux de difficulté différents : CSP (Carte de Séjour Pluriannuelle, 4 ans) est le plus accessible avec 191 questions officielles. CR (Carte de Résident, 10 ans) est plus exigeant avec 209 questions. NAT (Naturalisation) est le plus difficile avec 258 questions approfondies sur l'histoire et les institutions. Dans tous les cas, 40 questions sont tirées au sort le jour J et le nombre de bonnes réponses à donner reste le même (32/40).

1. [Question précédente](SCR_FAQ_004)
2. [Question suivante](SCR_FAQ_006)
3. [Nouvelle recherche](SCR_FAQ_SEARCH)
4. [Retour à la catégorie](SCR_FAQ_EXAMEN_MENU)
5. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : FAQ_COACH_CIVIQUE.md -->

## SCR_FAQ_006

### A quoi correspond l'examen civique pour la naturalisation ?

<!-- Variables : {categorie}=EXAMEN; {ordre}=6; {faq_id}=FAQ-006 -->

### Reponse markdown

L'examen civique pour la naturalisation est le test officiel demandé lorsque l'on souhaite demander la nationalité française. Il permet d'évaluer la connaissance des valeurs de la République, les droits et devoirs du citoyen français, de connaître l'histoire de la France et sa géograhie. La banque de questions pour la **naturalisation** compte 258 questions officielles, avec un format de 40 QCM en 45 minutes et un seuil de réussite établi à 80%.

1. [Question précédente](SCR_FAQ_005)
2. [Question suivante](SCR_FAQ_007)
3. [Nouvelle recherche](SCR_FAQ_SEARCH)
4. [Retour à la catégorie](SCR_FAQ_EXAMEN_MENU)
5. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : FAQ_COACH_CIVIQUE.md -->

## SCR_FAQ_007

### A quoi correspond l'examen civique pour la carte de résident ?

<!-- Variables : {categorie}=EXAMEN; {ordre}=7; {faq_id}=FAQ-007 -->

### Reponse markdown

L'examen civique pour la carte de résident est le test officiel demandé lorsque l'on effectue une première demande de carte de résident. Comme pour la naturalisation ,ce test permet d'évaluer la connaissance des valeurs de la République et des institutions, les droits et les devoirs du citoyen français, la culture française. La banque de questions pour la **carte résident** compte 209 questions officielles, avec un format de 40 QCM en 45 minutes et un seuil de réussite établi à 80%.

1. [Question précédente](SCR_FAQ_006)
2. [Question suivante](SCR_FAQ_008)
3. [Nouvelle recherche](SCR_FAQ_SEARCH)
4. [Retour à la catégorie](SCR_FAQ_EXAMEN_MENU)
5. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : FAQ_COACH_CIVIQUE.md -->

## SCR_FAQ_008

### A quoi correspond l'examen civique pour la carte de séjour pluriannuelle ?

<!-- Variables : {categorie}=EXAMEN; {ordre}=8; {faq_id}=FAQ-008 -->

### Reponse markdown

L'examen civique pour la carte de séjour pluriannuelle est le test officiel demandé lorsqu'on effectue une première demande de carte de séjour pluriannuelle. Comme pour la carte de résident et la demande de naturalisation, ce test va porter sur 5 grandes thématiques qui permettront d'évaluer les connaissances de la France et de son fonctionnement. La banque de questions CSP compte 191 questions officielles, avec un format de 40 QCM en 45 minutes et un seuil de réussite établi à 80%.

1. [Question précédente](SCR_FAQ_007)
2. [Question suivante](SCR_FAQ_009)
3. [Nouvelle recherche](SCR_FAQ_SEARCH)
4. [Retour à la catégorie](SCR_FAQ_EXAMEN_MENU)
5. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : FAQ_COACH_CIVIQUE.md -->

## SCR_FAQ_009

### Quel score doit-on obtenir pour réussir l'examen civique ?

<!-- Variables : {categorie}=EXAMEN; {ordre}=9; {faq_id}=FAQ-009 -->

### Reponse markdown

Pour réussir l'examen civique, vous devez obtenir 80 % de bonnes réponses soit 32 réponses sur 40. Si vous avez obtenu 31/40 alors c'est un échec.

1. [Question précédente](SCR_FAQ_008)
2. [Question suivante](SCR_FAQ_010)
3. [Nouvelle recherche](SCR_FAQ_SEARCH)
4. [Retour à la catégorie](SCR_FAQ_EXAMEN_MENU)
5. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : FAQ_COACH_CIVIQUE.md -->

## SCR_FAQ_010

### Que se passe-t-il si on triche à l'examen ?

<!-- Variables : {categorie}=EXAMEN; {ordre}=10; {faq_id}=FAQ-010 -->

### Reponse markdown

La fraude à l'examen civique a de lourdes conséquences : vous serez immédiatement exclu de la session en cours et votre tentative sera invalidée. De plus vous serez interdit de repasser l'examen pendant 2 ans. Cette interdiction peut également avoir un impact sur votre dossier administratif auprès de la préfecture.

1. [Question précédente](SCR_FAQ_009)
2. [Question suivante](SCR_FAQ_011)
3. [Nouvelle recherche](SCR_FAQ_SEARCH)
4. [Retour à la catégorie](SCR_FAQ_EXAMEN_MENU)
5. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : FAQ_COACH_CIVIQUE.md -->

## SCR_FAQ_011

### L'examen est-il difficile ?

<!-- Variables : {categorie}=EXAMEN; {ordre}=11; {faq_id}=FAQ-011 -->

### Reponse markdown

Cela dépend du type d'examen que vous passez. Le niveau pour la carte de séjour pluriannuelle est accessible, il demande du bon sens et une connaissance de base des cinq grandes thématiques (principes et valeurs de la République, Droits et devoirs...). Le niveau pour la carte de résident est plus difficile et nécessite d'apprendre des dates historiques et le fonctionnement des institutions. Enfin le niveau pour la naturalisation est le plux exigeant des trois. Les questions sont plus approfondies sur l'histoire, la culture ou encore les institutions françaises.

1. [Question précédente](SCR_FAQ_010)
2. [Question suivante](SCR_FAQ_012)
3. [Nouvelle recherche](SCR_FAQ_SEARCH)
4. [Retour à la catégorie](SCR_FAQ_EXAMEN_MENU)
5. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : FAQ_COACH_CIVIQUE.md -->

## SCR_FAQ_012

### Quel est le niveau de français requis pour passer l'examen ?

<!-- Variables : {categorie}=EXAMEN; {ordre}=12; {faq_id}=FAQ-012 -->

### Reponse markdown

L'examen se déroule uniquement en français, sans traduction disponible. Les questions sont formulées simplement (niveau A2/B1). Les questions sont des QCM aussi bien pour les 28 questions de connaissances générales que les 12 mises en situation.

1. [Question précédente](SCR_FAQ_011)
2. [Question suivante](SCR_FAQ_013)
3. [Nouvelle recherche](SCR_FAQ_SEARCH)
4. [Retour à la catégorie](SCR_FAQ_EXAMEN_MENU)
5. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : FAQ_COACH_CIVIQUE.md -->

## SCR_FAQ_013

### Existe-t-il des questions pièges dans cet examen ?

<!-- Variables : {categorie}=EXAMEN; {ordre}=13; {faq_id}=FAQ-013 -->

### Reponse markdown

Oui, notamment pour les "mises en situation" qui vous poussent à raisonner et à évaluer votre compréhension d'une situation en fonction des connaissances que vous avez acqusise. Exemple : Une entreprise refuse de recruter une personne en situation d'handicap. Quelle valeur républicaine n'est pas respectée ? 

Conseil : Lisez bien les mots comme "toujours", "jamais" ou "interdit" qui vous donneront des indices pour répondre.

1. [Question précédente](SCR_FAQ_012)
2. [Question suivante](SCR_FAQ_014)
3. [Nouvelle recherche](SCR_FAQ_SEARCH)
4. [Retour à la catégorie](SCR_FAQ_EXAMEN_MENU)
5. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : FAQ_COACH_CIVIQUE.md -->

## SCR_FAQ_014

### Qui peut être dispensé de passer l'examen civique ?

<!-- Variables : {categorie}=EXAMEN; {ordre}=14; {faq_id}=FAQ-014 -->

### Reponse markdown

Les dispenses dépendent du titre demandé — il n'existe pas de liste universelle. Pour la CSP : Passeport Talent (hors CIR), protection subsidiaire et apatrides (et familles), 65 ans ou plus, dispense médicale. Pour la carte de résident longue durée-UE, certains de ces statuts peuvent être concernés par l'examen. Pour la naturalisation, seule la dispense médicale est officiellement documentée ; la dispense à 65 ans n'y est pas explicitement confirmée. Vérifiez toujours la fiche Service-Public correspondant à votre démarche exacte. Les renouvellements de titre ne nécessitent pas l'examen.

1. [Question précédente](SCR_FAQ_013)
2. [Question suivante](SCR_FAQ_015)
3. [Nouvelle recherche](SCR_FAQ_SEARCH)
4. [Retour à la catégorie](SCR_FAQ_EXAMEN_MENU)
5. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : FAQ_COACH_CIVIQUE.md -->

## SCR_FAQ_015

### Peut-on repasser l'examen si on échoue ?

<!-- Variables : {categorie}=EXAMEN; {ordre}=15; {faq_id}=FAQ-015 -->

### Reponse markdown

Oui, il n'existe aucune limite de tentatives. Si vous échouez, vous pouvez retenter votre chance immédiatement (en repyant toute fois les frais d'examen). Rappel : en cas de fraude, vous serez interdit de le repasser pendant 2 ans.

1. [Question précédente](SCR_FAQ_014)
2. [Nouvelle recherche](SCR_FAQ_SEARCH)
3. [Retour à la catégorie](SCR_FAQ_EXAMEN_MENU)
4. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : FAQ_COACH_CIVIQUE.md -->

## SCR_FAQ_016

### Faut-il passer l'examen avant ou après avoir déposé sa demande ?

<!-- Variables : {categorie}=INSCRIPTION; {ordre}=1; {faq_id}=FAQ-016 -->

### Reponse markdown

Dans la plupart des démarches concernées, l'examen civique doit être réussi **avant** le dépôt de votre dossier. L'attestation de réussite est ensuite jointe à votre demande, selon les modalités prévues par l'administration.

👉 Pour vous inscrire facilement, vous pouvez :

- vous rendre dans la rubrique **« Je passe mon examen »** du Coach ;
- ou consulter la page d'inscription de puis choisir votre région et compléter le formulaire d'inscription.

1. [Question suivante](SCR_FAQ_017)
2. [Nouvelle recherche](SCR_FAQ_SEARCH)
3. [Retour à la catégorie](SCR_FAQ_INSCRIPTION_MENU)
4. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : FAQ_COACH_CIVIQUE.md -->

## SCR_FAQ_017

### Où puis-je passer l'examen civique ?

<!-- Variables : {categorie}=INSCRIPTION; {ordre}=2; {faq_id}=FAQ-017 -->

### Reponse markdown

L'examen se passe dans un **centre agréé** par l'Etat. Frate Formation est organisme agréé. 

Pour trouver une session près de chez vous :

- ouvrez la rubrique **« Je passe mon examen »** du Coach ;
- ou consultez et choisissez votre région.

Vous y trouverez les centres disponibles ainsi que les prochaines dates d'examen.

1. [Question précédente](SCR_FAQ_016)
2. [Question suivante](SCR_FAQ_018)
3. [Nouvelle recherche](SCR_FAQ_SEARCH)
4. [Retour à la catégorie](SCR_FAQ_INSCRIPTION_MENU)
5. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : FAQ_COACH_CIVIQUE.md -->

## SCR_FAQ_INSCRIPTION_MENU

### 📝 Inscription, prix et organisation

<!-- Variables : {categorie}=INSCRIPTION -->

<!-- Liste dynamique : LISTE_INSCRIPTION. Les choix sont générés depuis 99_NAVIGATION. -->

1. [Faut-il passer l'examen avant ou après avoir déposé sa demande ?](SCR_FAQ_016)
2. [Où puis-je passer l'examen civique ?](SCR_FAQ_017)
3. [Comment s'inscrire à l'examen civique ?](SCR_FAQ_018)
4. [Combien coûte l'examen civique ?](SCR_FAQ_019)
5. [Puis-je m'inscrire directement auprès de la préfecture ?](SCR_FAQ_020)
6. [Quels documents dois-je apporter le jour de l'examen ?](SCR_FAQ_021)
7. [Puis-je changer de centre après mon inscription ?](SCR_FAQ_022)
8. [Puis-je passer l'examen avec un récépissé expiré ?](SCR_FAQ_023)
9. [Comment choisir le centre d'examen le plus proche de chez moi ?](SCR_FAQ_024)
10. [Rechercher dans la FAQ](SCR_FAQ_SEARCH)
11. [Retour aux catégories](SCR_FAQ_CATEGORIES)
12. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Trouver un centre, s’inscrire, connaître le tarif et préparer le jour J. -->

## SCR_FAQ_018

### Comment s'inscrire à l'examen civique ?

<!-- Variables : {categorie}=INSCRIPTION; {ordre}=3; {faq_id}=FAQ-018 -->

### Reponse markdown

L'inscription est simple.

1. Choisissez la mention correspondant à votre démarche :
   - Carte de Séjour Pluriannuelle (CSP) ;
   - Carte de Résident (CR) ;
   - Naturalisation (NAT).

2. Sélectionnez le centre d'examen de votre choix.

3. Complétez le formulaire d'inscription.

👉 Vous pouvez effectuer cette démarche directement depuis :

- la rubrique **« Je passe mon examen »** du Coach ;
- ou le site officiel de.

1. [Question précédente](SCR_FAQ_017)
2. [Question suivante](SCR_FAQ_019)
3. [Nouvelle recherche](SCR_FAQ_SEARCH)
4. [Retour à la catégorie](SCR_FAQ_INSCRIPTION_MENU)
5. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : FAQ_COACH_CIVIQUE.md -->

## SCR_FAQ_019

### Combien coûte l'examen civique ?

<!-- Variables : {categorie}=INSCRIPTION; {ordre}=4; {faq_id}=FAQ-019 -->

### Reponse markdown

Les frais d'inscription sont fixés par chaque centre agréé et peuvent varier.

Le tarif applicable est de 75 € vous sera demandé au moment de votre inscription auprès du centre choisi.. Ce montant est à payer en ligne lors de la réservation. Il n'est pas remboursable si vous changez d'avis ou si vous ratez l'examen.

1. [Question précédente](SCR_FAQ_018)
2. [Question suivante](SCR_FAQ_020)
3. [Nouvelle recherche](SCR_FAQ_SEARCH)
4. [Retour à la catégorie](SCR_FAQ_INSCRIPTION_MENU)
5. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : FAQ_COACH_CIVIQUE.md -->

## SCR_FAQ_020

### Puis-je m'inscrire directement auprès de la préfecture ?

<!-- Variables : {categorie}=INSCRIPTION; {ordre}=5; {faq_id}=FAQ-020 -->

### Reponse markdown

Non.

L'inscription à l'examen ne s'effectue pas auprès de la préfecture.

Vous devez vous inscrire auprès d'un centre agréé.

Le moyen le plus simple est de :

- utiliser la rubrique **« Je passe mon examen »** du Coach ;
- ou consulter.

1. [Question précédente](SCR_FAQ_019)
2. [Question suivante](SCR_FAQ_021)
3. [Nouvelle recherche](SCR_FAQ_SEARCH)
4. [Retour à la catégorie](SCR_FAQ_INSCRIPTION_MENU)
5. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : FAQ_COACH_CIVIQUE.md -->

## SCR_FAQ_021

### Quels documents dois-je apporter le jour de l'examen ?

<!-- Variables : {categorie}=INSCRIPTION; {ordre}=6; {faq_id}=FAQ-021 -->

### Reponse markdown

Le jour de l'examen, pensez à apporter :

- votre convocation imprimée ;
- votre titre de séjour original ou votre passeport (attention : les photocopies sont refusées) ;
- tout autre document mentionné dans votre convocation.

Vérifiez toujours les consignes communiquées par votre centre avant votre déplacement.

1. [Question précédente](SCR_FAQ_020)
2. [Question suivante](SCR_FAQ_022)
3. [Nouvelle recherche](SCR_FAQ_SEARCH)
4. [Retour à la catégorie](SCR_FAQ_INSCRIPTION_MENU)
5. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : FAQ_COACH_CIVIQUE.md -->

## SCR_FAQ_022

### Puis-je changer de centre après mon inscription ?

<!-- Variables : {categorie}=INSCRIPTION; {ordre}=7; {faq_id}=FAQ-022 -->

### Reponse markdown

Les conditions de modification ou de report dépendent du centre d'examen.

Si vous souhaitez modifier votre inscription, contactez rapidement votre centre afin de connaître les possibilités qui s'offrent à vous.

1. [Question précédente](SCR_FAQ_021)
2. [Question suivante](SCR_FAQ_023)
3. [Nouvelle recherche](SCR_FAQ_SEARCH)
4. [Retour à la catégorie](SCR_FAQ_INSCRIPTION_MENU)
5. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : FAQ_COACH_CIVIQUE.md -->

## SCR_FAQ_023

### Puis-je passer l'examen avec un récépissé expiré ?

<!-- Variables : {categorie}=INSCRIPTION; {ordre}=8; {faq_id}=FAQ-023 -->

### Reponse markdown

Les documents acceptés pour vérifier votre identité sont définis par le centre d'examen.

En cas de doute sur la validité de vos documents, contactez votre centre avant le jour de l'épreuve afin d'éviter tout déplacement inutile.

1. [Question précédente](SCR_FAQ_022)
2. [Question suivante](SCR_FAQ_024)
3. [Nouvelle recherche](SCR_FAQ_SEARCH)
4. [Retour à la catégorie](SCR_FAQ_INSCRIPTION_MENU)
5. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : FAQ_COACH_CIVIQUE.md -->

## SCR_FAQ_024

### Comment choisir le centre d'examen le plus proche de chez moi ?

<!-- Variables : {categorie}=INSCRIPTION; {ordre}=9; {faq_id}=FAQ-024 -->

### Reponse markdown

Depuis la rubrique **« Je passe mon examen »**, le Coach vous oriente vers les centres disponibles.

Vous pouvez également consulter la page de, sélectionner votre région puis choisir le centre qui vous convient.

1. [Question précédente](SCR_FAQ_023)
2. [Nouvelle recherche](SCR_FAQ_SEARCH)
3. [Retour à la catégorie](SCR_FAQ_INSCRIPTION_MENU)
4. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source : FAQ_COACH_CIVIQUE.md -->

<!-- Fin du fichier source : modules\09_faq.md -->

<!-- Début du fichier source : modules\04_glossaire.md -->

<!-- Module généré automatiquement : Glossaire -->
<!-- Date : 2026-08-03T13:13:33+02:00 -->

## SCR_GLO_ALPHA_MENU

### 🔤 Parcourir par ordre alphabétique

<!-- Liste dynamique : LISTE_GROUPES_ALPHA. Les choix sont générés depuis 99_NAVIGATION. -->

<!-- Condition métier : Groupe actif | Valeur : A–C -->
1. [A–C](SCR_GLO_ALPHA_AC)
<!-- Condition métier : Groupe actif | Valeur : D–F -->
2. [D–F](SCR_GLO_ALPHA_DF)
<!-- Condition métier : Groupe actif | Valeur : G–L -->
3. [G–L](SCR_GLO_ALPHA_GL)
<!-- Condition métier : Groupe actif | Valeur : M–P -->
4. [M–P](SCR_GLO_ALPHA_MP)
<!-- Condition métier : Groupe actif | Valeur : Q–S -->
5. [Q–S](SCR_GLO_ALPHA_QS)
<!-- Condition métier : Groupe actif | Valeur : T–Z -->
6. [T–Z](SCR_GLO_ALPHA_TZ)
7. [Retour au glossaire](SCR_GLO_MENU)

## SCR_GLO_ALPHA_AC

### Mots de A–C

<!-- Règle métier : Afficher les notions actives du groupe, triées par ordre alphabétique -->

**Réponse attendue :** Choix d’une notion

<!-- Condition métier : Notion active | Valeur : GLO0001 -->
1. [Abstention](SCR_GLO_0001)
<!-- Condition métier : Notion active | Valeur : GLO0002 -->
2. [Alpes](SCR_GLO_0002)
<!-- Condition métier : Notion active | Valeur : GLO0003 -->
3. [APL](SCR_GLO_0003)
<!-- Condition métier : Notion active | Valeur : GLO0004 -->
4. [Assemblée nationale](SCR_GLO_0004)
<!-- Condition métier : Notion active | Valeur : GLO0005 -->
5. [Assistance à personne en danger](SCR_GLO_0005)
<!-- Condition métier : Notion active | Valeur : GLO0006 -->
6. [Assurance maladie](SCR_GLO_0006)
<!-- Condition métier : Notion active | Valeur : GLO0007 -->
7. [Bail](SCR_GLO_0007)
<!-- Condition métier : Notion active | Valeur : GLO0008 -->
8. [Bretagne](SCR_GLO_0008)
<!-- Condition métier : Notion active | Valeur : GLO0009 -->
9. [CAF](SCR_GLO_0009)
<!-- Condition métier : Notion active | Valeur : GLO0010 -->
10. [Carte de résident](SCR_GLO_0010)
<!-- Condition métier : Notion active | Valeur : GLO0011 -->
11. [Carte Vitale](SCR_GLO_0011)
<!-- Condition métier : Notion active | Valeur : GLO0012 -->
12. [CDD](SCR_GLO_0012)
<!-- Condition métier : Notion active | Valeur : GLO0013 -->
13. [CDI](SCR_GLO_0013)
<!-- Condition métier : Notion active | Valeur : GLO0014 -->
14. [Celtes](SCR_GLO_0014)
<!-- Condition métier : Notion active | Valeur : GLO0015 -->
15. [Charlemagne](SCR_GLO_0015)
<!-- Condition métier : Notion active | Valeur : GLO0016 -->
16. [Charte de l'environnement](SCR_GLO_0016)
<!-- Condition métier : Notion active | Valeur : GLO0017 -->
17. [Château de Versailles](SCR_GLO_0017)
<!-- Condition métier : Notion active | Valeur : GLO0018 -->
18. [Cinquième République](SCR_GLO_0018)
<!-- Condition métier : Notion active | Valeur : GLO0019 -->
19. [Citoyen](SCR_GLO_0019)
<!-- Condition métier : Notion active | Valeur : GLO0020 -->
20. [Citoyenneté](SCR_GLO_0020)
<!-- Condition métier : Notion active | Valeur : GLO0021 -->
21. [Clovis](SCR_GLO_0021)
<!-- Condition métier : Notion active | Valeur : GLO0022 -->
22. [Collège](SCR_GLO_0022)
<!-- Condition métier : Notion active | Valeur : GLO0023 -->
23. [Commission européenne](SCR_GLO_0023)
<!-- Condition métier : Notion active | Valeur : GLO0024 -->
24. [Commune](SCR_GLO_0024)
<!-- Condition métier : Notion active | Valeur : GLO0025 -->
25. [Conseil constitutionnel](SCR_GLO_0025)
<!-- Condition métier : Notion active | Valeur : GLO0026 -->
26. [Conseil de l'Union européenne](SCR_GLO_0026)
<!-- Condition métier : Notion active | Valeur : GLO0027 -->
27. [Conseil départemental](SCR_GLO_0027)
<!-- Condition métier : Notion active | Valeur : GLO0028 -->
28. [Conseil européen](SCR_GLO_0028)
<!-- Condition métier : Notion active | Valeur : GLO0029 -->
29. [Conseil municipal](SCR_GLO_0029)
<!-- Condition métier : Notion active | Valeur : GLO0030 -->
30. [Conseil régional](SCR_GLO_0030)
<!-- Condition métier : Notion active | Valeur : GLO0031 -->
31. [Consentement](SCR_GLO_0031)
<!-- Condition métier : Notion active | Valeur : GLO0032 -->
32. [Constitution](SCR_GLO_0032)
<!-- Condition métier : Notion active | Valeur : GLO0033 -->
33. [Contrat d'engagement à respecter les principes de la République](SCR_GLO_0033)
<!-- Condition métier : Notion active | Valeur : GLO0034 -->
34. [Contrat de travail](SCR_GLO_0034)
<!-- Condition métier : Notion active | Valeur : GLO0035 -->
35. [Contravention](SCR_GLO_0035)
<!-- Condition métier : Notion active | Valeur : GLO0036 -->
36. [CPAM](SCR_GLO_0036)
<!-- Condition métier : Notion active | Valeur : GLO0037 -->
37. [Crime](SCR_GLO_0037)

<!-- Prévoir pagination si nécessaire -->

## SCR_GLO_ALPHA_DF

### Mots de D–F

<!-- Règle métier : Afficher les notions actives du groupe, triées par ordre alphabétique -->

**Réponse attendue :** Choix d’une notion

<!-- Condition métier : Notion active | Valeur : GLO0038 -->
1. [Déclaration des droits de l'homme et du citoyen](SCR_GLO_0038)
<!-- Condition métier : Notion active | Valeur : GLO0039 -->
2. [Délit](SCR_GLO_0039)
<!-- Condition métier : Notion active | Valeur : GLO0040 -->
3. [Démocratie](SCR_GLO_0040)
<!-- Condition métier : Notion active | Valeur : GLO0041 -->
4. [Département](SCR_GLO_0041)
<!-- Condition métier : Notion active | Valeur : GLO0042 -->
5. [Député](SCR_GLO_0042)
<!-- Condition métier : Notion active | Valeur : GLO0043 -->
6. [Député européen](SCR_GLO_0043)
<!-- Condition métier : Notion active | Valeur : GLO0044 -->
7. [Devise de la République](SCR_GLO_0044)
<!-- Condition métier : Notion active | Valeur : GLO0045 -->
8. [Dignité humaine](SCR_GLO_0045)
<!-- Condition métier : Notion active | Valeur : GLO0046 -->
9. [Drapeau français](SCR_GLO_0046)
<!-- Condition métier : Notion active | Valeur : GLO0047 -->
10. [Droits fondamentaux](SCR_GLO_0047)
<!-- Condition métier : Notion active | Valeur : GLO0048 -->
11. [École](SCR_GLO_0048)
<!-- Condition métier : Notion active | Valeur : GLO0049 -->
12. [Égalité](SCR_GLO_0049)
<!-- Condition métier : Notion active | Valeur : GLO0050 -->
13. [Élection](SCR_GLO_0050)
<!-- Condition métier : Notion active | Valeur : GLO0051 -->
14. [Employeur](SCR_GLO_0051)
<!-- Condition métier : Notion active | Valeur : GLO0052 -->
15. [Environnement](SCR_GLO_0052)
<!-- Condition métier : Notion active | Valeur : GLO0053 -->
16. [Espace Schengen](SCR_GLO_0053)
<!-- Condition métier : Notion active | Valeur : GLO0054 -->
17. [État](SCR_GLO_0054)
<!-- Condition métier : Notion active | Valeur : GLO0055 -->
18. [Euro](SCR_GLO_0055)
<!-- Condition métier : Notion active | Valeur : GLO0056 -->
19. [Fête de la Musique](SCR_GLO_0056)
<!-- Condition métier : Notion active | Valeur : GLO0057 -->
20. [Fête nationale](SCR_GLO_0057)
<!-- Condition métier : Notion active | Valeur : GLO0058 -->
21. [France métropolitaine](SCR_GLO_0058)
<!-- Condition métier : Notion active | Valeur : GLO0059 -->
22. [France Services](SCR_GLO_0059)
<!-- Condition métier : Notion active | Valeur : GLO0060 -->
23. [France Travail](SCR_GLO_0060)
<!-- Condition métier : Notion active | Valeur : GLO0061 -->
24. [Francophonie](SCR_GLO_0061)
<!-- Condition métier : Notion active | Valeur : GLO0062 -->
25. [Fraternité](SCR_GLO_0062)

<!-- Prévoir pagination si nécessaire -->

## SCR_GLO_ALPHA_GL

### Mots de G–L

<!-- Règle métier : Afficher les notions actives du groupe, triées par ordre alphabétique -->

**Réponse attendue :** Choix d’une notion

<!-- Condition métier : Notion active | Valeur : GLO0063 -->
1. [Gastronomie française](SCR_GLO_0063)
<!-- Condition métier : Notion active | Valeur : GLO0064 -->
2. [Gaule](SCR_GLO_0064)
<!-- Condition métier : Notion active | Valeur : GLO0065 -->
3. [Gendarmerie](SCR_GLO_0065)
<!-- Condition métier : Notion active | Valeur : GLO0066 -->
4. [Gouvernement](SCR_GLO_0066)
<!-- Condition métier : Notion active | Valeur : GLO0067 -->
5. [Guadeloupe](SCR_GLO_0067)
<!-- Condition métier : Notion active | Valeur : GLO0068 -->
6. [Guyane](SCR_GLO_0068)
<!-- Condition métier : Notion active | Valeur : GLO0069 -->
7. [Harcèlement](SCR_GLO_0069)
<!-- Condition métier : Notion active | Valeur : GLO0070 -->
8. [Harcèlement scolaire](SCR_GLO_0070)
<!-- Condition métier : Notion active | Valeur : GLO0071 -->
9. [Hôpital](SCR_GLO_0071)
<!-- Condition métier : Notion active | Valeur : GLO0072 -->
10. [Île-de-France](SCR_GLO_0072)
<!-- Condition métier : Notion active | Valeur : GLO0073 -->
11. [Impôt](SCR_GLO_0073)
<!-- Condition métier : Notion active | Valeur : GLO0074 -->
12. [Infraction](SCR_GLO_0074)
<!-- Condition métier : Notion active | Valeur : GLO0075 -->
13. [Intégrité de la personne](SCR_GLO_0075)
<!-- Condition métier : Notion active | Valeur : GLO0076 -->
14. [Journées européennes du patrimoine](SCR_GLO_0076)
<!-- Condition métier : Notion active | Valeur : GLO0077 -->
15. [Justice](SCR_GLO_0077)
<!-- Condition métier : Notion active | Valeur : GLO0078 -->
16. [La Marseillaise](SCR_GLO_0078)
<!-- Condition métier : Notion active | Valeur : GLO0079 -->
17. [La Réunion](SCR_GLO_0079)
<!-- Condition métier : Notion active | Valeur : GLO0080 -->
18. [Laïcité](SCR_GLO_0080)
<!-- Condition métier : Notion active | Valeur : GLO0081 -->
19. [Langue de la République](SCR_GLO_0081)
<!-- Condition métier : Notion active | Valeur : GLO0082 -->
20. [Liberté](SCR_GLO_0082)
<!-- Condition métier : Notion active | Valeur : GLO0083 -->
21. [Liberté de conscience](SCR_GLO_0083)
<!-- Condition métier : Notion active | Valeur : GLO0084 -->
22. [Locataire](SCR_GLO_0084)
<!-- Condition métier : Notion active | Valeur : GLO0085 -->
23. [Loi](SCR_GLO_0085)
<!-- Condition métier : Notion active | Valeur : GLO0086 -->
24. [Lycée](SCR_GLO_0086)

<!-- Prévoir pagination si nécessaire -->

## SCR_GLO_ALPHA_MP

### Mots de M–P

<!-- Règle métier : Afficher les notions actives du groupe, triées par ordre alphabétique -->

**Réponse attendue :** Choix d’une notion

<!-- Condition métier : Notion active | Valeur : GLO0087 -->
1. [Maire](SCR_GLO_0087)
<!-- Condition métier : Notion active | Valeur : GLO0088 -->
2. [Mairie](SCR_GLO_0088)
<!-- Condition métier : Notion active | Valeur : GLO0089 -->
3. [Marianne](SCR_GLO_0089)
<!-- Condition métier : Notion active | Valeur : GLO0090 -->
4. [Martinique](SCR_GLO_0090)
<!-- Condition métier : Notion active | Valeur : GLO0091 -->
5. [Mayotte](SCR_GLO_0091)
<!-- Condition métier : Notion active | Valeur : GLO0092 -->
6. [Médecin traitant](SCR_GLO_0092)
<!-- Condition métier : Notion active | Valeur : GLO0093 -->
7. [Ministre](SCR_GLO_0093)
<!-- Condition métier : Notion active | Valeur : GLO0094 -->
8. [Mont-Saint-Michel](SCR_GLO_0094)
<!-- Condition métier : Notion active | Valeur : GLO0095 -->
9. [Musée du Louvre](SCR_GLO_0095)
<!-- Condition métier : Notion active | Valeur : GLO0096 -->
10. [Mutilations sexuelles féminines](SCR_GLO_0096)
<!-- Condition métier : Notion active | Valeur : GLO0097 -->
11. [Naturalisation](SCR_GLO_0097)
<!-- Condition métier : Notion active | Valeur : GLO0098 -->
12. [Neutralité](SCR_GLO_0098)
<!-- Condition métier : Notion active | Valeur : GLO0099 -->
13. [Ordre public](SCR_GLO_0099)
<!-- Condition métier : Notion active | Valeur : GLO0100 -->
14. [Outre-mer](SCR_GLO_0100)
<!-- Condition métier : Notion active | Valeur : GLO0101 -->
15. [Parlement](SCR_GLO_0101)
<!-- Condition métier : Notion active | Valeur : GLO0102 -->
16. [Parlement européen](SCR_GLO_0102)
<!-- Condition métier : Notion active | Valeur : GLO0103 -->
17. [Patrimoine](SCR_GLO_0103)
<!-- Condition métier : Notion active | Valeur : GLO0104 -->
18. [Police](SCR_GLO_0104)
<!-- Condition métier : Notion active | Valeur : GLO0105 -->
19. [Préfecture](SCR_GLO_0105)
<!-- Condition métier : Notion active | Valeur : GLO0106 -->
20. [Préfet](SCR_GLO_0106)
<!-- Condition métier : Notion active | Valeur : GLO0107 -->
21. [Premier ministre](SCR_GLO_0107)
<!-- Condition métier : Notion active | Valeur : GLO0108 -->
22. [Première Guerre mondiale](SCR_GLO_0108)
<!-- Condition métier : Notion active | Valeur : GLO0109 -->
23. [Président de la République](SCR_GLO_0109)
<!-- Condition métier : Notion active | Valeur : GLO0110 -->
24. [Présomption d'innocence](SCR_GLO_0110)
<!-- Condition métier : Notion active | Valeur : GLO0111 -->
25. [Procuration](SCR_GLO_0111)
<!-- Condition métier : Notion active | Valeur : GLO0112 -->
26. [Propriétaire](SCR_GLO_0112)
<!-- Condition métier : Notion active | Valeur : GLO0113 -->
27. [Prostitution](SCR_GLO_0113)
<!-- Condition métier : Notion active | Valeur : GLO0114 -->
28. [Provence-Alpes-Côte d'Azur](SCR_GLO_0114)
<!-- Condition métier : Notion active | Valeur : GLO0115 -->
29. [Pyrénées](SCR_GLO_0115)

<!-- Prévoir pagination si nécessaire -->

## SCR_GLO_ALPHA_QS

### Mots de Q–S

<!-- Règle métier : Afficher les notions actives du groupe, triées par ordre alphabétique -->

**Réponse attendue :** Choix d’une notion

<!-- Condition métier : Notion active | Valeur : GLO0116 -->
1. [Référendum](SCR_GLO_0116)
<!-- Condition métier : Notion active | Valeur : GLO0117 -->
2. [Région](SCR_GLO_0117)
<!-- Condition métier : Notion active | Valeur : GLO0118 -->
3. [République](SCR_GLO_0118)
<!-- Condition métier : Notion active | Valeur : GLO0119 -->
4. [Révolution française](SCR_GLO_0119)
<!-- Condition métier : Notion active | Valeur : GLO0120 -->
5. [Salaire](SCR_GLO_0120)
<!-- Condition métier : Notion active | Valeur : GLO0121 -->
6. [Seconde Guerre mondiale](SCR_GLO_0121)
<!-- Condition métier : Notion active | Valeur : GLO0122 -->
7. [Seine](SCR_GLO_0122)
<!-- Condition métier : Notion active | Valeur : GLO0123 -->
8. [Sénat](SCR_GLO_0123)
<!-- Condition métier : Notion active | Valeur : GLO0124 -->
9. [Sénateur](SCR_GLO_0124)
<!-- Condition métier : Notion active | Valeur : GLO0125 -->
10. [Service public](SCR_GLO_0125)
<!-- Condition métier : Notion active | Valeur : GLO0126 -->
11. [Souveraineté nationale](SCR_GLO_0126)
<!-- Condition métier : Notion active | Valeur : GLO0127 -->
12. [Suffrage universel](SCR_GLO_0127)
<!-- Condition métier : Notion active | Valeur : GLO0128 -->
13. [Sûreté](SCR_GLO_0128)

<!-- Prévoir pagination si nécessaire -->

## SCR_GLO_ALPHA_TZ

### Mots de T–Z

<!-- Règle métier : Afficher les notions actives du groupe, triées par ordre alphabétique -->

**Réponse attendue :** Choix d’une notion

<!-- Condition métier : Notion active | Valeur : GLO0129 -->
1. [Titre de séjour](SCR_GLO_0129)
<!-- Condition métier : Notion active | Valeur : GLO0130 -->
2. [Tour Eiffel](SCR_GLO_0130)
<!-- Condition métier : Notion active | Valeur : GLO0131 -->
3. [Traite des êtres humains](SCR_GLO_0131)
<!-- Condition métier : Notion active | Valeur : GLO0132 -->
4. [UNESCO](SCR_GLO_0132)
<!-- Condition métier : Notion active | Valeur : GLO0133 -->
5. [Union européenne](SCR_GLO_0133)
<!-- Condition métier : Notion active | Valeur : GLO0134 -->
6. [Urgences](SCR_GLO_0134)
<!-- Condition métier : Notion active | Valeur : GLO0135 -->
7. [Vercingétorix](SCR_GLO_0135)
<!-- Condition métier : Notion active | Valeur : GLO0136 -->
8. [Violence](SCR_GLO_0136)
<!-- Condition métier : Notion active | Valeur : GLO0137 -->
9. [Vote](SCR_GLO_0137)

<!-- Prévoir pagination si nécessaire -->

## SCR_GLO_0001

### Abstention

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T2)
<!-- Condition métier : Notion liée disponible | Valeur : vote -->
3. [Vote](SCR_GLO_0137)
4. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0002

### Alpes

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T4)
<!-- Condition métier : Notion liée disponible | Valeur : pyrenees -->
3. [Pyrénées](SCR_GLO_0115)
4. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0003

### APL

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T5)
<!-- Condition métier : Notion liée disponible | Valeur : caf -->
3. [CAF](SCR_GLO_0009)
4. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0004

### Assemblée nationale

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T2)
<!-- Condition métier : Notion liée disponible | Valeur : depute -->
3. [Député](SCR_GLO_0042)
<!-- Condition métier : Notion liée disponible | Valeur : parlement -->
4. [Parlement](SCR_GLO_0101)
5. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0005

### Assistance à personne en danger

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T3)
3. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0006

### Assurance maladie

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T5)
<!-- Condition métier : Notion liée disponible | Valeur : carte vitale -->
3. [Carte Vitale](SCR_GLO_0011)
<!-- Condition métier : Notion liée disponible | Valeur : cpam -->
4. [CPAM](SCR_GLO_0036)
<!-- Condition métier : Notion liée disponible | Valeur : medecin traitant -->
5. [Médecin traitant](SCR_GLO_0092)
6. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0007

### Bail

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T5)
3. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0008

### Bretagne

### A retenir

La Bretagne est connue pour son littoral, sa culture bretonne, ses ports de pêche, ses phares et ses spécialités culinaires comme les crêpes et le kouign-amann.

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T4)
<!-- Condition métier : Notion liée disponible | Valeur : region -->
3. [Région](SCR_GLO_0117)
4. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0009

### CAF

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T5)
<!-- Condition métier : Notion liée disponible | Valeur : apl -->
3. [APL](SCR_GLO_0003)
4. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0010

### Carte de résident

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T5)
<!-- Condition métier : Notion liée disponible | Valeur : titre de sejour -->
3. [Titre de séjour](SCR_GLO_0129)
4. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0011

### Carte Vitale

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T5)
<!-- Condition métier : Notion liée disponible | Valeur : assurance maladie -->
3. [Assurance maladie](SCR_GLO_0006)
<!-- Condition métier : Notion liée disponible | Valeur : cpam -->
4. [CPAM](SCR_GLO_0036)
5. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0012

### CDD

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T5)
<!-- Condition métier : Notion liée disponible | Valeur : contrat de travail -->
3. [Contrat de travail](SCR_GLO_0034)
<!-- Condition métier : Notion liée disponible | Valeur : cdi -->
4. [CDI](SCR_GLO_0013)
5. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0013

### CDI

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T5)
<!-- Condition métier : Notion liée disponible | Valeur : contrat de travail -->
3. [Contrat de travail](SCR_GLO_0034)
<!-- Condition métier : Notion liée disponible | Valeur : cdd -->
4. [CDD](SCR_GLO_0012)
5. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0014

### Celtes

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T4)
<!-- Condition métier : Notion liée disponible | Valeur : gaule -->
3. [Gaule](SCR_GLO_0064)
4. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0015

### Charlemagne

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T4)
3. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0016

### Charte de l'environnement

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T3)
<!-- Condition métier : Notion liée disponible | Valeur : environnement -->
3. [Environnement](SCR_GLO_0052)
4. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0017

### Château de Versailles

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T4)
3. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0018

### Cinquième République

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T4)
<!-- Condition métier : Notion liée disponible | Valeur : constitution -->
3. [Constitution](SCR_GLO_0032)
4. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0019

### Citoyen

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T1)
3. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0020

### Citoyenneté

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T3)
3. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0021

### Clovis

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T4)
<!-- Condition métier : Notion liée disponible | Valeur : charlemagne -->
3. [Charlemagne](SCR_GLO_0015)
4. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0022

### Collège

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T5)
<!-- Condition métier : Notion liée disponible | Valeur : lycee -->
3. [Lycée](SCR_GLO_0086)
4. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0023

### Commission européenne

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T2)
<!-- Condition métier : Notion liée disponible | Valeur : union europeenne -->
3. [Union européenne](SCR_GLO_0133)
4. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0024

### Commune

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T2)
<!-- Condition métier : Notion liée disponible | Valeur : maire -->
3. [Maire](SCR_GLO_0087)
4. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0025

### Conseil constitutionnel

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T2)
<!-- Condition métier : Notion liée disponible | Valeur : constitution -->
3. [Constitution](SCR_GLO_0032)
4. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0026

### Conseil de l'Union européenne

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T2)
<!-- Condition métier : Notion liée disponible | Valeur : commission europeenne -->
3. [Commission européenne](SCR_GLO_0023)
4. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0027

### Conseil départemental

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T2)
<!-- Condition métier : Notion liée disponible | Valeur : departement -->
3. [Département](SCR_GLO_0041)
4. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0028

### Conseil européen

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T2)
<!-- Condition métier : Notion liée disponible | Valeur : union europeenne -->
3. [Union européenne](SCR_GLO_0133)
4. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0029

### Conseil municipal

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T2)
<!-- Condition métier : Notion liée disponible | Valeur : maire -->
3. [Maire](SCR_GLO_0087)
4. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0030

### Conseil régional

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T2)
<!-- Condition métier : Notion liée disponible | Valeur : region -->
3. [Région](SCR_GLO_0117)
4. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0031

### Consentement

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T3)
3. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0032

### Constitution

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T1)
<!-- Condition métier : Notion liée disponible | Valeur : republique -->
3. [République](SCR_GLO_0118)
<!-- Condition métier : Notion liée disponible | Valeur : loi -->
4. [Loi](SCR_GLO_0085)
5. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0033

### Contrat d'engagement à respecter les principes de la République

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T1)
<!-- Condition métier : Notion liée disponible | Valeur : republique -->
3. [République](SCR_GLO_0118)
<!-- Condition métier : Notion liée disponible | Valeur : laicite -->
4. [Laïcité](SCR_GLO_0080)
5. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0034

### Contrat de travail

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T5)
<!-- Condition métier : Notion liée disponible | Valeur : cdi -->
3. [CDI](SCR_GLO_0013)
<!-- Condition métier : Notion liée disponible | Valeur : cdd -->
4. [CDD](SCR_GLO_0012)
5. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0035

### Contravention

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T3)
<!-- Condition métier : Notion liée disponible | Valeur : delit -->
3. [Délit](SCR_GLO_0039)
<!-- Condition métier : Notion liée disponible | Valeur : crime -->
4. [Crime](SCR_GLO_0037)
5. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0036

### CPAM

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T5)
<!-- Condition métier : Notion liée disponible | Valeur : carte vitale -->
3. [Carte Vitale](SCR_GLO_0011)
<!-- Condition métier : Notion liée disponible | Valeur : assurance maladie -->
4. [Assurance maladie](SCR_GLO_0006)
5. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0037

### Crime

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T3)
<!-- Condition métier : Notion liée disponible | Valeur : delit -->
3. [Délit](SCR_GLO_0039)
4. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0038

### Déclaration des droits de l'homme et du citoyen

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T3)
<!-- Condition métier : Notion liée disponible | Valeur : constitution -->
3. [Constitution](SCR_GLO_0032)
4. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0039

### Délit

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T3)
<!-- Condition métier : Notion liée disponible | Valeur : crime -->
3. [Crime](SCR_GLO_0037)
4. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0040

### Démocratie

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T1)
<!-- Condition métier : Notion liée disponible | Valeur : republique -->
3. [République](SCR_GLO_0118)
<!-- Condition métier : Notion liée disponible | Valeur : election -->
4. [Élection](SCR_GLO_0050)
5. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0041

### Département

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T2)
<!-- Condition métier : Notion liée disponible | Valeur : region -->
3. [Région](SCR_GLO_0117)
<!-- Condition métier : Notion liée disponible | Valeur : commune -->
4. [Commune](SCR_GLO_0024)
5. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0042

### Député

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T2)
<!-- Condition métier : Notion liée disponible | Valeur : assemblee nationale -->
3. [Assemblée nationale](SCR_GLO_0004)
4. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0043

### Député européen

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T2)
<!-- Condition métier : Notion liée disponible | Valeur : parlement europeen -->
3. [Parlement européen](SCR_GLO_0102)
4. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0044

### Devise de la République

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T1)
<!-- Condition métier : Notion liée disponible | Valeur : liberte -->
3. [Liberté](SCR_GLO_0082)
<!-- Condition métier : Notion liée disponible | Valeur : egalite -->
4. [Égalité](SCR_GLO_0049)
<!-- Condition métier : Notion liée disponible | Valeur : fraternite -->
5. [Fraternité](SCR_GLO_0062)
6. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0045

### Dignité humaine

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T3)
<!-- Condition métier : Notion liée disponible | Valeur : droits fondamentaux -->
3. [Droits fondamentaux](SCR_GLO_0047)
4. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0046

### Drapeau français

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T1)
<!-- Condition métier : Notion liée disponible | Valeur : la marseillaise -->
3. [La Marseillaise](SCR_GLO_0078)
4. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0047

### Droits fondamentaux

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T3)
<!-- Condition métier : Notion liée disponible | Valeur : constitution -->
3. [Constitution](SCR_GLO_0032)
<!-- Condition métier : Notion liée disponible | Valeur : liberte -->
4. [Liberté](SCR_GLO_0082)
<!-- Condition métier : Notion liée disponible | Valeur : egalite -->
5. [Égalité](SCR_GLO_0049)
6. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0048

### École

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T5)
<!-- Condition métier : Notion liée disponible | Valeur : college -->
3. [Collège](SCR_GLO_0022)
<!-- Condition métier : Notion liée disponible | Valeur : lycee -->
4. [Lycée](SCR_GLO_0086)
5. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0049

### Égalité

### Definition

Principe selon lequel toutes les personnes disposent des mêmes droits devant la loi.

Principe selon lequel toutes les personnes bénéficient des mêmes droits devant la loi.

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T1)
<!-- Condition métier : Notion liée disponible | Valeur : liberte -->
3. [Liberté](SCR_GLO_0082)
4. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0050

### Élection

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T2)
<!-- Condition métier : Notion liée disponible | Valeur : suffrage universel -->
3. [Suffrage universel](SCR_GLO_0127)
4. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0051

### Employeur

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T5)
3. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0052

### Environnement

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T3)
<!-- Condition métier : Notion liée disponible | Valeur : charte de l environnement -->
3. [Charte de l'environnement](SCR_GLO_0016)
4. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0053

### Espace Schengen

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T2)
<!-- Condition métier : Notion liée disponible | Valeur : union europeenne -->
3. [Union européenne](SCR_GLO_0133)
4. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0054

### État

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T2)
<!-- Condition métier : Notion liée disponible | Valeur : republique -->
3. [République](SCR_GLO_0118)
<!-- Condition métier : Notion liée disponible | Valeur : gouvernement -->
4. [Gouvernement](SCR_GLO_0066)
<!-- Condition métier : Notion liée disponible | Valeur : prefet -->
5. [Préfet](SCR_GLO_0106)
6. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0055

### Euro

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T2)
<!-- Condition métier : Notion liée disponible | Valeur : union europeenne -->
3. [Union européenne](SCR_GLO_0133)
4. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0056

### Fête de la Musique

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T4)
3. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0057

### Fête nationale

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T1)
<!-- Condition métier : Notion liée disponible | Valeur : republique -->
3. [République](SCR_GLO_0118)
4. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0058

### France métropolitaine

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T4)
<!-- Condition métier : Notion liée disponible | Valeur : outre mer -->
3. [Outre-mer](SCR_GLO_0100)
4. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0059

### France Services

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T5)
3. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0060

### France Travail

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T5)
3. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0061

### Francophonie

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T4)
3. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0062

### Fraternité

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T1)
3. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0063

### Gastronomie française

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T4)
<!-- Condition métier : Notion liée disponible | Valeur : unesco -->
3. [UNESCO](SCR_GLO_0132)
4. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0064

### Gaule

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T4)
<!-- Condition métier : Notion liée disponible | Valeur : celtes -->
3. [Celtes](SCR_GLO_0014)
<!-- Condition métier : Notion liée disponible | Valeur : vercingetorix -->
4. [Vercingétorix](SCR_GLO_0135)
5. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0065

### Gendarmerie

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T3)
<!-- Condition métier : Notion liée disponible | Valeur : police -->
3. [Police](SCR_GLO_0104)
4. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0066

### Gouvernement

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T2)
<!-- Condition métier : Notion liée disponible | Valeur : premier ministre -->
3. [Premier ministre](SCR_GLO_0107)
<!-- Condition métier : Notion liée disponible | Valeur : parlement -->
4. [Parlement](SCR_GLO_0101)
5. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0067

### Guadeloupe

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T4)
<!-- Condition métier : Notion liée disponible | Valeur : outre mer -->
3. [Outre-mer](SCR_GLO_0100)
4. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0068

### Guyane

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T4)
<!-- Condition métier : Notion liée disponible | Valeur : outre mer -->
3. [Outre-mer](SCR_GLO_0100)
4. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0069

### Harcèlement

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T3)
<!-- Condition métier : Notion liée disponible | Valeur : harcelement scolaire -->
3. [Harcèlement scolaire](SCR_GLO_0070)
4. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0070

### Harcèlement scolaire

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T3)
<!-- Condition métier : Notion liée disponible | Valeur : violence -->
3. [Violence](SCR_GLO_0136)
4. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0071

### Hôpital

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T5)
<!-- Condition métier : Notion liée disponible | Valeur : urgences -->
3. [Urgences](SCR_GLO_0134)
4. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0072

### Île-de-France

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T4)
3. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0073

### Impôt

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T3)
3. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0074

### Infraction

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T3)
<!-- Condition métier : Notion liée disponible | Valeur : contravention -->
3. [Contravention](SCR_GLO_0035)
<!-- Condition métier : Notion liée disponible | Valeur : delit -->
4. [Délit](SCR_GLO_0039)
<!-- Condition métier : Notion liée disponible | Valeur : crime -->
5. [Crime](SCR_GLO_0037)
6. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0075

### Intégrité de la personne

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T3)
<!-- Condition métier : Notion liée disponible | Valeur : dignite humaine -->
3. [Dignité humaine](SCR_GLO_0045)
4. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0076

### Journées européennes du patrimoine

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T4)
<!-- Condition métier : Notion liée disponible | Valeur : patrimoine -->
3. [Patrimoine](SCR_GLO_0103)
4. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0077

### Justice

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T2)
3. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0078

### La Marseillaise

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T1)
<!-- Condition métier : Notion liée disponible | Valeur : drapeau francais -->
3. [Drapeau français](SCR_GLO_0046)
4. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0079

### La Réunion

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T4)
<!-- Condition métier : Notion liée disponible | Valeur : outre mer -->
3. [Outre-mer](SCR_GLO_0100)
4. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0080

### Laïcité

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T1)
<!-- Condition métier : Notion liée disponible | Valeur : neutralite -->
3. [Neutralité](SCR_GLO_0098)
<!-- Condition métier : Notion liée disponible | Valeur : liberte de conscience -->
4. [Liberté de conscience](SCR_GLO_0083)
5. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0081

### Langue de la République

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T1)
<!-- Condition métier : Notion liée disponible | Valeur : republique -->
3. [République](SCR_GLO_0118)
4. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0082

### Liberté

### Definition

Valeur qui permet à chacun de penser, de s'exprimer et d'agir dans le respect de la loi et des autres.

Droit reconnu à chacun de penser, de s'exprimer et d'agir dans le respect de la loi.

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T1)
<!-- Condition métier : Notion liée disponible | Valeur : egalite -->
3. [Égalité](SCR_GLO_0049)
<!-- Condition métier : Notion liée disponible | Valeur : fraternite -->
4. [Fraternité](SCR_GLO_0062)
5. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0083

### Liberté de conscience

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T1)
<!-- Condition métier : Notion liée disponible | Valeur : laicite -->
3. [Laïcité](SCR_GLO_0080)
4. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0084

### Locataire

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T5)
<!-- Condition métier : Notion liée disponible | Valeur : bail -->
3. [Bail](SCR_GLO_0007)
4. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0085

### Loi

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T3)
<!-- Condition métier : Notion liée disponible | Valeur : parlement -->
3. [Parlement](SCR_GLO_0101)
4. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0086

### Lycée

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T5)
3. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0087

### Maire

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T2)
<!-- Condition métier : Notion liée disponible | Valeur : commune -->
3. [Commune](SCR_GLO_0024)
<!-- Condition métier : Notion liée disponible | Valeur : prefet -->
4. [Préfet](SCR_GLO_0106)
5. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0088

### Mairie

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T5)
<!-- Condition métier : Notion liée disponible | Valeur : commune -->
3. [Commune](SCR_GLO_0024)
<!-- Condition métier : Notion liée disponible | Valeur : maire -->
4. [Maire](SCR_GLO_0087)
5. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0089

### Marianne

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T1)
<!-- Condition métier : Notion liée disponible | Valeur : republique -->
3. [République](SCR_GLO_0118)
4. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0090

### Martinique

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T4)
<!-- Condition métier : Notion liée disponible | Valeur : outre mer -->
3. [Outre-mer](SCR_GLO_0100)
4. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0091

### Mayotte

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T4)
<!-- Condition métier : Notion liée disponible | Valeur : outre mer -->
3. [Outre-mer](SCR_GLO_0100)
4. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0092

### Médecin traitant

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T5)
<!-- Condition métier : Notion liée disponible | Valeur : assurance maladie -->
3. [Assurance maladie](SCR_GLO_0006)
4. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0093

### Ministre

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T2)
<!-- Condition métier : Notion liée disponible | Valeur : gouvernement -->
3. [Gouvernement](SCR_GLO_0066)
4. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0094

### Mont-Saint-Michel

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T4)
<!-- Condition métier : Notion liée disponible | Valeur : unesco -->
3. [UNESCO](SCR_GLO_0132)
4. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0095

### Musée du Louvre

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T4)
3. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0096

### Mutilations sexuelles féminines

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T3)
<!-- Condition métier : Notion liée disponible | Valeur : violence -->
3. [Violence](SCR_GLO_0136)
4. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0097

### Naturalisation

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T5)
3. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0098

### Neutralité

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T1)
<!-- Condition métier : Notion liée disponible | Valeur : laicite -->
3. [Laïcité](SCR_GLO_0080)
4. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0099

### Ordre public

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T3)
<!-- Condition métier : Notion liée disponible | Valeur : police -->
3. [Police](SCR_GLO_0104)
<!-- Condition métier : Notion liée disponible | Valeur : gendarmerie -->
4. [Gendarmerie](SCR_GLO_0065)
5. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0100

### Outre-mer

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T4)
<!-- Condition métier : Notion liée disponible | Valeur : guyane -->
3. [Guyane](SCR_GLO_0068)
<!-- Condition métier : Notion liée disponible | Valeur : guadeloupe -->
4. [Guadeloupe](SCR_GLO_0067)
<!-- Condition métier : Notion liée disponible | Valeur : martinique -->
5. [Martinique](SCR_GLO_0090)
<!-- Condition métier : Notion liée disponible | Valeur : la reunion -->
6. [La Réunion](SCR_GLO_0079)
<!-- Condition métier : Notion liée disponible | Valeur : mayotte -->
7. [Mayotte](SCR_GLO_0091)
8. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0101

### Parlement

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T2)
<!-- Condition métier : Notion liée disponible | Valeur : assemblee nationale -->
3. [Assemblée nationale](SCR_GLO_0004)
<!-- Condition métier : Notion liée disponible | Valeur : senat -->
4. [Sénat](SCR_GLO_0123)
5. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0102

### Parlement européen

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T2)
<!-- Condition métier : Notion liée disponible | Valeur : depute europeen -->
3. [Député européen](SCR_GLO_0043)
4. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0103

### Patrimoine

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T4)
<!-- Condition métier : Notion liée disponible | Valeur : unesco -->
3. [UNESCO](SCR_GLO_0132)
4. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0104

### Police

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T3)
<!-- Condition métier : Notion liée disponible | Valeur : gendarmerie -->
3. [Gendarmerie](SCR_GLO_0065)
4. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0105

### Préfecture

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T5)
<!-- Condition métier : Notion liée disponible | Valeur : prefet -->
3. [Préfet](SCR_GLO_0106)
4. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0106

### Préfet

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T2)
<!-- Condition métier : Notion liée disponible | Valeur : etat -->
3. [État](SCR_GLO_0054)
<!-- Condition métier : Notion liée disponible | Valeur : maire -->
4. [Maire](SCR_GLO_0087)
5. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0107

### Premier ministre

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T2)
<!-- Condition métier : Notion liée disponible | Valeur : gouvernement -->
3. [Gouvernement](SCR_GLO_0066)
4. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0108

### Première Guerre mondiale

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T4)
<!-- Condition métier : Notion liée disponible | Valeur : seconde guerre mondiale -->
3. [Seconde Guerre mondiale](SCR_GLO_0121)
4. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0109

### Président de la République

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T2)
<!-- Condition métier : Notion liée disponible | Valeur : gouvernement -->
3. [Gouvernement](SCR_GLO_0066)
<!-- Condition métier : Notion liée disponible | Valeur : premier ministre -->
4. [Premier ministre](SCR_GLO_0107)
5. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0110

### Présomption d'innocence

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T3)
<!-- Condition métier : Notion liée disponible | Valeur : justice -->
3. [Justice](SCR_GLO_0077)
4. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0111

### Procuration

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T2)
<!-- Condition métier : Notion liée disponible | Valeur : vote -->
3. [Vote](SCR_GLO_0137)
4. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0112

### Propriétaire

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T5)
<!-- Condition métier : Notion liée disponible | Valeur : bail -->
3. [Bail](SCR_GLO_0007)
4. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0113

### Prostitution

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T3)
<!-- Condition métier : Notion liée disponible | Valeur : traite des etres humains -->
3. [Traite des êtres humains](SCR_GLO_0131)
4. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0114

### Provence-Alpes-Côte d'Azur

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T4)
3. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0115

### Pyrénées

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T4)
<!-- Condition métier : Notion liée disponible | Valeur : alpes -->
3. [Alpes](SCR_GLO_0002)
4. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0116

### Référendum

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T2)
<!-- Condition métier : Notion liée disponible | Valeur : souverainete nationale -->
3. [Souveraineté nationale](SCR_GLO_0126)
4. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0117

### Région

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T2)
<!-- Condition métier : Notion liée disponible | Valeur : departement -->
3. [Département](SCR_GLO_0041)
4. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0118

### République

### Ne pas confondre

République ≠ démocratie.
La République est une forme d'organisation de l'État.
La démocratie est une manière d'exercer le pouvoir.

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T1)
<!-- Condition métier : Notion liée disponible | Valeur : constitution -->
3. [Constitution](SCR_GLO_0032)
<!-- Condition métier : Notion liée disponible | Valeur : democratie -->
4. [Démocratie](SCR_GLO_0040)
<!-- Condition métier : Notion liée disponible | Valeur : souverainete nationale -->
5. [Souveraineté nationale](SCR_GLO_0126)
6. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0119

### Révolution française

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T4)
<!-- Condition métier : Notion liée disponible | Valeur : declaration des droits de l homme et du citoyen -->
3. [Déclaration des droits de l'homme et du citoyen](SCR_GLO_0038)
4. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0120

### Salaire

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T5)
<!-- Condition métier : Notion liée disponible | Valeur : employeur -->
3. [Employeur](SCR_GLO_0051)
4. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0121

### Seconde Guerre mondiale

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T4)
3. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0122

### Seine

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T4)
3. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0123

### Sénat

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T2)
<!-- Condition métier : Notion liée disponible | Valeur : senateur -->
3. [Sénateur](SCR_GLO_0124)
<!-- Condition métier : Notion liée disponible | Valeur : parlement -->
4. [Parlement](SCR_GLO_0101)
5. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0124

### Sénateur

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T2)
<!-- Condition métier : Notion liée disponible | Valeur : senat -->
3. [Sénat](SCR_GLO_0123)
4. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0125

### Service public

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T5)
<!-- Condition métier : Notion liée disponible | Valeur : mairie -->
3. [Mairie](SCR_GLO_0088)
<!-- Condition métier : Notion liée disponible | Valeur : prefecture -->
4. [Préfecture](SCR_GLO_0105)
5. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0126

### Souveraineté nationale

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T1)
<!-- Condition métier : Notion liée disponible | Valeur : republique -->
3. [République](SCR_GLO_0118)
<!-- Condition métier : Notion liée disponible | Valeur : referendum -->
4. [Référendum](SCR_GLO_0116)
<!-- Condition métier : Notion liée disponible | Valeur : citoyen -->
5. [Citoyen](SCR_GLO_0019)
6. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0127

### Suffrage universel

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T2)
<!-- Condition métier : Notion liée disponible | Valeur : vote -->
3. [Vote](SCR_GLO_0137)
4. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0128

### Sûreté

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T3)
<!-- Condition métier : Notion liée disponible | Valeur : presomption d innocence -->
3. [Présomption d'innocence](SCR_GLO_0110)
<!-- Condition métier : Notion liée disponible | Valeur : justice -->
4. [Justice](SCR_GLO_0077)
5. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0129

### Titre de séjour

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T5)
<!-- Condition métier : Notion liée disponible | Valeur : prefecture -->
3. [Préfecture](SCR_GLO_0105)
4. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0130

### Tour Eiffel

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T4)
3. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0131

### Traite des êtres humains

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T3)
3. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0132

### UNESCO

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T4)
<!-- Condition métier : Notion liée disponible | Valeur : patrimoine -->
3. [Patrimoine](SCR_GLO_0103)
4. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0133

### Union européenne

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T2)
<!-- Condition métier : Notion liée disponible | Valeur : parlement europeen -->
3. [Parlement européen](SCR_GLO_0102)
<!-- Condition métier : Notion liée disponible | Valeur : euro -->
4. [Euro](SCR_GLO_0055)
5. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0134

### Urgences

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T5)
<!-- Condition métier : Notion liée disponible | Valeur : hopital -->
3. [Hôpital](SCR_GLO_0071)
4. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0135

### Vercingétorix

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T4)
<!-- Condition métier : Notion liée disponible | Valeur : gaule -->
3. [Gaule](SCR_GLO_0064)
4. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0136

### Violence

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T3)
<!-- Condition métier : Notion liée disponible | Valeur : consentement -->
3. [Consentement](SCR_GLO_0031)
4. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_0137

### Vote

<!-- Contenu non renseigné. -->

1. [📖 Voir un autre mot](SCR_GLO_SEARCH)
2. [📚 Retour au thème](SCR_GLO_THEME_T2)
<!-- Condition métier : Notion liée disponible | Valeur : election -->
3. [Élection](SCR_GLO_0050)
4. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran court, sans répéter les métadonnées techniques -->

## SCR_GLO_MENU

### 📖 Glossaire

<!-- Règle métier : Afficher au maximum 4 choix : recherche, thème, alphabet, retour menu -->

**Réponse attendue :** Choix d’un mode

1. [🔍 Rechercher un mot](SCR_GLO_SEARCH)
2. [📚 Parcourir par thème](SCR_GLO_THEME_MENU)
3. [🔤 Parcourir par ordre alphabétique](SCR_GLO_ALPHA_MENU)
4. [🏠 Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran d’entrée depuis le menu principal -->

## SCR_GLO_THEME_MENU

### 📚 Parcourir par thème

<!-- Liste dynamique : LISTE_THEMES. Les choix sont générés depuis 99_NAVIGATION. -->

<!-- Condition métier : Thème actif | Valeur : T1 -->
1. [Principes et valeurs de la République](SCR_GLO_THEME_T1)
<!-- Condition métier : Thème actif | Valeur : T2 -->
2. [Système institutionnel et politique français](SCR_GLO_THEME_T2)
<!-- Condition métier : Thème actif | Valeur : T3 -->
3. [Droits et devoirs](SCR_GLO_THEME_T3)
<!-- Condition métier : Thème actif | Valeur : T4 -->
4. [Histoire, géographie, patrimoine et culture](SCR_GLO_THEME_T4)
<!-- Condition métier : Thème actif | Valeur : T5 -->
5. [Vivre dans la société française](SCR_GLO_THEME_T5)
6. [Retour au glossaire](SCR_GLO_MENU)

## SCR_GLO_THEME_T1

### Principes et valeurs de la République

<!-- Règle métier : Afficher uniquement les notions actives du thème, triées par ordre alphabétique -->

**Réponse attendue :** Choix d’une notion

<!-- Condition métier : Notion active | Valeur : GLO0019 -->
1. [Citoyen](SCR_GLO_0019)
<!-- Condition métier : Notion active | Valeur : GLO0032 -->
2. [Constitution](SCR_GLO_0032)
<!-- Condition métier : Notion active | Valeur : GLO0033 -->
3. [Contrat d'engagement à respecter les principes de la République](SCR_GLO_0033)
<!-- Condition métier : Notion active | Valeur : GLO0040 -->
4. [Démocratie](SCR_GLO_0040)
<!-- Condition métier : Notion active | Valeur : GLO0044 -->
5. [Devise de la République](SCR_GLO_0044)
<!-- Condition métier : Notion active | Valeur : GLO0046 -->
6. [Drapeau français](SCR_GLO_0046)
<!-- Condition métier : Notion active | Valeur : GLO0049 -->
7. [Égalité](SCR_GLO_0049)
<!-- Condition métier : Notion active | Valeur : GLO0057 -->
8. [Fête nationale](SCR_GLO_0057)
<!-- Condition métier : Notion active | Valeur : GLO0062 -->
9. [Fraternité](SCR_GLO_0062)
<!-- Condition métier : Notion active | Valeur : GLO0078 -->
10. [La Marseillaise](SCR_GLO_0078)
<!-- Condition métier : Notion active | Valeur : GLO0080 -->
11. [Laïcité](SCR_GLO_0080)
<!-- Condition métier : Notion active | Valeur : GLO0081 -->
12. [Langue de la République](SCR_GLO_0081)
<!-- Condition métier : Notion active | Valeur : GLO0082 -->
13. [Liberté](SCR_GLO_0082)
<!-- Condition métier : Notion active | Valeur : GLO0083 -->
14. [Liberté de conscience](SCR_GLO_0083)
<!-- Condition métier : Notion active | Valeur : GLO0089 -->
15. [Marianne](SCR_GLO_0089)
<!-- Condition métier : Notion active | Valeur : GLO0098 -->
16. [Neutralité](SCR_GLO_0098)
<!-- Condition métier : Notion active | Valeur : GLO0118 -->
17. [République](SCR_GLO_0118)
<!-- Condition métier : Notion active | Valeur : GLO0126 -->
18. [Souveraineté nationale](SCR_GLO_0126)

<!-- Prévoir pagination si l’écran dépasse la capacité de ChatMD -->

## SCR_GLO_THEME_T2

### Système institutionnel et politique français

<!-- Règle métier : Afficher uniquement les notions actives du thème, triées par ordre alphabétique -->

**Réponse attendue :** Choix d’une notion

<!-- Condition métier : Notion active | Valeur : GLO0001 -->
1. [Abstention](SCR_GLO_0001)
<!-- Condition métier : Notion active | Valeur : GLO0004 -->
2. [Assemblée nationale](SCR_GLO_0004)
<!-- Condition métier : Notion active | Valeur : GLO0023 -->
3. [Commission européenne](SCR_GLO_0023)
<!-- Condition métier : Notion active | Valeur : GLO0024 -->
4. [Commune](SCR_GLO_0024)
<!-- Condition métier : Notion active | Valeur : GLO0025 -->
5. [Conseil constitutionnel](SCR_GLO_0025)
<!-- Condition métier : Notion active | Valeur : GLO0026 -->
6. [Conseil de l'Union européenne](SCR_GLO_0026)
<!-- Condition métier : Notion active | Valeur : GLO0027 -->
7. [Conseil départemental](SCR_GLO_0027)
<!-- Condition métier : Notion active | Valeur : GLO0028 -->
8. [Conseil européen](SCR_GLO_0028)
<!-- Condition métier : Notion active | Valeur : GLO0029 -->
9. [Conseil municipal](SCR_GLO_0029)
<!-- Condition métier : Notion active | Valeur : GLO0030 -->
10. [Conseil régional](SCR_GLO_0030)
<!-- Condition métier : Notion active | Valeur : GLO0041 -->
11. [Département](SCR_GLO_0041)
<!-- Condition métier : Notion active | Valeur : GLO0042 -->
12. [Député](SCR_GLO_0042)
<!-- Condition métier : Notion active | Valeur : GLO0043 -->
13. [Député européen](SCR_GLO_0043)
<!-- Condition métier : Notion active | Valeur : GLO0050 -->
14. [Élection](SCR_GLO_0050)
<!-- Condition métier : Notion active | Valeur : GLO0053 -->
15. [Espace Schengen](SCR_GLO_0053)
<!-- Condition métier : Notion active | Valeur : GLO0054 -->
16. [État](SCR_GLO_0054)
<!-- Condition métier : Notion active | Valeur : GLO0055 -->
17. [Euro](SCR_GLO_0055)
<!-- Condition métier : Notion active | Valeur : GLO0066 -->
18. [Gouvernement](SCR_GLO_0066)
<!-- Condition métier : Notion active | Valeur : GLO0077 -->
19. [Justice](SCR_GLO_0077)
<!-- Condition métier : Notion active | Valeur : GLO0087 -->
20. [Maire](SCR_GLO_0087)
<!-- Condition métier : Notion active | Valeur : GLO0093 -->
21. [Ministre](SCR_GLO_0093)
<!-- Condition métier : Notion active | Valeur : GLO0101 -->
22. [Parlement](SCR_GLO_0101)
<!-- Condition métier : Notion active | Valeur : GLO0102 -->
23. [Parlement européen](SCR_GLO_0102)
<!-- Condition métier : Notion active | Valeur : GLO0106 -->
24. [Préfet](SCR_GLO_0106)
<!-- Condition métier : Notion active | Valeur : GLO0107 -->
25. [Premier ministre](SCR_GLO_0107)
<!-- Condition métier : Notion active | Valeur : GLO0109 -->
26. [Président de la République](SCR_GLO_0109)
<!-- Condition métier : Notion active | Valeur : GLO0111 -->
27. [Procuration](SCR_GLO_0111)
<!-- Condition métier : Notion active | Valeur : GLO0116 -->
28. [Référendum](SCR_GLO_0116)
<!-- Condition métier : Notion active | Valeur : GLO0117 -->
29. [Région](SCR_GLO_0117)
<!-- Condition métier : Notion active | Valeur : GLO0123 -->
30. [Sénat](SCR_GLO_0123)
<!-- Condition métier : Notion active | Valeur : GLO0124 -->
31. [Sénateur](SCR_GLO_0124)
<!-- Condition métier : Notion active | Valeur : GLO0127 -->
32. [Suffrage universel](SCR_GLO_0127)
<!-- Condition métier : Notion active | Valeur : GLO0133 -->
33. [Union européenne](SCR_GLO_0133)
<!-- Condition métier : Notion active | Valeur : GLO0137 -->
34. [Vote](SCR_GLO_0137)

<!-- Prévoir pagination si l’écran dépasse la capacité de ChatMD -->

## SCR_GLO_THEME_T3

### Droits et devoirs

<!-- Règle métier : Afficher uniquement les notions actives du thème, triées par ordre alphabétique -->

**Réponse attendue :** Choix d’une notion

<!-- Condition métier : Notion active | Valeur : GLO0005 -->
1. [Assistance à personne en danger](SCR_GLO_0005)
<!-- Condition métier : Notion active | Valeur : GLO0016 -->
2. [Charte de l'environnement](SCR_GLO_0016)
<!-- Condition métier : Notion active | Valeur : GLO0020 -->
3. [Citoyenneté](SCR_GLO_0020)
<!-- Condition métier : Notion active | Valeur : GLO0031 -->
4. [Consentement](SCR_GLO_0031)
<!-- Condition métier : Notion active | Valeur : GLO0035 -->
5. [Contravention](SCR_GLO_0035)
<!-- Condition métier : Notion active | Valeur : GLO0037 -->
6. [Crime](SCR_GLO_0037)
<!-- Condition métier : Notion active | Valeur : GLO0038 -->
7. [Déclaration des droits de l'homme et du citoyen](SCR_GLO_0038)
<!-- Condition métier : Notion active | Valeur : GLO0039 -->
8. [Délit](SCR_GLO_0039)
<!-- Condition métier : Notion active | Valeur : GLO0045 -->
9. [Dignité humaine](SCR_GLO_0045)
<!-- Condition métier : Notion active | Valeur : GLO0047 -->
10. [Droits fondamentaux](SCR_GLO_0047)
<!-- Condition métier : Notion active | Valeur : GLO0049 -->
11. [Égalité](SCR_GLO_0049)
<!-- Condition métier : Notion active | Valeur : GLO0052 -->
12. [Environnement](SCR_GLO_0052)
<!-- Condition métier : Notion active | Valeur : GLO0065 -->
13. [Gendarmerie](SCR_GLO_0065)
<!-- Condition métier : Notion active | Valeur : GLO0069 -->
14. [Harcèlement](SCR_GLO_0069)
<!-- Condition métier : Notion active | Valeur : GLO0070 -->
15. [Harcèlement scolaire](SCR_GLO_0070)
<!-- Condition métier : Notion active | Valeur : GLO0073 -->
16. [Impôt](SCR_GLO_0073)
<!-- Condition métier : Notion active | Valeur : GLO0074 -->
17. [Infraction](SCR_GLO_0074)
<!-- Condition métier : Notion active | Valeur : GLO0075 -->
18. [Intégrité de la personne](SCR_GLO_0075)
<!-- Condition métier : Notion active | Valeur : GLO0082 -->
19. [Liberté](SCR_GLO_0082)
<!-- Condition métier : Notion active | Valeur : GLO0085 -->
20. [Loi](SCR_GLO_0085)
<!-- Condition métier : Notion active | Valeur : GLO0096 -->
21. [Mutilations sexuelles féminines](SCR_GLO_0096)
<!-- Condition métier : Notion active | Valeur : GLO0099 -->
22. [Ordre public](SCR_GLO_0099)
<!-- Condition métier : Notion active | Valeur : GLO0104 -->
23. [Police](SCR_GLO_0104)
<!-- Condition métier : Notion active | Valeur : GLO0110 -->
24. [Présomption d'innocence](SCR_GLO_0110)
<!-- Condition métier : Notion active | Valeur : GLO0113 -->
25. [Prostitution](SCR_GLO_0113)
<!-- Condition métier : Notion active | Valeur : GLO0128 -->
26. [Sûreté](SCR_GLO_0128)
<!-- Condition métier : Notion active | Valeur : GLO0131 -->
27. [Traite des êtres humains](SCR_GLO_0131)
<!-- Condition métier : Notion active | Valeur : GLO0136 -->
28. [Violence](SCR_GLO_0136)

<!-- Prévoir pagination si l’écran dépasse la capacité de ChatMD -->

## SCR_GLO_THEME_T4

### Histoire, géographie, patrimoine et culture

<!-- Règle métier : Afficher uniquement les notions actives du thème, triées par ordre alphabétique -->

**Réponse attendue :** Choix d’une notion

<!-- Condition métier : Notion active | Valeur : GLO0002 -->
1. [Alpes](SCR_GLO_0002)
<!-- Condition métier : Notion active | Valeur : GLO0008 -->
2. [Bretagne](SCR_GLO_0008)
<!-- Condition métier : Notion active | Valeur : GLO0014 -->
3. [Celtes](SCR_GLO_0014)
<!-- Condition métier : Notion active | Valeur : GLO0015 -->
4. [Charlemagne](SCR_GLO_0015)
<!-- Condition métier : Notion active | Valeur : GLO0017 -->
5. [Château de Versailles](SCR_GLO_0017)
<!-- Condition métier : Notion active | Valeur : GLO0018 -->
6. [Cinquième République](SCR_GLO_0018)
<!-- Condition métier : Notion active | Valeur : GLO0021 -->
7. [Clovis](SCR_GLO_0021)
<!-- Condition métier : Notion active | Valeur : GLO0056 -->
8. [Fête de la Musique](SCR_GLO_0056)
<!-- Condition métier : Notion active | Valeur : GLO0058 -->
9. [France métropolitaine](SCR_GLO_0058)
<!-- Condition métier : Notion active | Valeur : GLO0061 -->
10. [Francophonie](SCR_GLO_0061)
<!-- Condition métier : Notion active | Valeur : GLO0063 -->
11. [Gastronomie française](SCR_GLO_0063)
<!-- Condition métier : Notion active | Valeur : GLO0064 -->
12. [Gaule](SCR_GLO_0064)
<!-- Condition métier : Notion active | Valeur : GLO0067 -->
13. [Guadeloupe](SCR_GLO_0067)
<!-- Condition métier : Notion active | Valeur : GLO0068 -->
14. [Guyane](SCR_GLO_0068)
<!-- Condition métier : Notion active | Valeur : GLO0072 -->
15. [Île-de-France](SCR_GLO_0072)
<!-- Condition métier : Notion active | Valeur : GLO0076 -->
16. [Journées européennes du patrimoine](SCR_GLO_0076)
<!-- Condition métier : Notion active | Valeur : GLO0079 -->
17. [La Réunion](SCR_GLO_0079)
<!-- Condition métier : Notion active | Valeur : GLO0090 -->
18. [Martinique](SCR_GLO_0090)
<!-- Condition métier : Notion active | Valeur : GLO0091 -->
19. [Mayotte](SCR_GLO_0091)
<!-- Condition métier : Notion active | Valeur : GLO0094 -->
20. [Mont-Saint-Michel](SCR_GLO_0094)
<!-- Condition métier : Notion active | Valeur : GLO0095 -->
21. [Musée du Louvre](SCR_GLO_0095)
<!-- Condition métier : Notion active | Valeur : GLO0100 -->
22. [Outre-mer](SCR_GLO_0100)
<!-- Condition métier : Notion active | Valeur : GLO0103 -->
23. [Patrimoine](SCR_GLO_0103)
<!-- Condition métier : Notion active | Valeur : GLO0108 -->
24. [Première Guerre mondiale](SCR_GLO_0108)
<!-- Condition métier : Notion active | Valeur : GLO0114 -->
25. [Provence-Alpes-Côte d'Azur](SCR_GLO_0114)
<!-- Condition métier : Notion active | Valeur : GLO0115 -->
26. [Pyrénées](SCR_GLO_0115)
<!-- Condition métier : Notion active | Valeur : GLO0119 -->
27. [Révolution française](SCR_GLO_0119)
<!-- Condition métier : Notion active | Valeur : GLO0121 -->
28. [Seconde Guerre mondiale](SCR_GLO_0121)
<!-- Condition métier : Notion active | Valeur : GLO0122 -->
29. [Seine](SCR_GLO_0122)
<!-- Condition métier : Notion active | Valeur : GLO0130 -->
30. [Tour Eiffel](SCR_GLO_0130)
<!-- Condition métier : Notion active | Valeur : GLO0132 -->
31. [UNESCO](SCR_GLO_0132)
<!-- Condition métier : Notion active | Valeur : GLO0135 -->
32. [Vercingétorix](SCR_GLO_0135)

<!-- Prévoir pagination si l’écran dépasse la capacité de ChatMD -->

## SCR_GLO_THEME_T5

### Vivre dans la société française

<!-- Règle métier : Afficher uniquement les notions actives du thème, triées par ordre alphabétique -->

**Réponse attendue :** Choix d’une notion

<!-- Condition métier : Notion active | Valeur : GLO0003 -->
1. [APL](SCR_GLO_0003)
<!-- Condition métier : Notion active | Valeur : GLO0006 -->
2. [Assurance maladie](SCR_GLO_0006)
<!-- Condition métier : Notion active | Valeur : GLO0007 -->
3. [Bail](SCR_GLO_0007)
<!-- Condition métier : Notion active | Valeur : GLO0009 -->
4. [CAF](SCR_GLO_0009)
<!-- Condition métier : Notion active | Valeur : GLO0010 -->
5. [Carte de résident](SCR_GLO_0010)
<!-- Condition métier : Notion active | Valeur : GLO0011 -->
6. [Carte Vitale](SCR_GLO_0011)
<!-- Condition métier : Notion active | Valeur : GLO0012 -->
7. [CDD](SCR_GLO_0012)
<!-- Condition métier : Notion active | Valeur : GLO0013 -->
8. [CDI](SCR_GLO_0013)
<!-- Condition métier : Notion active | Valeur : GLO0022 -->
9. [Collège](SCR_GLO_0022)
<!-- Condition métier : Notion active | Valeur : GLO0034 -->
10. [Contrat de travail](SCR_GLO_0034)
<!-- Condition métier : Notion active | Valeur : GLO0036 -->
11. [CPAM](SCR_GLO_0036)
<!-- Condition métier : Notion active | Valeur : GLO0048 -->
12. [École](SCR_GLO_0048)
<!-- Condition métier : Notion active | Valeur : GLO0051 -->
13. [Employeur](SCR_GLO_0051)
<!-- Condition métier : Notion active | Valeur : GLO0059 -->
14. [France Services](SCR_GLO_0059)
<!-- Condition métier : Notion active | Valeur : GLO0060 -->
15. [France Travail](SCR_GLO_0060)
<!-- Condition métier : Notion active | Valeur : GLO0071 -->
16. [Hôpital](SCR_GLO_0071)
<!-- Condition métier : Notion active | Valeur : GLO0084 -->
17. [Locataire](SCR_GLO_0084)
<!-- Condition métier : Notion active | Valeur : GLO0086 -->
18. [Lycée](SCR_GLO_0086)
<!-- Condition métier : Notion active | Valeur : GLO0088 -->
19. [Mairie](SCR_GLO_0088)
<!-- Condition métier : Notion active | Valeur : GLO0092 -->
20. [Médecin traitant](SCR_GLO_0092)
<!-- Condition métier : Notion active | Valeur : GLO0097 -->
21. [Naturalisation](SCR_GLO_0097)
<!-- Condition métier : Notion active | Valeur : GLO0105 -->
22. [Préfecture](SCR_GLO_0105)
<!-- Condition métier : Notion active | Valeur : GLO0112 -->
23. [Propriétaire](SCR_GLO_0112)
<!-- Condition métier : Notion active | Valeur : GLO0120 -->
24. [Salaire](SCR_GLO_0120)
<!-- Condition métier : Notion active | Valeur : GLO0125 -->
25. [Service public](SCR_GLO_0125)
<!-- Condition métier : Notion active | Valeur : GLO0129 -->
26. [Titre de séjour](SCR_GLO_0129)
<!-- Condition métier : Notion active | Valeur : GLO0134 -->
27. [Urgences](SCR_GLO_0134)

<!-- Prévoir pagination si l’écran dépasse la capacité de ChatMD -->

## SCR_GLO_SEARCH

### 🔍 Rechercher un mot

<!-- Variables : {mot_recherche} -->

<!-- Règle métier : Normaliser la saisie, rechercher dans Mot, Mot normalisé et Mots-clés, puis ouvrir l’écran de la notion la plus pertinente -->

**Réponse attendue :** Texte libre

<!-- Transition automatique NAV_GLO_SEARCH_MATCH : Correspondance trouvée → SCR_GLO_* -->
1. [Afficher la définition](SCR_GLO_*)
<!-- Transition automatique NAV_GLO_SEARCH_NOMATCH : Aucune correspondance → SCR_GLO_SEARCH_NOT_FOUND -->
1. [Mot non trouvé](SCR_GLO_SEARCH_NOT_FOUND)

<!-- Accepte un mot ou une question courte -->

## SCR_GLO_SEARCH_NOT_FOUND

### Mot non trouvé

<!-- Variables : {mot_recherche} -->

<!-- Règle métier : Proposer une nouvelle recherche, les thèmes ou l’alphabet sans surcharger l’écran -->

**Réponse attendue :** Nouvelle saisie

1. [Rechercher un autre mot](SCR_GLO_SEARCH)
2. [Parcourir par thème](SCR_GLO_THEME_MENU)
3. [Parcourir par ordre alphabétique](SCR_GLO_ALPHA_MENU)
4. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Fin du fichier source : modules\04_glossaire.md -->

<!-- Début du fichier source : modules\06_entrainement.md -->

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

<!-- Fin du fichier source : modules\06_entrainement.md -->

<!-- Début du fichier source : modules\07_passer_examen.md -->

<!-- Module généré automatiquement : Passer examen -->
<!-- Date : 2026-08-03T13:13:33+02:00 -->

## SCR_PASS_CITY_ANNECY

### Annecy (74)

<!-- Variables : {centre}=Annecy; {region}=Rhône-Alpes; {lien_forms} -->

<!-- Règle métier : Afficher les trois prochaines dates futures, inscription et retours -->

**Réponse attendue :** Choix d’une action

<!-- Condition métier : Au moins une session future -->
1. [S’inscrire à une session](https://forms.office.com/pages/responsepage.aspx?id=Cf5pfw3SOUOtLY5q0AbYj15YUUzJ44lEjv9UrEuppChUMFVWWUZUWDBIV1FOT0xTTU5LTUdKVVlPQiQlQCN0PWcu&route=shorturl)
2. [Voir un autre centre de la région](SCR_PASS_REGION_RHONE_ALPES)
3. [Trouver les centres proches de moi](SCR_PASS_INPUT_COMMUNE)
4. [Retour au module](SCR_PASS_MENU)

<!-- 4 session(s) future(s) dans la source -->

## SCR_PASS_CITY_ANNEMASSE

### Annemasse (74)

<!-- Variables : {centre}=Annemasse; {region}=Rhône-Alpes; {lien_forms} -->

<!-- Règle métier : Afficher les trois prochaines dates futures, inscription et retours -->

**Réponse attendue :** Choix d’une action

<!-- Condition métier : Au moins une session future -->
1. [S’inscrire à une session](https://forms.office.com/pages/responsepage.aspx?id=Cf5pfw3SOUOtLY5q0AbYj15YUUzJ44lEjv9UrEuppChUMFVWWUZUWDBIV1FOT0xTTU5LTUdKVVlPQiQlQCN0PWcu&route=shorturl)
2. [Voir un autre centre de la région](SCR_PASS_REGION_RHONE_ALPES)
3. [Trouver les centres proches de moi](SCR_PASS_INPUT_COMMUNE)
4. [Retour au module](SCR_PASS_MENU)

<!-- 4 session(s) future(s) dans la source -->

## SCR_PASS_CITY_AUXERRE

### Auxerre (89)

<!-- Variables : {centre}=Auxerre; {region}=Bourgogne; {lien_forms} -->

<!-- Règle métier : Afficher les trois prochaines dates futures, inscription et retours -->

**Réponse attendue :** Choix d’une action

<!-- Condition métier : Au moins une session future -->
1. [S’inscrire à une session](https://forms.office.com/pages/responsepage.aspx?id=Cf5pfw3SOUOtLY5q0AbYj15YUUzJ44lEjv9UrEuppChUMU5BMzNJTE1ZVzJROEVXWkVTTEtTTjEzUyQlQCN0PWcu&route=shorturl)
2. [Voir un autre centre de la région](SCR_PASS_REGION_BOURGOGNE)
3. [Trouver les centres proches de moi](SCR_PASS_INPUT_COMMUNE)
4. [Retour au module](SCR_PASS_MENU)

<!-- 5 session(s) future(s) dans la source -->

## SCR_PASS_CITY_BESANCON

### Besançon (25)

<!-- Variables : {centre}=Besançon; {region}=Franche-Comté; {lien_forms} -->

<!-- Règle métier : Afficher les trois prochaines dates futures, inscription et retours -->

**Réponse attendue :** Choix d’une action

<!-- Condition métier : Au moins une session future -->
1. [S’inscrire à une session](https://forms.office.com/Pages/ResponsePage.aspx?id=Cf5pfw3SOUOtLY5q0AbYj15YUUzJ44lEjv9UrEuppChUNUo5SUNJN1o2MjVKOEtFVUxPVU9LSElDWCQlQCN0PWcu)
2. [Voir un autre centre de la région](SCR_PASS_REGION_FRANCHE_COMTE)
3. [Trouver les centres proches de moi](SCR_PASS_INPUT_COMMUNE)
4. [Retour au module](SCR_PASS_MENU)

<!-- 9 session(s) future(s) dans la source -->

## SCR_PASS_CITY_BOURG_EN_BRESSE

### Bourg-en-Bresse (01)

<!-- Variables : {centre}=Bourg-en-Bresse; {region}=Rhône-Alpes; {lien_forms} -->

<!-- Règle métier : Afficher les trois prochaines dates futures, inscription et retours -->

**Réponse attendue :** Choix d’une action

<!-- Condition métier : Au moins une session future -->
1. [S’inscrire à une session](https://forms.office.com/pages/responsepage.aspx?id=Cf5pfw3SOUOtLY5q0AbYj15YUUzJ44lEjv9UrEuppChUMFVWWUZUWDBIV1FOT0xTTU5LTUdKVVlPQiQlQCN0PWcu&route=shorturl)
2. [Voir un autre centre de la région](SCR_PASS_REGION_RHONE_ALPES)
3. [Trouver les centres proches de moi](SCR_PASS_INPUT_COMMUNE)
4. [Retour au module](SCR_PASS_MENU)

<!-- 4 session(s) future(s) dans la source -->

## SCR_PASS_CITY_BOURGES

### Bourges (18)

<!-- Variables : {centre}=Bourges; {region}=Cher; {lien_forms} -->

<!-- Règle métier : Afficher les trois prochaines dates futures, inscription et retours -->

**Réponse attendue :** Choix d’une action

<!-- Condition métier : Au moins une session future -->
1. [S’inscrire à une session](https://forms.office.com/pages/responsepage.aspx?id=Cf5pfw3SOUOtLY5q0AbYj15YUUzJ44lEjv9UrEuppChUM09TTktYSFJMSUc4T0lUMUdSRDA5Ukw2RSQlQCN0PWcu&route=shorturl)
2. [Voir un autre centre de la région](SCR_PASS_REGION_CHER)
3. [Trouver les centres proches de moi](SCR_PASS_INPUT_COMMUNE)
4. [Retour au module](SCR_PASS_MENU)

<!-- 4 session(s) future(s) dans la source -->

## SCR_PASS_CITY_CHAUMONT

### Chaumont (52)

<!-- Variables : {centre}=Chaumont; {region}=Grand Est; {lien_forms} -->

<!-- Règle métier : Afficher les trois prochaines dates futures, inscription et retours -->

**Réponse attendue :** Choix d’une action

<!-- Condition métier : Au moins une session future -->
1. [S’inscrire à une session](https://forms.office.com/pages/responsepage.aspx?id=Cf5pfw3SOUOtLY5q0AbYj15YUUzJ44lEjv9UrEuppChUNlpSVzg1VkxHUlhNVDFBQTk4N0pNUkU1WCQlQCN0PWcu&route=shorturl)
2. [Voir un autre centre de la région](SCR_PASS_REGION_GRAND_EST)
3. [Trouver les centres proches de moi](SCR_PASS_INPUT_COMMUNE)
4. [Retour au module](SCR_PASS_MENU)

<!-- 2 session(s) future(s) dans la source -->

## SCR_PASS_CITY_CLERMONT_FERRAND

### Clermont-Ferrand (63)

<!-- Variables : {centre}=Clermont-Ferrand; {region}=Auvergne; {lien_forms} -->

<!-- Règle métier : Afficher les trois prochaines dates futures, inscription et retours -->

**Réponse attendue :** Choix d’une action

<!-- Condition métier : Au moins une session future -->
1. [S’inscrire à une session](https://forms.cloud.microsoft/pages/responsepage.aspx?id=Cf5pfw3SOUOtLY5q0AbYj15YUUzJ44lEjv9UrEuppChURjEzQVlJWjdUMlFXODhXN1pPR0JGN1RDWCQlQCN0PWcu&route=shorturl)
2. [Voir un autre centre de la région](SCR_PASS_REGION_AUVERGNE)
3. [Trouver les centres proches de moi](SCR_PASS_INPUT_COMMUNE)
4. [Retour au module](SCR_PASS_MENU)

<!-- 7 session(s) future(s) dans la source -->

## SCR_PASS_CITY_DIJON

### Dijon (21)

<!-- Variables : {centre}=Dijon; {region}=Bourgogne; {lien_forms} -->

<!-- Règle métier : Afficher les trois prochaines dates futures, inscription et retours -->

**Réponse attendue :** Choix d’une action

<!-- Condition métier : Au moins une session future -->
1. [S’inscrire à une session](https://forms.office.com/pages/responsepage.aspx?id=Cf5pfw3SOUOtLY5q0AbYj15YUUzJ44lEjv9UrEuppChUMU5BMzNJTE1ZVzJROEVXWkVTTEtTTjEzUyQlQCN0PWcu&route=shorturl)
2. [Voir un autre centre de la région](SCR_PASS_REGION_BOURGOGNE)
3. [Trouver les centres proches de moi](SCR_PASS_INPUT_COMMUNE)
4. [Retour au module](SCR_PASS_MENU)

<!-- 5 session(s) future(s) dans la source -->

## SCR_PASS_CITY_LE_PUY_EN_VELAY

### Le Puy-en-Velay (43)

<!-- Variables : {centre}=Le Puy-en-Velay; {region}=Auvergne; {lien_forms} -->

<!-- Règle métier : Afficher les trois prochaines dates futures, inscription et retours -->

**Réponse attendue :** Choix d’une action

<!-- Condition métier : Au moins une session future -->
1. [S’inscrire à une session](https://forms.cloud.microsoft/pages/responsepage.aspx?id=Cf5pfw3SOUOtLY5q0AbYj15YUUzJ44lEjv9UrEuppChURjEzQVlJWjdUMlFXODhXN1pPR0JGN1RDWCQlQCN0PWcu&route=shorturl)
2. [Voir un autre centre de la région](SCR_PASS_REGION_AUVERGNE)
3. [Trouver les centres proches de moi](SCR_PASS_INPUT_COMMUNE)
4. [Retour au module](SCR_PASS_MENU)

<!-- 4 session(s) future(s) dans la source -->

## SCR_PASS_CITY_LONS_LE_SAUNIER

### Lons-le-Saunier (39)

<!-- Variables : {centre}=Lons-le-Saunier; {region}=Franche-Comté; {lien_forms} -->

<!-- Règle métier : Afficher les trois prochaines dates futures, inscription et retours -->

**Réponse attendue :** Choix d’une action

<!-- Condition métier : Au moins une session future -->
1. [S’inscrire à une session](https://forms.office.com/Pages/ResponsePage.aspx?id=Cf5pfw3SOUOtLY5q0AbYj15YUUzJ44lEjv9UrEuppChUNUo5SUNJN1o2MjVKOEtFVUxPVU9LSElDWCQlQCN0PWcu)
2. [Voir un autre centre de la région](SCR_PASS_REGION_FRANCHE_COMTE)
3. [Trouver les centres proches de moi](SCR_PASS_INPUT_COMMUNE)
4. [Retour au module](SCR_PASS_MENU)

<!-- 4 session(s) future(s) dans la source -->

## SCR_PASS_CITY_MONTBELIARD

### Montbéliard (25)

<!-- Variables : {centre}=Montbéliard; {region}=Franche-Comté; {lien_forms} -->

<!-- Règle métier : Afficher les trois prochaines dates futures, inscription et retours -->

**Réponse attendue :** Choix d’une action

<!-- Condition métier : Au moins une session future -->
1. [S’inscrire à une session](https://forms.office.com/Pages/ResponsePage.aspx?id=Cf5pfw3SOUOtLY5q0AbYj15YUUzJ44lEjv9UrEuppChUNUo5SUNJN1o2MjVKOEtFVUxPVU9LSElDWCQlQCN0PWcu)
2. [Voir un autre centre de la région](SCR_PASS_REGION_FRANCHE_COMTE)
3. [Trouver les centres proches de moi](SCR_PASS_INPUT_COMMUNE)
4. [Retour au module](SCR_PASS_MENU)

<!-- 4 session(s) future(s) dans la source -->

## SCR_PASS_CITY_MONTCEAU_LES_MINES

### Montceau-les-Mines (71)

<!-- Variables : {centre}=Montceau-les-Mines; {region}=Bourgogne; {lien_forms} -->

<!-- Règle métier : Afficher les trois prochaines dates futures, inscription et retours -->

**Réponse attendue :** Choix d’une action

<!-- Condition métier : Au moins une session future -->
1. [S’inscrire à une session](https://forms.office.com/pages/responsepage.aspx?id=Cf5pfw3SOUOtLY5q0AbYj15YUUzJ44lEjv9UrEuppChUMU5BMzNJTE1ZVzJROEVXWkVTTEtTTjEzUyQlQCN0PWcu&route=shorturl)
2. [Voir un autre centre de la région](SCR_PASS_REGION_BOURGOGNE)
3. [Trouver les centres proches de moi](SCR_PASS_INPUT_COMMUNE)
4. [Retour au module](SCR_PASS_MENU)

<!-- 3 session(s) future(s) dans la source -->

## SCR_PASS_CITY_MULHOUSE

### Mulhouse (68)

<!-- Variables : {centre}=Mulhouse; {region}=Grand Est; {lien_forms} -->

<!-- Règle métier : Afficher les trois prochaines dates futures, inscription et retours -->

**Réponse attendue :** Choix d’une action

<!-- Condition métier : Au moins une session future -->
1. [S’inscrire à une session](https://forms.office.com/pages/responsepage.aspx?id=Cf5pfw3SOUOtLY5q0AbYj15YUUzJ44lEjv9UrEuppChUNlpSVzg1VkxHUlhNVDFBQTk4N0pNUkU1WCQlQCN0PWcu&route=shorturl)
2. [Voir un autre centre de la région](SCR_PASS_REGION_GRAND_EST)
3. [Trouver les centres proches de moi](SCR_PASS_INPUT_COMMUNE)
4. [Retour au module](SCR_PASS_MENU)

<!-- 7 session(s) future(s) dans la source -->

## SCR_PASS_CITY_MACON

### Mâcon (71)

<!-- Variables : {centre}=Mâcon; {region}=Bourgogne; {lien_forms} -->

<!-- Règle métier : Afficher les trois prochaines dates futures, inscription et retours -->

**Réponse attendue :** Choix d’une action

<!-- Condition métier : Au moins une session future -->
1. [S’inscrire à une session](https://forms.office.com/pages/responsepage.aspx?id=Cf5pfw3SOUOtLY5q0AbYj15YUUzJ44lEjv9UrEuppChUMU5BMzNJTE1ZVzJROEVXWkVTTEtTTjEzUyQlQCN0PWcu&route=shorturl)
2. [Voir un autre centre de la région](SCR_PASS_REGION_BOURGOGNE)
3. [Trouver les centres proches de moi](SCR_PASS_INPUT_COMMUNE)
4. [Retour au module](SCR_PASS_MENU)

<!-- 2 session(s) future(s) dans la source -->

## SCR_PASS_CITY_NEVERS

### Nevers (58)

<!-- Variables : {centre}=Nevers; {region}=Bourgogne; {lien_forms} -->

<!-- Règle métier : Afficher les trois prochaines dates futures, inscription et retours -->

**Réponse attendue :** Choix d’une action

<!-- Condition métier : Au moins une session future -->
1. [S’inscrire à une session](https://forms.office.com/pages/responsepage.aspx?id=Cf5pfw3SOUOtLY5q0AbYj15YUUzJ44lEjv9UrEuppChUMU5BMzNJTE1ZVzJROEVXWkVTTEtTTjEzUyQlQCN0PWcu&route=shorturl)
2. [Voir un autre centre de la région](SCR_PASS_REGION_BOURGOGNE)
3. [Trouver les centres proches de moi](SCR_PASS_INPUT_COMMUNE)
4. [Retour au module](SCR_PASS_MENU)

<!-- 4 session(s) future(s) dans la source -->

## SCR_PASS_CITY_REIMS

### Reims (51)

<!-- Variables : {centre}=Reims; {region}=Grand Est; {lien_forms} -->

<!-- Règle métier : Afficher les trois prochaines dates futures, inscription et retours -->

**Réponse attendue :** Choix d’une action

<!-- Condition métier : Au moins une session future -->
1. [S’inscrire à une session](https://forms.office.com/pages/responsepage.aspx?id=Cf5pfw3SOUOtLY5q0AbYj15YUUzJ44lEjv9UrEuppChUNlpSVzg1VkxHUlhNVDFBQTk4N0pNUkU1WCQlQCN0PWcu&route=shorturl)
2. [Voir un autre centre de la région](SCR_PASS_REGION_GRAND_EST)
3. [Trouver les centres proches de moi](SCR_PASS_INPUT_COMMUNE)
4. [Retour au module](SCR_PASS_MENU)

<!-- 6 session(s) future(s) dans la source -->

## SCR_PASS_CITY_SAINT_DIE_DES_VOSGES

### Saint-Dié-des-Vosges (88)

<!-- Variables : {centre}=Saint-Dié-des-Vosges; {region}=Grand Est; {lien_forms} -->

<!-- Règle métier : Afficher les trois prochaines dates futures, inscription et retours -->

**Réponse attendue :** Choix d’une action

<!-- Condition métier : Au moins une session future -->
1. [S’inscrire à une session](https://forms.office.com/pages/responsepage.aspx?id=Cf5pfw3SOUOtLY5q0AbYj15YUUzJ44lEjv9UrEuppChUNlpSVzg1VkxHUlhNVDFBQTk4N0pNUkU1WCQlQCN0PWcu&route=shorturl)
2. [Voir un autre centre de la région](SCR_PASS_REGION_GRAND_EST)
3. [Trouver les centres proches de moi](SCR_PASS_INPUT_COMMUNE)
4. [Retour au module](SCR_PASS_MENU)

<!-- 3 session(s) future(s) dans la source -->

## SCR_PASS_CITY_SAINT_FLOUR

### Saint-Flour (15)

<!-- Variables : {centre}=Saint-Flour; {region}=Auvergne; {lien_forms} -->

<!-- Règle métier : Afficher les trois prochaines dates futures, inscription et retours -->

**Réponse attendue :** Choix d’une action

<!-- Condition métier : Au moins une session future -->
1. [S’inscrire à une session](https://forms.cloud.microsoft/pages/responsepage.aspx?id=Cf5pfw3SOUOtLY5q0AbYj15YUUzJ44lEjv9UrEuppChURjEzQVlJWjdUMlFXODhXN1pPR0JGN1RDWCQlQCN0PWcu&route=shorturl)
2. [Voir un autre centre de la région](SCR_PASS_REGION_AUVERGNE)
3. [Trouver les centres proches de moi](SCR_PASS_INPUT_COMMUNE)
4. [Retour au module](SCR_PASS_MENU)

<!-- 2 session(s) future(s) dans la source -->

## SCR_PASS_CITY_SENS

### Sens (89)

<!-- Variables : {centre}=Sens; {region}=Bourgogne; {lien_forms} -->

<!-- Règle métier : Afficher les trois prochaines dates futures, inscription et retours -->

**Réponse attendue :** Choix d’une action

<!-- Condition métier : Au moins une session future -->
1. [S’inscrire à une session](https://forms.office.com/pages/responsepage.aspx?id=Cf5pfw3SOUOtLY5q0AbYj15YUUzJ44lEjv9UrEuppChUMU5BMzNJTE1ZVzJROEVXWkVTTEtTTjEzUyQlQCN0PWcu&route=shorturl)
2. [Voir un autre centre de la région](SCR_PASS_REGION_BOURGOGNE)
3. [Trouver les centres proches de moi](SCR_PASS_INPUT_COMMUNE)
4. [Retour au module](SCR_PASS_MENU)

<!-- 4 session(s) future(s) dans la source -->

## SCR_PASS_CITY_STRASBOURG

### Strasbourg (67)

<!-- Variables : {centre}=Strasbourg; {region}=Grand Est; {lien_forms} -->

<!-- Règle métier : Afficher les trois prochaines dates futures, inscription et retours -->

**Réponse attendue :** Choix d’une action

<!-- Condition métier : Au moins une session future -->
1. [S’inscrire à une session](https://forms.office.com/pages/responsepage.aspx?id=Cf5pfw3SOUOtLY5q0AbYj15YUUzJ44lEjv9UrEuppChUNlpSVzg1VkxHUlhNVDFBQTk4N0pNUkU1WCQlQCN0PWcu&route=shorturl)
2. [Voir un autre centre de la région](SCR_PASS_REGION_GRAND_EST)
3. [Trouver les centres proches de moi](SCR_PASS_INPUT_COMMUNE)
4. [Retour au module](SCR_PASS_MENU)

<!-- 6 session(s) future(s) dans la source -->

## SCR_PASS_CITY_TROYES

### Troyes (10)

<!-- Variables : {centre}=Troyes; {region}=Grand Est; {lien_forms} -->

<!-- Règle métier : Afficher les trois prochaines dates futures, inscription et retours -->

**Réponse attendue :** Choix d’une action

<!-- Condition métier : Au moins une session future -->
1. [S’inscrire à une session](https://forms.office.com/pages/responsepage.aspx?id=Cf5pfw3SOUOtLY5q0AbYj15YUUzJ44lEjv9UrEuppChUNlpSVzg1VkxHUlhNVDFBQTk4N0pNUkU1WCQlQCN0PWcu&route=shorturl)
2. [Voir un autre centre de la région](SCR_PASS_REGION_GRAND_EST)
3. [Trouver les centres proches de moi](SCR_PASS_INPUT_COMMUNE)
4. [Retour au module](SCR_PASS_MENU)

<!-- 6 session(s) future(s) dans la source -->

## SCR_PASS_CITY_VALSERHONE

### Valserhône (01)

<!-- Variables : {centre}=Valserhône; {region}=Rhône-Alpes; {lien_forms} -->

<!-- Règle métier : Afficher les trois prochaines dates futures, inscription et retours -->

**Réponse attendue :** Choix d’une action

<!-- Condition métier : Au moins une session future -->
1. [S’inscrire à une session](https://forms.office.com/pages/responsepage.aspx?id=Cf5pfw3SOUOtLY5q0AbYj15YUUzJ44lEjv9UrEuppChUMFVWWUZUWDBIV1FOT0xTTU5LTUdKVVlPQiQlQCN0PWcu&route=shorturl)
2. [Voir un autre centre de la région](SCR_PASS_REGION_RHONE_ALPES)
3. [Trouver les centres proches de moi](SCR_PASS_INPUT_COMMUNE)
4. [Retour au module](SCR_PASS_MENU)

<!-- 4 session(s) future(s) dans la source -->

## SCR_PASS_CITY_VICHY

### Vichy (03)

<!-- Variables : {centre}=Vichy; {region}=Auvergne; {lien_forms} -->

<!-- Règle métier : Afficher les trois prochaines dates futures, inscription et retours -->

**Réponse attendue :** Choix d’une action

<!-- Condition métier : Au moins une session future -->
1. [S’inscrire à une session](https://forms.cloud.microsoft/pages/responsepage.aspx?id=Cf5pfw3SOUOtLY5q0AbYj15YUUzJ44lEjv9UrEuppChURjEzQVlJWjdUMlFXODhXN1pPR0JGN1RDWCQlQCN0PWcu&route=shorturl)
2. [Voir un autre centre de la région](SCR_PASS_REGION_AUVERGNE)
3. [Trouver les centres proches de moi](SCR_PASS_INPUT_COMMUNE)
4. [Retour au module](SCR_PASS_MENU)

<!-- 4 session(s) future(s) dans la source -->

## SCR_PASS_INFO_MENU

### Informations sur l’examen

Choisissez l’information que vous souhaitez consulter.

1. [Pourquoi un examen civique ?](SCR_PASS_INFO_WHY)
2. [Suis-je concerné ?](SCR_PASS_INFO_CONCERNE)
3. [Quel examen correspond à ma situation ?](SCR_PASS_INFO_MATCH)
4. [Comment se présente l’examen ?](SCR_PASS_INFO_FORMAT)
5. [Les cinq thématiques](SCR_PASS_INFO_THEMES)
6. [Comment préparer l’examen ?](SCR_PASS_INFO_PREP)
7. [Comment le chatbot peut-il m’aider ?](SCR_PASS_INFO_HELP)
8. [À retenir](SCR_PASS_INFO_REMEMBER)
9. [Retour au module](SCR_PASS_MENU)

## SCR_PASS_INFO_HELP

### Comment le chatbot peut-il t’aider ?

Expliquer une notion, répondre à une question, comprendre une erreur, proposer un entraînement et orienter vers les ressources.

1. [Voir une autre information](SCR_PASS_INFO_MENU)
2. [Trouver une session](SCR_PASS_SEARCH_MENU)
3. [Retour au menu principal](MENU_PRINCIPAL)

## SCR_PASS_INFO_MATCH

### Quel examen correspond à ma situation ?

<!-- Variables : {type_examen} -->

CSP pour une première carte de séjour pluriannuelle ; CR pour une première carte de résident ; Naturalisation pour une demande de naturalisation.

1. [Voir une autre information](SCR_PASS_INFO_MENU)
2. [Trouver une session](SCR_PASS_SEARCH_MENU)
3. [Retour au menu principal](MENU_PRINCIPAL)

## SCR_PASS_INFO_FORMAT

### Comment se présente l’examen ?

40 QCM, 45 minutes, une seule bonne réponse parmi quatre ; réussite à partir de 32/40, soit 80 %.

1. [Voir une autre information](SCR_PASS_INFO_MENU)
2. [Trouver une session](SCR_PASS_SEARCH_MENU)
3. [Retour au menu principal](MENU_PRINCIPAL)

## SCR_PASS_INFO_REMEMBER

### À retenir

L’examen évalue les connaissances sur la France et la vie en société ; 40 questions ; seuil de réussite 80 %.

1. [Voir une autre information](SCR_PASS_INFO_MENU)
2. [Trouver une session](SCR_PASS_SEARCH_MENU)
3. [Retour au menu principal](MENU_PRINCIPAL)

## SCR_PASS_INFO_WHY

### Pourquoi un examen civique ?

Vérifier les connaissances sur les valeurs républicaines, les institutions, les droits et devoirs, l’histoire, la géographie, la culture et la vie en société.

1. [Voir une autre information](SCR_PASS_INFO_MENU)
2. [Trouver une session](SCR_PASS_SEARCH_MENU)
3. [Retour au menu principal](MENU_PRINCIPAL)

## SCR_PASS_INFO_PREP

### Comment préparer l’examen ?

Réviser les cinq thèmes, consulter le glossaire, s’entraîner, revoir ses erreurs et utiliser les ressources NovaFrate.

1. [Voir une autre information](SCR_PASS_INFO_MENU)
2. [Trouver une session](SCR_PASS_SEARCH_MENU)
3. [Retour au menu principal](MENU_PRINCIPAL)

## SCR_PASS_INFO_CONCERNE

### Suis-je concerné ?

Première carte de séjour pluriannuelle, première carte de résident ou demande de naturalisation.

1. [Voir une autre information](SCR_PASS_INFO_MENU)
2. [Trouver une session](SCR_PASS_SEARCH_MENU)
3. [Retour au menu principal](MENU_PRINCIPAL)

## SCR_PASS_INFO_THEMES

### Les cinq thématiques

Principes et valeurs ; institutions ; droits et devoirs ; histoire, géographie et culture ; vivre dans la société française.

1. [Voir une autre information](SCR_PASS_INFO_MENU)
2. [Trouver une session](SCR_PASS_SEARCH_MENU)
3. [Retour au menu principal](MENU_PRINCIPAL)

## SCR_PASS_REGISTER

### S’inscrire à l’examen

<!-- Variables : {centre}; {region}; {lien_forms} -->

Cliquez sur le lien Forms pour vous inscrire à une session dans la région choisie.

## SCR_PASS_REGIONS

### Choisir une région

<!-- Variables : {region} -->

<!-- Liste dynamique : LISTE_REGIONS. Les choix sont générés depuis 99_NAVIGATION. -->

1. [Auvergne](SCR_PASS_REGION_AUVERGNE)
2. [Bourgogne](SCR_PASS_REGION_BOURGOGNE)
3. [Cher](SCR_PASS_REGION_CHER)
4. [Franche-Comté](SCR_PASS_REGION_FRANCHE_COMTE)
5. [Grand Est](SCR_PASS_REGION_GRAND_EST)
6. [Rhône-Alpes](SCR_PASS_REGION_RHONE_ALPES)
7. [Rechercher depuis ma commune](SCR_PASS_INPUT_COMMUNE)
8. [Retour au module](SCR_PASS_MENU)

## SCR_PASS_MENU

### Je passe mon examen

Que souhaitez-vous faire ? Consultez les informations pratiques, recherchez une session ou inscrivez-vous à l’examen.

1. [Toutes les informations sur l’examen](SCR_PASS_INFO_MENU)
2. [Trouver une session d’examen](SCR_PASS_SEARCH_MENU)
3. [M’inscrire à l’examen](SCR_PASS_REGIONS)
4. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran d’entrée -->

## SCR_PASS_SEARCH_MENU

### Trouver une session

<!-- Variables : {mode_recherche} -->

Comment souhaitez-vous rechercher une session : région, ville, commune, code postal, département ou adresse ?

1. [Rechercher par région](SCR_PASS_REGIONS)
2. [Rechercher une ville FRATE](SCR_PASS_INPUT_CITY)
3. [Trouver les centres proches de ma commune](SCR_PASS_INPUT_COMMUNE)
4. [Rechercher par code postal](SCR_PASS_INPUT_CP)
5. [Rechercher par département](SCR_PASS_INPUT_DEPT)
6. [Rechercher depuis une adresse](SCR_PASS_INPUT_ADDRESS)
7. [Retour au module](SCR_PASS_MENU)

## SCR_PASS_INPUT_ADDRESS

### Indiquez votre adresse

<!-- Variables : {mode_recherche}=ADRESSE; {saisie_utilisateur} -->

Indiquez votre {mode_recherche}. Exemple : Strasbourg, 67000 ou Lons-le-Saunier.

<!-- Condition métier : Saisie non vide -->
1. [Valider ma recherche](SCR_PASS_BAN_RESOLVE)
2. [Changer de mode de recherche](SCR_PASS_SEARCH_MENU)
3. [Retour au module](SCR_PASS_MENU)

## SCR_PASS_NO_SESSION

### Aucune session disponible

<!-- Variables : {centre}; {centre_alternatif} -->

Aucune session future n’est publiée dans ce centre. Je vous propose le centre suivant le plus proche.

<!-- Condition métier : Centre alternatif disponible -->
1. [Voir le centre alternatif](SCR_PASS_CITY_*)
2. [Nouvelle recherche](SCR_PASS_SEARCH_MENU)
3. [Retour au module](SCR_PASS_MENU)

## SCR_PASS_INPUT_CP

### Indiquez votre code postal

<!-- Variables : {mode_recherche}=CP; {saisie_utilisateur} -->

Indiquez votre {mode_recherche}. Exemple : Strasbourg, 67000 ou Lons-le-Saunier.

<!-- Condition métier : Saisie non vide -->
1. [Valider ma recherche](SCR_PASS_BAN_RESOLVE)
2. [Changer de mode de recherche](SCR_PASS_SEARCH_MENU)
3. [Retour au module](SCR_PASS_MENU)

## SCR_PASS_INPUT_COMMUNE

### Indiquez votre commune

<!-- Variables : {mode_recherche}=COMMUNE; {saisie_utilisateur} -->

Indiquez votre {mode_recherche}. Exemple : Strasbourg, 67000 ou Lons-le-Saunier.

<!-- Condition métier : Saisie non vide -->
1. [Valider ma recherche](SCR_PASS_BAN_RESOLVE)
2. [Changer de mode de recherche](SCR_PASS_SEARCH_MENU)
3. [Retour au module](SCR_PASS_MENU)

## SCR_PASS_DISTANCE

### Calcul des distances

<!-- Variables : {distances_centres}; {centre_1}; {centre_2}; {centre_3} -->

<!-- Règle métier : Classer les centres FRATE par distance croissante -->

<!-- Transition automatique NAV_PASS_068 : Calcul terminé → SCR_PASS_RESULTS_NEAR -->
1. [Afficher les résultats](SCR_PASS_RESULTS_NEAR)

<!-- Écran logique non affiché -->

## SCR_PASS_INPUT_DEPT

### Indiquez votre département

<!-- Variables : {mode_recherche}=DEPARTEMENT; {saisie_utilisateur} -->

Indiquez votre {mode_recherche}. Exemple : Strasbourg, 67000 ou Lons-le-Saunier.

<!-- Condition métier : Saisie non vide -->
1. [Valider ma recherche](SCR_PASS_BAN_RESOLVE)
2. [Changer de mode de recherche](SCR_PASS_SEARCH_MENU)
3. [Retour au module](SCR_PASS_MENU)

## SCR_PASS_NO_RESULT

### Lieu non trouvé

<!-- Variables : {saisie_utilisateur} -->

Je n’ai pas trouvé ce lieu. Vérifiez l’orthographe ou saisissez un code postal.

1. [Réessayer](SCR_PASS_SEARCH_MENU)
2. [Retour au module](SCR_PASS_MENU)

## SCR_PASS_BAN_CHOICE

### Précisez votre localisation

<!-- Variables : {ban_resultats}; {ban_choix} -->

Plusieurs lieux correspondent. Choisissez la proposition qui correspond à votre commune.

<!-- Condition métier : Réponse sélectionnée | Valeur : BAN_RESULT_* -->
1. [Utiliser ce lieu](SCR_PASS_DISTANCE)
2. [Recommencer la recherche](SCR_PASS_SEARCH_MENU)

## SCR_PASS_BAN_RESOLVE

### Recherche de la localisation

<!-- Variables : {ban_resultats}; {latitude_utilisateur}; {longitude_utilisateur} -->

<!-- Règle métier : Résoudre la saisie et compter les résultats pertinents -->

<!-- Transition automatique NAV_PASS_061 : 1 résultat pertinent → SCR_PASS_DISTANCE -->
1. [Résultat unique](SCR_PASS_DISTANCE)
<!-- Transition automatique NAV_PASS_062 : Plusieurs résultats pertinents → SCR_PASS_BAN_CHOICE -->
1. [Plusieurs résultats](SCR_PASS_BAN_CHOICE)
<!-- Transition automatique NAV_PASS_063 : 0 résultat pertinent → SCR_PASS_NO_RESULT -->
1. [Aucun résultat](SCR_PASS_NO_RESULT)

<!-- Écran logique non affiché -->

## SCR_PASS_RESULTS_NEAR

### Centres les plus proches

<!-- Variables : {lieu_utilisateur}; {centre_1}; {centre_2}; {centre_3} -->

Voici les trois centres FRATE les plus proches de {lieu_utilisateur}.

<!-- Condition métier : Centre disponible | Valeur : CENTRE_1 -->
1. [Voir le centre 1](SCR_PASS_CITY_*)
<!-- Condition métier : Centre disponible | Valeur : CENTRE_2 -->
2. [Voir le centre 2](SCR_PASS_CITY_*)
<!-- Condition métier : Centre disponible | Valeur : CENTRE_3 -->
3. [Voir le centre 3](SCR_PASS_CITY_*)
4. [Nouvelle recherche](SCR_PASS_SEARCH_MENU)
5. [Retour au module](SCR_PASS_MENU)

## SCR_PASS_INPUT_CITY

### Rechercher une ville FRATE

<!-- Variables : {mode_recherche}=VILLE; {saisie_utilisateur} -->

Indiquez votre {mode_recherche}. Exemple : Strasbourg, 67000 ou Lons-le-Saunier.

<!-- Transition automatique NAV_PASS_046 : Saisie validée → SCR_PASS_BAN_RESOLVE -->
1. [Rechercher la ville](SCR_PASS_BAN_RESOLVE)
1. [Changer de mode de recherche](SCR_PASS_SEARCH_MENU)
2. [Retour au module](SCR_PASS_MENU)

## SCR_PASS_REGION_AUVERGNE

### Auvergne

<!-- Variables : {region}=Auvergne -->

<!-- Règle métier : Afficher les 4 centres de la région -->

**Réponse attendue :** Choix d’un centre

1. [Clermont-Ferrand (63)](SCR_PASS_CITY_CLERMONT_FERRAND)
2. [Le Puy-en-Velay (43)](SCR_PASS_CITY_LE_PUY_EN_VELAY)
3. [Saint-Flour (15)](SCR_PASS_CITY_SAINT_FLOUR)
4. [Vichy (03)](SCR_PASS_CITY_VICHY)
5. [Choisir une autre région](SCR_PASS_REGIONS)
6. [Retour au module](SCR_PASS_MENU)

## SCR_PASS_REGION_BOURGOGNE

### Bourgogne

<!-- Variables : {region}=Bourgogne -->

<!-- Règle métier : Afficher les 6 centres de la région -->

**Réponse attendue :** Choix d’un centre

1. [Auxerre (89)](SCR_PASS_CITY_AUXERRE)
2. [Dijon (21)](SCR_PASS_CITY_DIJON)
3. [Mâcon (71)](SCR_PASS_CITY_MACON)
4. [Montceau-les-Mines (71)](SCR_PASS_CITY_MONTCEAU_LES_MINES)
5. [Nevers (58)](SCR_PASS_CITY_NEVERS)
6. [Sens (89)](SCR_PASS_CITY_SENS)
7. [Choisir une autre région](SCR_PASS_REGIONS)
8. [Retour au module](SCR_PASS_MENU)

## SCR_PASS_REGION_CHER

### Cher

<!-- Variables : {region}=Cher -->

<!-- Règle métier : Afficher les 1 centres de la région -->

**Réponse attendue :** Choix d’un centre

1. [Bourges (18)](SCR_PASS_CITY_BOURGES)
2. [Choisir une autre région](SCR_PASS_REGIONS)
3. [Retour au module](SCR_PASS_MENU)

## SCR_PASS_REGION_FRANCHE_COMTE

### Franche-Comté

<!-- Variables : {region}=Franche-Comté -->

<!-- Règle métier : Afficher les 3 centres de la région -->

**Réponse attendue :** Choix d’un centre

1. [Besançon (25)](SCR_PASS_CITY_BESANCON)
2. [Lons-le-Saunier (39)](SCR_PASS_CITY_LONS_LE_SAUNIER)
3. [Montbéliard (25)](SCR_PASS_CITY_MONTBELIARD)
4. [Choisir une autre région](SCR_PASS_REGIONS)
5. [Retour au module](SCR_PASS_MENU)

## SCR_PASS_REGION_GRAND_EST

### Grand Est

<!-- Variables : {region}=Grand Est -->

<!-- Règle métier : Afficher les 6 centres de la région -->

**Réponse attendue :** Choix d’un centre

1. [Chaumont (52)](SCR_PASS_CITY_CHAUMONT)
2. [Mulhouse (68)](SCR_PASS_CITY_MULHOUSE)
3. [Reims (51)](SCR_PASS_CITY_REIMS)
4. [Saint-Dié-des-Vosges (88)](SCR_PASS_CITY_SAINT_DIE_DES_VOSGES)
5. [Strasbourg (67)](SCR_PASS_CITY_STRASBOURG)
6. [Troyes (10)](SCR_PASS_CITY_TROYES)
7. [Choisir une autre région](SCR_PASS_REGIONS)
8. [Retour au module](SCR_PASS_MENU)

## SCR_PASS_REGION_RHONE_ALPES

### Rhône-Alpes

<!-- Variables : {region}=Rhône-Alpes -->

<!-- Règle métier : Afficher les 4 centres de la région -->

**Réponse attendue :** Choix d’un centre

1. [Annemasse (74)](SCR_PASS_CITY_ANNEMASSE)
2. [Annecy (74)](SCR_PASS_CITY_ANNECY)
3. [Bourg-en-Bresse (01)](SCR_PASS_CITY_BOURG_EN_BRESSE)
4. [Valserhône (01)](SCR_PASS_CITY_VALSERHONE)
5. [Choisir une autre région](SCR_PASS_REGIONS)
6. [Retour au module](SCR_PASS_MENU)

<!-- Fin du fichier source : modules\07_passer_examen.md -->

<!-- Début du fichier source : modules\05_preparer_examen.md -->

<!-- Module généré automatiquement : Préparer examen -->
<!-- Date : 2026-08-03T13:13:33+02:00 -->

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

<!-- Fin du fichier source : modules\05_preparer_examen.md -->

<!-- Début du fichier source : modules\10_question_libre.md -->

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

<!-- Fin du fichier source : modules\10_question_libre.md -->

<!-- Début du fichier source : modules\03_revisions.md -->

<!-- Module généré automatiquement : Révisions -->
<!-- Date : 2026-08-03T13:13:33+02:00 -->

## SCR_REV_MENU

### Révisions

Choisissez une thématique pour commencer ou poursuivre vos révisions.

<!-- Condition métier : Thématique active | Valeur : T1 -->
1. [Principes et valeurs de la République](SCR_REV_T1_MENU)
<!-- Condition métier : Thématique active | Valeur : T2 -->
2. [Système institutionnel et politique](SCR_REV_T2_MENU)
<!-- Condition métier : Thématique active | Valeur : T3 -->
3. [Droits et devoirs](SCR_REV_T3_MENU)
<!-- Condition métier : Thématique active | Valeur : T4 -->
4. [Histoire, géographie et culture](SCR_REV_T4_MENU)
<!-- Condition métier : Thématique active | Valeur : T5 -->
5. [Vivre dans la société française](SCR_REV_T5_MENU)
6. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Écran d’entrée depuis le menu principal -->

## SCR_REV_T1_MENU

### PRINCIPES ET VALEURS DE LA RÉPUBLIQUE 🇫🇷

<!-- Variables : {id_theme}=T1; {titre_theme} -->

### Objectif general

L'objectif de cette thématique est de permettre à l'apprenant de comprendre les principes fondamentaux de la République française, ses valeurs, ses symboles et les règles communes qui permettent de vivre ensemble.
À la fin de cette thématique, l'apprenant sera capable de :
• expliquer ce qu'est une République ;
• connaître les valeurs fondamentales de la République française ;
• comprendre la devise Liberté, Égalité, Fraternité ;
• identifier les symboles républicains ;
• expliquer le principe de laïcité ;
• connaître la place de la langue française ;
• comprendre le contrat d'engagement à respecter les principes de la République.

<!-- Condition métier : Chapitre actif | Valeur : T1_CH01 -->
1. [Connaître et comprendre la République](SCR_REV_T1_CH01_ACC)
<!-- Condition métier : Chapitre actif | Valeur : T1_CH02 -->
2. [La devise de la République française](SCR_REV_T1_CH02_ACC)
<!-- Condition métier : Chapitre actif | Valeur : T1_CH03 -->
3. [Les symboles de la République française](SCR_REV_T1_CH03_ACC)
<!-- Condition métier : Chapitre actif | Valeur : T1_CH04 -->
4. [La laïcité](SCR_REV_T1_CH04_ACC)
<!-- Condition métier : Chapitre actif | Valeur : T1_CH05 -->
5. [La langue de la République](SCR_REV_T1_CH05_ACC)
<!-- Condition métier : Chapitre actif | Valeur : T1_CH06 -->
6. [Le contrat d'engagement à respecter les principes de la République](SCR_REV_T1_CH06_ACC)
7. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source thématique : COURS/THEMATIQUE 1/THEMATIQUE_1_PRINCIPES_VALEURS.md -->

## SCR_REV_T1_CH01_ACC

### CONNAÎTRE ET COMPRENDRE LA RÉPUBLIQUE 🇫🇷

<!-- Variables : {id_theme}=T1; {id_chapitre}=T1_CH01; {ordre_chapitre}=1; {dernier_chapitre_theme}=Non -->

La compréhension de la République française est une base essentielle de l'examen civique.
Elle permet de comprendre :
• comment fonctionne la France ;
• qui détient le pouvoir ;
• quels sont les grands principes qui organisent la société française.

<!-- Condition métier : Objectifs disponibles -->
1. [Découvrir les objectifs](SCR_REV_T1_CH01_OBJ)
<!-- Condition métier : Objectifs absents -->
2. [Commencer le cours](SCR_REV_T1_CH01_COURS)
3. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Chapitre T1_CH01 — source : COURS/THEMATIQUE 1/Chapitre 1/CHAPITRE_1_VALEURS_REPUBLIQUE.md -->

## SCR_REV_T1_CH01_OBJ

### Objectifs du chapitre

<!-- Variables : {id_theme}=T1; {id_chapitre}=T1_CH01; {ordre_chapitre}=1; {dernier_chapitre_theme}=Non -->

À la fin de ce chapitre, tu seras capable de :
• définir ce qu'est une République ;
• comprendre le rôle du peuple dans la démocratie française ;
• expliquer le principe de souveraineté nationale ;
• connaître les quatre principes fondamentaux de la République française ;
• identifier les notions importantes attendues à l'examen civique.

1. [Commencer le cours](SCR_REV_T1_CH01_COURS)

<!-- Chapitre T1_CH01 — source : COURS/THEMATIQUE 1/Chapitre 1/CHAPITRE_1_VALEURS_REPUBLIQUE.md -->

## SCR_REV_T1_CH01_COURS

### CONNAÎTRE ET COMPRENDRE LA RÉPUBLIQUE 🇫🇷

<!-- Variables : {id_theme}=T1; {id_chapitre}=T1_CH01; {ordre_chapitre}=1; {dernier_chapitre_theme}=Non -->

<!-- Source Markdown attendue : COURS/THEMATIQUE 1/Chapitre 1/CHAPITRE_1_VALEURS_REPUBLIQUE.md. Utiliser --content-root pour l'intégrer. -->

<!-- Condition métier : Synthèse disponible -->
1. [Voir la synthèse](SCR_REV_T1_CH01_SYN)
<!-- Condition métier : Synthèse absente ET vigilance disponible -->
2. [Voir les points de vigilance](SCR_REV_T1_CH01_VIG)
<!-- Condition métier : Synthèse et vigilance absentes ET glossaire disponible -->
3. [Consulter les notions utiles](SCR_REV_T1_CH01_GLO)
<!-- Condition métier : Aucun bloc complémentaire disponible -->
4. [Terminer le chapitre](SCR_REV_T1_CH01_FIN)

<!-- Chapitre T1_CH01 — source : COURS/THEMATIQUE 1/Chapitre 1/CHAPITRE_1_VALEURS_REPUBLIQUE.md -->

## SCR_REV_T1_CH01_SYN

### À retenir

<!-- Variables : {id_theme}=T1; {id_chapitre}=T1_CH01; {ordre_chapitre}=1; {dernier_chapitre_theme}=Non -->

Une République est un mode d'organisation politique dans lequel le pouvoir appartient au peuple et est exercé selon des règles définies par une Constitution.

<!-- Condition métier : Vigilance disponible -->
1. [Voir les points de vigilance](SCR_REV_T1_CH01_VIG)
<!-- Condition métier : Vigilance absente ET glossaire disponible -->
2. [Consulter les notions utiles](SCR_REV_T1_CH01_GLO)
<!-- Condition métier : Vigilance et glossaire absents -->
3. [Terminer le chapitre](SCR_REV_T1_CH01_FIN)

<!-- Chapitre T1_CH01 — source : COURS/THEMATIQUE 1/Chapitre 1/CHAPITRE_1_VALEURS_REPUBLIQUE.md -->

## SCR_REV_T1_CH01_VIG

### Points de vigilance

<!-- Variables : {id_theme}=T1; {id_chapitre}=T1_CH01; {ordre_chapitre}=1; {dernier_chapitre_theme}=Non -->

<!-- Ce bloc n'est pas renseigné dans le moteur Excel pour T1_CH01:VIGILANCE. -->

<!-- Condition métier : Glossaire disponible -->
1. [Consulter les notions utiles](SCR_REV_T1_CH01_GLO)
<!-- Condition métier : Glossaire absent -->
2. [Terminer le chapitre](SCR_REV_T1_CH01_FIN)

<!-- Chapitre T1_CH01 — source : COURS/THEMATIQUE 1/Chapitre 1/CHAPITRE_1_VALEURS_REPUBLIQUE.md -->

## SCR_REV_T1_CH01_GLO

### Notions utiles

<!-- Variables : {id_theme}=T1; {id_chapitre}=T1_CH01; {ordre_chapitre}=1; {dernier_chapitre_theme}=Non -->

La souveraineté nationale appartient au peuple.
Le peuple l'exerce :
• par ses représentants ;
• par référendum.

1. [Terminer le chapitre](SCR_REV_T1_CH01_FIN)

<!-- Chapitre T1_CH01 — source : COURS/THEMATIQUE 1/Chapitre 1/CHAPITRE_1_VALEURS_REPUBLIQUE.md -->

## SCR_REV_T1_CH01_FIN

### Chapitre terminé

<!-- Variables : {id_theme}=T1; {id_chapitre}=T1_CH01; {ordre_chapitre}=1; {dernier_chapitre_theme}=Non -->

Vous pouvez passer au chapitre suivant ou revenir au menu principal.

1. [Chapitre suivant](SCR_REV_T1_CH02_ACC)
2. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Chapitre T1_CH01 — source : COURS/THEMATIQUE 1/Chapitre 1/CHAPITRE_1_VALEURS_REPUBLIQUE.md -->

## SCR_REV_T1_CH02_ACC

### LA DEVISE DE LA RÉPUBLIQUE FRANÇAISE

<!-- Variables : {id_theme}=T1; {id_chapitre}=T1_CH02; {ordre_chapitre}=2; {dernier_chapitre_theme}=Non -->

<!-- Ce bloc n'est pas renseigné dans le moteur Excel pour T1_CH02:INTRO. -->

<!-- Condition métier : Objectifs disponibles -->
1. [Découvrir les objectifs](SCR_REV_T1_CH02_OBJ)
<!-- Condition métier : Objectifs absents -->
2. [Commencer le cours](SCR_REV_T1_CH02_COURS)
3. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Chapitre T1_CH02 — source : COURS/THEMATIQUE 1/Chapitre 2/CHAPITRE_2_DEVISE_REPUBLIQUE.md -->

## SCR_REV_T1_CH02_OBJ

### Objectifs du chapitre

<!-- Variables : {id_theme}=T1; {id_chapitre}=T1_CH02; {ordre_chapitre}=2; {dernier_chapitre_theme}=Non -->

À la fin de ce chapitre, tu seras capable de :
• citer la devise officielle de la République française ;
• expliquer la signification de chaque valeur ;
• comprendre comment ces valeurs s'appliquent dans la vie quotidienne ;
• identifier des situations concrètes illustrant la liberté, l'égalité et la fraternité.

1. [Commencer le cours](SCR_REV_T1_CH02_COURS)

<!-- Chapitre T1_CH02 — source : COURS/THEMATIQUE 1/Chapitre 2/CHAPITRE_2_DEVISE_REPUBLIQUE.md -->

## SCR_REV_T1_CH02_COURS

### LA DEVISE DE LA RÉPUBLIQUE FRANÇAISE

<!-- Variables : {id_theme}=T1; {id_chapitre}=T1_CH02; {ordre_chapitre}=2; {dernier_chapitre_theme}=Non -->

<!-- Source Markdown attendue : COURS/THEMATIQUE 1/Chapitre 2/CHAPITRE_2_DEVISE_REPUBLIQUE.md. Utiliser --content-root pour l'intégrer. -->

<!-- Condition métier : Synthèse disponible -->
1. [Voir la synthèse](SCR_REV_T1_CH02_SYN)
<!-- Condition métier : Synthèse absente ET vigilance disponible -->
2. [Voir les points de vigilance](SCR_REV_T1_CH02_VIG)
<!-- Condition métier : Synthèse et vigilance absentes ET glossaire disponible -->
3. [Consulter les notions utiles](SCR_REV_T1_CH02_GLO)
<!-- Condition métier : Aucun bloc complémentaire disponible -->
4. [Terminer le chapitre](SCR_REV_T1_CH02_FIN)

<!-- Chapitre T1_CH02 — source : COURS/THEMATIQUE 1/Chapitre 2/CHAPITRE_2_DEVISE_REPUBLIQUE.md -->

## SCR_REV_T1_CH02_SYN

### À retenir

<!-- Variables : {id_theme}=T1; {id_chapitre}=T1_CH02; {ordre_chapitre}=2; {dernier_chapitre_theme}=Non -->

La devise officielle de la République française est :
Liberté – Égalité – Fraternité
Elle exprime les trois grandes valeurs qui fondent la République française et guident la vie en société.

<!-- Condition métier : Vigilance disponible -->
1. [Voir les points de vigilance](SCR_REV_T1_CH02_VIG)
<!-- Condition métier : Vigilance absente ET glossaire disponible -->
2. [Consulter les notions utiles](SCR_REV_T1_CH02_GLO)
<!-- Condition métier : Vigilance et glossaire absents -->
3. [Terminer le chapitre](SCR_REV_T1_CH02_FIN)

<!-- Chapitre T1_CH02 — source : COURS/THEMATIQUE 1/Chapitre 2/CHAPITRE_2_DEVISE_REPUBLIQUE.md -->

## SCR_REV_T1_CH02_VIG

### Points de vigilance

<!-- Variables : {id_theme}=T1; {id_chapitre}=T1_CH02; {ordre_chapitre}=2; {dernier_chapitre_theme}=Non -->

❌ Liberté = faire tout ce que l'on veut.
✅ Faux : la liberté est encadrée par la loi.
❌ Égalité = tout le monde reçoit exactement la même chose.
✅ Faux : chacun possède les mêmes droits, mais certaines adaptations peuvent être prévues selon les situations.
❌ Fraternité = seulement aider les autres.
✅ Faux : la fraternité comprend également le respect, la solidarité et l'engagement citoyen.

<!-- Condition métier : Glossaire disponible -->
1. [Consulter les notions utiles](SCR_REV_T1_CH02_GLO)
<!-- Condition métier : Glossaire absent -->
2. [Terminer le chapitre](SCR_REV_T1_CH02_FIN)

<!-- Chapitre T1_CH02 — source : COURS/THEMATIQUE 1/Chapitre 2/CHAPITRE_2_DEVISE_REPUBLIQUE.md -->

## SCR_REV_T1_CH02_GLO

### Notions utiles

<!-- Variables : {id_theme}=T1; {id_chapitre}=T1_CH02; {ordre_chapitre}=2; {dernier_chapitre_theme}=Non -->

La liberté est un droit fondamental, mais elle doit toujours respecter la loi et les droits des autres.

1. [Terminer le chapitre](SCR_REV_T1_CH02_FIN)

<!-- Chapitre T1_CH02 — source : COURS/THEMATIQUE 1/Chapitre 2/CHAPITRE_2_DEVISE_REPUBLIQUE.md -->

## SCR_REV_T1_CH02_FIN

### Chapitre terminé

<!-- Variables : {id_theme}=T1; {id_chapitre}=T1_CH02; {ordre_chapitre}=2; {dernier_chapitre_theme}=Non -->

Vous pouvez passer au chapitre suivant ou revenir au menu principal.

1. [Chapitre suivant](SCR_REV_T1_CH03_ACC)
2. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Chapitre T1_CH02 — source : COURS/THEMATIQUE 1/Chapitre 2/CHAPITRE_2_DEVISE_REPUBLIQUE.md -->

## SCR_REV_T1_CH03_ACC

### LES SYMBOLES DE LA RÉPUBLIQUE FRANÇAISE

<!-- Variables : {id_theme}=T1; {id_chapitre}=T1_CH03; {ordre_chapitre}=3; {dernier_chapitre_theme}=Non -->

<!-- Ce bloc n'est pas renseigné dans le moteur Excel pour T1_CH03:INTRO. -->

<!-- Condition métier : Objectifs disponibles -->
1. [Découvrir les objectifs](SCR_REV_T1_CH03_OBJ)
<!-- Condition métier : Objectifs absents -->
2. [Commencer le cours](SCR_REV_T1_CH03_COURS)
3. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Chapitre T1_CH03 — source : COURS/THEMATIQUE 1/Chapitre 3/CHAPITRE_3_SYMBOLES_REPUBLIQUE.md -->

## SCR_REV_T1_CH03_OBJ

### Objectifs du chapitre

<!-- Variables : {id_theme}=T1; {id_chapitre}=T1_CH03; {ordre_chapitre}=3; {dernier_chapitre_theme}=Non -->

À la fin de ce chapitre, tu seras capable de :
• identifier les symboles officiels de la République française ;
• expliquer leur origine et leur signification ;
• reconnaître les situations où ils sont utilisés ;
• distinguer les symboles officiels des symboles nationaux non officiels.

1. [Commencer le cours](SCR_REV_T1_CH03_COURS)

<!-- Chapitre T1_CH03 — source : COURS/THEMATIQUE 1/Chapitre 3/CHAPITRE_3_SYMBOLES_REPUBLIQUE.md -->

## SCR_REV_T1_CH03_COURS

### LES SYMBOLES DE LA RÉPUBLIQUE FRANÇAISE

<!-- Variables : {id_theme}=T1; {id_chapitre}=T1_CH03; {ordre_chapitre}=3; {dernier_chapitre_theme}=Non -->

<!-- Source Markdown attendue : COURS/THEMATIQUE 1/Chapitre 3/CHAPITRE_3_SYMBOLES_REPUBLIQUE.md. Utiliser --content-root pour l'intégrer. -->

<!-- Condition métier : Synthèse disponible -->
1. [Voir la synthèse](SCR_REV_T1_CH03_SYN)
<!-- Condition métier : Synthèse absente ET vigilance disponible -->
2. [Voir les points de vigilance](SCR_REV_T1_CH03_VIG)
<!-- Condition métier : Synthèse et vigilance absentes ET glossaire disponible -->
3. [Consulter les notions utiles](SCR_REV_T1_CH03_GLO)
<!-- Condition métier : Aucun bloc complémentaire disponible -->
4. [Terminer le chapitre](SCR_REV_T1_CH03_FIN)

<!-- Chapitre T1_CH03 — source : COURS/THEMATIQUE 1/Chapitre 3/CHAPITRE_3_SYMBOLES_REPUBLIQUE.md -->

## SCR_REV_T1_CH03_SYN

### À retenir

<!-- Variables : {id_theme}=T1; {id_chapitre}=T1_CH03; {ordre_chapitre}=3; {dernier_chapitre_theme}=Non -->

Les symboles de la République représentent les valeurs, l'histoire et l'identité de la France.
Ils permettent à tous les citoyens de partager des repères communs.
Les principaux symboles sont :
• 🇫🇷 le drapeau tricolore ;
• 🎵 la Marseillaise ;
• 👩 Marianne ;
• 🎉 la fête nationale du 14 juillet ;
• 📜 la devise « Liberté, Égalité, Fraternité ».

<!-- Condition métier : Vigilance disponible -->
1. [Voir les points de vigilance](SCR_REV_T1_CH03_VIG)
<!-- Condition métier : Vigilance absente ET glossaire disponible -->
2. [Consulter les notions utiles](SCR_REV_T1_CH03_GLO)
<!-- Condition métier : Vigilance et glossaire absents -->
3. [Terminer le chapitre](SCR_REV_T1_CH03_FIN)

<!-- Chapitre T1_CH03 — source : COURS/THEMATIQUE 1/Chapitre 3/CHAPITRE_3_SYMBOLES_REPUBLIQUE.md -->

## SCR_REV_T1_CH03_VIG

### Points de vigilance

<!-- Variables : {id_theme}=T1; {id_chapitre}=T1_CH03; {ordre_chapitre}=3; {dernier_chapitre_theme}=Non -->

❌ Les bandes du drapeau sont horizontales.
✅ Faux.
Les bandes sont verticales.
❌ La Marseillaise est la devise française.
✅ Faux.
La Marseillaise est l'hymne national.
❌ Marianne est un personnage historique.
✅ Faux.
Marianne est une représentation symbolique de la République.
❌ Le coq est un symbole officiel de la République.
✅ Faux.
Le coq est un symbole national, mais il n'est pas un symbole officiel inscrit dans la Constitution.

<!-- Condition métier : Glossaire disponible -->
1. [Consulter les notions utiles](SCR_REV_T1_CH03_GLO)
<!-- Condition métier : Glossaire absent -->
2. [Terminer le chapitre](SCR_REV_T1_CH03_FIN)

<!-- Chapitre T1_CH03 — source : COURS/THEMATIQUE 1/Chapitre 3/CHAPITRE_3_SYMBOLES_REPUBLIQUE.md -->

## SCR_REV_T1_CH03_GLO

### Notions utiles

<!-- Variables : {id_theme}=T1; {id_chapitre}=T1_CH03; {ordre_chapitre}=3; {dernier_chapitre_theme}=Non -->

Le drapeau français comporte trois bandes verticales :
Bleu – Blanc – Rouge

1. [Terminer le chapitre](SCR_REV_T1_CH03_FIN)

<!-- Chapitre T1_CH03 — source : COURS/THEMATIQUE 1/Chapitre 3/CHAPITRE_3_SYMBOLES_REPUBLIQUE.md -->

## SCR_REV_T1_CH03_FIN

### Chapitre terminé

<!-- Variables : {id_theme}=T1; {id_chapitre}=T1_CH03; {ordre_chapitre}=3; {dernier_chapitre_theme}=Non -->

Vous pouvez passer au chapitre suivant ou revenir au menu principal.

1. [Chapitre suivant](SCR_REV_T1_CH04_ACC)
2. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Chapitre T1_CH03 — source : COURS/THEMATIQUE 1/Chapitre 3/CHAPITRE_3_SYMBOLES_REPUBLIQUE.md -->

## SCR_REV_T1_CH04_ACC

### LA LAÏCITÉ

<!-- Variables : {id_theme}=T1; {id_chapitre}=T1_CH04; {ordre_chapitre}=4; {dernier_chapitre_theme}=Non -->

<!-- Ce bloc n'est pas renseigné dans le moteur Excel pour T1_CH04:INTRO. -->

<!-- Condition métier : Objectifs disponibles -->
1. [Découvrir les objectifs](SCR_REV_T1_CH04_OBJ)
<!-- Condition métier : Objectifs absents -->
2. [Commencer le cours](SCR_REV_T1_CH04_COURS)
3. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Chapitre T1_CH04 — source : COURS/THEMATIQUE 1/Chapitre 4/CHAPITRE_4_LA#U00cfCITE.md -->

## SCR_REV_T1_CH04_OBJ

### Objectifs du chapitre

<!-- Variables : {id_theme}=T1; {id_chapitre}=T1_CH04; {ordre_chapitre}=4; {dernier_chapitre_theme}=Non -->

À la fin de ce chapitre, tu seras capable de :
• définir le principe de laïcité ;
• comprendre les relations entre l'État et les religions ;
• distinguer les droits et les obligations liés à la laïcité ;
• analyser des situations concrètes en appliquant les règles de la République.

1. [Commencer le cours](SCR_REV_T1_CH04_COURS)

<!-- Chapitre T1_CH04 — source : COURS/THEMATIQUE 1/Chapitre 4/CHAPITRE_4_LA#U00cfCITE.md -->

## SCR_REV_T1_CH04_COURS

### LA LAÏCITÉ

<!-- Variables : {id_theme}=T1; {id_chapitre}=T1_CH04; {ordre_chapitre}=4; {dernier_chapitre_theme}=Non -->

<!-- Source Markdown attendue : COURS/THEMATIQUE 1/Chapitre 4/CHAPITRE_4_LA#U00cfCITE.md. Utiliser --content-root pour l'intégrer. -->

<!-- Condition métier : Synthèse disponible -->
1. [Voir la synthèse](SCR_REV_T1_CH04_SYN)
<!-- Condition métier : Synthèse absente ET vigilance disponible -->
2. [Voir les points de vigilance](SCR_REV_T1_CH04_VIG)
<!-- Condition métier : Synthèse et vigilance absentes ET glossaire disponible -->
3. [Consulter les notions utiles](SCR_REV_T1_CH04_GLO)
<!-- Condition métier : Aucun bloc complémentaire disponible -->
4. [Terminer le chapitre](SCR_REV_T1_CH04_FIN)

<!-- Chapitre T1_CH04 — source : COURS/THEMATIQUE 1/Chapitre 4/CHAPITRE_4_LA#U00cfCITE.md -->

## SCR_REV_T1_CH04_SYN

### À retenir

<!-- Variables : {id_theme}=T1; {id_chapitre}=T1_CH04; {ordre_chapitre}=4; {dernier_chapitre_theme}=Non -->

La laïcité est un principe fondamental de la République française qui organise les relations entre l'État et les religions.

<!-- Condition métier : Vigilance disponible -->
1. [Voir les points de vigilance](SCR_REV_T1_CH04_VIG)
<!-- Condition métier : Vigilance absente ET glossaire disponible -->
2. [Consulter les notions utiles](SCR_REV_T1_CH04_GLO)
<!-- Condition métier : Vigilance et glossaire absents -->
3. [Terminer le chapitre](SCR_REV_T1_CH04_FIN)

<!-- Chapitre T1_CH04 — source : COURS/THEMATIQUE 1/Chapitre 4/CHAPITRE_4_LA#U00cfCITE.md -->

## SCR_REV_T1_CH04_VIG

### Points de vigilance

<!-- Variables : {id_theme}=T1; {id_chapitre}=T1_CH04; {ordre_chapitre}=4; {dernier_chapitre_theme}=Non -->

❌ La laïcité interdit les religions.
✅ Faux.
Elle garantit la liberté de conscience.
❌ Les citoyens doivent être neutres comme les agents publics.
✅ Faux.
L'obligation de neutralité concerne les agents publics dans l'exercice de leurs fonctions.
❌ Le blasphème est interdit en France.
✅ Faux.
Le blasphème n'est pas une infraction, mais les injures, la diffamation et l'incitation à la haine sont interdites.
❌ Les élèves peuvent refuser certains cours pour des raisons religieuses.
✅ Faux.
Tous les enseignements obligatoires doivent être suivis.

<!-- Condition métier : Glossaire disponible -->
1. [Consulter les notions utiles](SCR_REV_T1_CH04_GLO)
<!-- Condition métier : Glossaire absent -->
2. [Terminer le chapitre](SCR_REV_T1_CH04_FIN)

<!-- Chapitre T1_CH04 — source : COURS/THEMATIQUE 1/Chapitre 4/CHAPITRE_4_LA#U00cfCITE.md -->

## SCR_REV_T1_CH04_GLO

### Notions utiles

<!-- Variables : {id_theme}=T1; {id_chapitre}=T1_CH04; {ordre_chapitre}=4; {dernier_chapitre_theme}=Non -->

La laïcité protège la liberté de conscience tout en garantissant la neutralité de l'État.

1. [Terminer le chapitre](SCR_REV_T1_CH04_FIN)

<!-- Chapitre T1_CH04 — source : COURS/THEMATIQUE 1/Chapitre 4/CHAPITRE_4_LA#U00cfCITE.md -->

## SCR_REV_T1_CH04_FIN

### Chapitre terminé

<!-- Variables : {id_theme}=T1; {id_chapitre}=T1_CH04; {ordre_chapitre}=4; {dernier_chapitre_theme}=Non -->

Vous pouvez passer au chapitre suivant ou revenir au menu principal.

1. [Chapitre suivant](SCR_REV_T1_CH05_ACC)
2. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Chapitre T1_CH04 — source : COURS/THEMATIQUE 1/Chapitre 4/CHAPITRE_4_LA#U00cfCITE.md -->

## SCR_REV_T1_CH05_ACC

### LA LANGUE DE LA RÉPUBLIQUE

<!-- Variables : {id_theme}=T1; {id_chapitre}=T1_CH05; {ordre_chapitre}=5; {dernier_chapitre_theme}=Non -->

<!-- Ce bloc n'est pas renseigné dans le moteur Excel pour T1_CH05:INTRO. -->

<!-- Condition métier : Objectifs disponibles -->
1. [Découvrir les objectifs](SCR_REV_T1_CH05_OBJ)
<!-- Condition métier : Objectifs absents -->
2. [Commencer le cours](SCR_REV_T1_CH05_COURS)
3. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Chapitre T1_CH05 — source : COURS/THEMATIQUE 1/Chapitre 5/CHAPITRE_5_LANGUE_DE_LA_REPUBLIQUE.md -->

## SCR_REV_T1_CH05_OBJ

### Objectifs du chapitre

<!-- Variables : {id_theme}=T1; {id_chapitre}=T1_CH05; {ordre_chapitre}=5; {dernier_chapitre_theme}=Non -->

À la fin de ce chapitre, tu seras capable de :
• connaître la langue officielle de la République française ;
• comprendre pourquoi le français est la langue de la République ;
• expliquer son rôle dans la vie publique et l'accès aux droits.

1. [Commencer le cours](SCR_REV_T1_CH05_COURS)

<!-- Chapitre T1_CH05 — source : COURS/THEMATIQUE 1/Chapitre 5/CHAPITRE_5_LANGUE_DE_LA_REPUBLIQUE.md -->

## SCR_REV_T1_CH05_COURS

### LA LANGUE DE LA RÉPUBLIQUE

<!-- Variables : {id_theme}=T1; {id_chapitre}=T1_CH05; {ordre_chapitre}=5; {dernier_chapitre_theme}=Non -->

<!-- Source Markdown attendue : COURS/THEMATIQUE 1/Chapitre 5/CHAPITRE_5_LANGUE_DE_LA_REPUBLIQUE.md. Utiliser --content-root pour l'intégrer. -->

<!-- Condition métier : Synthèse disponible -->
1. [Voir la synthèse](SCR_REV_T1_CH05_SYN)
<!-- Condition métier : Synthèse absente ET vigilance disponible -->
2. [Voir les points de vigilance](SCR_REV_T1_CH05_VIG)
<!-- Condition métier : Synthèse et vigilance absentes ET glossaire disponible -->
3. [Consulter les notions utiles](SCR_REV_T1_CH05_GLO)
<!-- Condition métier : Aucun bloc complémentaire disponible -->
4. [Terminer le chapitre](SCR_REV_T1_CH05_FIN)

<!-- Chapitre T1_CH05 — source : COURS/THEMATIQUE 1/Chapitre 5/CHAPITRE_5_LANGUE_DE_LA_REPUBLIQUE.md -->

## SCR_REV_T1_CH05_SYN

### À retenir

<!-- Variables : {id_theme}=T1; {id_chapitre}=T1_CH05; {ordre_chapitre}=5; {dernier_chapitre_theme}=Non -->

La langue officielle de la République française est le français.

<!-- Condition métier : Vigilance disponible -->
1. [Voir les points de vigilance](SCR_REV_T1_CH05_VIG)
<!-- Condition métier : Vigilance absente ET glossaire disponible -->
2. [Consulter les notions utiles](SCR_REV_T1_CH05_GLO)
<!-- Condition métier : Vigilance et glossaire absents -->
3. [Terminer le chapitre](SCR_REV_T1_CH05_FIN)

<!-- Chapitre T1_CH05 — source : COURS/THEMATIQUE 1/Chapitre 5/CHAPITRE_5_LANGUE_DE_LA_REPUBLIQUE.md -->

## SCR_REV_T1_CH05_VIG

### Points de vigilance

<!-- Variables : {id_theme}=T1; {id_chapitre}=T1_CH05; {ordre_chapitre}=5; {dernier_chapitre_theme}=Non -->

❌ La France interdit de parler d'autres langues.
✅ Faux.
Chacun est libre de parler la langue de son choix dans sa vie privée.
❌ Les documents administratifs peuvent être rédigés dans n'importe quelle langue.
✅ Faux.
Les documents officiels sont rédigés en français.
❌ Les langues régionales remplacent le français.
✅ Faux.
Les langues régionales font partie du patrimoine culturel français mais ne remplacent pas la langue officielle.

<!-- Condition métier : Glossaire disponible -->
1. [Consulter les notions utiles](SCR_REV_T1_CH05_GLO)
<!-- Condition métier : Glossaire absent -->
2. [Terminer le chapitre](SCR_REV_T1_CH05_FIN)

<!-- Chapitre T1_CH05 — source : COURS/THEMATIQUE 1/Chapitre 5/CHAPITRE_5_LANGUE_DE_LA_REPUBLIQUE.md -->

## SCR_REV_T1_CH05_GLO

### Notions utiles

<!-- Variables : {id_theme}=T1; {id_chapitre}=T1_CH05; {ordre_chapitre}=5; {dernier_chapitre_theme}=Non -->

La langue officielle de la République française est le français.

1. [Terminer le chapitre](SCR_REV_T1_CH05_FIN)

<!-- Chapitre T1_CH05 — source : COURS/THEMATIQUE 1/Chapitre 5/CHAPITRE_5_LANGUE_DE_LA_REPUBLIQUE.md -->

## SCR_REV_T1_CH05_FIN

### Chapitre terminé

<!-- Variables : {id_theme}=T1; {id_chapitre}=T1_CH05; {ordre_chapitre}=5; {dernier_chapitre_theme}=Non -->

Vous pouvez passer au chapitre suivant ou revenir au menu principal.

1. [Chapitre suivant](SCR_REV_T1_CH06_ACC)
2. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Chapitre T1_CH05 — source : COURS/THEMATIQUE 1/Chapitre 5/CHAPITRE_5_LANGUE_DE_LA_REPUBLIQUE.md -->

## SCR_REV_T1_CH06_ACC

### LE CONTRAT D'ENGAGEMENT À RESPECTER LES PRINCIPES DE LA RÉPUBLIQUE

<!-- Variables : {id_theme}=T1; {id_chapitre}=T1_CH06; {ordre_chapitre}=6; {dernier_chapitre_theme}=Oui -->

<!-- Ce bloc n'est pas renseigné dans le moteur Excel pour T1_CH06:INTRO. -->

<!-- Condition métier : Objectifs disponibles -->
1. [Découvrir les objectifs](SCR_REV_T1_CH06_OBJ)
<!-- Condition métier : Objectifs absents -->
2. [Commencer le cours](SCR_REV_T1_CH06_COURS)
3. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Chapitre T1_CH06 — source : COURS/THEMATIQUE 1/Chapitre 6/CHAPITRE_6_CONTRAT_ENGAGEMENT.md -->

## SCR_REV_T1_CH06_OBJ

### Objectifs du chapitre

<!-- Variables : {id_theme}=T1; {id_chapitre}=T1_CH06; {ordre_chapitre}=6; {dernier_chapitre_theme}=Oui -->

À la fin de ce chapitre, tu seras capable de :
• comprendre ce qu'est le contrat d'engagement à respecter les principes de la République ;
• savoir qui doit le signer ;
• connaître les engagements qu'il contient ;
• comprendre les conséquences d'un refus ou d'un non-respect.

1. [Commencer le cours](SCR_REV_T1_CH06_COURS)

<!-- Chapitre T1_CH06 — source : COURS/THEMATIQUE 1/Chapitre 6/CHAPITRE_6_CONTRAT_ENGAGEMENT.md -->

## SCR_REV_T1_CH06_COURS

### LE CONTRAT D'ENGAGEMENT À RESPECTER LES PRINCIPES DE LA RÉPUBLIQUE

<!-- Variables : {id_theme}=T1; {id_chapitre}=T1_CH06; {ordre_chapitre}=6; {dernier_chapitre_theme}=Oui -->

<!-- Source Markdown attendue : COURS/THEMATIQUE 1/Chapitre 6/CHAPITRE_6_CONTRAT_ENGAGEMENT.md. Utiliser --content-root pour l'intégrer. -->

<!-- Condition métier : Synthèse disponible -->
1. [Voir la synthèse](SCR_REV_T1_CH06_SYN)
<!-- Condition métier : Synthèse absente ET vigilance disponible -->
2. [Voir les points de vigilance](SCR_REV_T1_CH06_VIG)
<!-- Condition métier : Synthèse et vigilance absentes ET glossaire disponible -->
3. [Consulter les notions utiles](SCR_REV_T1_CH06_GLO)
<!-- Condition métier : Aucun bloc complémentaire disponible -->
4. [Terminer le chapitre](SCR_REV_T1_CH06_FIN)

<!-- Chapitre T1_CH06 — source : COURS/THEMATIQUE 1/Chapitre 6/CHAPITRE_6_CONTRAT_ENGAGEMENT.md -->

## SCR_REV_T1_CH06_SYN

### À retenir

<!-- Variables : {id_theme}=T1; {id_chapitre}=T1_CH06; {ordre_chapitre}=6; {dernier_chapitre_theme}=Oui -->

Le contrat d'engagement à respecter les principes de la République est un document officiel par lequel un étranger s'engage à respecter les valeurs fondamentales de la République française.

<!-- Condition métier : Vigilance disponible -->
1. [Voir les points de vigilance](SCR_REV_T1_CH06_VIG)
<!-- Condition métier : Vigilance absente ET glossaire disponible -->
2. [Consulter les notions utiles](SCR_REV_T1_CH06_GLO)
<!-- Condition métier : Vigilance et glossaire absents -->
3. [Terminer le chapitre](SCR_REV_T1_CH06_FIN)

<!-- Chapitre T1_CH06 — source : COURS/THEMATIQUE 1/Chapitre 6/CHAPITRE_6_CONTRAT_ENGAGEMENT.md -->

## SCR_REV_T1_CH06_VIG

### Points de vigilance

<!-- Variables : {id_theme}=T1; {id_chapitre}=T1_CH06; {ordre_chapitre}=6; {dernier_chapitre_theme}=Oui -->

❌ Le contrat est facultatif.
✅ Faux.
Il est obligatoire lorsque la réglementation le prévoit.
❌ Signer le contrat suffit pour obtenir un titre de séjour.
✅ Faux.
La signature est une condition parmi d'autres.
❌ Le contrat concerne uniquement les personnes demandant la nationalité française.
✅ Faux.
Il concerne principalement certaines demandes de titre de séjour.
❌ Les principes de la République ne concernent que la vie publique.
✅ Faux.
Le respect des principes de la République est attendu dans le cadre fixé par la loi.

<!-- Condition métier : Glossaire disponible -->
1. [Consulter les notions utiles](SCR_REV_T1_CH06_GLO)
<!-- Condition métier : Glossaire absent -->
2. [Terminer le chapitre](SCR_REV_T1_CH06_FIN)

<!-- Chapitre T1_CH06 — source : COURS/THEMATIQUE 1/Chapitre 6/CHAPITRE_6_CONTRAT_ENGAGEMENT.md -->

## SCR_REV_T1_CH06_GLO

### Notions utiles

<!-- Variables : {id_theme}=T1; {id_chapitre}=T1_CH06; {ordre_chapitre}=6; {dernier_chapitre_theme}=Oui -->

Le contrat d'engagement est obligatoire pour de nombreuses demandes de titre de séjour.

1. [Terminer le chapitre](SCR_REV_T1_CH06_FIN)

<!-- Chapitre T1_CH06 — source : COURS/THEMATIQUE 1/Chapitre 6/CHAPITRE_6_CONTRAT_ENGAGEMENT.md -->

## SCR_REV_T1_CH06_FIN

### Thématique terminée

<!-- Variables : {id_theme}=T1; {id_chapitre}=T1_CH06; {ordre_chapitre}=6; {dernier_chapitre_theme}=Oui -->

Vous avez terminé le dernier chapitre de cette thématique. Vous pouvez maintenant vous entraîner, consulter le glossaire ou revenir au menu principal.

1. [M'entraîner sur cette thématique](SCR_ENT_MENU)
2. [Consulter le glossaire](SCR_GLO_MENU)
3. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Chapitre T1_CH06 — source : COURS/THEMATIQUE 1/Chapitre 6/CHAPITRE_6_CONTRAT_ENGAGEMENT.md -->

## SCR_REV_T2_MENU

### SYSTÈME INSTITUTIONNEL ET POLITIQUE 🏛️

<!-- Variables : {id_theme}=T2; {titre_theme} -->

### Objectif general

L'objectif de cette thématique est de permettre à l'apprenant de comprendre le fonctionnement des institutions françaises, de la démocratie, de la séparation des pouvoirs ainsi que le rôle de l'Union européenne.
À la fin de cette thématique, l'apprenant sera capable de :
• comprendre le fonctionnement de l'État de droit ;
• expliquer la séparation des pouvoirs ;
• connaître le rôle des principales institutions françaises ;
• comprendre le fonctionnement de la démocratie française ;
• connaître les conditions du droit de vote ;
• comprendre comment une loi est adoptée ;
• identifier les principaux acteurs territoriaux ;
• comprendre le fonctionnement des institutions européennes.

<!-- Condition métier : Chapitre actif | Valeur : T2_CH01 -->
1. [État de droit et séparation des pouvoirs](SCR_REV_T2_CH01_ACC)
<!-- Condition métier : Chapitre actif | Valeur : T2_CH02 -->
2. [Démocratie et droit de vote](SCR_REV_T2_CH02_ACC)
<!-- Condition métier : Chapitre actif | Valeur : T2_CH03 -->
3. [Organisation de la République française](SCR_REV_T2_CH03_ACC)
<!-- Condition métier : Chapitre actif | Valeur : T2_CH04 -->
4. [Les institutions européennes](SCR_REV_T2_CH04_ACC)
5. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source thématique : COURS/THEMATIQUE 2/THEMATIQUE_2_SYSTEME_INSTITUTIONNEL.md -->

## SCR_REV_T2_CH01_ACC

### État de droit et séparation des pouvoirs

<!-- Variables : {id_theme}=T2; {id_chapitre}=T2_CH01; {ordre_chapitre}=1; {dernier_chapitre_theme}=Non -->

<!-- Ce bloc n'est pas renseigné dans le moteur Excel pour T2_CH01:INTRO. -->

<!-- Condition métier : Objectifs disponibles -->
1. [Découvrir les objectifs](SCR_REV_T2_CH01_OBJ)
<!-- Condition métier : Objectifs absents -->
2. [Commencer le cours](SCR_REV_T2_CH01_COURS)
3. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Chapitre T2_CH01 — source : COURS/THEMATIQUE 2/Chapitre 1/CHAPITRE_1_ETAT_DE_DROIT_SEPARATION_DES_POUVOIRS.md -->

## SCR_REV_T2_CH01_OBJ

### Objectifs du chapitre

<!-- Variables : {id_theme}=T2; {id_chapitre}=T2_CH01; {ordre_chapitre}=1; {dernier_chapitre_theme}=Non -->

Comprendre comment fonctionne un État de droit et pourquoi la séparation des pouvoirs est essentielle au fonctionnement d'une démocratie.
À la fin de ce chapitre, tu seras capable de :
• définir un État de droit ;
• expliquer pourquoi les pouvoirs sont séparés ;
• identifier le rôle du pouvoir législatif ;
• identifier le rôle du pouvoir exécutif ;
• comprendre le rôle de l'autorité judiciaire.

1. [Commencer le cours](SCR_REV_T2_CH01_COURS)

<!-- Chapitre T2_CH01 — source : COURS/THEMATIQUE 2/Chapitre 1/CHAPITRE_1_ETAT_DE_DROIT_SEPARATION_DES_POUVOIRS.md -->

## SCR_REV_T2_CH01_COURS

### État de droit et séparation des pouvoirs

<!-- Variables : {id_theme}=T2; {id_chapitre}=T2_CH01; {ordre_chapitre}=1; {dernier_chapitre_theme}=Non -->

<!-- Source Markdown attendue : COURS/THEMATIQUE 2/Chapitre 1/CHAPITRE_1_ETAT_DE_DROIT_SEPARATION_DES_POUVOIRS.md. Utiliser --content-root pour l'intégrer. -->

<!-- Condition métier : Synthèse disponible -->
1. [Voir la synthèse](SCR_REV_T2_CH01_SYN)
<!-- Condition métier : Synthèse absente ET vigilance disponible -->
2. [Voir les points de vigilance](SCR_REV_T2_CH01_VIG)
<!-- Condition métier : Synthèse et vigilance absentes ET glossaire disponible -->
3. [Consulter les notions utiles](SCR_REV_T2_CH01_GLO)
<!-- Condition métier : Aucun bloc complémentaire disponible -->
4. [Terminer le chapitre](SCR_REV_T2_CH01_FIN)

<!-- Chapitre T2_CH01 — source : COURS/THEMATIQUE 2/Chapitre 1/CHAPITRE_1_ETAT_DE_DROIT_SEPARATION_DES_POUVOIRS.md -->

## SCR_REV_T2_CH01_SYN

### À retenir

<!-- Variables : {id_theme}=T2; {id_chapitre}=T2_CH01; {ordre_chapitre}=1; {dernier_chapitre_theme}=Non -->

La France est un État de droit.
Cela signifie que :
• l'État et ses représentants doivent respecter les lois ;
• les citoyens sont protégés par des règles communes ;
• les droits et libertés fondamentales sont garantis ;
• la justice est indépendante.
L'État de droit repose notamment sur la séparation des pouvoirs :
• le pouvoir législatif ;
• le pouvoir exécutif ;
• le pouvoir judiciaire.

<!-- Condition métier : Vigilance disponible -->
1. [Voir les points de vigilance](SCR_REV_T2_CH01_VIG)
<!-- Condition métier : Vigilance absente ET glossaire disponible -->
2. [Consulter les notions utiles](SCR_REV_T2_CH01_GLO)
<!-- Condition métier : Vigilance et glossaire absents -->
3. [Terminer le chapitre](SCR_REV_T2_CH01_FIN)

<!-- Chapitre T2_CH01 — source : COURS/THEMATIQUE 2/Chapitre 1/CHAPITRE_1_ETAT_DE_DROIT_SEPARATION_DES_POUVOIRS.md -->

## SCR_REV_T2_CH01_VIG

### Points de vigilance

<!-- Variables : {id_theme}=T2; {id_chapitre}=T2_CH01; {ordre_chapitre}=1; {dernier_chapitre_theme}=Non -->

❌ Le Président de la République possède tous les pouvoirs.
✅ Le Président exerce le pouvoir exécutif avec le Gouvernement.
❌ Le Parlement applique les lois.
✅ Le Parlement vote les lois.
❌ La justice dépend du Gouvernement.
✅ La justice est indépendante des autres pouvoirs.
❌ Un État de droit signifie que seuls les citoyens doivent respecter les lois.
✅ Dans un État de droit, l'État lui-même doit respecter les lois.

<!-- Condition métier : Glossaire disponible -->
1. [Consulter les notions utiles](SCR_REV_T2_CH01_GLO)
<!-- Condition métier : Glossaire absent -->
2. [Terminer le chapitre](SCR_REV_T2_CH01_FIN)

<!-- Chapitre T2_CH01 — source : COURS/THEMATIQUE 2/Chapitre 1/CHAPITRE_1_ETAT_DE_DROIT_SEPARATION_DES_POUVOIRS.md -->

## SCR_REV_T2_CH01_GLO

### Notions utiles

<!-- Variables : {id_theme}=T2; {id_chapitre}=T2_CH01; {ordre_chapitre}=1; {dernier_chapitre_theme}=Non -->

La France est un État de droit car :
• l'État respecte les lois ;
• les citoyens sont égaux devant la loi ;
• les libertés fondamentales sont protégées.
La séparation des pouvoirs repose sur trois pouvoirs :
✅ Le pouvoir législatif → vote les lois.
✅ Le pouvoir exécutif → applique les lois.
✅ Le pouvoir judiciaire → juge et fait respecter la loi.

1. [Terminer le chapitre](SCR_REV_T2_CH01_FIN)

<!-- Chapitre T2_CH01 — source : COURS/THEMATIQUE 2/Chapitre 1/CHAPITRE_1_ETAT_DE_DROIT_SEPARATION_DES_POUVOIRS.md -->

## SCR_REV_T2_CH01_FIN

### Chapitre terminé

<!-- Variables : {id_theme}=T2; {id_chapitre}=T2_CH01; {ordre_chapitre}=1; {dernier_chapitre_theme}=Non -->

Vous pouvez passer au chapitre suivant ou revenir au menu principal.

1. [Chapitre suivant](SCR_REV_T2_CH02_ACC)
2. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Chapitre T2_CH01 — source : COURS/THEMATIQUE 2/Chapitre 1/CHAPITRE_1_ETAT_DE_DROIT_SEPARATION_DES_POUVOIRS.md -->

## SCR_REV_T2_CH02_ACC

### Démocratie et droit de vote

<!-- Variables : {id_theme}=T2; {id_chapitre}=T2_CH02; {ordre_chapitre}=2; {dernier_chapitre_theme}=Non -->

<!-- Ce bloc n'est pas renseigné dans le moteur Excel pour T2_CH02:INTRO. -->

<!-- Condition métier : Objectifs disponibles -->
1. [Découvrir les objectifs](SCR_REV_T2_CH02_OBJ)
<!-- Condition métier : Objectifs absents -->
2. [Commencer le cours](SCR_REV_T2_CH02_COURS)
3. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Chapitre T2_CH02 — source : COURS/THEMATIQUE 2/Chapitre 2/CHAPITRE_2_DEMOCRATIE_ET_DROIT_DE_VOTE.md -->

## SCR_REV_T2_CH02_OBJ

### Objectifs du chapitre

<!-- Variables : {id_theme}=T2; {id_chapitre}=T2_CH02; {ordre_chapitre}=2; {dernier_chapitre_theme}=Non -->

Comprendre comment fonctionne la démocratie française et comment les citoyens participent aux décisions politiques grâce au droit de vote.
À la fin de ce chapitre, tu seras capable de :
• définir la démocratie ;
• expliquer la différence entre démocratie et République ;
• connaître les conditions pour voter en France ;
• identifier les principales élections françaises ;
• comprendre le rôle des partis politiques ;
• comprendre les grandes étapes du vote d'une loi.

1. [Commencer le cours](SCR_REV_T2_CH02_COURS)

<!-- Chapitre T2_CH02 — source : COURS/THEMATIQUE 2/Chapitre 2/CHAPITRE_2_DEMOCRATIE_ET_DROIT_DE_VOTE.md -->

## SCR_REV_T2_CH02_COURS

### Démocratie et droit de vote

<!-- Variables : {id_theme}=T2; {id_chapitre}=T2_CH02; {ordre_chapitre}=2; {dernier_chapitre_theme}=Non -->

<!-- Source Markdown attendue : COURS/THEMATIQUE 2/Chapitre 2/CHAPITRE_2_DEMOCRATIE_ET_DROIT_DE_VOTE.md. Utiliser --content-root pour l'intégrer. -->

<!-- Condition métier : Synthèse disponible -->
1. [Voir la synthèse](SCR_REV_T2_CH02_SYN)
<!-- Condition métier : Synthèse absente ET vigilance disponible -->
2. [Voir les points de vigilance](SCR_REV_T2_CH02_VIG)
<!-- Condition métier : Synthèse et vigilance absentes ET glossaire disponible -->
3. [Consulter les notions utiles](SCR_REV_T2_CH02_GLO)
<!-- Condition métier : Aucun bloc complémentaire disponible -->
4. [Terminer le chapitre](SCR_REV_T2_CH02_FIN)

<!-- Chapitre T2_CH02 — source : COURS/THEMATIQUE 2/Chapitre 2/CHAPITRE_2_DEMOCRATIE_ET_DROIT_DE_VOTE.md -->

## SCR_REV_T2_CH02_SYN

### À retenir

<!-- Variables : {id_theme}=T2; {id_chapitre}=T2_CH02; {ordre_chapitre}=2; {dernier_chapitre_theme}=Non -->

La démocratie est un régime politique dans lequel le pouvoir appartient au peuple.
En France, les citoyens participent à la vie politique principalement :
• en élisant des représentants ;
• en participant à des référendums.
Le droit de vote permet aux citoyens d'exprimer leur choix lors des élections.

<!-- Condition métier : Vigilance disponible -->
1. [Voir les points de vigilance](SCR_REV_T2_CH02_VIG)
<!-- Condition métier : Vigilance absente ET glossaire disponible -->
2. [Consulter les notions utiles](SCR_REV_T2_CH02_GLO)
<!-- Condition métier : Vigilance et glossaire absents -->
3. [Terminer le chapitre](SCR_REV_T2_CH02_FIN)

<!-- Chapitre T2_CH02 — source : COURS/THEMATIQUE 2/Chapitre 2/CHAPITRE_2_DEMOCRATIE_ET_DROIT_DE_VOTE.md -->

## SCR_REV_T2_CH02_VIG

### Points de vigilance

<!-- Variables : {id_theme}=T2; {id_chapitre}=T2_CH02; {ordre_chapitre}=2; {dernier_chapitre_theme}=Non -->

❌ Une démocratie signifie que chacun peut décider seul des règles.
✅ Une démocratie fonctionne avec des institutions et des représentants élus.
❌ La République et la démocratie veulent dire exactement la même chose.
✅ La République désigne une forme d'organisation du pouvoir ; la démocratie désigne la participation du peuple.
❌ Le Gouvernement vote les lois.
✅ Le Parlement vote les lois.
❌ Le Président de la République écrit toutes les lois.
✅ Les lois peuvent être proposées par le Gouvernement ou les parlementaires.

<!-- Condition métier : Glossaire disponible -->
1. [Consulter les notions utiles](SCR_REV_T2_CH02_GLO)
<!-- Condition métier : Glossaire absent -->
2. [Terminer le chapitre](SCR_REV_T2_CH02_FIN)

<!-- Chapitre T2_CH02 — source : COURS/THEMATIQUE 2/Chapitre 2/CHAPITRE_2_DEMOCRATIE_ET_DROIT_DE_VOTE.md -->

## SCR_REV_T2_CH02_GLO

### Notions utiles

<!-- Variables : {id_theme}=T2; {id_chapitre}=T2_CH02; {ordre_chapitre}=2; {dernier_chapitre_theme}=Non -->

La démocratie est un régime dans lequel :
✅ le pouvoir appartient au peuple.
Le droit de vote permet aux citoyens :
✅ de choisir leurs représentants.
En France :
✅ le vote est universel, libre et secret.
Une loi est :
✅ proposée → discutée → votée → appliquée.

1. [Terminer le chapitre](SCR_REV_T2_CH02_FIN)

<!-- Chapitre T2_CH02 — source : COURS/THEMATIQUE 2/Chapitre 2/CHAPITRE_2_DEMOCRATIE_ET_DROIT_DE_VOTE.md -->

## SCR_REV_T2_CH02_FIN

### Chapitre terminé

<!-- Variables : {id_theme}=T2; {id_chapitre}=T2_CH02; {ordre_chapitre}=2; {dernier_chapitre_theme}=Non -->

Vous pouvez passer au chapitre suivant ou revenir au menu principal.

1. [Chapitre suivant](SCR_REV_T2_CH03_ACC)
2. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Chapitre T2_CH02 — source : COURS/THEMATIQUE 2/Chapitre 2/CHAPITRE_2_DEMOCRATIE_ET_DROIT_DE_VOTE.md -->

## SCR_REV_T2_CH03_ACC

### Organisation de la République française

<!-- Variables : {id_theme}=T2; {id_chapitre}=T2_CH03; {ordre_chapitre}=3; {dernier_chapitre_theme}=Non -->

<!-- Ce bloc n'est pas renseigné dans le moteur Excel pour T2_CH03:INTRO. -->

<!-- Condition métier : Objectifs disponibles -->
1. [Découvrir les objectifs](SCR_REV_T2_CH03_OBJ)
<!-- Condition métier : Objectifs absents -->
2. [Commencer le cours](SCR_REV_T2_CH03_COURS)
3. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Chapitre T2_CH03 — source : COURS/THEMATIQUE 2/Chapitre 3/CHAPITRE_3_ORGANISATION_REPUBLIQUE_FRANCAISE.md -->

## SCR_REV_T2_CH03_OBJ

### Objectifs du chapitre

<!-- Variables : {id_theme}=T2; {id_chapitre}=T2_CH03; {ordre_chapitre}=3; {dernier_chapitre_theme}=Non -->

Comprendre comment la République française est organisée au niveau national et local, et connaître le rôle des différents acteurs qui participent au fonctionnement de l'État.
À la fin de ce chapitre, tu seras capable de :
• identifier les principaux acteurs politiques nationaux ;
• connaître le rôle des élus locaux ;
• comprendre le rôle du préfet ;
• connaître le découpage administratif français ;
• comprendre le rôle de l'État et des collectivités territoriales.

1. [Commencer le cours](SCR_REV_T2_CH03_COURS)

<!-- Chapitre T2_CH03 — source : COURS/THEMATIQUE 2/Chapitre 3/CHAPITRE_3_ORGANISATION_REPUBLIQUE_FRANCAISE.md -->

## SCR_REV_T2_CH03_COURS

### Organisation de la République française

<!-- Variables : {id_theme}=T2; {id_chapitre}=T2_CH03; {ordre_chapitre}=3; {dernier_chapitre_theme}=Non -->

<!-- Source Markdown attendue : COURS/THEMATIQUE 2/Chapitre 3/CHAPITRE_3_ORGANISATION_REPUBLIQUE_FRANCAISE.md. Utiliser --content-root pour l'intégrer. -->

<!-- Condition métier : Synthèse disponible -->
1. [Voir la synthèse](SCR_REV_T2_CH03_SYN)
<!-- Condition métier : Synthèse absente ET vigilance disponible -->
2. [Voir les points de vigilance](SCR_REV_T2_CH03_VIG)
<!-- Condition métier : Synthèse et vigilance absentes ET glossaire disponible -->
3. [Consulter les notions utiles](SCR_REV_T2_CH03_GLO)
<!-- Condition métier : Aucun bloc complémentaire disponible -->
4. [Terminer le chapitre](SCR_REV_T2_CH03_FIN)

<!-- Chapitre T2_CH03 — source : COURS/THEMATIQUE 2/Chapitre 3/CHAPITRE_3_ORGANISATION_REPUBLIQUE_FRANCAISE.md -->

## SCR_REV_T2_CH03_SYN

### À retenir

<!-- Variables : {id_theme}=T2; {id_chapitre}=T2_CH03; {ordre_chapitre}=3; {dernier_chapitre_theme}=Non -->

La République française est organisée à plusieurs niveaux :
• le niveau national ;
• le niveau territorial.
L'État, les collectivités territoriales et les services publics travaillent ensemble pour répondre aux besoins des citoyens.

<!-- Condition métier : Vigilance disponible -->
1. [Voir les points de vigilance](SCR_REV_T2_CH03_VIG)
<!-- Condition métier : Vigilance absente ET glossaire disponible -->
2. [Consulter les notions utiles](SCR_REV_T2_CH03_GLO)
<!-- Condition métier : Vigilance et glossaire absents -->
3. [Terminer le chapitre](SCR_REV_T2_CH03_FIN)

<!-- Chapitre T2_CH03 — source : COURS/THEMATIQUE 2/Chapitre 3/CHAPITRE_3_ORGANISATION_REPUBLIQUE_FRANCAISE.md -->

## SCR_REV_T2_CH03_VIG

### Points de vigilance

<!-- Variables : {id_theme}=T2; {id_chapitre}=T2_CH03; {ordre_chapitre}=3; {dernier_chapitre_theme}=Non -->

❌ Le préfet est élu par les citoyens.
✅ Le préfet est nommé par l'État.
❌ Le maire représente directement l'État.
✅ Le maire dirige la commune et représente aussi les habitants.
❌ La région gère les écoles primaires.
✅ La commune gère les écoles maternelles et élémentaires.
❌ Le département vote les lois.
✅ Les lois sont votées par le Parlement.
❌ Les collectivités territoriales remplacent l'État.
✅ Elles exercent certaines compétences mais l'État conserve ses missions nationales.

<!-- Condition métier : Glossaire disponible -->
1. [Consulter les notions utiles](SCR_REV_T2_CH03_GLO)
<!-- Condition métier : Glossaire absent -->
2. [Terminer le chapitre](SCR_REV_T2_CH03_FIN)

<!-- Chapitre T2_CH03 — source : COURS/THEMATIQUE 2/Chapitre 3/CHAPITRE_3_ORGANISATION_REPUBLIQUE_FRANCAISE.md -->

## SCR_REV_T2_CH03_GLO

### Notions utiles

<!-- Variables : {id_theme}=T2; {id_chapitre}=T2_CH03; {ordre_chapitre}=3; {dernier_chapitre_theme}=Non -->

La République française fonctionne avec plusieurs niveaux :
✅ L'État décide des grandes orientations nationales.
✅ Les collectivités territoriales gèrent des compétences locales.
✅ Le préfet représente l'État dans le territoire.
Les trois principaux niveaux territoriaux sont :
• commune ;
• département ;
• région.

1. [Terminer le chapitre](SCR_REV_T2_CH03_FIN)

<!-- Chapitre T2_CH03 — source : COURS/THEMATIQUE 2/Chapitre 3/CHAPITRE_3_ORGANISATION_REPUBLIQUE_FRANCAISE.md -->

## SCR_REV_T2_CH03_FIN

### Chapitre terminé

<!-- Variables : {id_theme}=T2; {id_chapitre}=T2_CH03; {ordre_chapitre}=3; {dernier_chapitre_theme}=Non -->

Vous pouvez passer au chapitre suivant ou revenir au menu principal.

1. [Chapitre suivant](SCR_REV_T2_CH04_ACC)
2. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Chapitre T2_CH03 — source : COURS/THEMATIQUE 2/Chapitre 3/CHAPITRE_3_ORGANISATION_REPUBLIQUE_FRANCAISE.md -->

## SCR_REV_T2_CH04_ACC

### Les institutions européennes 🇪🇺

<!-- Variables : {id_theme}=T2; {id_chapitre}=T2_CH04; {ordre_chapitre}=4; {dernier_chapitre_theme}=Oui -->

<!-- Ce bloc n'est pas renseigné dans le moteur Excel pour T2_CH04:INTRO. -->

<!-- Condition métier : Objectifs disponibles -->
1. [Découvrir les objectifs](SCR_REV_T2_CH04_OBJ)
<!-- Condition métier : Objectifs absents -->
2. [Commencer le cours](SCR_REV_T2_CH04_COURS)
3. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Chapitre T2_CH04 — source : COURS/THEMATIQUE 2/Chapitre 4/CHAPITRE_4_INSTITUTIONS_EUROPEENNES.md -->

## SCR_REV_T2_CH04_OBJ

### Objectifs du chapitre

<!-- Variables : {id_theme}=T2; {id_chapitre}=T2_CH04; {ordre_chapitre}=4; {dernier_chapitre_theme}=Oui -->

Comprendre la construction européenne, les symboles de l'Union européenne et le rôle des principales institutions européennes.
À la fin de ce chapitre, tu seras capable de :
• expliquer pourquoi l'Union européenne a été créée ;
• connaître les grandes étapes de la construction européenne ;
• identifier les symboles européens ;
• reconnaître les principales institutions européennes ;
• comprendre le rôle des élections européennes.

1. [Commencer le cours](SCR_REV_T2_CH04_COURS)

<!-- Chapitre T2_CH04 — source : COURS/THEMATIQUE 2/Chapitre 4/CHAPITRE_4_INSTITUTIONS_EUROPEENNES.md -->

## SCR_REV_T2_CH04_COURS

### Les institutions européennes 🇪🇺

<!-- Variables : {id_theme}=T2; {id_chapitre}=T2_CH04; {ordre_chapitre}=4; {dernier_chapitre_theme}=Oui -->

<!-- Source Markdown attendue : COURS/THEMATIQUE 2/Chapitre 4/CHAPITRE_4_INSTITUTIONS_EUROPEENNES.md. Utiliser --content-root pour l'intégrer. -->

<!-- Condition métier : Synthèse disponible -->
1. [Voir la synthèse](SCR_REV_T2_CH04_SYN)
<!-- Condition métier : Synthèse absente ET vigilance disponible -->
2. [Voir les points de vigilance](SCR_REV_T2_CH04_VIG)
<!-- Condition métier : Synthèse et vigilance absentes ET glossaire disponible -->
3. [Consulter les notions utiles](SCR_REV_T2_CH04_GLO)
<!-- Condition métier : Aucun bloc complémentaire disponible -->
4. [Terminer le chapitre](SCR_REV_T2_CH04_FIN)

<!-- Chapitre T2_CH04 — source : COURS/THEMATIQUE 2/Chapitre 4/CHAPITRE_4_INSTITUTIONS_EUROPEENNES.md -->

## SCR_REV_T2_CH04_SYN

### À retenir

<!-- Variables : {id_theme}=T2; {id_chapitre}=T2_CH04; {ordre_chapitre}=4; {dernier_chapitre_theme}=Oui -->

L'Union européenne est une organisation politique et économique créée par plusieurs pays européens afin de favoriser :
• la paix ;
• la coopération ;
• la stabilité ;
• le développement économique.
Aujourd'hui, l'Union européenne rassemble 27 États membres.

<!-- Condition métier : Vigilance disponible -->
1. [Voir les points de vigilance](SCR_REV_T2_CH04_VIG)
<!-- Condition métier : Vigilance absente ET glossaire disponible -->
2. [Consulter les notions utiles](SCR_REV_T2_CH04_GLO)
<!-- Condition métier : Vigilance et glossaire absents -->
3. [Terminer le chapitre](SCR_REV_T2_CH04_FIN)

<!-- Chapitre T2_CH04 — source : COURS/THEMATIQUE 2/Chapitre 4/CHAPITRE_4_INSTITUTIONS_EUROPEENNES.md -->

## SCR_REV_T2_CH04_VIG

### Points de vigilance

<!-- Variables : {id_theme}=T2; {id_chapitre}=T2_CH04; {ordre_chapitre}=4; {dernier_chapitre_theme}=Oui -->

❌ Le Conseil européen vote directement toutes les lois européennes.
✅ Il donne les grandes orientations politiques.
❌ La Commission européenne est élue directement par les citoyens.
✅ Elle est composée de commissaires proposés par les États membres et approuvés selon les règles européennes.
❌ Le Parlement européen représente uniquement les gouvernements.
✅ Le Parlement européen représente les citoyens européens.
❌ L'Europe et l'Union européenne sont exactement la même chose.
✅ L'Europe est un continent ; l'Union européenne est une organisation composée de plusieurs États européens.

<!-- Condition métier : Glossaire disponible -->
1. [Consulter les notions utiles](SCR_REV_T2_CH04_GLO)
<!-- Condition métier : Glossaire absent -->
2. [Terminer le chapitre](SCR_REV_T2_CH04_FIN)

<!-- Chapitre T2_CH04 — source : COURS/THEMATIQUE 2/Chapitre 4/CHAPITRE_4_INSTITUTIONS_EUROPEENNES.md -->

## SCR_REV_T2_CH04_GLO

### Notions utiles

<!-- Variables : {id_theme}=T2; {id_chapitre}=T2_CH04; {ordre_chapitre}=4; {dernier_chapitre_theme}=Oui -->

L'Union européenne est une organisation composée de 27 États membres.
Les citoyens européens élisent :
✅ les députés européens.
Les principales institutions à connaître :
✅ Conseil européen → donne les grandes orientations.
✅ Commission européenne → propose et applique les politiques européennes.
✅ Parlement européen → vote les lois européennes et contrôle la Commission.
✅ Conseil de l'Union européenne → participe au vote des lois.

1. [Terminer le chapitre](SCR_REV_T2_CH04_FIN)

<!-- Chapitre T2_CH04 — source : COURS/THEMATIQUE 2/Chapitre 4/CHAPITRE_4_INSTITUTIONS_EUROPEENNES.md -->

## SCR_REV_T2_CH04_FIN

### Thématique terminée

<!-- Variables : {id_theme}=T2; {id_chapitre}=T2_CH04; {ordre_chapitre}=4; {dernier_chapitre_theme}=Oui -->

Vous avez terminé le dernier chapitre de cette thématique. Vous pouvez maintenant vous entraîner, consulter le glossaire ou revenir au menu principal.

1. [M'entraîner sur cette thématique](SCR_ENT_MENU)
2. [Consulter le glossaire](SCR_GLO_MENU)
3. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Chapitre T2_CH04 — source : COURS/THEMATIQUE 2/Chapitre 4/CHAPITRE_4_INSTITUTIONS_EUROPEENNES.md -->

## SCR_REV_T3_MENU

### DROITS ET DEVOIRS ⚖️

<!-- Variables : {id_theme}=T3; {titre_theme} -->

### Objectif general

L'objectif de cette thématique est de permettre à l'apprenant de connaître les principaux droits garantis par la République française ainsi que les devoirs et obligations nécessaires pour vivre ensemble dans le respect des lois et des autres.
À la fin de cette thématique, l'apprenant sera capable de :
• identifier les droits fondamentaux garantis par la République ;
• comprendre les libertés individuelles et leurs limites ;
• connaître les principaux textes qui protègent les droits ;
• distinguer les droits des devoirs ;
• comprendre les obligations des personnes vivant en France ;
• connaître les comportements interdits par la loi ;
• comprendre le rôle de chacun dans la protection des personnes et de l'environnement.

<!-- Condition métier : Chapitre actif | Valeur : T3_CH01 -->
1. [Les droits fondamentaux](SCR_REV_T3_CH01_ACC)
<!-- Condition métier : Chapitre actif | Valeur : T3_CH02 -->
2. [Les obligations et les devoirs](SCR_REV_T3_CH02_ACC)
3. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source thématique : COURS/THEMATIQUE 3/THEMATIQUE_3_DROITS_ET_DEVOIRS.md -->

## SCR_REV_T3_CH01_ACC

### 🎯 Objectif du chapitre

<!-- Variables : {id_theme}=T3; {id_chapitre}=T3_CH01; {ordre_chapitre}=1; {dernier_chapitre_theme}=Non -->

<!-- Ce bloc n'est pas renseigné dans le moteur Excel pour T3_CH01:INTRO. -->

<!-- Condition métier : Objectifs disponibles -->
1. [Découvrir les objectifs](SCR_REV_T3_CH01_OBJ)
<!-- Condition métier : Objectifs absents -->
2. [Commencer le cours](SCR_REV_T3_CH01_COURS)
3. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Chapitre T3_CH01 — source : COURS/THEMATIQUE 3/Chapitre 1/CHAPITRE_1_DROITS_FONDAMENTAUX.md -->

## SCR_REV_T3_CH01_OBJ

### Objectifs du chapitre

<!-- Variables : {id_theme}=T3; {id_chapitre}=T3_CH01; {ordre_chapitre}=1; {dernier_chapitre_theme}=Non -->

Comprendre les principaux droits garantis par la République française, connaître les textes qui les protègent et savoir comment ils s'appliquent dans la vie quotidienne.

1. [Commencer le cours](SCR_REV_T3_CH01_COURS)

<!-- Chapitre T3_CH01 — source : COURS/THEMATIQUE 3/Chapitre 1/CHAPITRE_1_DROITS_FONDAMENTAUX.md -->

## SCR_REV_T3_CH01_COURS

### 🎯 Objectif du chapitre

<!-- Variables : {id_theme}=T3; {id_chapitre}=T3_CH01; {ordre_chapitre}=1; {dernier_chapitre_theme}=Non -->

<!-- Source Markdown attendue : COURS/THEMATIQUE 3/Chapitre 1/CHAPITRE_1_DROITS_FONDAMENTAUX.md. Utiliser --content-root pour l'intégrer. -->

<!-- Condition métier : Synthèse disponible -->
1. [Voir la synthèse](SCR_REV_T3_CH01_SYN)
<!-- Condition métier : Synthèse absente ET vigilance disponible -->
2. [Voir les points de vigilance](SCR_REV_T3_CH01_VIG)
<!-- Condition métier : Synthèse et vigilance absentes ET glossaire disponible -->
3. [Consulter les notions utiles](SCR_REV_T3_CH01_GLO)
<!-- Condition métier : Aucun bloc complémentaire disponible -->
4. [Terminer le chapitre](SCR_REV_T3_CH01_FIN)

<!-- Chapitre T3_CH01 — source : COURS/THEMATIQUE 3/Chapitre 1/CHAPITRE_1_DROITS_FONDAMENTAUX.md -->

## SCR_REV_T3_CH01_SYN

### À retenir

<!-- Variables : {id_theme}=T3; {id_chapitre}=T3_CH01; {ordre_chapitre}=1; {dernier_chapitre_theme}=Non -->

Les droits fondamentaux sont les droits et libertés reconnus à toute personne.
Ils sont protégés par la Constitution française et par plusieurs textes fondamentaux.
Ils garantissent :
• la liberté ;
• l'égalité ;
• la dignité ;
• la sécurité ;
• le respect de la personne.

<!-- Condition métier : Vigilance disponible -->
1. [Voir les points de vigilance](SCR_REV_T3_CH01_VIG)
<!-- Condition métier : Vigilance absente ET glossaire disponible -->
2. [Consulter les notions utiles](SCR_REV_T3_CH01_GLO)
<!-- Condition métier : Vigilance et glossaire absents -->
3. [Terminer le chapitre](SCR_REV_T3_CH01_FIN)

<!-- Chapitre T3_CH01 — source : COURS/THEMATIQUE 3/Chapitre 1/CHAPITRE_1_DROITS_FONDAMENTAUX.md -->

## SCR_REV_T3_CH01_VIG

### Points de vigilance

<!-- Variables : {id_theme}=T3; {id_chapitre}=T3_CH01; {ordre_chapitre}=1; {dernier_chapitre_theme}=Non -->

❌ Les droits fondamentaux concernent uniquement les Français.
✅ Ils protègent toute personne.

<!-- Condition métier : Glossaire disponible -->
1. [Consulter les notions utiles](SCR_REV_T3_CH01_GLO)
<!-- Condition métier : Glossaire absent -->
2. [Terminer le chapitre](SCR_REV_T3_CH01_FIN)

<!-- Chapitre T3_CH01 — source : COURS/THEMATIQUE 3/Chapitre 1/CHAPITRE_1_DROITS_FONDAMENTAUX.md -->

## SCR_REV_T3_CH01_GLO

### Notions utiles

<!-- Variables : {id_theme}=T3; {id_chapitre}=T3_CH01; {ordre_chapitre}=1; {dernier_chapitre_theme}=Non -->

Les droits fondamentaux protègent toutes les personnes vivant en France.
Ils sont garantis par la Constitution.

1. [Terminer le chapitre](SCR_REV_T3_CH01_FIN)

<!-- Chapitre T3_CH01 — source : COURS/THEMATIQUE 3/Chapitre 1/CHAPITRE_1_DROITS_FONDAMENTAUX.md -->

## SCR_REV_T3_CH01_FIN

### Chapitre terminé

<!-- Variables : {id_theme}=T3; {id_chapitre}=T3_CH01; {ordre_chapitre}=1; {dernier_chapitre_theme}=Non -->

Vous pouvez passer au chapitre suivant ou revenir au menu principal.

1. [Chapitre suivant](SCR_REV_T3_CH02_ACC)
2. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Chapitre T3_CH01 — source : COURS/THEMATIQUE 3/Chapitre 1/CHAPITRE_1_DROITS_FONDAMENTAUX.md -->

## SCR_REV_T3_CH02_ACC

### 🎯 Objectif du chapitre

<!-- Variables : {id_theme}=T3; {id_chapitre}=T3_CH02; {ordre_chapitre}=2; {dernier_chapitre_theme}=Oui -->

<!-- Ce bloc n'est pas renseigné dans le moteur Excel pour T3_CH02:INTRO. -->

<!-- Condition métier : Objectifs disponibles -->
1. [Découvrir les objectifs](SCR_REV_T3_CH02_OBJ)
<!-- Condition métier : Objectifs absents -->
2. [Commencer le cours](SCR_REV_T3_CH02_COURS)
3. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Chapitre T3_CH02 — source : COURS/THEMATIQUE 3/Chapitre 2/CHAPITRE_2_OBLIGATIONS_ET_DEVOIRS.md -->

## SCR_REV_T3_CH02_OBJ

### Objectifs du chapitre

<!-- Variables : {id_theme}=T3; {id_chapitre}=T3_CH02; {ordre_chapitre}=2; {dernier_chapitre_theme}=Oui -->

Comprendre que vivre en France implique des droits mais également des devoirs. Connaître les principales obligations des personnes résidant en France et adopter un comportement conforme aux valeurs de la République.

1. [Commencer le cours](SCR_REV_T3_CH02_COURS)

<!-- Chapitre T3_CH02 — source : COURS/THEMATIQUE 3/Chapitre 2/CHAPITRE_2_OBLIGATIONS_ET_DEVOIRS.md -->

## SCR_REV_T3_CH02_COURS

### 🎯 Objectif du chapitre

<!-- Variables : {id_theme}=T3; {id_chapitre}=T3_CH02; {ordre_chapitre}=2; {dernier_chapitre_theme}=Oui -->

<!-- Source Markdown attendue : COURS/THEMATIQUE 3/Chapitre 2/CHAPITRE_2_OBLIGATIONS_ET_DEVOIRS.md. Utiliser --content-root pour l'intégrer. -->

<!-- Condition métier : Synthèse disponible -->
1. [Voir la synthèse](SCR_REV_T3_CH02_SYN)
<!-- Condition métier : Synthèse absente ET vigilance disponible -->
2. [Voir les points de vigilance](SCR_REV_T3_CH02_VIG)
<!-- Condition métier : Synthèse et vigilance absentes ET glossaire disponible -->
3. [Consulter les notions utiles](SCR_REV_T3_CH02_GLO)
<!-- Condition métier : Aucun bloc complémentaire disponible -->
4. [Terminer le chapitre](SCR_REV_T3_CH02_FIN)

<!-- Chapitre T3_CH02 — source : COURS/THEMATIQUE 3/Chapitre 2/CHAPITRE_2_OBLIGATIONS_ET_DEVOIRS.md -->

## SCR_REV_T3_CH02_SYN

### À retenir

<!-- Variables : {id_theme}=T3; {id_chapitre}=T3_CH02; {ordre_chapitre}=2; {dernier_chapitre_theme}=Oui -->

En France, chacun est libre, mais les libertés s'exercent dans le respect de la loi.

<!-- Condition métier : Vigilance disponible -->
1. [Voir les points de vigilance](SCR_REV_T3_CH02_VIG)
<!-- Condition métier : Vigilance absente ET glossaire disponible -->
2. [Consulter les notions utiles](SCR_REV_T3_CH02_GLO)
<!-- Condition métier : Vigilance et glossaire absents -->
3. [Terminer le chapitre](SCR_REV_T3_CH02_FIN)

<!-- Chapitre T3_CH02 — source : COURS/THEMATIQUE 3/Chapitre 2/CHAPITRE_2_OBLIGATIONS_ET_DEVOIRS.md -->

## SCR_REV_T3_CH02_VIG

### Points de vigilance

<!-- Variables : {id_theme}=T3; {id_chapitre}=T3_CH02; {ordre_chapitre}=2; {dernier_chapitre_theme}=Oui -->

❌ Être libre signifie ne respecter aucune règle.
✅ Les libertés sont toujours encadrées par la loi.

<!-- Condition métier : Glossaire disponible -->
1. [Consulter les notions utiles](SCR_REV_T3_CH02_GLO)
<!-- Condition métier : Glossaire absent -->
2. [Terminer le chapitre](SCR_REV_T3_CH02_FIN)

<!-- Chapitre T3_CH02 — source : COURS/THEMATIQUE 3/Chapitre 2/CHAPITRE_2_OBLIGATIONS_ET_DEVOIRS.md -->

## SCR_REV_T3_CH02_GLO

### Notions utiles

<!-- Variables : {id_theme}=T3; {id_chapitre}=T3_CH02; {ordre_chapitre}=2; {dernier_chapitre_theme}=Oui -->

La liberté ne signifie jamais que l'on peut faire tout ce que l'on veut.

1. [Terminer le chapitre](SCR_REV_T3_CH02_FIN)

<!-- Chapitre T3_CH02 — source : COURS/THEMATIQUE 3/Chapitre 2/CHAPITRE_2_OBLIGATIONS_ET_DEVOIRS.md -->

## SCR_REV_T3_CH02_FIN

### Thématique terminée

<!-- Variables : {id_theme}=T3; {id_chapitre}=T3_CH02; {ordre_chapitre}=2; {dernier_chapitre_theme}=Oui -->

Vous avez terminé le dernier chapitre de cette thématique. Vous pouvez maintenant vous entraîner, consulter le glossaire ou revenir au menu principal.

1. [M'entraîner sur cette thématique](SCR_ENT_MENU)
2. [Consulter le glossaire](SCR_GLO_MENU)
3. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Chapitre T3_CH02 — source : COURS/THEMATIQUE 3/Chapitre 2/CHAPITRE_2_OBLIGATIONS_ET_DEVOIRS.md -->

## SCR_REV_T4_MENU

### HISTOIRE, GÉOGRAPHIE ET CULTURE 🇫🇷

<!-- Variables : {id_theme}=T4; {titre_theme} -->

### Objectif general

L'objectif de cette thématique est de permettre à l'apprenant de découvrir les grands repères historiques, géographiques et culturels de la France afin de mieux comprendre son identité, son patrimoine et sa richesse culturelle.
À la fin de cette thématique, l'apprenant sera capable de :
• connaître les grandes périodes de l'histoire de France ;
• comprendre l'organisation géographique du territoire français ;
• identifier les principales régions et les territoires d'Outre-mer ;
• reconnaître les principaux monuments et sites du patrimoine français ;
• connaître plusieurs grandes figures artistiques françaises ;
• comprendre l'importance de préserver le patrimoine et de participer à la vie culturelle.

<!-- Condition métier : Chapitre actif | Valeur : T4_CH01 -->
1. [Histoire de France](SCR_REV_T4_CH01_ACC)
<!-- Condition métier : Chapitre actif | Valeur : T4_CH02 -->
2. [Territoires et géographie de la France](SCR_REV_T4_CH02_ACC)
<!-- Condition métier : Chapitre actif | Valeur : T4_CH03 -->
3. [Patrimoine et culture française](SCR_REV_T4_CH03_ACC)
4. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source thématique : COURS/THEMATIQUE 4/THEMATIQUE_4_HISTOIRE_GEOGRAPHIE_CULTURE.md -->

## SCR_REV_T4_CH01_ACC

### Histoire de France

<!-- Variables : {id_theme}=T4; {id_chapitre}=T4_CH01; {ordre_chapitre}=1; {dernier_chapitre_theme}=Non -->

<!-- Ce bloc n'est pas renseigné dans le moteur Excel pour T4_CH01:INTRO. -->

<!-- Condition métier : Objectifs disponibles -->
1. [Découvrir les objectifs](SCR_REV_T4_CH01_OBJ)
<!-- Condition métier : Objectifs absents -->
2. [Commencer le cours](SCR_REV_T4_CH01_COURS)
3. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Chapitre T4_CH01 — source : COURS/THEMATIQUE 4/Chapitre 1/CHAPITRE_1_HISTOIRE.md -->

## SCR_REV_T4_CH01_OBJ

### Objectifs du chapitre

<!-- Variables : {id_theme}=T4; {id_chapitre}=T4_CH01; {ordre_chapitre}=1; {dernier_chapitre_theme}=Non -->

Comprendre les grandes périodes de l'histoire de France et connaître les principaux événements qui ont contribué à la construction de la République française.

1. [Commencer le cours](SCR_REV_T4_CH01_COURS)

<!-- Chapitre T4_CH01 — source : COURS/THEMATIQUE 4/Chapitre 1/CHAPITRE_1_HISTOIRE.md -->

## SCR_REV_T4_CH01_COURS

### Histoire de France

<!-- Variables : {id_theme}=T4; {id_chapitre}=T4_CH01; {ordre_chapitre}=1; {dernier_chapitre_theme}=Non -->

<!-- Source Markdown attendue : COURS/THEMATIQUE 4/Chapitre 1/CHAPITRE_1_HISTOIRE.md. Utiliser --content-root pour l'intégrer. -->

<!-- Condition métier : Synthèse disponible -->
1. [Voir la synthèse](SCR_REV_T4_CH01_SYN)
<!-- Condition métier : Synthèse absente ET vigilance disponible -->
2. [Voir les points de vigilance](SCR_REV_T4_CH01_VIG)
<!-- Condition métier : Synthèse et vigilance absentes ET glossaire disponible -->
3. [Consulter les notions utiles](SCR_REV_T4_CH01_GLO)
<!-- Condition métier : Aucun bloc complémentaire disponible -->
4. [Terminer le chapitre](SCR_REV_T4_CH01_FIN)

<!-- Chapitre T4_CH01 — source : COURS/THEMATIQUE 4/Chapitre 1/CHAPITRE_1_HISTOIRE.md -->

## SCR_REV_T4_CH01_SYN

### À retenir

<!-- Variables : {id_theme}=T4; {id_chapitre}=T4_CH01; {ordre_chapitre}=1; {dernier_chapitre_theme}=Non -->

L'histoire de France est composée de plusieurs grandes périodes qui ont façonné les institutions, les valeurs et l'identité de la République.
Connaître les principaux repères historiques permet de mieux comprendre la France d'aujourd'hui.

<!-- Condition métier : Vigilance disponible -->
1. [Voir les points de vigilance](SCR_REV_T4_CH01_VIG)
<!-- Condition métier : Vigilance absente ET glossaire disponible -->
2. [Consulter les notions utiles](SCR_REV_T4_CH01_GLO)
<!-- Condition métier : Vigilance et glossaire absents -->
3. [Terminer le chapitre](SCR_REV_T4_CH01_FIN)

<!-- Chapitre T4_CH01 — source : COURS/THEMATIQUE 4/Chapitre 1/CHAPITRE_1_HISTOIRE.md -->

## SCR_REV_T4_CH01_VIG

### Points de vigilance

<!-- Variables : {id_theme}=T4; {id_chapitre}=T4_CH01; {ordre_chapitre}=1; {dernier_chapitre_theme}=Non -->

❌ La République commence au Moyen Âge.
✅ La République apparaît après la Révolution française.
❌ La Révolution française a lieu en 1799.
✅ Elle débute en 1789.
❌ La Ve République existe depuis toujours.
✅ Elle est instaurée en 1958.

<!-- Condition métier : Glossaire disponible -->
1. [Consulter les notions utiles](SCR_REV_T4_CH01_GLO)
<!-- Condition métier : Glossaire absent -->
2. [Terminer le chapitre](SCR_REV_T4_CH01_FIN)

<!-- Chapitre T4_CH01 — source : COURS/THEMATIQUE 4/Chapitre 1/CHAPITRE_1_HISTOIRE.md -->

## SCR_REV_T4_CH01_GLO

### Notions utiles

<!-- Variables : {id_theme}=T4; {id_chapitre}=T4_CH01; {ordre_chapitre}=1; {dernier_chapitre_theme}=Non -->

Les dates essentielles à connaître :
• 52 avant J.-C. : victoire de Jules César à Alésia ;
• 496 : baptême de Clovis ;
• 800 : Charlemagne est couronné empereur ;
• 1789 : Révolution française et Déclaration des Droits de l'Homme et du Citoyen ;
• 1905 : séparation des Églises et de l'État ;
• 1914-1918 : Première Guerre mondiale ;
• 1939-1945 : Seconde Guerre mondiale ;
• 1958 : naissance de la Ve République.

1. [Terminer le chapitre](SCR_REV_T4_CH01_FIN)

<!-- Chapitre T4_CH01 — source : COURS/THEMATIQUE 4/Chapitre 1/CHAPITRE_1_HISTOIRE.md -->

## SCR_REV_T4_CH01_FIN

### Chapitre terminé

<!-- Variables : {id_theme}=T4; {id_chapitre}=T4_CH01; {ordre_chapitre}=1; {dernier_chapitre_theme}=Non -->

Vous pouvez passer au chapitre suivant ou revenir au menu principal.

1. [Chapitre suivant](SCR_REV_T4_CH02_ACC)
2. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Chapitre T4_CH01 — source : COURS/THEMATIQUE 4/Chapitre 1/CHAPITRE_1_HISTOIRE.md -->

## SCR_REV_T4_CH02_ACC

### Territoires et géographie de la France

<!-- Variables : {id_theme}=T4; {id_chapitre}=T4_CH02; {ordre_chapitre}=2; {dernier_chapitre_theme}=Non -->

<!-- Ce bloc n'est pas renseigné dans le moteur Excel pour T4_CH02:INTRO. -->

<!-- Condition métier : Objectifs disponibles -->
1. [Découvrir les objectifs](SCR_REV_T4_CH02_OBJ)
<!-- Condition métier : Objectifs absents -->
2. [Commencer le cours](SCR_REV_T4_CH02_COURS)
3. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Chapitre T4_CH02 — source : COURS/THEMATIQUE 4/Chapitre 2/CHAPITRE_2_GEOGRAPHIE.md -->

## SCR_REV_T4_CH02_OBJ

### Objectifs du chapitre

<!-- Variables : {id_theme}=T4; {id_chapitre}=T4_CH02; {ordre_chapitre}=2; {dernier_chapitre_theme}=Non -->

Découvrir le territoire français, son organisation, ses paysages, ses ressources, ses régions et sa place en Europe et dans le monde.

1. [Commencer le cours](SCR_REV_T4_CH02_COURS)

<!-- Chapitre T4_CH02 — source : COURS/THEMATIQUE 4/Chapitre 2/CHAPITRE_2_GEOGRAPHIE.md -->

## SCR_REV_T4_CH02_COURS

### Territoires et géographie de la France

<!-- Variables : {id_theme}=T4; {id_chapitre}=T4_CH02; {ordre_chapitre}=2; {dernier_chapitre_theme}=Non -->

<!-- Source Markdown attendue : COURS/THEMATIQUE 4/Chapitre 2/CHAPITRE_2_GEOGRAPHIE.md. Utiliser --content-root pour l'intégrer. -->

<!-- Condition métier : Synthèse disponible -->
1. [Voir la synthèse](SCR_REV_T4_CH02_SYN)
<!-- Condition métier : Synthèse absente ET vigilance disponible -->
2. [Voir les points de vigilance](SCR_REV_T4_CH02_VIG)
<!-- Condition métier : Synthèse et vigilance absentes ET glossaire disponible -->
3. [Consulter les notions utiles](SCR_REV_T4_CH02_GLO)
<!-- Condition métier : Aucun bloc complémentaire disponible -->
4. [Terminer le chapitre](SCR_REV_T4_CH02_FIN)

<!-- Chapitre T4_CH02 — source : COURS/THEMATIQUE 4/Chapitre 2/CHAPITRE_2_GEOGRAPHIE.md -->

## SCR_REV_T4_CH02_SYN

### À retenir

<!-- Variables : {id_theme}=T4; {id_chapitre}=T4_CH02; {ordre_chapitre}=2; {dernier_chapitre_theme}=Non -->

La France est un territoire vaste et diversifié.
Elle comprend :
• la France métropolitaine située en Europe ;
• les territoires d’Outre-mer répartis dans plusieurs régions du monde.
La diversité de ses paysages, de ses ressources et de ses territoires constitue une richesse importante.

<!-- Condition métier : Vigilance disponible -->
1. [Voir les points de vigilance](SCR_REV_T4_CH02_VIG)
<!-- Condition métier : Vigilance absente ET glossaire disponible -->
2. [Consulter les notions utiles](SCR_REV_T4_CH02_GLO)
<!-- Condition métier : Vigilance et glossaire absents -->
3. [Terminer le chapitre](SCR_REV_T4_CH02_FIN)

<!-- Chapitre T4_CH02 — source : COURS/THEMATIQUE 4/Chapitre 2/CHAPITRE_2_GEOGRAPHIE.md -->

## SCR_REV_T4_CH02_VIG

### Points de vigilance

<!-- Variables : {id_theme}=T4; {id_chapitre}=T4_CH02; {ordre_chapitre}=2; {dernier_chapitre_theme}=Non -->

❌ L’Outre-mer est un territoire étranger.
✅ Les territoires d’Outre-mer appartiennent à la République française.
❌ La France est uniquement située en Europe.
✅ La France est présente sur plusieurs continents grâce à ses territoires ultramarins.

<!-- Condition métier : Glossaire disponible -->
1. [Consulter les notions utiles](SCR_REV_T4_CH02_GLO)
<!-- Condition métier : Glossaire absent -->
2. [Terminer le chapitre](SCR_REV_T4_CH02_FIN)

<!-- Chapitre T4_CH02 — source : COURS/THEMATIQUE 4/Chapitre 2/CHAPITRE_2_GEOGRAPHIE.md -->

## SCR_REV_T4_CH02_GLO

### Notions utiles

<!-- Variables : {id_theme}=T4; {id_chapitre}=T4_CH02; {ordre_chapitre}=2; {dernier_chapitre_theme}=Non -->

• La France possède un territoire métropolitain et des territoires d’Outre-mer.
• Elle compte 18 régions et 101 départements.
• Ses paysages sont très variés.
• Les grandes villes concentrent les populations et les activités économiques.
• La France est une puissance agricole, industrielle, touristique et maritime.
• Chaque région possède une identité géographique et culturelle particulière.

1. [Terminer le chapitre](SCR_REV_T4_CH02_FIN)

<!-- Chapitre T4_CH02 — source : COURS/THEMATIQUE 4/Chapitre 2/CHAPITRE_2_GEOGRAPHIE.md -->

## SCR_REV_T4_CH02_FIN

### Chapitre terminé

<!-- Variables : {id_theme}=T4; {id_chapitre}=T4_CH02; {ordre_chapitre}=2; {dernier_chapitre_theme}=Non -->

Vous pouvez passer au chapitre suivant ou revenir au menu principal.

1. [Chapitre suivant](SCR_REV_T4_CH03_ACC)
2. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Chapitre T4_CH02 — source : COURS/THEMATIQUE 4/Chapitre 2/CHAPITRE_2_GEOGRAPHIE.md -->

## SCR_REV_T4_CH03_ACC

### Patrimoine et culture française

<!-- Variables : {id_theme}=T4; {id_chapitre}=T4_CH03; {ordre_chapitre}=3; {dernier_chapitre_theme}=Oui -->

<!-- Ce bloc n'est pas renseigné dans le moteur Excel pour T4_CH03:INTRO. -->

<!-- Condition métier : Objectifs disponibles -->
1. [Découvrir les objectifs](SCR_REV_T4_CH03_OBJ)
<!-- Condition métier : Objectifs absents -->
2. [Commencer le cours](SCR_REV_T4_CH03_COURS)
3. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Chapitre T4_CH03 — source : COURS/THEMATIQUE 4/Chapitre 3/CHAPITRE_3_CULTURE.md -->

## SCR_REV_T4_CH03_OBJ

### Objectifs du chapitre

<!-- Variables : {id_theme}=T4; {id_chapitre}=T4_CH03; {ordre_chapitre}=3; {dernier_chapitre_theme}=Oui -->

Découvrir la richesse culturelle de la France, son patrimoine, sa langue, sa gastronomie, ses artistes et les moyens mis en place pour préserver et rendre accessible la culture.

1. [Commencer le cours](SCR_REV_T4_CH03_COURS)

<!-- Chapitre T4_CH03 — source : COURS/THEMATIQUE 4/Chapitre 3/CHAPITRE_3_CULTURE.md -->

## SCR_REV_T4_CH03_COURS

### Patrimoine et culture française

<!-- Variables : {id_theme}=T4; {id_chapitre}=T4_CH03; {ordre_chapitre}=3; {dernier_chapitre_theme}=Oui -->

<!-- Source Markdown attendue : COURS/THEMATIQUE 4/Chapitre 3/CHAPITRE_3_CULTURE.md. Utiliser --content-root pour l'intégrer. -->

<!-- Condition métier : Synthèse disponible -->
1. [Voir la synthèse](SCR_REV_T4_CH03_SYN)
<!-- Condition métier : Synthèse absente ET vigilance disponible -->
2. [Voir les points de vigilance](SCR_REV_T4_CH03_VIG)
<!-- Condition métier : Synthèse et vigilance absentes ET glossaire disponible -->
3. [Consulter les notions utiles](SCR_REV_T4_CH03_GLO)
<!-- Condition métier : Aucun bloc complémentaire disponible -->
4. [Terminer le chapitre](SCR_REV_T4_CH03_FIN)

<!-- Chapitre T4_CH03 — source : COURS/THEMATIQUE 4/Chapitre 3/CHAPITRE_3_CULTURE.md -->

## SCR_REV_T4_CH03_SYN

### À retenir

<!-- Variables : {id_theme}=T4; {id_chapitre}=T4_CH03; {ordre_chapitre}=3; {dernier_chapitre_theme}=Oui -->

La France possède un patrimoine culturel riche et reconnu dans le monde entier.
Ce patrimoine comprend :
• les monuments ;
• les œuvres artistiques ;
• la langue française ;
• les traditions ;
• la gastronomie ;
• les savoir-faire.
La culture française participe au rayonnement international du pays.

<!-- Condition métier : Vigilance disponible -->
1. [Voir les points de vigilance](SCR_REV_T4_CH03_VIG)
<!-- Condition métier : Vigilance absente ET glossaire disponible -->
2. [Consulter les notions utiles](SCR_REV_T4_CH03_GLO)
<!-- Condition métier : Vigilance et glossaire absents -->
3. [Terminer le chapitre](SCR_REV_T4_CH03_FIN)

<!-- Chapitre T4_CH03 — source : COURS/THEMATIQUE 4/Chapitre 3/CHAPITRE_3_CULTURE.md -->

## SCR_REV_T4_CH03_VIG

### Points de vigilance

<!-- Variables : {id_theme}=T4; {id_chapitre}=T4_CH03; {ordre_chapitre}=3; {dernier_chapitre_theme}=Oui -->

❌ Le patrimoine correspond uniquement aux monuments.
✅ Le patrimoine comprend aussi les traditions, les paysages, la langue et les savoir-faire.
❌ La culture française existe seulement en France.
✅ La culture française rayonne dans le monde entier.
❌ La protection du patrimoine concerne uniquement l’État.
✅ Les citoyens, associations et professionnels participent aussi à sa préservation.

<!-- Condition métier : Glossaire disponible -->
1. [Consulter les notions utiles](SCR_REV_T4_CH03_GLO)
<!-- Condition métier : Glossaire absent -->
2. [Terminer le chapitre](SCR_REV_T4_CH03_FIN)

<!-- Chapitre T4_CH03 — source : COURS/THEMATIQUE 4/Chapitre 3/CHAPITRE_3_CULTURE.md -->

## SCR_REV_T4_CH03_GLO

### Notions utiles

<!-- Variables : {id_theme}=T4; {id_chapitre}=T4_CH03; {ordre_chapitre}=3; {dernier_chapitre_theme}=Oui -->

• La France possède une grande influence culturelle mondiale.
• Le patrimoine comprend les monuments, les traditions, la langue et les savoir-faire.
• La langue française est parlée sur les cinq continents.
• La gastronomie française fait partie de l’identité culturelle du pays.
• De nombreux artistes français ont marqué l’histoire mondiale.
• La préservation du patrimoine est l’affaire de tous.
• La culture doit être accessible au plus grand nombre.

1. [Terminer le chapitre](SCR_REV_T4_CH03_FIN)

<!-- Chapitre T4_CH03 — source : COURS/THEMATIQUE 4/Chapitre 3/CHAPITRE_3_CULTURE.md -->

## SCR_REV_T4_CH03_FIN

### Thématique terminée

<!-- Variables : {id_theme}=T4; {id_chapitre}=T4_CH03; {ordre_chapitre}=3; {dernier_chapitre_theme}=Oui -->

Vous avez terminé le dernier chapitre de cette thématique. Vous pouvez maintenant vous entraîner, consulter le glossaire ou revenir au menu principal.

1. [M'entraîner sur cette thématique](SCR_ENT_MENU)
2. [Consulter le glossaire](SCR_GLO_MENU)
3. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Chapitre T4_CH03 — source : COURS/THEMATIQUE 4/Chapitre 3/CHAPITRE_3_CULTURE.md -->

## SCR_REV_T5_MENU

### VIVRE DANS LA SOCIÉTÉ FRANÇAISE 🇫🇷

<!-- Variables : {id_theme}=T5; {titre_theme} -->

### Objectif general

L'objectif de cette thématique est de permettre à l'apprenant de comprendre les principales démarches de la vie quotidienne en France, de connaître le fonctionnement du système de santé, de s'insérer dans le monde professionnel et d'exercer pleinement son rôle de parent dans le respect des valeurs de la République.
À la fin de cette thématique, l'apprenant sera capable de :
• réaliser les principales démarches administratives ;
• comprendre le fonctionnement du système de santé français ;
• connaître les règles essentielles liées à l'emploi ;
• comprendre les droits et les responsabilités des parents ;
• identifier les principaux services publics utiles au quotidien.

<!-- Condition métier : Chapitre actif | Valeur : T5_CH01 -->
1. [Les démarches administratives](SCR_REV_T5_CH01_ACC)
<!-- Condition métier : Chapitre actif | Valeur : T5_CH02 -->
2. [La santé](SCR_REV_T5_CH02_ACC)
<!-- Condition métier : Chapitre actif | Valeur : T5_CH03 -->
3. [L'emploi](SCR_REV_T5_CH03_ACC)
<!-- Condition métier : Chapitre actif | Valeur : T5_CH04 -->
4. [La parentalité](SCR_REV_T5_CH04_ACC)
5. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Source thématique : COURS/THEMATIQUE 5/THEMATIQUE_5_VIVRE_DANS_LA_SOCIETE_FRANCAISE.md -->

## SCR_REV_T5_CH01_ACC

### Les démarches administratives 📄

<!-- Variables : {id_theme}=T5; {id_chapitre}=T5_CH01; {ordre_chapitre}=1; {dernier_chapitre_theme}=Non -->

Les démarches administratives rythment la vie quotidienne.
Elles permettent notamment :
• d'accéder aux droits sociaux ;
• de travailler ;
• de louer un logement ;
• de recevoir un salaire ;
• de bénéficier des services publics.
Certaines démarches sont obligatoires.

<!-- Condition métier : Objectifs disponibles -->
1. [Découvrir les objectifs](SCR_REV_T5_CH01_OBJ)
<!-- Condition métier : Objectifs absents -->
2. [Commencer le cours](SCR_REV_T5_CH01_COURS)
3. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Chapitre T5_CH01 — source : COURS/THEMATIQUE 5/Chapitre 1/CHAPITRE_1_DEMARCHES_ADMINISTRATIVES.md -->

## SCR_REV_T5_CH01_OBJ

### Objectifs du chapitre

<!-- Variables : {id_theme}=T5; {id_chapitre}=T5_CH01; {ordre_chapitre}=1; {dernier_chapitre_theme}=Non -->

Comprendre les principales démarches administratives de la vie quotidienne afin de pouvoir vivre, travailler et exercer ses droits en France.
À la fin de ce chapitre, tu seras capable de :
• connaître les principales démarches administratives ;
• comprendre leur utilité ;
• identifier les documents nécessaires ;
• savoir vers quel organisme se tourner.

1. [Commencer le cours](SCR_REV_T5_CH01_COURS)

<!-- Chapitre T5_CH01 — source : COURS/THEMATIQUE 5/Chapitre 1/CHAPITRE_1_DEMARCHES_ADMINISTRATIVES.md -->

## SCR_REV_T5_CH01_COURS

### Les démarches administratives 📄

<!-- Variables : {id_theme}=T5; {id_chapitre}=T5_CH01; {ordre_chapitre}=1; {dernier_chapitre_theme}=Non -->

<!-- Source Markdown attendue : COURS/THEMATIQUE 5/Chapitre 1/CHAPITRE_1_DEMARCHES_ADMINISTRATIVES.md. Utiliser --content-root pour l'intégrer. -->

<!-- Condition métier : Synthèse disponible -->
1. [Voir la synthèse](SCR_REV_T5_CH01_SYN)
<!-- Condition métier : Synthèse absente ET vigilance disponible -->
2. [Voir les points de vigilance](SCR_REV_T5_CH01_VIG)
<!-- Condition métier : Synthèse et vigilance absentes ET glossaire disponible -->
3. [Consulter les notions utiles](SCR_REV_T5_CH01_GLO)
<!-- Condition métier : Aucun bloc complémentaire disponible -->
4. [Terminer le chapitre](SCR_REV_T5_CH01_FIN)

<!-- Chapitre T5_CH01 — source : COURS/THEMATIQUE 5/Chapitre 1/CHAPITRE_1_DEMARCHES_ADMINISTRATIVES.md -->

## SCR_REV_T5_CH01_SYN

### À retenir

<!-- Variables : {id_theme}=T5; {id_chapitre}=T5_CH01; {ordre_chapitre}=1; {dernier_chapitre_theme}=Non -->

<!-- Ce bloc n'est pas renseigné dans le moteur Excel pour T5_CH01:SYNTHESE. -->

<!-- Condition métier : Vigilance disponible -->
1. [Voir les points de vigilance](SCR_REV_T5_CH01_VIG)
<!-- Condition métier : Vigilance absente ET glossaire disponible -->
2. [Consulter les notions utiles](SCR_REV_T5_CH01_GLO)
<!-- Condition métier : Vigilance et glossaire absents -->
3. [Terminer le chapitre](SCR_REV_T5_CH01_FIN)

<!-- Chapitre T5_CH01 — source : COURS/THEMATIQUE 5/Chapitre 1/CHAPITRE_1_DEMARCHES_ADMINISTRATIVES.md -->

## SCR_REV_T5_CH01_VIG

### Points de vigilance

<!-- Variables : {id_theme}=T5; {id_chapitre}=T5_CH01; {ordre_chapitre}=1; {dernier_chapitre_theme}=Non -->

❌ Une déclaration de revenus est nécessaire uniquement si l'on paie des impôts.
✅ La déclaration peut être obligatoire même lorsqu'aucun impôt n'est dû.
❌ On peut renouveler son titre de séjour après sa date d'expiration sans conséquence.
✅ Il est recommandé d'effectuer la demande avant l'expiration du titre.
❌ Le mariage religieux remplace le mariage civil.
✅ Seul le mariage célébré à la mairie est reconnu par la République française.
❌ Le numéro 112 fonctionne uniquement en France.
✅ Le 112 est le numéro d'urgence commun à toute l'Union européenne.

<!-- Condition métier : Glossaire disponible -->
1. [Consulter les notions utiles](SCR_REV_T5_CH01_GLO)
<!-- Condition métier : Glossaire absent -->
2. [Terminer le chapitre](SCR_REV_T5_CH01_FIN)

<!-- Chapitre T5_CH01 — source : COURS/THEMATIQUE 5/Chapitre 1/CHAPITRE_1_DEMARCHES_ADMINISTRATIVES.md -->

## SCR_REV_T5_CH01_GLO

### Notions utiles

<!-- Variables : {id_theme}=T5; {id_chapitre}=T5_CH01; {ordre_chapitre}=1; {dernier_chapitre_theme}=Non -->

Une adresse stable est indispensable pour accéder à de nombreux droits.

1. [Terminer le chapitre](SCR_REV_T5_CH01_FIN)

<!-- Chapitre T5_CH01 — source : COURS/THEMATIQUE 5/Chapitre 1/CHAPITRE_1_DEMARCHES_ADMINISTRATIVES.md -->

## SCR_REV_T5_CH01_FIN

### Chapitre terminé

<!-- Variables : {id_theme}=T5; {id_chapitre}=T5_CH01; {ordre_chapitre}=1; {dernier_chapitre_theme}=Non -->

Vous pouvez passer au chapitre suivant ou revenir au menu principal.

1. [Chapitre suivant](SCR_REV_T5_CH02_ACC)
2. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Chapitre T5_CH01 — source : COURS/THEMATIQUE 5/Chapitre 1/CHAPITRE_1_DEMARCHES_ADMINISTRATIVES.md -->

## SCR_REV_T5_CH02_ACC

### La santé 🩺

<!-- Variables : {id_theme}=T5; {id_chapitre}=T5_CH02; {ordre_chapitre}=2; {dernier_chapitre_theme}=Non -->

La santé est un droit fondamental.
En France, chacun peut bénéficier d'un accès aux soins grâce à un système de santé organisé autour de l'Assurance Maladie et des professionnels de santé.

<!-- Condition métier : Objectifs disponibles -->
1. [Découvrir les objectifs](SCR_REV_T5_CH02_OBJ)
<!-- Condition métier : Objectifs absents -->
2. [Commencer le cours](SCR_REV_T5_CH02_COURS)
3. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Chapitre T5_CH02 — source : COURS/THEMATIQUE 5/Chapitre 2/CHAPITRE_2_SANTE.md -->

## SCR_REV_T5_CH02_OBJ

### Objectifs du chapitre

<!-- Variables : {id_theme}=T5; {id_chapitre}=T5_CH02; {ordre_chapitre}=2; {dernier_chapitre_theme}=Non -->

Comprendre le fonctionnement du système de santé français afin de savoir accéder aux soins, connaître ses droits et adopter les bons réflexes pour préserver sa santé.
À la fin de ce chapitre, tu seras capable de :
• comprendre l'organisation du système de santé ;
• connaître le rôle des principaux professionnels de santé ;
• savoir comment accéder aux soins ;
• identifier les situations d'urgence.

1. [Commencer le cours](SCR_REV_T5_CH02_COURS)

<!-- Chapitre T5_CH02 — source : COURS/THEMATIQUE 5/Chapitre 2/CHAPITRE_2_SANTE.md -->

## SCR_REV_T5_CH02_COURS

### La santé 🩺

<!-- Variables : {id_theme}=T5; {id_chapitre}=T5_CH02; {ordre_chapitre}=2; {dernier_chapitre_theme}=Non -->

<!-- Source Markdown attendue : COURS/THEMATIQUE 5/Chapitre 2/CHAPITRE_2_SANTE.md. Utiliser --content-root pour l'intégrer. -->

<!-- Condition métier : Synthèse disponible -->
1. [Voir la synthèse](SCR_REV_T5_CH02_SYN)
<!-- Condition métier : Synthèse absente ET vigilance disponible -->
2. [Voir les points de vigilance](SCR_REV_T5_CH02_VIG)
<!-- Condition métier : Synthèse et vigilance absentes ET glossaire disponible -->
3. [Consulter les notions utiles](SCR_REV_T5_CH02_GLO)
<!-- Condition métier : Aucun bloc complémentaire disponible -->
4. [Terminer le chapitre](SCR_REV_T5_CH02_FIN)

<!-- Chapitre T5_CH02 — source : COURS/THEMATIQUE 5/Chapitre 2/CHAPITRE_2_SANTE.md -->

## SCR_REV_T5_CH02_SYN

### À retenir

<!-- Variables : {id_theme}=T5; {id_chapitre}=T5_CH02; {ordre_chapitre}=2; {dernier_chapitre_theme}=Non -->

<!-- Ce bloc n'est pas renseigné dans le moteur Excel pour T5_CH02:SYNTHESE. -->

<!-- Condition métier : Vigilance disponible -->
1. [Voir les points de vigilance](SCR_REV_T5_CH02_VIG)
<!-- Condition métier : Vigilance absente ET glossaire disponible -->
2. [Consulter les notions utiles](SCR_REV_T5_CH02_GLO)
<!-- Condition métier : Vigilance et glossaire absents -->
3. [Terminer le chapitre](SCR_REV_T5_CH02_FIN)

<!-- Chapitre T5_CH02 — source : COURS/THEMATIQUE 5/Chapitre 2/CHAPITRE_2_SANTE.md -->

## SCR_REV_T5_CH02_VIG

### Points de vigilance

<!-- Variables : {id_theme}=T5; {id_chapitre}=T5_CH02; {ordre_chapitre}=2; {dernier_chapitre_theme}=Non -->

❌ Aller directement aux urgences pour un simple rhume.
✅ En cas de problème courant, il est préférable de consulter son médecin traitant.
❌ La carte Vitale permet de consulter gratuitement tous les médecins.
✅ Elle facilite les remboursements, mais certains soins peuvent rester partiellement à la charge du patient.
❌ L'Assurance Maladie et la mutuelle sont la même chose.
✅ La mutuelle complète les remboursements de l'Assurance Maladie.
❌ Le pharmacien est uniquement un vendeur de médicaments.
✅ Le pharmacien est un professionnel de santé qui conseille les patients et délivre les médicaments.
❌ La vaccination protège uniquement la personne vaccinée.
✅ Elle contribue également à protéger l'ensemble de la population.

<!-- Condition métier : Glossaire disponible -->
1. [Consulter les notions utiles](SCR_REV_T5_CH02_GLO)
<!-- Condition métier : Glossaire absent -->
2. [Terminer le chapitre](SCR_REV_T5_CH02_FIN)

<!-- Chapitre T5_CH02 — source : COURS/THEMATIQUE 5/Chapitre 2/CHAPITRE_2_SANTE.md -->

## SCR_REV_T5_CH02_GLO

### Notions utiles

<!-- Variables : {id_theme}=T5; {id_chapitre}=T5_CH02; {ordre_chapitre}=2; {dernier_chapitre_theme}=Non -->

Le médecin traitant est le premier interlocuteur en cas de problème de santé.

1. [Terminer le chapitre](SCR_REV_T5_CH02_FIN)

<!-- Chapitre T5_CH02 — source : COURS/THEMATIQUE 5/Chapitre 2/CHAPITRE_2_SANTE.md -->

## SCR_REV_T5_CH02_FIN

### Chapitre terminé

<!-- Variables : {id_theme}=T5; {id_chapitre}=T5_CH02; {ordre_chapitre}=2; {dernier_chapitre_theme}=Non -->

Vous pouvez passer au chapitre suivant ou revenir au menu principal.

1. [Chapitre suivant](SCR_REV_T5_CH03_ACC)
2. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Chapitre T5_CH02 — source : COURS/THEMATIQUE 5/Chapitre 2/CHAPITRE_2_SANTE.md -->

## SCR_REV_T5_CH03_ACC

### L'emploi 💼

<!-- Variables : {id_theme}=T5; {id_chapitre}=T5_CH03; {ordre_chapitre}=3; {dernier_chapitre_theme}=Non -->

Le travail permet de participer à la vie économique, de développer ses compétences et de construire son projet professionnel.
En France, le droit du travail protège les salariés tout en définissant leurs obligations.

<!-- Condition métier : Objectifs disponibles -->
1. [Découvrir les objectifs](SCR_REV_T5_CH03_OBJ)
<!-- Condition métier : Objectifs absents -->
2. [Commencer le cours](SCR_REV_T5_CH03_COURS)
3. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Chapitre T5_CH03 — source : COURS/THEMATIQUE 5/Chapitre 3/CHAPITRE_3_EMPLOI.md -->

## SCR_REV_T5_CH03_OBJ

### Objectifs du chapitre

<!-- Variables : {id_theme}=T5; {id_chapitre}=T5_CH03; {ordre_chapitre}=3; {dernier_chapitre_theme}=Non -->

Comprendre le fonctionnement du monde du travail en France afin de connaître ses droits, ses devoirs et les principaux dispositifs favorisant l'insertion professionnelle.
À la fin de ce chapitre, tu seras capable de :
• comprendre le fonctionnement du marché du travail ;
• connaître les principaux contrats de travail ;
• identifier les organismes qui accompagnent les demandeurs d'emploi ;
• connaître les droits et obligations du salarié ;
• comprendre les dispositifs de formation professionnelle.

1. [Commencer le cours](SCR_REV_T5_CH03_COURS)

<!-- Chapitre T5_CH03 — source : COURS/THEMATIQUE 5/Chapitre 3/CHAPITRE_3_EMPLOI.md -->

## SCR_REV_T5_CH03_COURS

### L'emploi 💼

<!-- Variables : {id_theme}=T5; {id_chapitre}=T5_CH03; {ordre_chapitre}=3; {dernier_chapitre_theme}=Non -->

<!-- Source Markdown attendue : COURS/THEMATIQUE 5/Chapitre 3/CHAPITRE_3_EMPLOI.md. Utiliser --content-root pour l'intégrer. -->

<!-- Condition métier : Synthèse disponible -->
1. [Voir la synthèse](SCR_REV_T5_CH03_SYN)
<!-- Condition métier : Synthèse absente ET vigilance disponible -->
2. [Voir les points de vigilance](SCR_REV_T5_CH03_VIG)
<!-- Condition métier : Synthèse et vigilance absentes ET glossaire disponible -->
3. [Consulter les notions utiles](SCR_REV_T5_CH03_GLO)
<!-- Condition métier : Aucun bloc complémentaire disponible -->
4. [Terminer le chapitre](SCR_REV_T5_CH03_FIN)

<!-- Chapitre T5_CH03 — source : COURS/THEMATIQUE 5/Chapitre 3/CHAPITRE_3_EMPLOI.md -->

## SCR_REV_T5_CH03_SYN

### À retenir

<!-- Variables : {id_theme}=T5; {id_chapitre}=T5_CH03; {ordre_chapitre}=3; {dernier_chapitre_theme}=Non -->

<!-- Ce bloc n'est pas renseigné dans le moteur Excel pour T5_CH03:SYNTHESE. -->

<!-- Condition métier : Vigilance disponible -->
1. [Voir les points de vigilance](SCR_REV_T5_CH03_VIG)
<!-- Condition métier : Vigilance absente ET glossaire disponible -->
2. [Consulter les notions utiles](SCR_REV_T5_CH03_GLO)
<!-- Condition métier : Vigilance et glossaire absents -->
3. [Terminer le chapitre](SCR_REV_T5_CH03_FIN)

<!-- Chapitre T5_CH03 — source : COURS/THEMATIQUE 5/Chapitre 3/CHAPITRE_3_EMPLOI.md -->

## SCR_REV_T5_CH03_VIG

### Points de vigilance

<!-- Variables : {id_theme}=T5; {id_chapitre}=T5_CH03; {ordre_chapitre}=3; {dernier_chapitre_theme}=Non -->

❌ Le CDI possède une date de fin.
✅ Le CDI est un contrat à durée indéterminée.
❌ Le CDD peut être utilisé dans toutes les situations.
✅ Le CDD est réservé aux cas prévus par la loi.
❌ Le CPF est réservé aux étudiants.
✅ Le CPF est ouvert aux actifs pour financer des formations.
❌ L'inspection du travail défend uniquement les employeurs.
✅ Elle veille au respect du Code du travail pour tous.
❌ France Travail trouve automatiquement un emploi.
✅ France Travail accompagne les demandeurs d'emploi et propose des services, mais la recherche d'emploi reste une démarche active.

<!-- Condition métier : Glossaire disponible -->
1. [Consulter les notions utiles](SCR_REV_T5_CH03_GLO)
<!-- Condition métier : Glossaire absent -->
2. [Terminer le chapitre](SCR_REV_T5_CH03_FIN)

<!-- Chapitre T5_CH03 — source : COURS/THEMATIQUE 5/Chapitre 3/CHAPITRE_3_EMPLOI.md -->

## SCR_REV_T5_CH03_GLO

### Notions utiles

<!-- Variables : {id_theme}=T5; {id_chapitre}=T5_CH03; {ordre_chapitre}=3; {dernier_chapitre_theme}=Non -->

France Travail accompagne les demandeurs d'emploi et favorise leur insertion professionnelle.

1. [Terminer le chapitre](SCR_REV_T5_CH03_FIN)

<!-- Chapitre T5_CH03 — source : COURS/THEMATIQUE 5/Chapitre 3/CHAPITRE_3_EMPLOI.md -->

## SCR_REV_T5_CH03_FIN

### Chapitre terminé

<!-- Variables : {id_theme}=T5; {id_chapitre}=T5_CH03; {ordre_chapitre}=3; {dernier_chapitre_theme}=Non -->

Vous pouvez passer au chapitre suivant ou revenir au menu principal.

1. [Chapitre suivant](SCR_REV_T5_CH04_ACC)
2. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Chapitre T5_CH03 — source : COURS/THEMATIQUE 5/Chapitre 3/CHAPITRE_3_EMPLOI.md -->

## SCR_REV_T5_CH04_ACC

### La parentalité 👨‍👩‍👧

<!-- Variables : {id_theme}=T5; {id_chapitre}=T5_CH04; {ordre_chapitre}=4; {dernier_chapitre_theme}=Oui -->

En France, les parents jouent un rôle essentiel dans :
• la protection de leur enfant ;
• son éducation ;
• sa santé ;
• sa réussite scolaire.
L'école et les familles travaillent ensemble dans l'intérêt de l'enfant.

<!-- Condition métier : Objectifs disponibles -->
1. [Découvrir les objectifs](SCR_REV_T5_CH04_OBJ)
<!-- Condition métier : Objectifs absents -->
2. [Commencer le cours](SCR_REV_T5_CH04_COURS)
3. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Chapitre T5_CH04 — source : COURS/THEMATIQUE 5/Chapitre 4/CHAPITRE_4_PARENTALITE.md -->

## SCR_REV_T5_CH04_OBJ

### Objectifs du chapitre

<!-- Variables : {id_theme}=T5; {id_chapitre}=T5_CH04; {ordre_chapitre}=4; {dernier_chapitre_theme}=Oui -->

Comprendre les droits de l'enfant, les responsabilités des parents et le fonctionnement du système éducatif français afin d'accompagner son enfant dans son développement et sa scolarité.
À la fin de ce chapitre, tu seras capable de :
• connaître les droits fondamentaux de l'enfant ;
• comprendre les responsabilités des parents ;
• connaître les principales étapes de la scolarité en France ;
• participer à la vie scolaire de ton enfant.

1. [Commencer le cours](SCR_REV_T5_CH04_COURS)

<!-- Chapitre T5_CH04 — source : COURS/THEMATIQUE 5/Chapitre 4/CHAPITRE_4_PARENTALITE.md -->

## SCR_REV_T5_CH04_COURS

### La parentalité 👨‍👩‍👧

<!-- Variables : {id_theme}=T5; {id_chapitre}=T5_CH04; {ordre_chapitre}=4; {dernier_chapitre_theme}=Oui -->

<!-- Source Markdown attendue : COURS/THEMATIQUE 5/Chapitre 4/CHAPITRE_4_PARENTALITE.md. Utiliser --content-root pour l'intégrer. -->

<!-- Condition métier : Synthèse disponible -->
1. [Voir la synthèse](SCR_REV_T5_CH04_SYN)
<!-- Condition métier : Synthèse absente ET vigilance disponible -->
2. [Voir les points de vigilance](SCR_REV_T5_CH04_VIG)
<!-- Condition métier : Synthèse et vigilance absentes ET glossaire disponible -->
3. [Consulter les notions utiles](SCR_REV_T5_CH04_GLO)
<!-- Condition métier : Aucun bloc complémentaire disponible -->
4. [Terminer le chapitre](SCR_REV_T5_CH04_FIN)

<!-- Chapitre T5_CH04 — source : COURS/THEMATIQUE 5/Chapitre 4/CHAPITRE_4_PARENTALITE.md -->

## SCR_REV_T5_CH04_SYN

### À retenir

<!-- Variables : {id_theme}=T5; {id_chapitre}=T5_CH04; {ordre_chapitre}=4; {dernier_chapitre_theme}=Oui -->

<!-- Ce bloc n'est pas renseigné dans le moteur Excel pour T5_CH04:SYNTHESE. -->

<!-- Condition métier : Vigilance disponible -->
1. [Voir les points de vigilance](SCR_REV_T5_CH04_VIG)
<!-- Condition métier : Vigilance absente ET glossaire disponible -->
2. [Consulter les notions utiles](SCR_REV_T5_CH04_GLO)
<!-- Condition métier : Vigilance et glossaire absents -->
3. [Terminer le chapitre](SCR_REV_T5_CH04_FIN)

<!-- Chapitre T5_CH04 — source : COURS/THEMATIQUE 5/Chapitre 4/CHAPITRE_4_PARENTALITE.md -->

## SCR_REV_T5_CH04_VIG

### Points de vigilance

<!-- Variables : {id_theme}=T5; {id_chapitre}=T5_CH04; {ordre_chapitre}=4; {dernier_chapitre_theme}=Oui -->

❌ Les parents peuvent décider de ne pas scolariser leur enfant.
✅ L'instruction est obligatoire de 3 à 16 ans selon les règles prévues par la loi.
❌ L'autorité parentale donne tous les pouvoirs aux parents.
✅ Elle doit toujours être exercée dans l'intérêt de l'enfant et dans le respect de ses droits.
❌ Seuls les enseignants sont responsables de l'éducation.
✅ L'éducation est une responsabilité partagée entre les parents et l'école.
❌ Le brevet est obligatoire pour entrer au lycée.
✅ Le brevet est un diplôme de fin de collège, mais il n'est pas une condition d'accès au lycée.
❌ Le numéro 119 est réservé uniquement aux professionnels.
✅ Toute personne peut signaler une situation préoccupante concernant un enfant.

<!-- Condition métier : Glossaire disponible -->
1. [Consulter les notions utiles](SCR_REV_T5_CH04_GLO)
<!-- Condition métier : Glossaire absent -->
2. [Terminer le chapitre](SCR_REV_T5_CH04_FIN)

<!-- Chapitre T5_CH04 — source : COURS/THEMATIQUE 5/Chapitre 4/CHAPITRE_4_PARENTALITE.md -->

## SCR_REV_T5_CH04_GLO

### Notions utiles

<!-- Variables : {id_theme}=T5; {id_chapitre}=T5_CH04; {ordre_chapitre}=4; {dernier_chapitre_theme}=Oui -->

Tous les enfants bénéficient des mêmes droits, sans discrimination.

1. [Terminer le chapitre](SCR_REV_T5_CH04_FIN)

<!-- Chapitre T5_CH04 — source : COURS/THEMATIQUE 5/Chapitre 4/CHAPITRE_4_PARENTALITE.md -->

## SCR_REV_T5_CH04_FIN

### Thématique terminée

<!-- Variables : {id_theme}=T5; {id_chapitre}=T5_CH04; {ordre_chapitre}=4; {dernier_chapitre_theme}=Oui -->

Vous avez terminé le dernier chapitre de cette thématique. Vous pouvez maintenant vous entraîner, consulter le glossaire ou revenir au menu principal.

1. [M'entraîner sur cette thématique](SCR_ENT_MENU)
2. [Consulter le glossaire](SCR_GLO_MENU)
3. [Retour au menu principal](MENU_PRINCIPAL)

<!-- Chapitre T5_CH04 — source : COURS/THEMATIQUE 5/Chapitre 4/CHAPITRE_4_PARENTALITE.md -->

<!-- Fin du fichier source : modules\03_revisions.md -->
