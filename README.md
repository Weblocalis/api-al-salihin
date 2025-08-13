> بِسْمِ اللَّهِ الرَّحْمَٰنِ الرَّحِيمِ

# Quran API - Al Salihin

![License](https://img.shields.io/github/license/Weblocalis/quran-api-al-salihin?style=flat-square)
![Repo Size](https://img.shields.io/github/repo-size/Weblocalis/quran-api-al-salihin?color=blue&style=flat-square)
![Last Commit](https://img.shields.io/github/last-commit/Weblocalis/quran-api-al-salihin?style=flat-square)
![Contributors](https://img.shields.io/github/contributors/Weblocalis/quran-api-al-salihin?style=flat-square)
![Issues](https://img.shields.io/github/issues/Weblocalis/quran-api-al-salihin?style=flat-square)
![Pull Requests](https://img.shields.io/github/issues-pr/Weblocalis/quran-api-al-salihin?style=flat-square)

**Static API to access the Quran text, Juz divisions, and Tafsir in multiple languages.**  
API statique pour accéder au texte du Coran, aux découpages par Juz et aux Tafsir en plusieurs langues.

---

## Project Structure / Structure du projet

**🇬🇧:** The `data` folder contains all Quran text data and Tafsir (commentaries), organized by language.  
**🇫🇷:** Le dossier `data` contient toutes les données textuelles et les commentaires (tafsir) du Coran, organisés par langue.

```sh
.
├── CONTRIBUTING.md
├── LICENSE
├── README.md
└── data
    ├── juz.json          # EN: Division of the Quran into 30 Juz
    │                     # FR: Division du Coran en 30 Juz
    ├── quran-text        # EN: Quran text / FR: Texte du Coran
    │   ├── ar            # Arabic (original)
    │   │   └── surah     # Surahs in JSON files
    │   ├── fr            # French (translation)
    │   │   └── surah
    │   ├── en            # English
    │   ├── ...           # Other languages (de, es, id, etc.)
    └── tafsir            # EN: Commentaries (Tafsir) / FR: Commentaires (Tafsir)
        ├── ar
        ├── fr
        └── en
```
> Each language folder contains Surahs as individual JSON files (e.g., `001.json`) and an `index.json` file listing all Surahs.
---

## Contenu des fichiers

### Fichier surah/ar individuel (`001.json`)

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