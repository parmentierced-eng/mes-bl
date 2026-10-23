# Contrôle de préparation publique

- 51 fichiers et entrées ZIP analysés (sources et application construite).
- Aucune identité de l’édition privée, liste de clients, coordonnées d’origine, chemin utilisateur local ou référence du BL réel de test détectés.
- Démarrage vierge : clients, fournisseurs, stocks, réceptions et archives vides.
- Aucun logo ou document métier copié dans cette édition.
- Stockage distinct de l’édition privée ; absence de lecture automatique de ses données vérifiée dans Edge.
- Adaptateur Goldschmaus conservé en tant que format de fichier public pris en charge, sans fournisseur ni réception préchargés.
- Tests : calculs de stock, import avec données fictives, six palettes, nom, coordonnées, persistance, export JSON et BL personnalisés.
- Aucun appel HTTP/HTTPS pendant le parcours de test hors ligne.

Le contrôle porte sur les fichiers livrés. Les utilisateurs peuvent ensuite saisir leurs propres données et doivent conserver leurs sauvegardes JSON et leurs BL séparément d’un dépôt public.
