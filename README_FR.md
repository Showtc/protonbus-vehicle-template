# Ago'Projects – Template véhicule
Ce dépôt fournit une structure de base standardisée pour la création de véhicules, ainsi qu’une nomenclature claire pour les noms de fichiers et de variables. Il est conçu pour faciliter la collaboration et assurer la cohérence entre les projets.

An english version is here : [README_EN.md](README_EN.md)

---

## Important
Supprimez les fichiers `.gitkeep` : Ils sont présents uniquement pour forcer Git à versionner les dossiers vides. Ils ne doivent pas être inclus dans votre projet final.

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
│   │   └── CHANGELOG.md
│   │   └── CHANGELOG_FR.md
│   │   └── thumbnails
│   ├── models
│   │   └── common
│   ├── repaints
│   ├── resources
│   │   ├── dev_files
│   │   │   └── requirements.txt
│   │   └── templates
│   ├── scripts
│   │   ├── doors
│   │   │   ├── right_door_1.txt
│   │   │   ├── right_door_2.txt
│   │   │   └── right_door_3.txt
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
│   │   └── doors
│   ├── textures
│   ├── model_vehicle.txt
│   └── sounds_motor_name.txt
└── Vehicle_solo_configuration.ini
```

### Description des dossiers et fichiers

| Dossier/Fichier | Description |
|-----------------|-------------|
| `Vehicle_solo_configuration.ini` / `Vehicle_articulated_configuration.ini` | Fichiers de configuration définissant les paramètres obligatoires pour les vues et la physique du véhicule. |
| `Vehicle_folder/` | Dossier racine du véhicule. |
| `content_info/` | Contient les métadonnées supplémentaires du véhicule. |
| `content_info/CHANGELOG.md` / `content_info/CHANGELOG_FR.md` | Journal des modifications entre chaque version publique et de développement. |
| `content_info/thumbnails/` | Miniatures utilisées pour les aperçus (`preview`) dans les fichiers de configuration. |
| `models/` | Modèles 3D du véhicule, et les fichiers de configuration des véhicules avec l'animation du compte-tours, vitesse. |
| `repaints/` | Livrées personnalisées pour le véhicule. |
| `resources/` | Ressources utilisateur (templates, etc.). *Note : Ago'Projects n’utilise pas ce dossier pour les manuels des véhicules.* |
| `resources/dev_files/` | Fichiers de développement comme les fichiers `.blend` (Blender) utilisés. |
| `resources/dev_files/requirements.text` | Fichier permettant à l'utilisateur de savoir quelle est la version minimale de Blender à utiliser, ou bien d'autres logiciels. |
| `scripts/` | Logique principale du véhicule (portes, boîtes de vitesses, éclairages, roues, etc.). |
| `sounds/` | Sons du véhicule, et les fichiers de configuration des sons. |
| `textures/` | Textures du véhicule. |

Note pour les fichiers de configuration des sons et des modèles 3D, vous devez mettre le chemin entier depuis la racine du véhicule. C'est pour cela que vous pouvez voir `sounds/` et `models/` même si les fichiers sont déjà dans ces dossiers.

## Nomenclature

### Règles générales
- Caractères autorisés : Utilisez uniquement des caractères ASCII (A-Z, a-z, 0-9, `_`, `-`).
- Encodage : Tous les fichiers doivent être encodés en UTF-8.
- Snake case : Utilisez le `snake_case` pour les noms de fichiers et variables
- Nom des fichiers et des variables : Uniquement en anglais

### Exemple de nommage
Pour les textures d’une pièce comme le boîtier Hanover EG3, utilisez un préfixe commun pour regrouper les fichiers :
- `Hanover_EG3.png`
- `Hanover_EG3_buttons.png`
- `Hanover_EG3_buttons_on.png`

## Historique des versions
Afin d'avoir une trace écrite de chaque version en dehors des manuels pour la version publique, il est obligatoire de rédiger les changements entre les versions dans les fichiers `CHANGELOG.md` et `CHANGELOG_FR.md`.

Le format doit se baser sur [Keep a Changelog](https://keepachangelog.com/fr/1.1.0/), dont la sémantique des versions [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## Bonnes pratiques
- Dossiers `common/` : Contiennent uniquement les fichiers partagés entre toutes les variantes du véhicule.
- Sous-dossiers dans `repaints/` : Vous pouvez créer des sous-dossiers pour organiser les livrées par véhicule.
- Cohérence : Respectez la même convention de nommage pour tous les fichiers et variables.
- Taille des images : Les images doivent être des puissances de 2, c'est-à-dire 16x16, 32x32, 64x64, 256x256, 512x512, 1024x1024, 2048x2048 (max).
