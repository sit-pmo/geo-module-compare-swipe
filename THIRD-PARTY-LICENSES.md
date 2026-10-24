# Licences des composants tiers

Ce fichier liste les composants tiers **embarqués dans le fichier `main.js`** livré avec le module
(`npm run build`). Le code propre du module est publié sous GPL-3.0-or-later (voir `LICENSE`).

## Composant embarqué

### ol-ext 4.0.38 — Jean-Marc Viglino, IGN-France

- Source : <https://github.com/Viglino/ol-ext> — fichiers `ol-ext/dist/ol-ext.js` et `ol-ext/control/Swipe.css`.
- Licence : **BSD-3-Clause** (champ `license` du paquet npm et fichier `LICENSE-BSD.md` du paquet). Les en-têtes des
  fichiers sources et le fichier `LICENSE.md` du paquet mentionnent aussi la **CeCILL-B** (licence « BSD à la
  française »). Le module s'appuie sur l'option BSD-3-Clause, compatible avec la GPL-3.0.
- Texte (copié de `LICENSE-BSD.md` du paquet) :

    BSD 3-Clause License
    
    Copyright (c) 2016-2021, Jean-Marc Viglino, IGN-France
    All rights reserved.
    
    Redistribution and use in source and binary forms, with or without
    modification, are permitted provided that the following conditions are met:
    
    1. Redistributions of source code must retain the above copyright notice, this
       list of conditions and the following disclaimer.
    
    2. Redistributions in binary form must reproduce the above copyright notice,
       this list of conditions and the following disclaimer in the documentation
       and/or other materials provided with the distribution.
    
    3. Neither the name of the copyright holder nor the names of its
       contributors may be used to endorse or promote products derived from
       this software without specific prior written permission.
    
    THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS "AS IS"
    AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE
    IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE
    DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT HOLDER OR CONTRIBUTORS BE LIABLE
    FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL
    DAMAGES (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR
    SERVICES; LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER
    CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY,
    OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE
    OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.

## Autres composants

- **OpenLayers (`ol`)** : fourni par la plateforme GEO à l'exécution, **non embarqué** dans le module
  (BSD-2-Clause). ol-ext complète cet objet global.
- **Angular** : fourni par la plateforme GEO (`externals` de webpack), non embarqué.
- **Dépendances de développement** (webpack, archiver, loaders…) : utilisées pour construire le module,
  non livrées dans `main.js`.

## Inspiration

Le module s'inspire du script communautaire « geo_swipe_control » (Malo Tartevet, Quimperlé Communauté, licence
Beerware, puis Pierre C du CD 07). Il a été réécrit sous forme de module. La licence Beerware n'impose que de conserver
la mention de ses auteurs, ce que ce fichier, le README et l'en-tête de `extension.js` font.

## Génération

Liste vérifiée avec `license-checker --production` sur une installation propre (`npm ci --omit=dev`), puis
croisée avec le contenu réel du bundle. À refaire à chaque changement de dépendance.
