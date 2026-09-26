# Retro CRT Tetris

Clone de Tetris en HTML/CSS/JS pur, sans dépendance, avec esthétique terminal rétro (années 70/80) : scanlines CRT, glow phosphore, châssis d'écran, police pixel.

Jouable sur ordinateur (clavier) et sur smartphone (boutons tactiles + swipe).

## Menu et difficulté

Au lancement, un écran de menu propose 3 niveaux de difficulté (FACILE / NORMAL / DIFFICILE), qui fixent la vitesse de chute de départ et sa progression par niveau. Le bouton PAUSE (ou `P` / `Échap`) ouvre un menu de pause avec :
- **REPRENDRE**
- **RECOMMENCER** (relance une partie avec la même difficulté)
- **MENU PRINCIPAL** (retour à l'écran de sélection de difficulté)

## Son

Bruitages synthétisés en direct via Web Audio API (ondes carrées/triangulaires façon puce sonore 80s) — aucun fichier audio externe, aucune musique de fond. Un son pour chaque action : déplacement, rotation, chute, verrouillage, lignes complétées (fanfare spéciale pour un tetris), montée de niveau, game over, et navigation dans les menus. Bouton **🔊 SON** pour couper/réactiver.

## Contrôles

**Clavier**
- `←` / `→` : déplacer
- `↓` : descente rapide (soft drop)
- `↑` : rotation
- `Espace` : chute instantanée (hard drop)
- `P` ou `Échap` : pause

**Tactile**
- Boutons à l'écran : gauche / droite / rotation / bas / drop
- Swipe gauche/droite sur la grille : déplacer
- Swipe bas : descente rapide
- Tap court sur la grille : rotation

## Règles implémentées

- Sac de 7 pièces (bag randomizer)
- Ghost piece (aperçu de la position d'atterrissage)
- Score standard : simple 40×niveau, double 100×niveau, triple 300×niveau, tetris 1200×niveau
- Montée de niveau tous les 10 lignes, vitesse de chute croissante
- Pause / Game Over avec redémarrage

## Stack technique

- HTML5 Canvas, CSS3, JavaScript vanilla (aucune dépendance, aucun build)
- Police `Press Start 2P` (Google Fonts) pour l'UI
- Un seul fichier `index.html` autonome

## Structure

```
.
├── index.html   # jeu complet (HTML + CSS + JS)
├── LICENSE
└── README.md
```

## Licence

MIT — voir `LICENSE`.
