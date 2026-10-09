# Outil LMNP

Petit outil web pour tenir la comptabilité d'une location meublée non professionnelle (LMNP) au régime réel simplifié :

- saisie des recettes et dépenses, avec des filtres combinables (période, nature ou compte, texte, montant, pointage sur le relevé, justificatif) que l'on peut enregistrer sous un nom ;
- import du relevé bancaire CSV, avec tri des opérations, règles mémorisées par mot-clé et détection des doublons ;
- une seule zone de dépôt pour les pièces : PDF, photos, échéanciers et factures électroniques de la plateforme agréée (Factur-X, UBL, CII, ZIP), lues et rattachées automatiquement au paiement de même montant ;
- amortissements par composant (logement hors terrain, travaux, mobilier) ;
- échéancier d'emprunt mois par mois ; le PDF de la banque, une fois déposé, est lu dans le navigateur et comparé à l'échéancier du dossier, avec la liste des corrections à faire sur l'année ;
- calcul du résultat fiscal, avec report des amortissements non déductibles (art. 39 C du CGI) et des déficits ;
- fiche de déclaration case par case (2033-A, B, C, D, 2031, 2042-C-PRO).
- plan de comptes derrière chaque nature (affichage au choix), balance des comptes et export FEC.
- reprise d'une année antérieure depuis l'ancien classeur Excel « Dossier de travail » (Paramètres du dossier > Années), lu sur l'ordinateur et contrôlé avec son compte de résultat et son bilan.

## Confidentialité

Ce dépôt ne contient **que le code**. Les données comptables sont dans un fichier `lmnp-donnees.json`, conservé dans un dossier iCloud privé. Elles ne sont jamais envoyées sur internet : la page lit et écrit ce fichier directement sur l'ordinateur.

**Ne jamais ajouter de fichier `.json` de données dans ce dépôt.**

## Utilisation

- **Mac, Chrome ou Edge** : bouton « Ouvrir le dossier LMNP… », puis choisir le dossier iCloud. Chaque enregistrement met à jour le fichier et ajoute une copie datée dans `Sauvegardes/`.
- **Safari, iPhone** : consultation et impression ; l'enregistrement télécharge le fichier, qu'il faut ensuite replacer dans le dossier iCloud.

Les pièces se déposent sur la page Pièces, ou directement dans `Justificatifs/<année>/` (app Fichiers de l'iPhone) : l'outil les y retrouve, reconnaît les factures électroniques et propose de rattacher le reste. Rien n'est envoyé sur internet.

Les montants produits sont à vérifier avant chaque déclaration.
