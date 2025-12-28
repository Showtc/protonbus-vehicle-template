# Ago'Projects – Template véhicule
Ce dépôt fournit une structure de base standardisée pour la création de véhicules, ainsi qu’une nomenclature claire pour les noms de fichiers et de variables. Il est conçu pour faciliter la collaboration et assurer la cohérence entre les projets.

An english version is here : [README_EN.md](README_EN.md)

---

## Important
**Supprimez les fichiers `.gitkeep`** : Ils sont présents uniquement pour forcer Git à versionner les dossiers vides. Ils ne doivent pas être inclus dans votre projet final.

---

## Structure du dépôt
Voici l’arbre des dossiers et fichiers du dépôt :

```bash
.
├── LICENSE
├── README.md
├── README_EN.md
├── Vehicle_articulated_configuration.ini
├── Vehicle_folder
│   ├── content_info
│   │   └── thumbnails
│   ├── models
│   │   ├── Brand_type.txt
│   │   └── common
│   ├── repaints
│   ├── resources
│   │   ├── dev_files
│   │   │   └── requirements.txt
│   │   └── templates
│   ├── scripts
│   │   ├── doors
│   │   │   ├── rightdoor1.txt
│   │   │   ├── rightdoor2.txt
│   │   │   └── rightdoor3.txt
│   │   ├── physics
│   │   │   └── physics_Voith_euro2.txt
│   │   ├── lights
│   │   │   └── lights.txt
│   │   └── wheels
│   │       └── wheels.txt
│   ├── sounds
│   │   ├── MIDR_06-20-45
│   │   ├── common
│   │   ├── compressor
│   │   ├── doors
│   │   └── sounds.txt
│   └── textures
└── Vehicle_solo_configuration.ini
```

### Description des dossiers et fichiers

| Dossier/Fichier | Description |
|-----------------|-------------|
| `Vehicle_solo_configuration.ini` / `Vehicle_articulated_configuration.ini` | Fichiers de configuration définissant les paramètres obligatoires pour les vues et la physique du véhicule. |
| `Vehicle_folder/` | Dossier racine du véhicule. |
| `content_info/` | Contient les métadonnées supplémentaires du véhicule. |
| `content_info/thumbnails/` | Miniatures utilisées pour les aperçus (`preview`) dans les fichiers de configuration. |
| `models/` | Modèles 3D du véhicule et fichiers de configuration associés (ex : animation du compte-tours, vitesse). |
| `repaints/` | Livrées personnalisées pour le véhicule. |
| `resources/` | Ressources utilisateur (templates, etc.). *Note : Ago'Projects n’utilise pas ce dossier pour les manuels des véhicules.* |
| `resources/dev_files/` | Fichiers de développement comme les fichiers `.blend` (Blender) utilisés. |
| `resources/dev_files/requirements.text` | Fichier permettant à l'utilisateur de savoir quelle est la version minimale de Blender à utiliser, ou bien d'autres logiciels. |
| `scripts/` | Logique principale du véhicule (portes, boîtes de vitesses, éclairages, roues, etc.). |
| `sounds/` | Sons du véhicule et fichiers de configuration audio. |
| `textures/` | Textures du véhicule. |

## Nomenclature

### Règles générales
- **Caractères autorisés** : Utilisez uniquement des caractères ASCII (A-Z, a-z, 0-9, `_`, `-`).
- **Encodage** : Tous les fichiers doivent être encodés en **UTF-8**.
- **Casse** : Les noms de fichiers et dossiers doivent être en **minuscules**, avec des `_` (underscores) pour remplacer les espaces.
- **Points** : Remplacez les `.` par des `-` (ex : `MIDR_06-20-45`).
- **Snake case** : Utilisez le `snake_case` pour les noms de fichiers et variables, sauf pour les noms de marques (ex : `floor_e5.png`, ou dans le cas d'une marque `Hanover_EG3.png`)
- **Nom des fichiers et des variables** : Uniquement en anglais

### **Exemple de nommage**
Pour les textures d’une pièce comme le boîtier **Hanover EG3**, utilisez un préfixe commun pour regrouper les fichiers :
- `Hanover_EG3.png`
- `Hanover_EG3_buttons.png`
- `Hanover_EG3_buttons_on.png`

## Bonnes pratiques
- **Dossiers `common/`** : Contiennent uniquement les fichiers partagés entre toutes les variantes du véhicule.
- **Sous-dossiers dans `repaints/`** : Vous pouvez créer des sous-dossiers pour organiser les livrées par véhicule.
- **Cohérence** : Respectez la même convention de nommage pour tous les fichiers et variables.
- **Taille des images** : Les images doivent être des puissances de 2, c'est-à-dire 16x16, 32x32, 64x64, 256x256, 512x512, 1024x1024, 2048x2048 (max)
