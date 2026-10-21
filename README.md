# Candidature Ed.ai — le privé sous contrat de l'académie de Lyon

Page d'étude jointe à ma candidature chez Ed.ai. Elle chiffre et priorise le segment que l'équipe peut signer en direct, sans passer par le catalogue LDE de la Région : les 126 ensembles scolaires privés sous contrat de l'académie de Lyon (Ain, Loire, Rhône), données DEPP de la rentrée 2025.

## Contenu du dossier

| Fichier | Rôle |
|---|---|
| `index.html` | La page, autonome : styles, données et scripts dans un seul fichier, sans étape de build |
| `edai_prive_academie_lyon.xlsx` | Le fichier CRM, téléchargeable depuis la page : une ligne par compte, avec ses UAI |
| `scripts/construire_liste.py` | Le script qui produit le fichier CRM et les données de la page, téléchargeable lui aussi |
| `scripts/requirements.txt` | Sa seule dépendance : openpyxl |
| `README.md` | Ce fichier : structure de la page, mise à jour, vérifications |
| `CLAUDE.md` | Consignes pour les sessions Claude Code sur ce dossier |
| `.gitignore` | Fichiers système et caches exclus du suivi |

Version d'origine : `Downloads/edai-prive-aura.html` (21/10/2026), livrée sans squelette HTML (format artifact). `index.html` ajoute seulement `<!doctype html>`, `<html lang="fr">`, `<meta charset>` et `<meta viewport>`, pour que la page s'affiche correctement ouverte en local (accents, mode standard, mobile). Le reste est identique à l'original, en dehors des liens de téléchargement ajoutés ensuite dans « Méthode ».

## Ouvrir la page

- Double-clic sur `index.html` : tout fonctionne en local, seules les polices viennent de Google Fonts.
- Depuis Claude Code (app desktop) : aperçu `candidature-edai`, déclaré dans `.claude/launch.json` à la racine de l'espace de travail (port 8761).

## Comment la page est construite

Dans l'ordre de `index.html` :

1. **Styles** (`<style>`). Les couleurs sont des tokens sur `:root`, redéfinis pour le mode sombre à deux endroits : `@media (prefers-color-scheme: dark)` et `:root[data-theme="dark"]`. Polices : Fraunces (titres), Atkinson Hyperlegible (texte), Kalam (note manuscrite), JetBrains Mono (chiffres).
2. **Contenu** : en-tête sur papier Seyès, bandeau de 4 chiffres clés (`#kpis`), carte (`<canvas id="map">`) et sa colonne « Lecture », liste filtrable (`#rows`), méthode, pied de page.
3. **Données** (`<script>`) :
   - `const DATA` : un objet par compte (126 objets, sur une seule ligne) ;
   - `const S` : les agrégats affichés dans le titre, les chiffres clés et la colonne « Lecture ».
4. **Rendu** : chiffres clés, tableau (onglets Top 25 / Tous les comptes, filtre texte), carte en projection équirectangulaire, redessinée quand le thème change.

### Champs de `DATA`

| Champ | Contenu |
|---|---|
| `nom`, `commune`, `dep` | Nom de l'ensemble scolaire et commune (en majuscules, la page les passe en casse titre), département (`01`, `42`, `69`) |
| `niveaux` | `Collège`, `Lycée GT` ou `Collège + Lycée GT` ; le `+` donne la pastille bleue |
| `eleves` | Effectif DEPP du compte, collège et lycée réunis |
| `arr_1_matiere` | Valeur annuelle pour une matière : `eleves × 6` |
| `client_probable` | `true` pour les établissements du réseau Centre scolaire Notre-Dame (logo sur le site Ed.ai), sortis du top 25 |
| `top25`, `rang` | Appartenance au top 25 et rang de 1 à 25 (`0` hors top 25) |
| `lat`, `lon` | Coordonnées, issues de l'annuaire de l'Éducation nationale |
| `web` | Site de l'établissement, parfois vide |
| `km_siege` | Distance aux bureaux Ed.ai, en km |

## Mettre à jour les données (à chaque rentrée)

`scripts/construire_liste.py` produit le fichier CRM et les données de la page (`DATA` et `S`) à partir des données ouvertes de l'Éducation nationale. Relancé sur les fichiers de la rentrée 2025, il redonne la page à l'octet près et l'export d'origine cellule par cellule (vérifié le 21/10/2026). Les paramètres (tarif, bonus du score, coordonnées des bureaux, clients probables) sont des constantes en tête du script.

1. Télécharger les trois fichiers CSV dans un dossier `sources/` à la racine du projet (ignoré par git, environ 65 Mo) :
   - [effectifs des collèges](https://data.education.gouv.fr/api/explore/v2.1/catalog/datasets/fr-en-college-effectifs-niveau-sexe-lv/exports/csv?delimiter=%3B)
   - [effectifs des lycées GT](https://data.education.gouv.fr/api/explore/v2.1/catalog/datasets/fr-en-lycee_gt-effectifs-niveau-sexe-lv/exports/csv?delimiter=%3B)
   - [annuaire de l'éducation](https://data.education.gouv.fr/api/explore/v2.1/catalog/datasets/fr-en-annuaire-education/exports/csv?delimiter=%3B)
2. Installer la dépendance : `pip install -r scripts/requirements.txt`.
3. Depuis la racine du projet :
   ```bash
   python scripts/construire_liste.py sources --sortie edai_prive_academie_lyon.xlsx --html index.html
   ```
   Le script prend la rentrée la plus récente des fichiers ; `--rentree 2025` force une année. `--html` ne touche qu'aux lignes `const DATA` et `const S`, au `126` du titre et au `2025` du sur-titre.
4. Ne jamais modifier `DATA` ou `S` à la main : relancer le script.
5. Relire les **textes écrits en dur**, que le script ne met pas à jour :
   - la note manuscrite « 69 % des élèves… » de l'en-tête (doublon de `S.part_college_pct`) ;
   - « Le plus proche, Chevreul Lestonnac, est à 1,2 km de la rue Chevreul » (colonne « Lecture ») ;
   - le paragraphe sur le Centre scolaire Notre-Dame ;
   - le tarif de 6 € par matière (sous-titre de la liste) et les coefficients du score (section « Méthode ») ;
   - la taille des fichiers dans les liens de téléchargement (section « Méthode »).
6. Paramètres de la carte, dans la fonction `draw()` de la page : coordonnées des bureaux (`45.7487, 4.8436`), rayons de 20 et 50 km, villes repères.

## Avant d'envoyer ou de publier

- [ ] Mode clair et mode sombre
- [ ] Largeur mobile (375 px) : la page ne défile pas horizontalement (seul le tableau défile)
- [ ] Onglets Top 25 / Tous les comptes et filtre texte
- [ ] Survol de la carte (infobulle) et liens « site »
- [ ] Console du navigateur sans erreur
- [ ] Les deux liens de téléchargement de la section « Méthode »

## Points ouverts

- Notre-Dame de Mongré (Villefranche) est marqué client probable, mais son site est mongre.org, pas csnd.fr. S'il n'est pas client, il entre dans le top 25 à la 7e place (score 15 430).
- Les « 174 établissements » sont 174 lignes collège ou lycée GT pour 171 UAI : trois lycées polyvalents ont aussi une petite section collège.
- L'infobulle de la carte ne réagit qu'à la souris : rien ne s'affiche au toucher sur mobile.
- 7 comptes n'ont pas de site, et 14 sites sont en `http://`.
- `S.clients_probables` contient trois fois « NOTRE DAME » : des établissements différents au même nom, qu'on ne distingue pas sans la commune.
