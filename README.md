# Tournée Colis — Orléans Centre

Organisateur de tournée de livraison : import d'adresses par OCR de screenshots,
optimisation du parcours par proximité, tracé routier réel et navigation Google Maps.

## Utilisation

Ouvre la page (GitHub Pages) sur ton téléphone :

1. **📸 Lire des screenshots** — dépose les captures de la liste des colis.
   L'OCR lit les adresses et les valide via la Base Adresse Nationale.
2. Vérifie les adresses détectées dans la fenêtre de revue, puis **Ajouter à la tournée**.
3. **⚡ Calculer le parcours optimal** — ordonne les arrêts depuis le dépôt.
4. **🧭 Ouvrir dans Google Maps** — navigation GPS (découpée en tronçons de 10 arrêts).
5. Coche les colis livrés au fur et à mesure.

> ⚠️ **Astuce OCR** : si l'OCR renvoie du charabia, une extension du navigateur
> interfère. Utilise la **navigation privée** ou désactive les extensions sur la page.

> 💾 La tournée est **sauvegardée automatiquement** dans le navigateur (localStorage) :
> tu peux fermer et rouvrir, elle est restaurée (adresses + colis livrés + notes).
> Le bouton **🗑️ Tout vider** efface cette sauvegarde.

## Technique

100 % client (aucun serveur) :
- [Leaflet](https://leafletjs.com/) — carte
- [Tesseract.js](https://tesseract.projectnaptha.com/) — OCR navigateur
- [Base Adresse Nationale](https://adresse.data.gouv.fr/) — géocodage
- [OSRM](http://project-osrm.org/) — routage routier
