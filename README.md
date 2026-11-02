# Ago'Projects – Vehicle Template
This repository provides a standardized base structure for vehicle creation, along with clear naming conventions for files and variables. It is designed to facilitate collaboration and ensure consistency across projects.

Une version française est disponible ici : [README_FR.md](README_FR.md)

---

## Important
Delete `.gitkeep` files: These files are only present to force Git to track empty directories. They should not be included in your final project.

---

## Repository Structure
Here is the directory and file tree of the repository:

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

### Description of Folders and Files

| Folder/File | Description |
|-------------|-------------|
| `Vehicle_solo_configuration.ini` / `Vehicle_articulated_configuration.ini` | Configuration files defining mandatory parameters for vehicle views and physics. |
| `Vehicle_folder/` | Root folder for the vehicle. |
| `content_info/` | Contains additional metadata for the vehicle, with the LICENSE file. |
| `content_info/CHANGELOG.md` / `content_info/CHANGELOG_FR.md` | Changelog between each versions, public and development. |
| `content_info/thumbnails/` | Thumbnails used for previews (`preview`) in configuration files. |
| `models/` | 3D models of the vehicle, and vehicle configuration files with tachometer animation, speed. |
| `repaints/` | Custom liveries for the vehicle. |
| `resources/` | User resources (templates, manuals, etc.). |
| `resources/dev_files/` | Developement files as `.blend` (Blender) files used. |
| `resources/dev_files/requirements.text` | A file that allows the user to know what the minimum version of Blender to use is, or other software. |
| `scripts/` | Main logic of the vehicle (doors, gearboxes, lighting, wheels, etc.). |
| `sounds/` | Vehicle sounds and audio configuration files. |
| `textures/` | Vehicle textures. |

Note for sounds and models files, you need to put the whole path from the root folder. Hence why you will see `sounds/` and `models/` even if configuration files are in those folders.

## Nomenclature

### General Rules
- Allowed Characters: Use only ASCII characters (A-Z, a-z, 0-9, `_`, `-`)
- Encoding: All files must be encoded in UTF-8
- Snake Case: Use `snake_case` for file and variable names
- Files names and variables: Only in english

### Naming Example
For textures of a part like the Hanover EG3 unit, use a common prefix to group files:
- `Hanover_EG3.png`
- `Hanover_EG3_buttons.png`
- `Hanover_EG3_buttons_on.png`

## Version History
To maintain a written record of each version outside the public version manuals, it is mandatory to document the changes between versions in the `CHANGELOG.md` and `CHANGELOG_FR.md` files.

The format should follow [Keep a Changelog](https://keepachangelog.com/en/1.1.0/), using the versioning semantics of [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## Best Practices
- `common/` Folders: Only contain files shared among all vehicle variants.
- Subfolders in `repaints/`: You can create subfolders to organize liveries by vehicle.
- Consistency: Follow the same naming convention for all files and variables.
- Images size : Images must be powers of 2, i.e. 16x16, 32x32, 64x64, 256x256, 512x512, 1024x1024, 2048x2048 (max).
