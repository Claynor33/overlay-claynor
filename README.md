# Overlay Claynor — version web (GitHub Pages)

Tous les overlays sont reliés : change de jeu ou le nombre de trophées
n'importe où (widget OU scène), et l'info + la couleur se répercutent
partout automatiquement. Style HUD cyan · trophées or · alertes Streamlabs.

## Déployer sur GitHub Pages (≈ 3 min)
1. Crée un dépôt **public** (ex. `overlay-claynor`).
2. Upload tout ce dossier à la racine (garde le dossier `scenes/`).
3. Settings → Pages → Deploy from branch `main` / `/root` → Save.
4. Ouvre `https://TON-PSEUDO.github.io/overlay-claynor/` → la page de
   config te donne toutes tes URL OBS toutes prêtes.

> Le dépôt reste sans secret : le token est lu depuis l'URL (`?token=...`)
> que tu colles dans OBS.

## La synchronisation (widgets ET scènes)
Tout partage le même état (même origine GitHub Pages). Change le jeu / les
trophées depuis n'importe quelle page :
- les **widgets** (caméra, soutiens, objectif, alertes, célébration) suivent ;
- les **scènes** Just Chatting et Jeu tout-en-un suivent aussi (jeu + trophées
  + couleur) ;
- l'écran **Début de stream** suit la couleur d'accent.

## Dans OBS
Chaque overlay = une source Navigateur (URL donnée par `index.html`), à la
taille indiquée. Ordre : `celebration` › `alertes` › widgets › webcam ›
capture du jeu. Change de jeu : clic droit sur `jeu-trophees` (ou le panneau
d'une scène) → Interagir → champ « Jeu » → OK.

## Réglages / test
- `demo:true` → exemples ; mets `false` pour le direct.
- Test console : testFollow() testSub() testRaid() testBits() testCelebrate()
