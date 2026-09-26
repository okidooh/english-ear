# English Ear — sources audio

## Étincelle 2 — REAL SPEECH

Les 20 extraits de démonstration REAL SPEECH utilisent **LibriSpeech**, corpus de parole anglaise lue, préparé par Vassil Panayotov, Guoguo Chen, Daniel Povey et Sanjeev Khudanpur.

- Source officielle : OpenSLR SLR12
- Licence du corpus : Creative Commons Attribution 4.0 International (CC BY 4.0)
- Corpus dérivé d'enregistrements LibriVox et de textes du domaine public.
- Sous-ensemble utilisé ici : `dev-clean`, locuteur 1272, chapitres 128104 et 135031.
- Fichiers : 1272-128104-0000 à 0014 et 1272-135031-0000 à 0004.
- Les fichiers sont lus à distance depuis une copie de démonstration LibriSpeech hébergée sur Hugging Face (patrickvonplaten/LibriSpeechTest). Ils ne sont pas copiés dans ce dépôt.

Référence : V. Panayotov, G. Chen, D. Povey, S. Khudanpur, “LibriSpeech: An ASR Corpus Based on Public Domain Audio Books”, ICASSP 2015.

Cette Étincelle valide uniquement la chaîne technique « vraie voix humaine → dictée → comparaison ». LibriSpeech est de la parole lue et n'est pas considéré comme le corpus final de conversation spontanée d'English Ear.


## Progression pédagogique

- Niveau 1 — TRAINING : synthèse vocale en-US, vitesse réglable.
- Niveau 2 — HUMAN : sélection de phrases LibriSpeech `dev-clean/1272/135031` courtes et simples, avec vraie voix humaine. Cette sélection vise une marche intermédiaire accessible ; le corpus reste de la parole lue.
- Niveau 3 — HARD : sélection LibriSpeech plus longue et lexicalement difficile, dont le chapitre 128104.
- Niveau 4 — SLANG : réservé à un futur corpus de parole spontanée/argot ; aucun audio n'est encore intégré.

LibriSpeech est un corpus d'anglais lu, et non de conversation spontanée. Il est utilisé aux niveaux 2 et 3 parce que sa licence CC BY 4.0 permet cette preuve pédagogique et technique. La source officielle OpenSLR SLR12 reste la référence de licence.


## Niveau 4 — conversation spontanée

Le niveau 4 utilise le Santa Barbara Corpus of Spoken American English (SBCSAE), principalement l'enregistrement SBC006 « Cuz », conversation animée entre deux cousines enregistrée à Los Angeles. Le corpus contient de la parole américaine naturellement produite, avec transcriptions et repères temporels au niveau des unités d'intonation.

Source : University of California, Santa Barbara, Santa Barbara Corpus of Spoken American English, Parts 1–4. Licence indiquée par UCSB/OpenSLR : Creative Commons Attribution-NoDerivatives 3.0 United States (CC BY-ND 3.0 US). Les médias restent servis depuis TalkBank ; English Ear ne modifie pas l'enregistrement source et ne le republie pas dans le dépôt.

Citation : Du Bois, John W., et al. (2000–2005), Santa Barbara Corpus of Spoken American English, Parts 1–4.

Important : « SLANG » est le nom pédagogique du niveau difficile de conversation spontanée. Tous les extraits ne contiennent pas nécessairement de l'argot lexical ; la difficulté vient aussi des réductions, du rythme, des tours conversationnels et de la parole non lue.
