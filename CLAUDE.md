# CLAUDE.md

Consignes pour Claude Code dans `candidature-edai/`. Le contexte, la structure de la page et la procédure de mise à jour des données sont dans `README.md` : le lire avant toute modification.

## Le projet

Une page unique, `index.html`, jointe à la candidature de Rémi chez Ed.ai. Ses lecteurs sont l'équipe Ed.ai : chaque modification doit tenir devant eux.

## Règles

- **Un seul fichier, sans build.** Styles, données et scripts restent dans `index.html`. Seule dépendance : Leaflet 1.9.4, chargé depuis cdnjs, pour la carte ; pas d'autre framework. La page doit fonctionner ouverte en double-clic : pas de `fetch` vers un fichier local.
- **Charte d'Ed.ai, sans logo.** Le système visuel est décrit dans `DESIGN.md` (couleurs, typos Figtree et Inter, formes) et le contexte produit dans `PRODUCT.md`. Ne jamais ajouter le logo d'Ed.ai : la page doit rester visiblement celle de Rémi.
- **Français, vouvoiement** envers l'équipe Ed.ai (« vos bureaux », « vos inscrits »). Phrases courtes, chiffres précis, pas de superlatifs.
- **Couleurs uniquement via les tokens** de `:root`. Une nouvelle couleur se déclare dans les trois blocs : clair, `@media (prefers-color-scheme: dark)` et `:root[data-theme="dark"]`. Les points de la carte lisent les tokens avec `css("--…")` (fonctions `dotStyle` et `restyle`) : pas de couleur en dur dans le JavaScript.
- **`DATA` et `S` viennent du script.** Ils ne se modifient jamais à la main : changer `scripts/construire_liste.py` puis le relancer avec `--html index.html` (procédure dans le README). Après une modification du script, vérifier que les chiffres ne bougent pas sans raison. Quand un chiffre change, relire les textes écrits en dur listés dans le README.
- **Le fichier CRM et le script sont téléchargeables depuis la page.** Garder leurs liens, et la taille affichée, à jour.
- **Pas de données de contact nominatives** (chefs d'établissement, e-mails, téléphones) : la page cible des établissements, pas des personnes (RGPD).

## Vérifier une modification

Aperçu `candidature-edai` (`.claude/launch.json` à la racine de l'espace de travail). Contrôler : console sans erreur, mode clair et mode sombre, largeur 375 px sans défilement horizontal de la page, onglets et filtre de la liste, clic sur un point de la carte (fiche) et sur un nom de la liste (la carte se déplace).
