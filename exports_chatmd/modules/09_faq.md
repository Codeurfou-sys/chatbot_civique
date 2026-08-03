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
