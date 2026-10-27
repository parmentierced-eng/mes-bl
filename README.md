# Mes BL

**Bons de livraison, stock et dispatch — sur votre ordinateur, sans connexion.**

Application portable en français, avec nom et logo personnalisables, six palettes de couleurs et coordonnées configurables sur les BL. Elle démarre entièrement vide, sans client, fournisseur ou document préchargé.

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
- Personnalisation du nom, du logo, des couleurs et des coordonnées de l’entreprise. Le logo apparaît sur les BL et voyage dans les sauvegardes JSON.
- Import des BL Goldschmaus, Cordts, Unifleisch, Färber et Ulmer Fleisch aux formats pris en charge : lecture PDF ou OCR local, contrôle et correction, classement mémorisé et doublons bloqués.
- Sauvegardes JSON, archives hebdomadaires et report du stock restant.

## Confidentialité

Les saisies restent dans le stockage local du navigateur. Aucun compte ou serveur nécessaire, aucun suivi d’utilisation, aucun CDN. Exporter régulièrement une sauvegarde JSON avec **Sauvegarder**. Restaurer ce fichier pour changer d’ordinateur ou de navigateur.

Le HTML partagé ne contient pas vos saisies. Gardez vos exports JSON, documents fournisseurs et BL PDF séparément du dépôt public.

## Sources et vérifications

L’archive **Mes-BL-sources.zip**, jointe à chaque version publiée, contient les sources structurées et la documentation détaillée. Après extraction :

```sh
node tools/build.js
node --test tests/public.test.cjs tests/adapters.test.cjs
```

Node.js 18 ou ultérieur suffit, sans installation de paquets. Les licences des composants tiers sont incluses dans les archives.

## Limites

Application portable dans un navigateur, sans installateur natif ni synchronisation entre PC. Les scans des formats reconnus passent par un OCR local : vérifier et corriger chaque référence, date, carton et poids avant validation. Les formats non reconnus et Steinemann ne sont pas encore pris en charge. Vérifier les contrôles et l’aperçu avant impression. Pour retirer les mentions ajoutées par le navigateur, décocher **En-têtes et pieds de page** dans les paramètres d’impression.

## Mise à jour 1.1.0

Avant de remplacer le fichier HTML, exporter une sauvegarde JSON. Fermer l’application, remplacer **distribution/Mes-BL.html** au même emplacement puis rouvrir dans le même navigateur. Les anciennes sauvegardes sans logo restent acceptées. En cas de changement de dossier ou de PC, restaurer le JSON.

Dans **Personnalisation → Logo de l’entreprise**, choisir un PNG, JPEG ou WebP (5 Mo maximum), vérifier l’aperçu puis enregistrer. Le logo peut être remplacé ou supprimé ; aucun logo personnel n’est intégré aux fichiers distribués.

Pour les nouveaux imports fournisseurs, le document source est affiché et les champs sont modifiables avant classement. Les CMR et attestations ne sont pas additionnés au BL détaillé. Pour Ulmer, sélectionner le fournisseur bœuf/porc ; les cartons proviennent des lignes d’emballage. Pour Cordts, un écart de total de 0,01 kg est signalé et toléré ; les poids des lignes restent la base du stock.
