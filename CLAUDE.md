# CLAUDE.md

Consignes pour Claude Code dans `candidature-edai/`. Le contexte, la structure de la page et la procédure de mise à jour des données sont dans `README.md` : le lire avant toute modification.

## Le projet

Une page unique, `index.html`, jointe à la candidature de Rémi chez Ed.ai. Ses lecteurs sont l'équipe Ed.ai : chaque modification doit tenir devant eux.

## Règles

- **Un seul fichier, sans build.** Styles, données et scripts restent dans `index.html`, sans framework ni dépendance ajoutée. La page doit fonctionner ouverte en double-clic : pas de `fetch` vers un fichier local.
- **Français, vouvoiement** envers l'équipe Ed.ai (« vos bureaux », « vos inscrits »). Phrases courtes, chiffres précis, pas de superlatifs.
- **Couleurs uniquement via les tokens** de `:root`. Une nouvelle couleur se déclare dans les trois blocs : clair, `@media (prefers-color-scheme: dark)` et `:root[data-theme="dark"]`. Le canvas lit les tokens avec `css("--…")` : pas de couleur en dur dans `draw()`.
- **`DATA` et `S` vont ensemble.** Aucun chiffre de `S` ne se modifie à la main sans être recalculé depuis `DATA` (contrôles listés dans le README). Quand un chiffre change, relire les textes écrits en dur listés dans le README.
- **Pas de données de contact nominatives** (chefs d'établissement, e-mails, téléphones) : la page cible des établissements, pas des personnes (RGPD).

## Vérifier une modification

Aperçu `candidature-edai` (`.claude/launch.json` à la racine de l'espace de travail). Contrôler : console sans erreur, mode clair et mode sombre, largeur 375 px sans défilement horizontal de la page, onglets et filtre de la liste, survol de la carte.
