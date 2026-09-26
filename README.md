# Mon IA — pages de branding OAuth

Ce dossier contient les deux pages exigées par l'écran de consentement OAuth de
l'application Google Cloud **Mon IA** (projet `deuxieme-cerveau`) :

| Fichier | Champ Google Cloud |
| --- | --- |
| `index.html` | URL de la page d'accueil |
| `confidentialite.html` | URL de la politique de confidentialité |
| `conditions.html` | URL des conditions d'utilisation |

`.nojekyll` empêche GitHub Pages de passer le dossier dans Jekyll.

## Déploiement

Rendu disponible sur `https://<ton-pseudo>.github.io/mon-ia/`.

1. Créer un dépôt **public** nommé `mon-ia` sur github.com
2. Uploader le contenu de `public/` à la racine du dépôt
3. Repo → Settings → Pages → Source : *Deploy from a branch*, branche `main`, dossier `/ (root)`
4. Attendre 1 à 2 minutes, l'URL apparaît en haut de la page

## Pourquoi GitHub Pages et pas Free.fr

L'espace `frederic.stol.free.fr` renvoie un 500 sur toutes les URL, y compris
les fichiers inexistants. Cause : le `.htaccess` de 2014 contient
`<IfDefine Free> php 1 </IfDefine>`, rejete depuis le passage de Free à PHP 8.5.
Free bloque en FTP toute lecture, écriture, renommage et suppression de fichier
`.ht*`, donc le fichier est irrécupérable sans leur support. Le vhost est de plus
en HTTP seul, sans certificat.

## Fichiers de diagnostic conservés à la racine du projet

`diagnostiquer.sh`, `publier.sh`, `reparer.sh` : scripts du diagnostic Free.fr.
`reparer.sh` est désormais inutile, Free refusant toute opération sur le `.htaccess`.
