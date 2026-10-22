---
name: Ed.ai — Privé académie de Lyon
description: Étude de candidature aux couleurs de la charte d'Ed.ai (ed.ai/fr), relevée le 21/10/2026, mise à jour après la revue de finition du 22/10/2026
colors:
  edai-violet: "#5e58f4"
  edai-cyan: "#02b3ff"
  cyan-ink: "#00719f"
  aubergine: "#291846"
  body-ink: "#2b2541"
  slate-muted: "#5f6480"
  lavender: "#efefff"
  lavender-deep: "#e3dfff"
  hairline: "#e7e5f6"
  paper: "#ffffff"
  dot-lilac: "#a9a5e4"
  ring-lilac: "#8d88c9"
  violet-tint: "rgba(94,88,244,.10)"
  cyan-tint: "rgba(2,179,255,.12)"
  seyes-line: "rgba(94,88,244,.07)"
  seyes-major: "rgba(94,88,244,.16)"
  margin-rule: "rgba(203,102,226,.55)"
  glow-blue: "rgba(0,128,255,.11)"
  glow-orchid: "rgba(203,102,226,.18)"
  night-bg: "#120c22"
  night-surface: "#1a1330"
  night-lavender: "#1f1838"
  night-lavender-deep: "#2d2452"
  night-hairline: "#2a2246"
  night-ink: "#f3f1ff"
  night-text: "#dedbf3"
  night-muted: "#a8a5c6"
  night-violet: "#8f8aff"
  night-cyan: "#3cc7ff"
  night-cyan-ink: "#6fd6ff"
  night-dot: "#5c5694"
  night-ring: "#7d78b8"
typography:
  display:
    fontFamily: "Figtree, Segoe UI, system-ui, sans-serif"
    fontSize: "clamp(34px, 5.4vw, 58px)"
    fontWeight: 600
    lineHeight: 1.06
    letterSpacing: "-0.02em"
  headline:
    fontFamily: "Figtree, Segoe UI, system-ui, sans-serif"
    fontSize: "clamp(26px, 3.2vw, 34px)"
    fontWeight: 600
    lineHeight: 1.15
    letterSpacing: "-0.015em"
  kpi-value:
    fontFamily: "Figtree, Segoe UI, system-ui, sans-serif"
    fontSize: "clamp(28px, 3.6vw, 40px)"
    fontWeight: 600
    lineHeight: 1.05
    letterSpacing: "-0.02em"
    fontFeature: "tnum"
  title:
    fontFamily: "Figtree, Segoe UI, system-ui, sans-serif"
    fontSize: "17px"
    fontWeight: 600
    lineHeight: 1.3
  lede:
    fontFamily: "Inter, system-ui, sans-serif"
    fontSize: "18px"
    fontWeight: 400
    lineHeight: 1.6
  body:
    fontFamily: "Inter, system-ui, sans-serif"
    fontSize: "16px"
    fontWeight: 400
    lineHeight: 1.6
  data:
    fontFamily: "Inter, system-ui, sans-serif"
    fontSize: "15px"
    fontWeight: 400
    lineHeight: 1.4
  secondary:
    fontFamily: "Inter, system-ui, sans-serif"
    fontSize: "14px"
    fontWeight: 400
    lineHeight: 1.45
  label:
    fontFamily: "Inter, system-ui, sans-serif"
    fontSize: "13px"
    fontWeight: 600
  caption:
    fontFamily: "Inter, system-ui, sans-serif"
    fontSize: "12px"
    fontWeight: 500
  pin-numeral:
    fontFamily: "Figtree, Segoe UI, system-ui, sans-serif"
    fontSize: "11px"
    fontWeight: 700
    lineHeight: 1
  annotation:
    fontFamily: "Kalam, Segoe Print, cursive"
    fontSize: "22px"
    fontWeight: 400
    lineHeight: 1.3
rounded:
  pill: "999px"
  panel: "24px"
  card: "20px"
  popup: "18px"
  row: "16px"
  control: "14px"
  tooltip: "10px"
  marker: "4px"
spacing:
  section: "72px"
  gutter: "16px"
  hero-indent: "24px"
  seyes-line: "8px"
  seyes-major: "32px"
components:
  tab-active:
    backgroundColor: "{colors.edai-violet}"
    textColor: "{colors.paper}"
    rounded: "{rounded.pill}"
    padding: "10px 18px"
  tab:
    backgroundColor: "{colors.lavender}"
    textColor: "{colors.aubergine}"
    typography: "{typography.secondary}"
    rounded: "{rounded.pill}"
    padding: "10px 18px"
  search-field:
    backgroundColor: "{colors.paper}"
    textColor: "{colors.body-ink}"
    typography: "{typography.data}"
    rounded: "{rounded.pill}"
    padding: "10px 18px"
  chip:
    backgroundColor: "{colors.lavender}"
    textColor: "{colors.body-ink}"
    typography: "{typography.label}"
    rounded: "{rounded.pill}"
    padding: "7px 14px"
  kpi-panel:
    backgroundColor: "{colors.lavender}"
    rounded: "{rounded.panel}"
    padding: "8px"
  table-frame:
    backgroundColor: "{colors.paper}"
    typography: "{typography.data}"
    rounded: "{rounded.card}"
  pill:
    backgroundColor: "{colors.lavender}"
    textColor: "{colors.body-ink}"
    typography: "{typography.caption}"
    rounded: "{rounded.pill}"
    padding: "3px 10px"
  pill-both:
    backgroundColor: "{colors.violet-tint}"
    textColor: "{colors.edai-violet}"
    typography: "{typography.caption}"
    rounded: "{rounded.pill}"
    padding: "3px 10px"
  pill-client:
    backgroundColor: "{colors.cyan-tint}"
    textColor: "{colors.cyan-ink}"
    typography: "{typography.caption}"
    rounded: "{rounded.pill}"
    padding: "3px 10px"
  download-row:
    backgroundColor: "{colors.lavender}"
    rounded: "{rounded.row}"
    padding: "14px 16px"
  map-popup:
    backgroundColor: "{colors.paper}"
    textColor: "{colors.body-ink}"
    rounded: "{rounded.popup}"
    padding: "18px 20px 16px"
  map-tooltip:
    backgroundColor: "{colors.aubergine}"
    textColor: "{colors.paper}"
    typography: "{typography.label}"
    rounded: "{rounded.tooltip}"
    padding: "6px 10px"
  zoom-control:
    backgroundColor: "{colors.paper}"
    textColor: "{colors.aubergine}"
    rounded: "{rounded.control}"
  pin-top:
    backgroundColor: "{colors.edai-violet}"
    textColor: "{colors.paper}"
    typography: "{typography.pin-numeral}"
    rounded: "{rounded.pill}"
    size: "20px"
  office-marker:
    backgroundColor: "{colors.aubergine}"
    rounded: "{rounded.marker}"
    size: "14px"
  office-label:
    backgroundColor: "{colors.paper}"
    textColor: "{colors.aubergine}"
    rounded: "{rounded.pill}"
    padding: "3px 9px"
---

# Design System: Ed.ai — Privé académie de Lyon

## Overview

**Creative North Star : « La copie corrigée aux couleurs d'Ed.ai »**

La page reprend la langue visuelle d'ed.ai (« Faire de chaque copie un tremplin ») pour présenter une étude de prospection. Fond blanc baigné de halos lavande, titres Figtree aubergine, violet Ed.ai pour tout ce qui agit ou compte. Le souvenir de la copie d'élève tient dans l'en-tête : une réglure Seyès légère (interligne fin toutes les 8 px, ligne forte toutes les 32 px, colonnes de 32 px), un trait de marge vertical sur toute la hauteur, et une seule annotation manuscrite en violet.

La page reste celle de Rémi, adressée à l'équipe Ed.ai : pas de logo Ed.ai, signature en pied de page (voir PRODUCT.md). Chaque couleur existe en deux thèmes, clair et sombre, déclarée dans `:root` et dans les deux blocs sombres.

**Key Characteristics:**
- Halos d'ed.ai, bleu en haut à gauche et violet rosé à droite, peints sous l'en-tête et débordant sous la bande des chiffres.
- Réglure Seyès à deux intensités et trait de marge rosé, fondus en haut et en bas par un masque.
- Violet pour les actions, le top 25 et les liens ; cyan réservé aux clients probables.
- Pilules pour tout ce qui se clique, panneaux lavande arrondis pour ce qui se lit.
- Plan OpenStreetMap désaturé par filtre CSS, jamais par transparence.

## Colors

Une palette lavande et violette, froide, sur blanc, avec un aubergine profond pour l'encre des titres ; en sombre, une nuit violette où le violet et le cyan s'éclaircissent.

### Primary
- **Violet Ed.ai** (#5e58f4, relevé sur ed.ai/fr) : boutons actifs, pastilles du top 25 sur la carte, rangs de la liste, liens, chiffres mis en avant, annotation manuscrite, anneau de focus. Contraste 5:1 sur blanc, utilisable en texte. Sa teinte à 10 % (**Voile violet**) marque la ligne sélectionnée et la pilule « Top 25 ».

### Secondary
- **Cyan Ed.ai** (#02b3ff, relevé sur ed.ai/fr) : points des clients probables, fin du dégradé du titre. Jamais en texte sur fond clair ; le texte cyan passe par **Cyan encre** (#00719f), sur un **Voile cyan** à 12 %.

### Neutral
- **Aubergine** (#291846, relevé sur ed.ai/fr) : titres, valeurs des chiffres clés, fond des infobulles, losange des bureaux.
- **Encre texte** (#2b2541) : texte courant.
- **Ardoise** (#5f6480) : texte secondaire, légendes, en-têtes de tableau, étiquettes des cercles.
- **Lavande** (#efefff) et **Lavande profonde** (#e3dfff), relevées sur ed.ai/fr : panneaux, onglets inactifs, filtres, survols, fond de carte ; la lavande profonde sépare les cellules des chiffres et borde le champ de recherche.
- **Filet** (#e7e5f6) : bordures et séparateurs.
- **Lilas** (#a9a5e4) : disques des comptes hors top 25. **Lilas des cercles** (#8d88c9) : cercles de 20 et 50 km en pointillés.
- **Matières de l'en-tête** : interligne Seyès (violet à 7 %), ligne forte (violet à 16 %), trait de marge (orchidée à 55 %), halos bleu (11 %) et orchidée (18 %).

### Mode sombre
Chaque jeton clair a son pendant nocturne : fond Nuit, surfaces, lavandes et filet sombres, encres claires (titres, texte, secondaire), violet éclairci, cyan et cyan encre éclaircis, lilas des points et des cercles assombris (valeurs `night-*` du frontmatter). Sur violet, le texte passe en encre de nuit. Les voiles, la réglure, la marge et les halos gardent leur teinte avec une opacité ajustée ; l'infobulle s'inverse (lavande, encre aubergine) ; le plan est inversé et assombri par le même filtre.

### Named Rules
**La règle du cyan rare.** Le cyan ne désigne que les clients probables (et la fin du dégradé du titre). Un deuxième usage brouillerait la légende de la carte.

**La règle du dégradé unique.** Le dégradé violet→cyan en texte est la signature d'ed.ai : il n'apparaît qu'une fois, sur le chiffre du titre, avec un repli `CanvasText` en couleurs forcées.

**La règle des trois blocs.** Une couleur n'existe que comme jeton de `:root`, redéfinie dans `@media (prefers-color-scheme: dark)` et dans `:root[data-theme="dark"]`. Le JavaScript de la carte lit ces jetons ; aucune couleur en dur.

## Typography

**Display Font:** Figtree (repli Segoe UI, system-ui)
**Body Font:** Inter (repli system-ui)
**Annotation:** Kalam, une seule fois par page

**Character :** les deux faces d'ed.ai, telles quelles. Figtree arrondie et franche pour les titres et les chiffres, Inter neutre et lisible pour les données.

### Hierarchy
- **Display** (600, clamp 34 à 58 px, 1.06) : titre de la page uniquement.
- **Headline** (600, clamp 26 à 34 px, 1.15) : titres de section.
- **Chiffre clé** (Figtree 600, clamp 28 à 40 px, 1.05, chiffres tabulaires) : valeurs de la bande des chiffres.
- **Title** (600, 17 px, 1.3) : intertitres de la colonne de lecture, titres des fiches de la carte.
- **Chapeau** (Inter 400, 18 px, 1.6, 62 caractères maximum) : le paragraphe sous le titre, seul.
- **Body** (400, 16 px, 1.6) : texte courant, 68 caractères maximum.
- **Données** (15 px) : tableau, noms cliquables de la liste, champ de recherche ; rangs en Figtree 700.
- **Secondaire** (14 px) : ligne de source, légendes des chiffres, onglets (600), compteur, téléchargements, pied de page, texte de la carte.
- **Label** (500 à 600, 13 px) : en-têtes de tableau, filtres de la carte, infobulles, communes, détails des fiches. Jamais en capitales.
- **Légende fine** (500 à 600, 12 px) : pilules de statut, étiquettes des cercles, étiquette « Vos bureaux ».
- **Numéro de pastille** (Figtree 700, 11 px) : numéros du top 25 dans les pastilles de la carte, et rien d'autre.

### Named Rules
**La règle des chiffres alignés.** Tout chiffre comparé (chiffres clés, colonnes numériques, rangs, détails des fiches) utilise `font-variant-numeric: tabular-nums`.

## Layout

Conteneur de 1080 px maximum, marges latérales `max(16px, env(safe-area-inset-*))`. Sections espacées de 72 px. L'en-tête occupe toute la largeur : 72 px au-dessus, 56 px en dessous ; le trait de marge suit le bord gauche du conteneur et le texte s'en écarte de 24 px (780 px maximum). Ordre de l'en-tête : titre, chapeau, ligne de source, annotation, puis la bande des chiffres collée dessous.

La carte et la colonne de lecture se partagent la largeur (1,6 / 1, écart de 32 px) et passent sur une colonne sous 860 px. La carte fait 580 px de haut ; sous 760 px elle devient carrée (rayon 20 px) et les chiffres passent sur deux colonnes. Le tableau défile horizontalement dans son cadre, jamais la page ; sous 600 px il tient sans défilement : les colonnes Niveaux et Site disparaissent, la pilule de niveau et le lien du site passent sous la commune.

## Elevation & Depth

Surfaces plates : la profondeur vient du ton (lavande sur blanc) et des halos. Les ombres, toutes douces et teintées d'aubergine (noires en sombre), sont réservées à ce qui flotte au-dessus de la carte.

### Shadow Vocabulary
- **Flottant** (`box-shadow: 0 14px 34px var(--shadow)`) : fiches de la carte.
- **Contrôle** (`box-shadow: 0 6px 18px var(--shadow)`) : boutons de zoom ; les infobulles en prennent une variante à 16 px de flou.
- **Repère** (`box-shadow: 0 3px 8px var(--shadow)`) : pastilles numérotées du top 25 ; l'étiquette « Vos bureaux » à 10 px de flou.

### Named Rules
**La règle du plat par défaut.** Rien dans le flux de la page ne porte d'ombre ; seuls les éléments posés sur le plan en ont.

## Shapes

Pilules (999 px) pour les onglets, filtres, champ de recherche, pastilles et étiquettes. Rayons dégressifs selon la taille de l'objet : 24 px pour la carte et le panneau des chiffres, 20 px pour le cadre du tableau (et la carte sur mobile), 18 px pour les fiches, 16 px pour les lignes de téléchargement, 14 px pour le contrôle de zoom, 10 px pour les infobulles. Les points de la carte sont des disques ; les bureaux sont un carré de 14 px à coins de 4 px tourné à 45°, un losange aubergine. Les cercles de distance sont en pointillés (5 / 7).

## Components

### Buttons
- **Onglets** : pilules lavande, texte aubergine 14 px 600, actifs en violet plein ; survol en lavande profonde.
- **Noms de la liste** : boutons sans fond, en encre, qui passent au violet souligné au survol et amènent la carte sur le compte.
- **Focus** : contour violet de 2 px décalé de 3 px sur tout ce qui se clique.

### Chips
- **Filtres de la carte** : pilules lavande 13 px avec une pastille de couleur de la couche ; une couche masquée s'estompe (55 %) et sa pastille devient un anneau ardoise. « Vue d'ensemble » est poussé à droite, en violet.
- **Pilules de statut** : lavande par défaut, voile violet pour le top 25, voile cyan avec encre cyan pour les clients probables.

### Cards / Containers
- **Chiffres clés** : un seul panneau lavande, quatre cellules séparées par des filets lavande profonde, le dernier chiffre en violet.
- **Tableau** : cadre blanc au filet, en-tête lavande, lignes séparées par des filets, survol lavande, ligne sélectionnée sous voile violet.
- **Téléchargements** : lignes lavande avec une icône de flèche dessinée en SVG, lien violet, taille du fichier en ardoise.

### Inputs / Fields
- **Recherche** : pilule blanche bordée de lavande profonde, 15 px, placeholder ardoise, focus violet.

### Plan (Leaflet)
Tuiles OpenStreetMap désaturées par le filtre du panneau de tuiles (niveaux de gris, contraste 0,82, luminosité 1,1 ; inversées et assombries en sombre), sans opacité. Zoom entier uniquement. La vue de départ cadre le top 25, « Vue d'ensemble » montre les 126 comptes. Top 25 en pastilles violettes numérotées cerclées de blanc (20 px minimum, taille selon les élèves), autres comptes en disques lilas, clients probables en cyan. Cercles de 20 et 50 km : l'étiquette « 20 km » se place juste à l'extérieur de son cercle, côté est, « 50 km » juste à l'intérieur ; « 20 km » disparaît sous le zoom 9 et « Vos bureaux » sous le zoom 10. Un clic sur un point ouvre sa fiche (nom, commune, statut, élèves, valeur, distance, site) et surligne la ligne de la liste ; un clic sur un nom de la liste amène la carte sur le compte. La molette ne zoome qu'après un clic sur le plan. Transitions de 0,15 s, vol de 0,9 s, tout coupé en mouvement réduit.

### En-tête
Halos peints par un calque sous l'en-tête qui déborde de 260 px vers le bas ; réglure Seyès à deux intensités masquée en fondu ; trait de marge orchidée de 1,5 px sur toute la hauteur ; chiffre du titre en dégradé ; annotation Kalam inclinée de 1°.

## Do's and Don'ts

### Do:
- **Do** garder le contenu, les chiffres et les identifiants que le script réécrit (`const DATA`, `const S`, `#h-n`, `#rentree`).
- **Do** passer toute nouvelle couleur par les jetons de `:root` et la redéfinir dans les deux blocs sombres.
- **Do** teinter le plan par le seul filtre du panneau de tuiles et garder un zoom entier, pour éviter les coutures entre tuiles.
- **Do** garder la réglure à deux intensités (8 px et 32 px) et le trait de marge plein, comme sur une copie Seyès.

### Don't:
- **Don't** ajouter le logo d'Ed.ai ni rien qui fasse passer la page pour une page officielle d'Ed.ai.
- **Don't** mettre de sur-titre au-dessus d'un titre, ni de libellés en capitales.
- **Don't** réutiliser le dégradé en texte ailleurs que sur le chiffre du titre.
- **Don't** baisser l'opacité du panneau de tuiles ni d'une tuile : le plan se teinte par filtre.
- **Don't** utiliser le cyan pour autre chose que les clients probables.
