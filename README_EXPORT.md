# Export ChatMD — Coach Civique NovaFrate

## Fichier à ouvrir dans ChatMD

`chat_bot.md`

## Organisation

- `modules/` : écrans générés depuis les onglets 00 et 90 à 98 ;
- `data/` : CSV et JSON intermédiaires ;
- `reports/` : contrôles de cohérence ;
- `manifest.json` : résumé de l’export.

## Contrôle avant publication

- Erreurs : **0**
- Avertissements : **207**

Consultez `reports/validation_report.md` avant de déposer les fichiers sur GitHub.

## Fichiers de modules

- `modules\start.md`
- `modules\00_accueil_complements.md`
- `modules\02_bilan.md`
- `modules\08_conseils.md`
- `modules\09_faq.md`
- `modules\04_glossaire.md`
- `modules\06_entrainement.md`
- `modules\07_passer_examen.md`
- `modules\05_preparer_examen.md`
- `modules\10_question_libre.md`
- `modules\03_revisions.md`

## Fichiers de données

- `data\faq.csv`
- `data\glossaire.csv`
- `data\intentions.csv`
- `data\entites.csv`
- `data\sessions.json`
- `data\variables.json`

## Publication GitHub

1. Déposer le contenu du dossier d’export dans le dépôt.
2. Utiliser les URL `raw.githubusercontent.com` dans les inclusions ChatMD.
3. Tester le menu principal, puis chaque module.
4. Tester particulièrement le module 07 et la question libre.
