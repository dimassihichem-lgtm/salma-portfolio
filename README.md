# Site portfolio — Salma Megdiche

Un seul fichier de contenu : `index.html`. Tout ce qui se modifie est dans le bloc
`CONTENU` au début du `<script>`. Rien à installer, aucun compte à créer pour éditer.

## Structure du dossier

    index.html              ← le site (texte + liste des projets)
    images/projets/         ← photos des projets (jpg, 1600 px de large max, < 400 Ko)
    images/materiaux/       ← les pastilles de matières de la planche
    images/portrait.jpg     ← portrait (à ajouter)
    cv/CV_Salma_Megdiche.pdf ← le CV téléchargeable

## Modifier un texte

1. Ouvrir `index.html` avec un éditeur de texte (TextEdit, Notepad, VS Code…).
2. Chercher le bloc `CONTENT` : chaque phrase du site y est, en clair.
3. Modifier entre les guillemets. Ne pas toucher aux guillemets ni aux virgules.
4. Enregistrer, ouvrir le fichier dans un navigateur pour vérifier.

## Ajouter un projet

1. Déposer les photos dans `images/projets/`, ex. `salon-dupont-01.jpg`, `salon-dupont-02.jpg`.
2. Dans `index.html`, bloc `PROJECTS` : copier un bloc `{ ... },` existant, le coller juste après.
3. Changer `id` (unique, sans espace), `cat` (interieur / staging / showroom / evenement),
   `year`, `place`, `title`, `mission`, `surface`, `desc`, et `images:["images/projets/salon-dupont-01.jpg", "…"]`.
4. Retirer `sample:true` — c'est ce qui affiche « Exemple ».
5. `size:"wide"` pour une case large. Pour une grille sans trou : 3 larges pour 6 carrés, ou uniquement des carrés.

## Supprimer un projet

Supprimer son bloc `{ ... },` en entier, accolade à accolade.

## Image d'ouverture et portrait

En haut du bloc CONTENU : `HERO_IMAGE`, `HERO_SMALL_IMAGE`, `PORTRAIT_IMAGE`.
Mettre le chemin du fichier entre guillemets, ex. `"images/projets/salon-dupont-01.jpg"`.

## Activer l'anglais plus tard

Passer `SHOW_LANGUAGE_TOGGLE` à `true`. Les textes anglais sont déjà dans `CONTENT.en`
et dans chaque projet (`title.en`, `desc.en`…) — les compléter avant.

## Mettre en ligne (Netlify)

1. Créer un compte gratuit sur netlify.com.
2. Menu « Sites » → « Add new site » → « Deploy manually ».
3. Glisser-déposer le dossier `site` entier dans la zone. Le site est en ligne en quelques secondes
   sur une adresse du type `nom-aleatoire.netlify.app`.
4. « Site configuration » → « Change site name » pour obtenir `salma-megdiche.netlify.app`.
5. Pour mettre à jour : onglet « Deploys » → glisser-déposer à nouveau le dossier. L'adresse ne change pas.

## Nom de domaine (plus tard)

Acheter `salmamegdiche.fr` chez OVH ou Gandi (~10 €/an), puis dans Netlify :
« Domain management » → « Add a domain » et suivre les instructions DNS.
