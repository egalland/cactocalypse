# Cactocalypse

Jeu de survie 2D dans le navigateur, créé pour le thème **Cactus** d’Inktober 2026. Version **4.1**, avec le correctif du plantage lors de l’affichage des boosts au sol.

## Jouer en local

Le jeu utilise des modules JavaScript : il faut le servir en HTTP.

```bash
python -m http.server 8080
```

Ouvrir ensuite <http://localhost:8080> dans un navigateur récent. Aucun paquet à installer ni compilation nécessaire.

## Commandes

- ZQSD, WASD ou flèches : déplacement.
- Espace : esquive.
- E : ouverture d’un coffre à proximité.
- Échap : pause.
- 1, 2 ou 3 : choix d’une mutation.
- Attaques automatiques ; joystick et boutons sur mobile.

## Contenu

- Quatre cactus jouables aux capacités différentes.
- Trois mondes : désert, glace et magma, chacun avec ses monstres et son boss.
- Glace glissante, lave dangereuse, obstacles fixes et soins à ramasser.
- 52 objets, 21 mutations et plusieurs combinaisons d’effets.
- Coffres dont le prix augmente sur l’ensemble de la partie.
- Aimant d’XP rare et boosts temporaires de 20 secondes.
- Animations, illustrations et audio inclus.

## Organisation

- `index.html` : écran de jeu et interface.
- `style.css` : présentation et commandes mobiles.
- `engine.mjs` : règles, progression, ennemis, objets et sorts.
- `game.js` : affichage Canvas, saisie et interface.
- `appearance.mjs` : assemblage du cactus et animations.
- `asset-rects.mjs` : zones des planches d’images.
- `audio.mjs` : sons et musique synthétisés.
- `*.png` : personnages, monstres, objets et éléments du décor.

Tous les chemins sont relatifs, pour permettre l’hébergement à la racine ou dans un sous-dossier. Le dépôt peut être servi directement comme site statique.

## Vérifier la syntaxe

```bash
node --check game.js
node --check engine.mjs
node --check appearance.mjs
node --check audio.mjs
```

Les illustrations sont générées par IA. Aucune clé API ni dépendance à ChatGPT n’est nécessaire pour jouer. La partie actuelle reste en mémoire et recommence lorsque la page est rechargée.
