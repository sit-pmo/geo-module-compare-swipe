# Journal des nouveautés

Toutes les évolutions notables du module « Comparateur de rasters (rideau / loupe) ». Le format suit
[Keep a Changelog](https://keepachangelog.com/fr/1.1.0/) et le versionnement
[SemVer](https://semver.org/lang/fr/).

Ce fichier est affiché dans GEO, dans la fenêtre « Nouveautés » du module : il s'écrit pour les
**utilisateurs**, en français, pas pour les développeurs (la liste des commits est dans git). La version
la plus récente publiée doit être celle de `package.json` et de `src/plugin.geoext.json`
(`npm test` le vérifie).

## [Non publié]

## [0.2.0] — 2026-10-24

Première version publiée du module : comparer deux rasters directement sur la carte principale de l'application.

### Ajouté

- Mode « Rideau » : un curseur déplaçable sépare le raster de gauche et celui de droite
- Mode « Loupe » : le raster de droite n'apparaît que dans un cercle qui suit la souris
- Catalogue IGN : dernière orthophoto, éditions de 2003 à 2021 et prises de vues historiques 1950-1980
- Les fonds de plan configurés dans GEO (WMTS, WMS, XYZ) peuvent être comparés, en plus du catalogue IGN ; réglage
  « Fonds de plan GEO à comparer » dans le Générateur
- Réglage « Emplacement des menus » : barre sur la carte ou panneau latéral
- Réglages du Générateur : rasters de départ à gauche et à droite, mode initial, rayon de la loupe, libellé et
  position du bouton
- Fenêtre « Nouveautés » : le lien « v0.2.0 · Nouveautés » de la barre de comparaison (ou du panneau latéral)
  ouvre ce journal, avec un point rouge tant que la dernière version n'a pas été lue
