
# DeadGrid: Offline Survival Tablet Setup Guide

DeadGrid OS transforms an Android tablet into a fully-offline survival reference system. This guide walks you through every step from preparing your device, structuring your folders, installing apps, configuring custom icons, to enabling advanced functionality like offline AI chat and rooted file access for unrestricted archive use.

---

## Table of Contents

1. [Overview](#overview)
2. [System Requirements](#system-requirements)
3. [Step 1: Prepare Your Android Tablet](#step-1-prepare-your-android-tablet)
4. [Step 2: Download and Organize Resources](#step-2-download-and-organize-resources)
5. [Step 3: Install and Configure Apps](#step-3-install-and-configure-apps)
6. [Step 4: Folder Structure](#step-4-folder-structure)
7. [Step 5: Configure Nova Launcher](#step-5-configure-nova-launcher)
8. [Step 6: Add Custom Icons](#step-6-add-custom-icons)
9. [Step 7: Maps + GPX Files with OsmAnd](#step-7-maps--gpx-files-with-osmand)
10. [Step 8: (Optional) Root + Advanced Access](#step-8-optional-root--advanced-access)
11. [Step 9: (Optional) Offline Terminal LLM Chat](#step-9-optional-offline-terminal-llm-chat)
12. [Known Issues & Workarounds](#known-issues--workarounds)
13. [Credits and License](#credits-and-license)

---

## Overview

DeadGrid OS is an offline-first toolkit and archive designed for preppers, survivalists, and off-grid scenarios. It’s a curated environment of apps, icons, files, maps, and knowledge. Designed to be instantly usable without a network connection.

---

## System Requirements

* **Android Tablet**: Android 10+, 4GB+ RAM
* **Recommended**: 10.1" screen, expandable microSD (A1/A2 class)
* **MicroSD Storage**: 512 GB (ideal for full ZIM + map archives)

---

## Step 1: Prepare Your Android Tablet

1. **Factory Reset** (Optional): Start fresh if repurposing a device.
2. **Enable Unknown Sources**: Settings > Security > Allow unknown sources.
3. **Install a File Manager**: Use *Material Files* or *MiXplorer* (F-Droid).

---

## Step 2: Download and Organize Resources

### Recommended Sources:

* **Kiwix Library**: [https://library.kiwix.org](https://library.kiwix.org)
* **OsmAnd Map Tiles**: [http://download.osmand.net](http://download.osmand.net)
* **GPX Trails**: AllTrails, OpenStreetMap, Hiking Project
* **Offline APKs**: F-Droid, GitHub, trusted mirrors

Downloading ZIM, GPX, PDF, and map files to your PC first is recommended.

---

## Step 3: Install and Configure Apps

Install the following apps via APK:

* **Kiwix** (ZIM reader)
* **KOReader** (ebook/pdf reader)
* **Markor** (notes/markdown)
* **OsmAnd\~** (maps + GPX viewer)
* **Termux** (scripts/local terminal)
* **Morse Trainer**
* **ShroomID / Pl@ntNet** (limited offline)

> Note: Some apps (like OsmAnd and Kiwix) may need special folders or root access to fully enable custom file access.

---

## Step 4: Folder Structure

Create the following folders on the microSD card:

```
/DeadGrid
  ├── 01_Core_Survival
  ├── 02_Medicine
  ├── 03_Field_Biology
  ├── 04_Repair_Tools
  ├── 05_Navigation_Maps
  ├── 06_Comms_Signals
  ├── 07_Core_Library
  ├── 08_Tech_Dev
  ├── 09_Academic_STEM
  ├── 10_Philosophy_Mindset
  ├── 11_Cognitive_Training
  ├── 12_Cultural_Archive
```

Populate each with relevant ZIM, PDF, and GPX content.

---

## Step 5: Configure Nova Launcher

1. **Install Nova Launcher (Free)** from Play Store.
2. **Set as Default Launcher**.
3. **Configure**:

   * Dock: Disabled
   * Padding: Medium
   * Icon Size: 120–150%
4. **Create folders**:

   * Drag apps into each folder
   * Long-press → Edit → Tap icon → Custom PNG icon from storage

Use "Simple Icons Widget" or KWGT to fake widgets that link to PDF/ZIM categories.

---

## Step 6: Add Custom Icons

* Icons: PNG, 1:1 square, 512px+, transparent or black background

Included in this repository are custom Terminal theme icons

---

## Step 7: Maps + GPX Files with OsmAnd

### Maps

1. Download `.obf.zip` files from \[download.osmand.net].
2. Extract `.obf` files.
3. Move them to:

   ```
   /Android/data/net.osmand.plus/files/
   ```
4. Restart OsmAnd\~ and verify map display.

### GPX Trails

1. Download GPX files.
2. Move to:

   ```
   /OsmAnd/tracks/
   ```
3. View trails inside OsmAnd.

> Tip: Rooted devices can modify additional routing and style configs.

---

## Step 8: (Optional) Root + Advanced Access

**Why root?** To bypass sandbox restrictions in Android 11+.

* **Benefit**: Access all ZIMs directly from `/DeadGrid` folders.

### Steps:

1. Use **Magisk** + compatible custom recovery (e.g. TWRP)
2. Grant root permissions to:

   * Kiwix
   * OsmAnd
   * Termux (for file operations)
3. Use Termux to symlink `/sdcard/DeadGrid/07_Core_Library` into Kiwix’s internal folder.

---

## Step 9: (Optional) Offline Terminal LLM Chat

1. **Install Termux**
2. **Install Ollama for Android** (if available)
3. Load local LLM (e.g. `tinyllama`)
4. Create Termux scripts to run:

   ```bash
   ./ollama run tinyllama
   ```
5. Optional: Build UI with Termux\:Styling skin-like terminal

---

## Known Issues & Workarounds

| Problem                                  | Workaround                                                                          |
| ---------------------------------------- | ----------------------------------------------------------------------------------- |
| Kiwix can’t open ZIMs outside app folder | Root device OR move files manually into `Android/data/org.kiwix.kiwixmobile/files/` |
| No shortcuts to ZIM/PDF inside folder    | Use Nova Launcher + folder structure or widgets                                     |
| ShroomID or Pl@natNet needs login/internet    | Download region-based plant guides                                  |
| OsmAnd folder restrictions               | Root, or use app’s internal file manager to import                                  |

---

## Credits and License

**Created by:** Grant-Ad-Nauseum (2025)
**License:** Open use. Attribution appreciated. Survive well.

Feel free to fork, clone, remix, and share.
