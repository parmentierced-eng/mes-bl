# Mes BL

**Bons de livraison, stock et dispatch — sur votre ordinateur, sans connexion.**

Application portable en français, avec nom personnalisable, six palettes de couleurs et coordonnées configurables sur les BL. Elle démarre entièrement vide, sans client, fournisseur ou document préchargé.

## Télécharger

**[Télécharger la dernière version](https://github.com/parmentierced-eng/mes-bl/releases/latest)**

Dans **Assets**, choisir **Mes-BL-portable.zip** puis :

1. Extraire tout le ZIP dans un dossier permanent.
2. Sous Windows, ouvrir **Lancer Mes BL.vbs**.
3. Sinon, ouvrir **distribution/Mes-BL.html** dans Edge, Chrome ou Firefox.

Aucune installation ou connexion nécessaire après téléchargement. Le fichier HTML fonctionne aussi sur macOS et Linux avec un navigateur récent.

## Fonctions

- Clients et fournisseurs, stock d’ouverture et réceptions.
- Dispatch selon les commandes et stock réel selon les BL préparés.
- Poids individuels et groupés, cartons, palettes et observations.
- Impression unitaire ou groupée A4 et PDF via le navigateur.
- Personnalisation du nom, des couleurs et des coordonnées de l’entreprise.
- Import des PDF texte Goldschmaus au format pris en charge : choix des produits, classement mémorisé, total net vérifié et doublons bloqués.
- Sauvegardes JSON, archives hebdomadaires et report du stock restant.

## Confidentialité

Les saisies restent dans le stockage local du navigateur. Aucun compte ou serveur nécessaire, aucun suivi d’utilisation, aucun CDN. Exporter régulièrement une sauvegarde JSON avec **Sauvegarder**. Restaurer ce fichier pour changer d’ordinateur ou de navigateur.

Le HTML partagé ne contient pas vos saisies. Gardez vos exports JSON, documents fournisseurs et BL PDF séparément du dépôt public.

## Sources et vérifications

L’archive **Mes-BL-sources.zip**, jointe à chaque version publiée, contient les sources structurées et la documentation détaillée. Après extraction :

```sh
node tools/build.js
node --test tests/public.test.cjs
```

Node.js 18 ou ultérieur suffit, sans installation de paquets. Les licences des composants tiers sont incluses dans les archives.

## Limites

Application portable dans un navigateur, sans installateur natif ni synchronisation entre PC. Les scans et autres formats fournisseurs ne sont pas encore pris en charge. Vérifier les contrôles et l’aperçu avant impression. Pour retirer les mentions ajoutées par le navigateur, décocher **En-têtes et pieds de page** dans les paramètres d’impression.
