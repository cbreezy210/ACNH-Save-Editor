# ACNH Save Editor 🍃
**The first 100% native Switch save editor for Animal Crossing: New Horizons.**

![Status](https://img.shields.io/badge/Status-Stable-green?style=flat-square)
![Platform](https://img.shields.io/badge/Platform-Nintendo%20Switch-E60012?style=flat-square&logo=nintendo-switch&logoColor=white)
![Language](https://img.shields.io/badge/Language-C++-00599C?style=flat-square&logo=c%2B%2B&logoColor=white)
![License](https://img.shields.io/github/license/cbreezy210/ACNH-Save-Editor?style=flat-square&color=blue)
[![Latest Release](https://img.shields.io/github/v/release/cbreezy210/ACNH-Save-Editor?include_prereleases&style=flat-square&color=blueviolet)](https://github.com/cbreezy210/ACNH-Save-Editor/releases) [![Total Downloads](https://img.shields.io/github/downloads/cbreezy210/ACNH-Save-Editor/total?style=flat-square&color=orange)](https://github.com/cbreezy210/ACNH-Save-Editor/releases)

> **🍃 Milestone:** 1,000+ downloads across GitHub & GameBanana.

> **🛡️ Safety Record:** 1,000+ installs, **zero lost saves**. Byte-verified backups + automatic hash healing.

> **Note:** This is an educational project. Always keep backups of your save files. Modifying save data always carries a risk. The author is not responsible for corrupted islands or banned consoles. Use offline and at your own risk. Not affiliated with Nintendo.
>
> **Responsible Use:** This app edits only items and values that exist in the base game. Please do not trade or use unreleased/internal items in online play, as they can ruin the experience for other players and are not easily removable on non-CFW consoles.

## 🎯 What This App Is
| ACNH Save Editor IS: | ACNH Save Editor IS NOT: |
|---|---|
| A safe, offline save editor with automatic backups and hash healing | A RAM editor, live spawner, or online mod |
| 100% on-console (no PC, phone, or sysmodules required) | A companion app or web tool |
| Clamped to in-game maximums (no impossible values) | A way to spawn unreleased/internal items |

## 🆕 What's New in v1.4.0
*   **Paginated Favorites Menu:** Browse 22 curated high-value items with smooth auto-scrolling and A-Z sorting.
*   **Applet Mode Guard:** Hard-blocks Album launches to prevent permission-based crashes, with on-screen instructions to relaunch correctly.
*   **Embedded Homebrew Icon:** The `.nro` now includes the custom leaf icon for the Homebrew Menu.
*   **Search & UI Polish:** Fixed search footer overlaps, corrected pagination jumps, and added DBI/MTP drag-and-drop installation support.

## ⚠️ CRITICAL LAUNCH INSTRUCTIONS
For full memory and SD card access, you **MUST** launch this app via **Title Override** (hold [R] while launching a game like Animal Crossing) OR install it as a forwarder.

**Do NOT launch it from the Album / Applet mode** — the app will refuse to run and show you exactly how to relaunch correctly, preventing save-access crashes!

## ✨ Features (v1.4.0)
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
Based on your feedback! Inject furniture, wallpapers, and flooring directly into your rooms. 

**🗳️ Help Decide v1.6.0!** We're choosing between **Turnip Price Trends** and **DIY Recipe Unlocks** for the next major update. Cast your vote here: 
👉 **[Vote in the Community Poll](https://github.com/cbreezy210/ACNH-Save-Editor/discussions/3)**

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

## 🩺 Troubleshooting: "My edits didn't stick / counts reverted"

If your changes vanish after jumping back into the game, work this checklist top to bottom — it resolves the vast majority of cases.

### 0. First: breathe, your save is probably fine
Both editors write a byte-verified backup before every change. If anything looks wrong, restore the backup (ACNH: **ZL** on the ready screen; PKHeX-NX: follow the on-screen restore prompt) and start over. Nothing below is worth risking a save over.

### 1. Fully close the game before editing — the #1 cause
A **suspended** game keeps its save state in memory. Edit while it's suspended (or resume a suspended session after editing) and the game writes its in-memory state back over your changes on the next autosave. It looks exactly like "my edits didn't stick."
**Fix:** Home menu → highlight the game → **X → Close** → *then* edit → *then* relaunch. Never edit into a suspended session.

### 2. Make sure you actually committed
Edits live in the editor's memory until you run the step that writes them to the save file.
- **ACNH Save Editor:** use the on-screen **Save/Quit** step (A). Exiting any other way discards your changes.
- **PKHeX-NX:** complete the commit step and exit via **graceful quit** (v0.9.5+). Killing the applet mid-edit writes nothing.

Not sure you committed? Reopen the editor: if the edited values aren't there, they were never written.

### 3. On the DBI path? Make sure you re-imported
The DBI workflow is export → edit the SD dump → **import back**. Editing the dump and launching the game without re-importing leaves the console save untouched. (Standard / Title-Override builds write in place and have no such step.)

### 4. Check you edited the right target
- **ACNH:** v1.4.0 edits the **primary resident's** wallet only — if you're playing as a different resident, wallet changes won't appear in your game (the resident selector arrives in v1.6). Bank and loan are island-wide, so those always apply.
- **PKHeX-NX:** confirm the right box/slot — and remember multiple Switch profiles mean multiple save files.

### 5. Check your version
- **PKHeX-NX:** the header prints the version (v0.9.5+). No version line = pre-0.9.5 build → update.
- **ACNH:** version shows on the title screen.

Older builds predate commit and safety fixes. Always reproduce on the latest release.

### Still stuck?
Open a GitHub Issue (or ask in the GBATemp thread) with these five answers and most problems diagnose themselves in one reply:
1. Which tool + version (header / title screen)
2. Standard or DBI install
3. Exactly what didn't stick (wallet, bank, IVs, items…)
4. Game error, or silent revert?
5. Was the game fully closed while editing?

---

## ❓ Launch, Display & Other FAQ

**Q: The app won't launch, or it shows a black screen/error message.**

**A:** You are likely launching from the Album (Applet Mode). Applet Mode restricts SD card and memory access. You **must** launch via Title Override: fully close ACNH, then hold [R] while launching the game from the Home Menu to enter the Homebrew Launcher.

**Q: The app opens but shows a blank green screen with no text.**

**A:** This usually means the `font.ttf` file is missing or in the wrong place. The graphical UI requires this specific font file to render text. Ensure `font.ttf` is located directly inside the `acnh_editor/` folder alongside the `.nro`. If you renamed the folder to `acnh-editor` (hyphen) or just `ACNH`, the app may also fail to find its assets. Rename the folder to exactly `acnh_editor` (underscore).

**Q: Why can't I edit my second player's (Player 2) items or pockets?**

**A:** v1.4.0 currently only edits the primary resident (`/Villager0/`). Multi-resident support (Player 1–8 selector) is actively being developed and planned for v1.6.0. *(See also step 4 of the checklist above — this is the most common "my edits didn't stick" cause.)*

**Q: My game crashed when I tried to save.**

**A:** Ensure Animal Crossing is fully closed (not just suspended in the background) before launching the editor. Also, never run the editor and the game at the exact same time. *(Suspended sessions cause both crashes and silent reverts — this is step 1 of the checklist above.)*

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
