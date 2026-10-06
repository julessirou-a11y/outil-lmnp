# Outil LMNP

Petit outil web pour tenir la comptabilité d'une location meublée non professionnelle (LMNP) au régime réel simplifié :

- saisie des recettes et dépenses ;
- amortissements par composant (logement hors terrain, travaux, mobilier) ;
- échéancier d'emprunt ;
- calcul du résultat fiscal, avec report des amortissements non déductibles (art. 39 C du CGI) et des déficits ;
- fiche de déclaration case par case (2033-A, B, C, D, 2031, 2042-C-PRO).

## Confidentialité

Ce dépôt ne contient **que le code**. Les données comptables sont dans un fichier `lmnp-donnees.json`, conservé dans un dossier iCloud privé. Elles ne sont jamais envoyées sur internet : la page lit et écrit ce fichier directement sur l'ordinateur.

**Ne jamais ajouter de fichier `.json` de données dans ce dépôt.**

## Utilisation

- **Mac, Chrome ou Edge** : bouton « Ouvrir le dossier LMNP… », puis choisir le dossier iCloud. Chaque enregistrement met à jour le fichier et ajoute une copie datée dans `Sauvegardes/`.
- **Safari, iPhone** : consultation et impression ; l'enregistrement télécharge le fichier, qu'il faut ensuite replacer dans le dossier iCloud.

Les montants produits sont à vérifier avant chaque déclaration.
