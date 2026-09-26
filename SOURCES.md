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
- Niveau 4 — CONVERSATION : parole spontanée multi-locuteurs issue de l’AMI Meeting Corpus. Le futur palier « slang/AAVE » pourra utiliser une source distincte lorsque sa licence et sa diffusion navigateur seront vérifiées.

LibriSpeech est un corpus d'anglais lu, et non de conversation spontanée. Il est utilisé aux niveaux 2 et 3 parce que sa licence CC BY 4.0 permet cette preuve pédagogique et technique. La source officielle OpenSLR SLR12 reste la référence de licence.


## Niveau 4 — conversation spontanée

Le niveau 4 utilise un extrait de **l’AMI Meeting Corpus**, réunion **ES2002a**, enregistrement Mix-Headset. Il s’agit de vraie parole conversationnelle multi-locuteurs avec hésitations, contractions et débit naturel.

- Source originale : AMI Meeting Corpus, The University of Edinburgh.
- Licence : Creative Commons Attribution 4.0 International (CC BY 4.0).
- Fichier utilisé : `ami_sample.wav`, extrait des ~180 premières secondes de `ES2002a.Mix-Headset.wav`.
- Le fichier de test est publié dans le dépôt public `rh-aiservices-bu/speaker-diarization` avec une attribution explicite CC BY 4.0.
- English Ear lit ce fichier à distance sans le copier dans ce dépôt.
- Les phrases et timestamps utilisés par l’exercice proviennent des annotations manuelles AMI au niveau des mots pour ES2002a.

Important : ce niveau est nommé **CONVERSATION** plutôt que **SLANG**. L’AMI Meeting Corpus fournit bien de la parole spontanée, mais ce n’est pas un corpus d’argot américain/AAVE. Un futur niveau réellement slang pourra être ajouté séparément sans prétendre que cette source en est une.


## Étincelle 10 — réservoir de contenu

English Ear ne dépend plus d'une petite liste fixe pour les niveaux LibriSpeech.

- Niveau 1 — TRAINING : 100 exercices TTS construits localement à partir de phrases de base et de combinaisons conversationnelles contrôlées.
- Niveaux 2–3 : l'application lit `CHAPTERS.TXT` du dépôt LibriSpeech `dev-clean`, choisit de façon stable un pack de 24 chapitres pour l'appareil, charge leurs transcriptions puis construit les exercices à partir des vrais identifiants audio.
- HUMAN conserve les énoncés courts (2–8 mots).
- HARD conserve les énoncés intermédiaires (9–14 mots), afin d'éviter les phrases interminables.
- Les identifiants LibriSpeech sont utilisés comme clés stables pour la mémoire adaptative ; l'ordre du corpus peut donc évoluer sans rattacher l'historique à la mauvaise phrase.
- Si la découverte distante des chapitres échoue, l'application retombe sur un petit pack local de secours.

Le pack de 24 chapitres est sélectionné de manière stable par appareil dans le catalogue `dev-clean`. Le corpus source contient des milliers d'énoncés ; English Ear n'a donc plus besoin de coder chaque phrase à la main.

Le niveau 4 CONVERSATION utilise encore le fichier AMI de trois minutes documenté ci-dessus. Il contient actuellement 24 segments conversationnels vérifiés ; il devra être élargi avec d'autres enregistrements conversationnels avant d'atteindre la même profondeur que les niveaux 2–3.
