# 🍃 ACNH Save Editor (Native Switch)
**The ACNH companion tool that never leaves your Switch.**

A 100% native Nintendo Switch homebrew application for editing Animal Crossing: New Horizons save files directly on your console. No PC, no pulling the SD card, no complicated dumping tools required.

[![Version](https://img.shields.io/github/v/release/cbreezy210/ACNH-Save-Editor)](https://github.com/cbreezy210/ACNH-Save-Editor/releases) [![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

> **Note:** This is an educational project. Always keep backups of your save files. Modifying save data always carries a risk. The author is not responsible for corrupted islands or banned consoles. Use offline and at your own risk. Not affiliated with Nintendo.
>
> **Responsible Use:** This app edits only items and values that exist in the base game. Please do not trade or use unreleased/internal items in online play, as they can ruin the experience for other players and are not easily removable on non-CFW consoles.

## 🎯 What This App Is
| ACNH Save Editor IS: | ACNH Save Editor IS NOT: |
|---|---|
| A safe, offline save editor with automatic backups and hash healing | A RAM editor, live spawner, or online mod |
| 100% on-console (no PC, phone, or sysmodules required) | A companion app or web tool |
| Clamped to in-game maximums (no impossible values) | A way to spawn unreleased/internal items |

## ️ CRITICAL LAUNCH INSTRUCTIONS
For full memory and SD card access, you **MUST** launch this app via **Title Override** (hold [R] while launching a game like Animal Crossing) OR install it as a forwarder.

**Do NOT launch it from the Album / Applet mode** — the app will refuse to run and show you exactly how to relaunch correctly, preventing save-access crashes!

## ✨ Features (v1.4.1)
* **Dual-File Engine:** Edits both `personal.dat` (Wallet, Bank, Pockets, Nook Miles) and `main.dat` (House Loan) simultaneously.
* **Forensically Clean Save Engine & Auto-Repair:** Safely updates EncryptedInt32 checksums without overwriting untouched memory. Includes a permanent heal loop that automatically repairs saves corrupted by older versions the next time you save.
* **Native Item Search:** Press Plus (+) to open the native Switch keyboard and instantly search the 13,000+ item database by name, with smooth paginated results. No more guessing hex codes!
* **Graphical UI:** Built with SDL2, featuring a clean, highlight-bar navigation system with an expanded, perfectly centered layout (900x480 panel) to prevent text overflow.
* **Favorites Menu:** Press X to browse an alphabetically sorted, paginated list of 22 curated high-value items (NMTs, Bell bags, 99,000 Bells, gold roses, cherry-blossom petals, pearls, gold bars, all 6 golden tools, and both crowns). Favorites resolve by name at boot, so they always stay in sync with your `items.txt`.
* **Visual Slot Picker:** Choose exactly which pocket slot to inject items into without guessing.
* **Pocket Loadouts:** Press Y to save and load up to 5 custom pocket setups (Mining, Fishing, Terraforming) to your SD card.
* **Bulletproof Safety Net:** Automatic SD card backups before every single write, byte-verified after creation. Press ZL on the main menu to instantly rollback to your last backup.
* **Applet Mode Guard:** The app hard-blocks Album/Applet launches and shows on-screen instructions for relaunching correctly.
* **Embedded Homebrew Icon:** The `.nro` now includes the custom icon.

## 🛡️ Backup System & Safety
When loading a save on Switch, a full backup copy is created **before** any modification:

```text
sdmc:/switch/acnh_editor/backup_personal.dat
sdmc:/switch/acnh_editor/backup_main.dat
```

**One-Button Rollback:** Press [ZL] on the main menu to instantly restore the last backup to NAND.

**Safety Guarantees:**
* Every save operation creates a backup *before* writing to NAND
* All edits are clamped to in-game maximums (no impossible values)
* EncryptedInt32 checksums are recalculated on every save, and untouched memory is left pristine
* The app refuses to run in Applet Mode to prevent save-access crashes

**Honest Note:** The backup is a single rolling slot (your last known-good state). For long-term archiving, occasionally copy these two files to your PC. Your island, your redundancy.

## ✅ Compatibility
| Game | Tested Version | Save Format | Edited Files |
|---|---|---|---|
| Animal Crossing: New Horizons | 3.0.3 | Dual-file (`personal.dat` + `main.dat`) | Wallet, Bank, Miles, Loan, Pockets |

Tested by the author on FW 22.5.0 (Atmosphère 1.11.2 E). When Nintendo ships an ACNH update, compatibility is re-verified and noted in the changelog.

## 🎨 Coming in v1.5: Room Decorations Injector
Based on your feedback! Inject furniture, wallpapers, and flooring directly into your rooms. Still deciding between Turnip Price Trends or DIY Recipe Unlocks for v1.6 — which would you rather see? Let us know on GitHub Discussions!

## 📥 Installation
Ensure your Switch is running Custom Firmware (Atmosphere).

### Standard Installation (SD Card)

1. Download the latest `acnh_editor_v1.4.0.zip` from the [Releases](https://github.com/cbreezy210/ACNH-Save-Editor/releases) page.
2. Extract the `switch` folder to the **root** of your SD card.
3. Verify your folder structure matches this exactly:

```text
SD:/
  switch/
    ┗ acnh_editor/
       ├ acnh_editor.nro
       ├ font.ttf
       ├ icon.png
       └ items.txt
```
4. Fully close Animal Crossing: New Horizons (do not leave it suspended).
5. Hold [R] and launch ACNH from the Home Menu to open the Homebrew Menu.
6. Select "ACNH Save Editor" to launch (do not run ACNH at the same time!).

### Alternative Installation (DBI via MTP)

For users with DBI installed on their Switch, you can install via USB MTP:

1. Download `ACNH-Save-Editor-DBI-v1.4.0.zip` from the [Releases](https://github.com/cbreezy210/ACNH-Save-Editor/releases) page.
2. Connect your Switch to PC via USB.
3. Launch DBI on your Switch and select **MTP responder**.
4. On your PC, open the DBI MTP drive and navigate to **NAND Titles** or **SD Card**.
5. Drag and drop the `acnh_editor.nro` file from the zip into the drive.
6. Launch via Title Override (hold [R] on ACNH from Home Menu).

## 🎮 Controls
| Button | Action |
|---|---|
| Up / Down | Navigate menus / Select items || Left / Right | Step values (+/- 1) or navigate columns |
| L / R | Big step values (+/- 10 or 100,000) |
| A | Backup to SD & Save changes to NAND (or select "Quit App") |
| X | Open Favorites Menu |
| Y | Open Loadout Manager |
| Minus (-) | Clear the currently selected pocket slot |
| ZL | Restore from last SD backup (Emergency Rollback) |
| Plus (+) | Open Native Item Search |

## 🗺️ Roadmap & Known Gaps
See [ROADMAP.md](ROADMAP.md) for the full list of shipped and planned features.

**Known Gaps (v1.4.0):**
* Single resident only (edits `/Villager0/`); multi-resident selector planned for v1.6
* No map editing yet (weed/rock cleanup planned for v1.6)
* No turnip price preview yet (under consideration for v1.6)
* No design pattern preview yet (planned for v1.7)

## 🛠️ Building from Source
Requires devkitPro with switch-dev installed.

```text
pacman -S switch-sdl2 switch-sdl2_ttf switch-sdl2_image
git clone https://github.com/cbreezy210/ACNH-Save-Editor.git
cd ACNH-Save-Editor
make
```

After building, copy `acnh_editor.nro` and `icon.png` from the repo root, along with `items.txt` and `font.ttf` from the `assets/` folder, to your SD card at `sdmc:/switch/acnh_editor/` before running.

## 🙏 Credits
* **kwsch and the NHSE project** — ACNH save-structure research and reference: https://github.com/kwsch/NHSE
* **devkitPro and libnx communities** — Switch homebrew tooling: https://devkitpro.org
* **SDL2, SDL_ttf and stb_image authors**
* **micaturtle** — community testing and documentation contributions
* **The ACNH homebrew community** — for feedback, testing, and feature requests

## ⚠️ Disclaimer
This is an educational project. Always keep backups of your save files. Modifying save data always carries a risk. I am not responsible for corrupted islands or banned consoles. Use at your own risk!

## 💬 Community & External Links
* **GitHub Releases (Download):** https://github.com/cbreezy210/ACNH-Save-Editor/releases
* **GameBrew Wiki:** https://www.gamebrew.org/wiki/ACNH_Save_Editor_Switch
* **GameBanana:** https://gamebanana.com/tools/23811
* **GBATemp:** https://gbatemp.net/threads/release-acnh-save-editor-a-new-save-editor-for-animal-crossing-new-horizons.683771/
* **Reddit — v1.4.0 release thread:** https://www.reddit.com/r/SwitchHacks/comments/1vzs3p7/updaterelease_acnh_save_editor_v140_native_switch/
