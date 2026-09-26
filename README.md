# English Ear — Étincelle 0

But unique : valider sur un vrai iPhone que Safari/PWA sait :
1. prononcer une phrase anglaise (LISTEN),
2. varier la vitesse,
3. écouter le micro et afficher la transcription (SPEAK).

## Test le plus simple
Cette page doit être servie en HTTPS pour que les fonctions micro soient testées dans de bonnes conditions sur iPhone.
Dépose `index.html` sur un hébergement statique HTTPS (GitHub Pages, Cloudflare Pages, Netlify, etc.), puis ouvre l'URL dans Safari sur l'iPhone.

## Protocole
- LISTEN à 0.8x, 1.0x, 1.2x et 1.4x.
- SPEAK et autoriser le micro.
- Lire la phrase affichée et vérifier la transcription.
- Faire au moins 10 cycles LISTEN → SPEAK.
- Ajouter ensuite la page à l'écran d'accueil et refaire plusieurs cycles.
- Noter toute erreur affichée dans la zone État.

Critère GO : TTS et transcription restent fiables après les cycles répétés dans Safari et depuis l'icône écran d'accueil.
