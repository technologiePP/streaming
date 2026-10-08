# ÉcoStreaming

Outil pédagogique sur l'impact carbone du streaming vidéo et l'indice de réparabilité :
simulateur, exercices, défis et jeu vidéo (« Opération Éco-Soirée »).

Le site est **une seule page statique** (`index.html`). Toutes les bibliothèques (Tailwind CSS compilé,
Chart.js, Font Awesome, police Inter) sont dans le dossier `assets/` : le site fonctionne **sans connexion
à des serveurs externes** (utile sur un Wi-Fi d'établissement filtré).

## Mettre le site en ligne avec GitHub Pages

1. Créer un dépôt GitHub (par exemple `ecostreaming`), public (ou privé avec un compte qui le permet).
2. Y envoyer **tout le contenu de ce dossier** (`index.html`, `assets/`, `.nojekyll`…), à la racine du dépôt :
   *Add file → Upload files* depuis le site GitHub, puis *Commit changes*.
3. Dans le dépôt : **Settings → Pages**. Sous *Build and deployment*, choisir **Deploy from a branch**,
   branche **main**, dossier **/ (root)**, puis *Save*.
4. Après une à deux minutes, le site est disponible à l'adresse :
   `https://<votre-identifiant>.github.io/<nom-du-depot>/`

Cette adresse peut être donnée aux élèves (ENT, Pronote, QR code…). Elle fonctionne sur ordinateur, iPad et tablette.

## Remarques

- **Progression des élèves** : enregistrée dans le navigateur de chaque appareil (sans envoi sur internet).
  Le lien « Effacer ma progression enregistrée » en bas de page la supprime.
- **Jeu vidéo** : verrouillé tant que l'élève n'a pas 80 % de bonnes réponses (du premier coup) sur l'ensemble des
  exercices et défis. Le code enseignant de déblocage est indiqué dans le formulaire « Accès enseignant ».
- Les pages ont chacune une adresse directe : `#simulateur`, `#exercices`, `#reparabilite`,
  `#exercices-reparabilite`, `#defis`, `#jeu-video`.

## Modifier le style (facultatif)

Le fichier `assets/tailwind.css` est généré à partir de `index.html` et de `tailwind.config.js`
avec la version 3.4 de Tailwind CSS (exécutable autonome) :

```
tailwindcss -c tailwind.config.js -i entree.css -o assets/tailwind.css --minify
```

où `entree.css` contient les trois lignes `@tailwind base; @tailwind components; @tailwind utilities;`.
À refaire uniquement si de nouvelles classes Tailwind sont ajoutées dans `index.html`.

## Licences des bibliothèques incluses

Chart.js (MIT), Font Awesome Free 6.4.0 (icônes CC BY 4.0, polices SIL OFL, code MIT), Inter (SIL OFL 1.1).
Les licences sont dans `assets/`.
