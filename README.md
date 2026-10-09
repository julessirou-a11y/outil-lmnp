# Outil LMNP

Petit outil web pour tenir la comptabilité d'une location meublée non professionnelle (LMNP) au régime réel simplifié :

- saisie des recettes et dépenses, avec des filtres à cumuler façon Inqom (compte, dates, période, journal, libellé, montant, pointage, nature, tiers, justificatif), aussi en grand livre, et enregistrables sous un nom ;
- import du relevé bancaire CSV, avec tri des opérations, règles mémorisées par mot-clé et détection des doublons ;
- une seule zone de dépôt pour les pièces : PDF, photos, échéanciers et factures électroniques de la plateforme agréée (Factur-X, UBL, CII, ZIP), lues et rattachées automatiquement au paiement de même montant ;
- amortissements par composant (logement hors terrain, travaux, mobilier) ;
- emprunt : seules les écritures bancaires (intérêts, capital, assurance) sont comptabilisées ; l'échéancier de la page Emprunt indique pour chaque échéance passée si elle est rapprochée (vert), en partie (jaune) ou sans écriture ou avec écart (rouge). Un seul échéancier : celui saisi d'après les caractéristiques du prêt, remplacé par celui de la banque dès que son PDF est déposé (lu dans le navigateur, rattaché d'office comme justificatif aux écritures d'emprunt) ;
- calcul du résultat fiscal, avec report des amortissements non déductibles (art. 39 C du CGI) et des déficits ;
- fiche de déclaration case par case (2033-A, B, C, D, 2031, 2042-C-PRO).
- plan de comptes derrière chaque nature, journal des écritures mois par mois (reçu, payé, justificatif manquant), balance des comptes avec solde N-1 et variation, grand livre avec solde progressif par compte et export FEC ; un clic sur un montant ou un numéro de compte ouvre, dans un nouvel onglet, le grand livre filtré sur ce montant exact ou ce compte.
- reprise d'une année antérieure depuis l'ancien classeur Excel « Dossier de travail » (Paramètres du dossier > Années), lu sur l'ordinateur et contrôlé avec son compte de résultat et son bilan.

## Confidentialité

Ce dépôt ne contient **que le code**. Les données comptables sont dans un fichier `lmnp-donnees.json`, conservé dans un dossier iCloud privé. Elles ne sont jamais envoyées sur internet : la page lit et écrit ce fichier directement sur l'ordinateur.

**Ne jamais ajouter de fichier `.json` de données dans ce dépôt.**

## Utilisation

- **Mac, Chrome ou Edge** : bouton « Ouvrir le dossier LMNP… », puis choisir le dossier iCloud. Chaque enregistrement met à jour le fichier et ajoute une copie datée dans `Sauvegardes/`.
- **Safari, iPhone** : consultation et impression ; l'enregistrement télécharge le fichier, qu'il faut ensuite replacer dans le dossier iCloud.

Les pièces se déposent sur la page Pièces, ou directement dans `Justificatifs/<année>/` (app Fichiers de l'iPhone) : l'outil les y retrouve, reconnaît les factures électroniques et propose de rattacher le reste. Rien n'est envoyé sur internet.

Les montants produits sont à vérifier avant chaque déclaration.
