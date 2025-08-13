> بِسْمِ اللَّهِ الرَّحْمَٰنِ الرَّحِيمِ
# Quran API - Al Salihin

**Static API to access the Quran text, Juz divisions, and Tafsir in multiple languages.**

API statique pour accéder au texte du Coran, aux découpages par Juz et aux Tafsir en plusieurs langues.

---

## Project Structure

The `data` folder contains all Quran text data and Tafsir (commentaries), organized by language.

Le dossier `data` contient toutes les données textuelles et les commentaires (tafsir) du Coran, organisés par langue.

```sh
.
├── CONTRIBUTING.md
├── LICENSE
├── README.md
└── data
    ├── juz.json
    ├── quran-text
    │   ├── ar
    │   │   └── surah
    │   │       ├── 001.json
    │   │       ├── 002.json
    │   │       ├── 003.json
    │   │       └── index.json
    │   ├── de
    │   ├── en
    │   ├── es
    │   ├── fr
    │   │   └── surah
    │   │       ├── 001.json
    │   │       └── index.json
    │   ├── id
    │   ├── ja
    │   ├── ms
    │   ├── ru
    │   ├── tr
    │   ├── ur
    │   └── zh
    └── tafsir
        ├── ar
        ├── en
        └── fr
```

---

## Contenu des fichiers

### Fichier sourate individuel (`001.json`)

- `surah_number` : numéro de la sourate (1-114)  
- `lang` : code langue (ex: "fr", "ar")  
- `name_ar` : nom arabe original  
- `verses_count` : nombre total de versets  
- `revelation_place` : "Mecque" ou "Médine"  
- `revelation_type` : `"Makkia"` ou `"Madaniya"`  
- `translated_by` : nom du traducteur ou source  
- `verses` : tableau des versets avec :  
  - `verse_number` : numéro du verset  
  - `text` : texte du verset  

### Fichier `index.json` (dans chaque langue)

Liste des sourates disponibles avec métadonnées et chemin vers fichier.

### Fichier `juz.json`

Liste des 30 Juz avec début et fin en termes de sourate et verset, pour découpage précis.

---

## Utilisation de l’API

Les fichiers JSON sont accessibles via URLs structurées, par exemple :

- `https://api.al-salihin.com/data/quran-text/fr/surah/001.json` 
- `https://api.al-salihin.com/data/juz.json`

---

## Contribution

Merci de lire le fichier `CONTRIBUTING.md` avant de proposer des modifications.  
Nous acceptons les contributions pour :

- Ajout ou correction de traductions  
- Ajout de tafsir  
- Mise à jour des fichiers `index.json` et `juz.json`  
- Amélioration de la documentation  

---

## Licence

Ce projet est sous licence MIT. Voir le fichier `LICENSE` pour plus de détails.

---

## Contact

Pour toute question, suggestion ou problème, merci d’ouvrir une issue sur GitHub.

---

*Al Salihin - Projet communautaire pour un accès libre au Coran multilingue.*