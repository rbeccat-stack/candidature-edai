---
name: Ed.ai — Privé académie de Lyon
description: Étude de candidature aux couleurs de la charte d'Ed.ai (ed.ai/fr), relevée le 21/10/2026
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
  night-bg: "#120c22"
  night-surface: "#1a1330"
  night-violet: "#8f8aff"
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
  title:
    fontFamily: "Figtree, Segoe UI, system-ui, sans-serif"
    fontSize: "17px"
    fontWeight: 600
    lineHeight: 1.3
  body:
    fontFamily: "Inter, system-ui, sans-serif"
    fontSize: "16px"
    fontWeight: 400
    lineHeight: 1.6
  label:
    fontFamily: "Inter, system-ui, sans-serif"
    fontSize: "13px"
    fontWeight: 600
  annotation:
    fontFamily: "Kalam, Segoe Print, cursive"
    fontSize: "22px"
    fontWeight: 400
    lineHeight: 1.3
rounded:
  pill: "999px"
  panel: "24px"
  card: "20px"
  row: "16px"
spacing:
  section: "72px"
  gutter: "16px"
components:
  tab-active:
    backgroundColor: "{colors.edai-violet}"
    textColor: "{colors.paper}"
    rounded: "{rounded.pill}"
    padding: "10px 18px"
  tab:
    backgroundColor: "{colors.lavender}"
    textColor: "{colors.aubergine}"
    rounded: "{rounded.pill}"
    padding: "10px 18px"
  kpi-panel:
    backgroundColor: "{colors.lavender}"
    rounded: "{rounded.panel}"
    padding: "8px"
  pill-both:
    backgroundColor: "rgba(94,88,244,.10)"
    textColor: "{colors.edai-violet}"
    rounded: "{rounded.pill}"
    padding: "3px 10px"
  pill-client:
    backgroundColor: "rgba(2,179,255,.12)"
    textColor: "{colors.cyan-ink}"
    rounded: "{rounded.pill}"
    padding: "3px 10px"
  download-row:
    backgroundColor: "{colors.lavender}"
    rounded: "{rounded.row}"
    padding: "14px 16px"
---

# Design System: Ed.ai — Privé académie de Lyon

## Overview

**Creative North Star : « La copie corrigée aux couleurs d'Ed.ai »**

La page reprend la langue visuelle d'ed.ai (« Faire de chaque copie un tremplin ») pour présenter une étude de prospection. Fond blanc baigné de halos lavande, titres Figtree aubergine, violet Ed.ai pour tout ce qui agit ou compte. Le souvenir de la copie d'élève tient en deux détails : une réglure Seyès très légère dans l'en-tête, avec sa marge, et une seule annotation manuscrite en violet.

La page reste celle de Rémi, adressée à l'équipe Ed.ai : pas de logo Ed.ai, signature en pied de page (voir PRODUCT.md).

**Key Characteristics:**
- Halos d'ed.ai : bleu en haut à gauche, violet rosé en bas à droite, sur l'en-tête seulement.
- Violet pour les actions, le top 25 et les liens ; cyan réservé aux clients probables.
- Pilules pour tout ce qui se clique, panneaux lavande arrondis pour ce qui se lit.
- Plan OpenStreetMap désaturé et teinté par sa propre transparence sur la lavande.

## Colors

Une palette lavande et violette, froide, sur blanc, avec un aubergine profond pour l'encre des titres.

### Primary
- **Violet Ed.ai** (#5e58f4) : boutons actifs, numéros du top 25 sur la carte et dans la liste, liens, chiffres mis en avant, annotation manuscrite. Contraste 5:1 sur blanc, utilisable en texte.

### Secondary
- **Cyan Ed.ai** (#02b3ff) : points des clients probables, fin du dégradé du titre. Jamais en texte sur fond clair ; le texte cyan passe par **Cyan encre** (#00719f).

### Neutral
- **Aubergine** (#291846) : titres, valeurs des chiffres clés, infobulles de la carte (fond).
- **Encre texte** (#2b2541) : texte courant.
- **Ardoise** (#5f6480) : texte secondaire, légendes, en-têtes de tableau.
- **Lavande** (#efefff) et **Lavande profonde** (#e3dfff) : panneaux, onglets inactifs, survols, fond de carte.
- **Filet** (#e7e5f6) : bordures et séparateurs.
- **Lilas** (#a9a5e4) : points des comptes hors top 25.

### Mode sombre
Fond #120c22, surfaces #1a1330, violet éclairci #8f8aff (le texte sur violet passe en encre sombre), cyan #3cc7ff. Le plan est inversé et assombri par filtre CSS.

### Named Rules
**La règle du cyan rare.** Le cyan ne désigne que les clients probables (et la fin du dégradé du titre). Un deuxième usage brouillerait la légende de la carte.

**La règle du dégradé unique.** Le dégradé violet→cyan en texte est la signature d'ed.ai : il n'apparaît qu'une fois, sur le chiffre du titre.

## Typography

**Display Font:** Figtree (repli Segoe UI, system-ui)
**Body Font:** Inter (repli system-ui)
**Annotation:** Kalam, une seule fois par page

**Character :** les deux faces d'ed.ai, telles quelles. Figtree arrondie et franche pour les titres, Inter neutre et lisible pour les données.

### Hierarchy
- **Display** (600, clamp(34px, 5.4vw, 58px), 1.06) : titre de la page uniquement.
- **Headline** (600, clamp(26px, 3.2vw, 34px), 1.15) : titres de section.
- **Title** (600, 17px, 1.3) : intertitres de la colonne de lecture, titres des fiches de la carte.
- **Body** (400, 16px, 1.6) : texte courant, chapeau en 18px, 62 à 68 caractères par ligne.
- **Label** (500 à 600, 13px) : en-têtes de tableau, pastilles, légende. Jamais en capitales.

Les chiffres alignés utilisent `font-variant-numeric: tabular-nums`.

## Layout

Conteneur de 1080 px maximum, marges latérales `max(16px, env(safe-area-inset-*))`. Sections espacées de 72 px. L'en-tête occupe toute la largeur (halos), le contenu suit dans le conteneur. La carte et la colonne de lecture se partagent la largeur (1,6 / 1) et passent sur une colonne sous 860 px. La carte fait 580 px de haut (460 px sur mobile). Le tableau défile horizontalement dans son cadre, jamais la page.

## Elevation & Depth

Surfaces plates : la profondeur vient du ton (lavande sur blanc). Les ombres sont réservées à ce qui flotte au-dessus de la carte.

### Shadow Vocabulary
- **Flottant** (`box-shadow: 0 14px 34px rgba(41,24,70,.16)`) : fiches de la carte.
- **Contrôle** (`box-shadow: 0 6px 18px rgba(41,24,70,.16)`) : boutons de zoom, infobulles.
- **Repère** (`box-shadow: 0 3px 8px rgba(41,24,70,.16)`) : pastilles numérotées du top 25.

## Shapes

Pilules (999 px) pour les onglets, filtres, pastilles et étiquettes ; 24 px pour la carte et le panneau des chiffres ; 20 px pour le cadre du tableau ; 16 px pour les lignes de téléchargement et les fiches. Les points de la carte sont des disques ; le repère des bureaux est un losange aubergine.

## Components

- **Onglets et filtres** : pilules lavande, actives en violet plein. Les filtres de la carte s'estompent quand la couche est masquée.
- **Chiffres clés** : un seul panneau lavande, quatre cellules séparées par des filets, le dernier chiffre en violet.
- **Carte (Leaflet)** : top 25 en pastilles violettes numérotées, autres comptes en disques lilas, clients probables en cyan, cercles de 20 et 50 km en pointillés. Un clic ouvre une fiche (nom, commune, statut, élèves, valeur, distance, site) et surligne la ligne de la liste ; un clic sur un nom de la liste amène la carte sur le compte.
- **Tableau** : en-tête lavande, lignes séparées par des filets, ligne sélectionnée teintée de violet.
- **Téléchargements** : lignes lavande avec une icône de flèche dessinée en SVG, lien violet, taille du fichier en ardoise.

## Do's and Don'ts

- **Do** garder le contenu, les chiffres et les identifiants que le script réécrit (`const DATA`, `const S`, `#h-n`, `#rentree`).
- **Do** passer toute nouvelle couleur par les jetons de `:root` et la redéfinir dans les deux blocs sombres.
- **Don't** ajouter le logo d'Ed.ai ni rien qui fasse passer la page pour une page officielle d'Ed.ai.
- **Don't** mettre de sur-titre au-dessus d'un titre, ni de libellés en capitales.
- **Don't** réutiliser le dégradé en texte ailleurs que sur le chiffre du titre.
