# Candidature Ed.ai — le privé sous contrat de l'académie de Lyon

Page d'étude jointe à ma candidature chez Ed.ai. Elle chiffre et priorise le segment que l'équipe peut signer en direct, sans passer par le catalogue LDE de la Région : les 126 ensembles scolaires privés sous contrat de l'académie de Lyon (Ain, Loire, Rhône), données DEPP de la rentrée 2025.

## Contenu du dossier

| Fichier | Rôle |
|---|---|
| `index.html` | La page, autonome : styles, données et scripts dans un seul fichier, sans étape de build |
| `README.md` | Ce fichier : structure de la page, mise à jour, vérifications |
| `CLAUDE.md` | Consignes pour les sessions Claude Code sur ce dossier |
| `.gitignore` | Fichiers système et caches exclus du suivi |

Version d'origine : `Downloads/edai-prive-aura.html` (21/10/2026), livrée sans squelette HTML (format artifact). `index.html` ajoute seulement `<!doctype html>`, `<html lang="fr">`, `<meta charset>` et `<meta viewport>`, pour que la page s'affiche correctement ouverte en local (accents, mode standard, mobile). Le reste est identique à l'original.

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

Le script qui produit `DATA` et `S` n'est pas dans ce dossier, alors que la page annonce qu'il « se relance à chaque rentrée ». Le ranger dans `scripts/` est la première chose à faire pour que la mise à jour soit reproductible.

En attendant, pour remplacer les données :

1. Remplacer `DATA` et `S` **ensemble**, jamais l'un sans l'autre.
2. Contrôler que `S` correspond à `DATA` (fait le 21/10/2026 : tout concorde) :
   - `nb_comptes` = nombre d'objets dans `DATA` ;
   - `eleves_total`, `arr_1_matiere_total` = sommes sur `DATA` ;
   - `nb_college_et_lycee` = comptes dont `niveaux` contient `+` ;
   - `top25_eleves`, `top25_arr_1_matiere` = sommes sur le top 25, et `top25_arr_3_matieres` = 3 × `top25_arr_1_matiere` ;
   - `top25_a_moins_de_20km` = comptes du top 25 avec `km_siege < 20` ;
   - `comptes_par_dep` = décompte par `dep`, `clients_probables_eleves` = somme sur les clients probables ;
   - pour chaque compte, `arr_1_matiere` = `eleves × 6`.
3. Relire les **textes écrits en dur**, que les données ne mettent pas à jour :
   - la note manuscrite « 69 % des élèves… » de l'en-tête (doublon de `S.part_college_pct`) ;
   - « Le plus proche, Chevreul Lestonnac, est à 1,2 km de la rue Chevreul » (colonne « Lecture ») ;
   - le paragraphe sur le Centre scolaire Notre-Dame ;
   - le tarif de 6 € par matière (sous-titre de la liste) et les coefficients du score (section « Méthode ») ;
   - `126` dans le `<h1>` et `2025` dans le sur-titre : le script les remplace par les valeurs de `S`, mais ce sont elles qui s'affichent si le JavaScript échoue.
4. Paramètres de la carte, dans la fonction `draw()` : coordonnées des bureaux (`45.7487, 4.8436`), rayons de 20 et 50 km, villes repères.

## Avant d'envoyer ou de publier

- [ ] Mode clair et mode sombre
- [ ] Largeur mobile (375 px) : la page ne défile pas horizontalement (seul le tableau défile)
- [ ] Onglets Top 25 / Tous les comptes et filtre texte
- [ ] Survol de la carte (infobulle) et liens « site »
- [ ] Console du navigateur sans erreur
- [ ] Chiffres de `S` cohérents avec `DATA` (étape 2 ci-dessus)

## Points ouverts

- La section « Méthode » parle d'un fichier prêt à importer dans un CRM, avec l'identifiant UAI de chaque établissement : ni ce fichier ni les UAI ne sont ici (`DATA` n'a pas de champ UAI).
- L'infobulle de la carte ne réagit qu'à la souris : rien ne s'affiche au toucher sur mobile.
- 7 comptes n'ont pas de site, et 14 sites sont en `http://`.
- `S.clients_probables` contient trois fois « NOTRE DAME » : des établissements différents au même nom, qu'on ne distingue pas sans la commune.
