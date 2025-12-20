# Ago'Projects – Vehicle Templates
This repository provides a standardized base structure for vehicle creation, along with clear naming conventions for files and variables. It is designed to facilitate collaboration and ensure consistency across projects.

---

## Important
**Delete `.gitkeep` files**: These files are only present to force Git to track empty directories. They should not be included in your final project.

---

## Repository Structure
Here is the directory and file tree of the repository:

```bash
.
├── README.md
├── README_EN.md
├── Vehicle_articulated_configuration.ini
├── Vehicle_folder/
│   ├── content_info/
│   │   └── thumbnails/
│   ├── models/
│   │   ├── Brand_type.txt
│   │   └── common/
│   ├── repaints/
│   ├── resources/
│   │   └── templates/
│   ├── scripts/
│   │   ├── doors/
│   │   │   ├── rightdoor1.txt
│   │   │   ├── rightdoor2.txt
│   │   │   └── rightdoor3.txt
│   │   ├── gearboxes/
│   │   │   ├── Voith_euro2.txt
│   │   │   └── ZF_euro2.txt
│   │   ├── lights/
│   │   │   └── lights.txt
│   │   └── wheels/
│   │       └── wheels.txt
│   ├── sounds/
│   │   ├── MIDR_06-20-45/
│   │   ├── common/
│   │   ├── compressor/
│   │   ├── doors/
│   │   └── sounds.txt
│   └── textures/
│       └── _dev_files/
│           └── requirements.txt
└── Vehicle_solo_configuration.ini
```

### Description of Folders and Files

| Folder/File | Description |
|-------------|-------------|
| `Vehicle_solo_configuration.ini` / `Vehicle_articulated_configuration.ini` | Configuration files defining mandatory parameters for vehicle views and physics. |
| `Vehicle_folder/` | Root folder for the vehicle. |
| `content_info/` | Contains additional metadata for the vehicle. |
| `content_info/thumbnails/` | Thumbnails used for previews (`preview`) in configuration files. |
| `models/` | 3D models of the vehicle and associated configuration files (e.g., tachometer animation, speed). |
| `repaints/` | Custom liveries for the vehicle. |
| `resources/` | User resources (templates, etc.). *Note: Ago'Projects does not use this folder for vehicle manuals.* |
| `scripts/` | Main logic of the vehicle (doors, gearboxes, lighting, wheels, etc.). |
| `sounds/` | Vehicle sounds and audio configuration files. |
| `textures/` | Vehicle textures. |
| `textures/_dev_files/` | Development files such as `.blend` files (Blender) used. |
| `textures/_dev_files/requirements.txt` | File informing the user about the minimum required version of Blender or other software. |

## Nomenclature

### General Rules
- **Allowed Characters**: Use only ASCII characters (A-Z, a-z, 0-9, `_`, `-`).
- **Encoding**: All files must be encoded in **UTF-8**.
- **Case**: File and folder names must be in **lowercase**, with `_` (underscores) replacing spaces.
- **Dots**: Replace `.` with `-` (e.g., `MIDR_06-20-45`).
- **Snake Case**: Use `snake_case` for file and variable names, except for brand names (e.g., `Hanover_EG3`).

### Naming Example
For textures of a part like the **Hanover EG3** unit, use a common prefix to group files:
- `Hanover_EG3.png`
- `Hanover_EG3_buttons.png`
- `Hanover_EG3_buttons_on.png`

## Best Practices
- **`common/` Folders**: Only contain files shared among all vehicle variants.
- **Subfolders in `repaints/`**: You can create subfolders to organize liveries by vehicle.
- **Consistency**: Follow the same naming convention for all files and variables.