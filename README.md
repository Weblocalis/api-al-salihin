> <p align="center" dir="rtl" lang="ar" style="font-size:1.5em; font-style: italic; color: #0d6efd;">
> بِسْمِ اللَّهِ الرَّحْمَٰنِ الرَّحِيمِ
> </p>

> <p align="center" dir="rtl" lang="ar" style="font-size:1.3em; font-weight: bold; color: #198754;">
> السلام عليكم
> </p>

# Quran API - Al Salihin

![License](https://img.shields.io/github/license/Weblocalis/quran-api-al-salihin?style=flat-square)
![Repo Size](https://img.shields.io/github/repo-size/Weblocalis/quran-api-al-salihin?color=blue&style=flat-square)
![Last Commit](https://img.shields.io/github/last-commit/Weblocalis/quran-api-al-salihin?style=flat-square)
![Contributors](https://img.shields.io/github/contributors/Weblocalis/quran-api-al-salihin?style=flat-square)
![Issues](https://img.shields.io/github/issues/Weblocalis/quran-api-al-salihin?style=flat-square)
![Pull Requests](https://img.shields.io/github/issues-pr/Weblocalis/quran-api-al-salihin?style=flat-square)
![Made with ❤️ by Al Salihin](https://img.shields.io/badge/Made%20with-%E2%9D%A4%20by%20Al%20Salihin-red?style=flat-square)

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

## 📄 File Contents | Contenu des fichiers
**This section describes the structure of each JSON file containing Quran text.**

Cette section décrit la structure de chaque fichier JSON contenant le texte du Coran.

**Each Surah file follows a consistent schema to make it easy to parse and use in any application.**

Chaque fichier de sourate suit un schéma cohérent pour être facilement exploitable dans toute application.

### 🗂 Individual File | Fichier individuel

> JSON database of individual Surahs.  
Base de données JSON des sourates individuelles.  

Example / Exemple : **Al-Fatiha → `001.json`**  
Path / Chemin : `quran-text/(lang)/surah/<001:114>.json`

| Key | Description (EN) | Description (FR) |
|-----|------------------|------------------|
| `surah_number` | Surah number (1–114) | Numéro de la sourate (1–114) |
| `lang` | Language code (e.g., `"ar"`) | Code langue (ex: `"ar"`) |
| `name_ar` | Original Arabic name | Nom arabe original |
| `verses_count` | Total number of verses | Nombre total de versets |
| `revelation_place` | `"Mecca"` or `"Medina"` | `"Mecque"` ou `"Médine"` |
| `revelation_type` | `"Makkia"` or `"Madaniya"` | `"Makkia"` ou `"Madaniya"` |
| `translated_by` | Translator or source name | Nom du traducteur ou source |
| `verses` | Array of verses | Tableau des versets |
| `verses[].verse_number` | Verse number | Numéro du verset |
| `verses[].text` | Verse text | Texte du verset |

### 📄 index.json

JSON file listing metadata for all Surahs in a given language (like a table of contents).  
Fichier JSON listant les métadonnées de toutes les sourates dans une langue donnée (comme une table des matières).  

Example / Exemple : `data/quran-text/ar/surah/index.json`

| Key | Description (EN) | Description (FR) |
|-----|------------------|------------------|
| `surah_number` | Surah number (1–114) | Numéro de la sourate (1–114) |
| `lang` | Language code (e.g., `"ar"`) | Code langue (ex: `"ar"`) |
| `name_ar` | Original Arabic name | Nom arabe original |
| `name_translated` | Translated Surah name in the language | Nom traduit de la sourate dans la langue |
| `verses_count` | Total number of verses | Nombre total de versets |
| `revelation_place` | `"Mecca"` or `"Medina"` | `"Mecque"` ou `"Médine"` |
| `revelation_type` | `"Makkia"` or `"Madaniya"` | `"Makkia"` ou `"Madaniya"` |

### 📄 surah.json

JSON file containing the full Quran text for one Surah (all verses).  
Fichier JSON contenant le texte complet d’une sourate (tous les versets).  

Example / Exemple : `data/quran-text/ar/surah/001.json`

| Key | Description (EN) | Description (FR) |
|-----|------------------|------------------|
| `surah_number` | Surah number (1–114) | Numéro de la sourate (1–114) |
| `lang` | Language code (e.g., `"ar"`) | Code langue (ex: `"ar"`) |
| `name_ar` | Original Arabic name | Nom arabe original |
| `verses_count` | Total number of verses | Nombre total de versets |
| `revelation_place` | `"Mecca"` or `"Medina"` | `"Mecque"` ou `"Médine"` |
| `revelation_type` | `"Makkia"` or `"Madaniya"` | `"Makkia"` ou `"Madaniya"` |
| `translated_by` | Translator or source name | Nom du traducteur ou source |
| `verses` | Array of verses with verse number and text | Tableau des versets avec numéro et texte |
| `verses[].verse_number` | Verse number | Numéro du verset |
| `verses[].text` | Verse text | Texte du verset |

### 📄 Juz File | Fichier Juz

JSON file listing the 30 divisions (Juz) of the Quran, with their starting and ending Surah/Ayah.  
Fichier JSON listant les 30 divisions (Juz) du Coran, avec leur début et fin (Sourate/Ayah).  

Example / Exemple : `data/juz.json`

| Key | Description (EN) | Description (FR) |
|-----|------------------|------------------|
| `juz_number` | Juz number (1–30) | Numéro du Juz (1–30) |
| `start` | Starting point of the Juz | Point de départ du Juz |
| `start.surah_number` | Surah number where the Juz starts | Numéro de la sourate où commence le Juz |
| `start.verse_number` | Verse number where the Juz starts | Numéro du verset où commence le Juz |
| `end` | Ending point of the Juz | Point de fin du Juz |
| `end.surah_number` | Surah number where the Juz ends | Numéro de la sourate où se termine le Juz |
| `end.verse_number` | Verse number where the Juz ends | Numéro du verset où se termine le Juz |

---

## Utilisation de l’API | API Usage

Les fichiers JSON sont accessibles via des URLs structurées, par exemple :  
The JSON files are accessible via structured URLs, for example:

- `https://api.al-salihin.com/data/quran-text/fr/surah/001.json`  
  (Texte complet de la sourate 1 en français / Full text of Surah 1 in French)

- `https://api.al-salihin.com/data/juz.json`  
  (Découpage par Juz / Juz division)

Ces URLs permettent à toute application ou utilisateur d’accéder facilement aux données du Coran et aux Tafsir.  
These URLs allow any application or user to easily access Quran data and Tafsir.

### Exemple de requête JavaScript | JavaScript Fetch Example

```js
// Exemple pour récupérer la sourate 1 (Al-Fatiha) en français
fetch('https://api.al-salihin.com/data/quran-text/fr/surah/001.json')
  .then(response => {
    if (!response.ok) {
      throw new Error('Erreur réseau : ' + response.status);
    }
    return response.json();
  })
  .then(data => {
    console.log('Sourate:', data.name_ar, '(en français)');
    data.verses.forEach(verse => {
      console.log(`Verset ${verse.verse_number}: ${verse.text}`);
    });
  })
  .catch(error => {
    console.error('Erreur lors de la récupération:', error);
  });
```
---

## Contribution

Merci de lire le fichier [`CONTRIBUTING.md`](CONTRIBUTING.md) avant de proposer des modifications.  
Please read the [`CONTRIBUTING.md`](CONTRIBUTING.md) file before submitting any changes.

Nous acceptons les contributions pour :  
We welcome contributions for:

- Ajout ou correction de traductions  
- Adding or correcting translations

- Ajout de tafsir  
- Adding Tafsir (commentaries)

- Mise à jour des fichiers `index.json` et `juz.json`  
- Updating the `index.json` and `juz.json` files

- Amélioration de la documentation  
- Improving the documentation

---

## Licence

Ce projet est distribué sous la licence [MIT](LICENSE).  
Pour plus d’informations, consultez le fichier `LICENSE` à la racine du dépôt.

---
## Auteur | Author

**A. Mharzi** / **WebLocalis**

[![AbSphere](https://img.shields.io/github/followers/AbSphere?label=AbSphere&style=social)](https://github.com/AbSphere) &nbsp;&nbsp;|&nbsp;&nbsp; [![Weblocalis](https://img.shields.io/github/followers/Weblocalis?label=Weblocalis&style=social)](https://github.com/Weblocalis)

Contributions, suggestions et questions sont les bienvenues !  
Vous pouvez me contacter via GitHub ou [email](mailto:abdelhakmharzi@gmail.com).

---

*Al Salihin - Projet communautaire pour un accès libre au Coran multilingue.*