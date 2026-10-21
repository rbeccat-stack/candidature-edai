# Product

<!-- impeccable:product-schema 1 -->

## Platform

web

## Users

L'équipe d'Ed.ai, lectrice de la candidature de Rémi : responsables commerciaux, growth et recrutement. Ils ouvrent la page depuis un lien, sur ordinateur ou sur téléphone, pour juger en quelques minutes si le candidat sait trouver et prioriser des comptes signables.

## Product Purpose

Une page d'étude unique qui chiffre et priorise le segment qu'Ed.ai peut signer en direct, sans passer par le catalogue LDE de la Région : les 126 ensembles scolaires privés sous contrat de l'académie de Lyon (Ain, Loire, Rhône), données DEPP de la rentrée 2025. La page réussit si le lecteur repart avec le top 25, sa valeur annuelle et la méthode, et s'il peut télécharger le fichier CRM et le script.

## Positioning

Des données publiques (DEPP, annuaire de l'Éducation nationale) transformées en liste de comptes prête pour le CRM, avec une méthode de score explicite et reproductible : un script relance le calcul à chaque rentrée.

## Operating Context

- Page statique servie par Vercel sur edai.remibk-studio.fr, depuis le dépôt public rbeccat-stack/candidature-edai.
- Les données de la page (`const DATA`, `const S`) sont produites par `scripts/construire_liste.py`, jamais à la main.
- Le fichier CRM (`edai_prive_academie_lyon.xlsx`) et le script sont téléchargeables depuis la section « Méthode ».

## Capabilities and Constraints

- Un seul fichier HTML, sans étape de build. Le script réécrit sur place `const DATA`, `const S`, `#h-n` et `#rentree` : ces identifiants et ces lignes doivent rester.
- Textes en français, vouvoiement envers l'équipe Ed.ai. Le contenu, les chiffres et l'ordre des sections sont validés par Rémi (21/10/2026) : une refonte visuelle ne les modifie pas.
- Pas de données de contact nominatives (RGPD).
- La page est en `noindex`.

## Brand Commitments

- Rémi a demandé (21/10/2026) que la page reprenne la charte d'Ed.ai telle qu'elle apparaît sur ed.ai/fr : couleurs et typographies. Pas de logo Ed.ai : la page doit rester visiblement celle de Rémi, adressée à Ed.ai, sans passer pour une page officielle.
- Signature en pied de page : « Préparé par Rémi · growth et automatisation, Lyon », avec le lien vers remibk-studio.fr.

## Evidence on Hand

- Données DEPP rentrée 2025 et annuaire de l'Éducation nationale (data.education.gouv.fr), embarquées dans la page.
- `edai_prive_academie_lyon.xlsx` (126 comptes avec leurs UAI) et `scripts/construire_liste.py`.
- Aucun chiffre d'Ed.ai (clients, inscrits, chiffre d'affaires) : ne pas en inventer. Les « clients probables » reposent seulement sur les logos publics du site d'Ed.ai.

## Product Principles

- Chaque chiffre affiché se recalcule depuis les données publiques.
- La liste sert à agir : top 25 d'abord, tous les comptes ensuite, prêts pour le CRM.
- La méthode et ses limites sont dites sur la page, sans les enjoliver.
