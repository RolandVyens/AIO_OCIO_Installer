# AIO-OCIO Updater

A Blender addon to install and update OCIO color configurations from GitHub releases.

![Blender](https://img.shields.io/badge/Blender-4.1%2B-orange)
![License](https://img.shields.io/badge/License-GPL--3.0-blue)

## Features

- **Multiple OCIO Sources**: Choose between AIO-OCIO, PixelManager, or a custom repository
- **One-Click Install/Update**: Download the latest release directly from GitHub
- **Progress Bar**: Visual feedback during download
- **Version Tracking**: Displays installed version, date, and source
- **Auto Backup**: Existing colormanagement folder is backed up before replacement
- **Open Repository**: Quick button to open the source repository in your browser

## Supported Sources

| Source | Repository | Description |
|--------|------------|-------------|
| **AIO-OCIO** | [RolandVyens/AIO-OCIO](https://github.com/RolandVyens/AIO-OCIO) | Recommended for Blender (default) |
| **PixelManager** | [Joegenco/PixelManager](https://github.com/Joegenco/PixelManager) | Original OCIO config source |
| **Custom** | User-defined | Any GitHub repository with OCIO releases |

## Installation

### Install the Addon

1. Download this repository as a ZIP file
2. In Blender, go to **Edit > Preferences > Add-ons**
3. Click **Install...** and select the ZIP file
4. Enable the addon by checking the box next to "AIO-OCIO Updater"

### Install OCIO Config

1. Go to **Properties > Render > AIO-OCIO Updater** panel
2. (Optional) Change the OCIO source in addon preferences
3. Click **Install AIO-OCIO** (or Update if already installed)
4. Wait for the download to complete
5. **Restart Blender** to apply the new color configuration

## Usage

### Panel Location

The addon panel is located in:
```
Properties Editor > Render Properties > AIO-OCIO Updater
```

### Changing OCIO Source

1. Go to **Edit > Preferences > Add-ons**
2. Find "AIO-OCIO Updater" and expand it
3. Select your preferred source from the dropdown:
   - **AIO-OCIO** - Recommended for Blender
   - **PixelManager** - Original source
   - **Custom** - Enter your own GitHub repository URL

## Requirements

- Blender 4.1 or later
- Internet connection (to download from GitHub)

## Technical Details

- Installs to: `<Blender User>/datafiles/colormanagement/`
- Backup location: `<Blender User>/datafiles/colormanagement_backup/`
- Config renamed: `config_CG_Lin709.ocio` → `config.ocio`
- Version info stored in: `.aio_ocio_version.json`

## License

GPL-3.0-or-later
