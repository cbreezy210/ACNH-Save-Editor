# 🗺️ ACNH Save Editor — Roadmap
**The ACNH companion tool that never leaves your Switch.** 🍃

A native Nintendo Switch homebrew save editor for Animal Crossing: New Horizons — no PC required.

This file tracks what's shipped and what's coming next. Suggestions welcome — open an issue or find me on GBATemp/Reddit!

## ✅ Shipped — v1.0
- [x] Wallet & Bank Bells editing (encrypted ints, healed Murmur3 hashes)
- [x] Pocket item injector with live English item-name lookup
- [x] Automatic SD backup before every NAND write
- [x] GitHub Releases with ready-to-install .nro + items.txt
- [x] Submitted to the Homebrew App Store & sphaira++

## ✅ Shipped — v1.1
- [x] Full graphical UI (SDL2 renderer replaces the text console)
- [x] PNG icon rendering from the SD card (stb_image)
- [x] Crisp text via SDL2_ttf with bundled rounded font
- [x] Graphical menu with highlight navigation (Bells / Slot / Item / Count)

## ✅ Shipped — v1.2
- [x] Dual-file save engine (personal.dat + main.dat with dual hash healing)
- [x] House Loan editing (zero out Tom Nook's debt)
- [x] Nook Miles editing (max the miles balance)
- [x] Favorites Menu with visual Slot Picker (NMTs, Star Fragments, gold tools & nuggets)
- [x] Pocket Loadouts (save/load 5 named setups to the SD card)
- [x] Backup Restore (press ZL to rollback to the last SD backup)
- [x] Clear Slot (press Minus to empty a pocket)

## ✅ Shipped — v1.3.0
- [x] Native Item Search — Press (+) to open the Switch keyboard and search the 13,000+ item database by name
- [x] Optimized Item Database — Parsed into std::vector at boot for instant, lag-free name lookups
- [x] Expanded UI Panel — Increased to 900x480 for better text containment and a premium look
- [x] Centered Footer Text — Reorganized control guide into two clean, perfectly centered lines
- [x] Search Results Truncation — Long item names safely truncated to prevent horizontal overflow
- [x] Search Screen Pagination — Displays 6 items at a time with increased line height (38px)
- [x] Graceful App Exit — Added a dedicated "Quit App" option to the main menu

## ✅ Shipped — v1.4.0 (The Favorites Overhaul & UI Polish)
- [x] Search Footer Overlap Fix — Reduced search results per page to prevent text clipping
- [x] Search Pagination Fix — Corrected page jump calculation to prevent skipping items
- [x] Paginated Favorites Menu — Displays 8 items per page with smooth auto-scrolling (matches Search Screen UX)
- [x] Alphabetical Sorting — Favorites auto-sort A–Z at boot for instant scanning
- [x] Dynamic Name Resolution — No hardcoded hex IDs; favorites resolve via exact string matching from items.txt (future-proof)
- [x] Expanded 22-Item Roster — Bell bag, Bell voucher, 99,000 Bells, gold roses, cherry-blossom petal, pearl, gold bars, all 6 golden tools, and both crowns
- [x] Embedded Homebrew Icon (community request) — Embedded the leaf PNG into the .nro so the Homebrew Menu displays the proper icon instead of the default loading icon
- [x] In-App Title Bump — Title bar updated to "ACNH Save Editor v1.4"

## 🟡 Coming Next — v1.5.x (Decorations, Safety & Deep Edit Update)
Target Release: Q4 2026

### 🎨 Room Decorations (Community Priority)
- [ ] Room Decorations Injector — v1.5.0 HEADLINE — Inject furniture, wallpapers, and flooring directly into player rooms. Requested by solamentenieves on GBATemp. Fills a major gap in on-console tools.
- [ ] Furniture Placement Editor — Move, rotate, and scale placed items within a room grid.
- [ ] Wallpaper/Flooring Swapper — Instantly change room aesthetics without buying/cataloguing items first.

### 🛡️ Safety & Reliability
- [ ] Backup Verification — Checksum/size validation after SD backup creation (abort write if 0-byte or mismatch to prevent corruption).
- [ ] Game Version Validator — warn if save offsets don't match your game version (major.minor check).
- [ ] "Dry Run" Preview Mode — see exactly what will change before writing to NAND.
- [ ] Rolling Backup Manager — keep the last 3 backups with timestamps and version tracking.
- [ ] "Safe Mode" Toggle — restrict edits to offline-safe values to prevent console bans.
- [ ] Sanity Checks — automatically prevent impossible values (e.g., negative Bells, invalid Item IDs).

### 📦 Inventory & Storage
- [ ] House Storage Editing — parse and edit the ~2,400+ slot storage array with pagination/search.

### 🏝️ Island & Environment
- [ ] Villager Management — force specific villagers to move in, kick out unwanted villagers, edit catchphrases.
- [ ] Player Customization — edit Player Name, Appearance, Passport info, and Catchphrase.
- [ ] Island Infrastructure — max out all bridges/inclines, change Native Fruit, force K.K. Slider songs.

### 🧪 Quality of Life & QA
- [ ] Crash Logging — write a crash.log to the SD card on unrecoverable SDL2 errors for easy debugging.
- [ ] Beta Testing Channel — establish a Discord/GitHub Pre-release channel for power users to test features early.
- [ ] items.txt Build Docs — Document where the item database comes from for open-source contributors.

## 🟠 v1.6.0 — Residents, Market & Map Update
Target Release: Early 2027

### 👥 Multi-Resident Support
- [ ] Multi-Villager / Player Selector — edit Player 1–8 house blocks (Villager0–7, Base + player_index * 0x28A28); doubles as the community-requested Player/Account Selection.

### 💰 Money & Progression
- [ ] Stalk Market Assistant (Turnip Pattern Prediction) — Read-only & non-destructive: reads your buy price + revealed AM/PM prices and runs the documented pattern algorithm (Fluctuating / Large Spike / Decreasing / Small Spike) to predict the week's prices. Your save stays 100% forensically clean.
- [ ] Turnip Price Overwrite (opt-in advanced) — set your own weekly stalk market prices, force Big/Small Spike patterns. Ships only AFTER the prediction feature.
- [ ] Nook Miles & Achievements Unlocker — unlock all Nook Miles+ achievements and passport stamps.

### 🌟 God-Mode Unlocks
- [ ] DIY Recipe Unlocker — learn every recipe, golden tools included (bitfield manipulation).

### 🧹 Map Chores Utility (NEW)
- [ ] Weed / rock / spoiled-turnip cleanup + bulk item spawn on the map grid — the most-requested utility category in the ACNH tool scene.

## 🏝️ v1.7.0 — Island Blueprint & Read-Only Insights
Target Release: Mid 2027

- [ ] Island Blueprint JSON Export (read-only, zero risk) — export your full island layout (terrain, paths, placed furniture, building positions) to a standardized JSON file.
- [ ] Open Blueprint JSON Schema — published as a community standard so layouts can be shared and adopted by other tools.
- [ ] No import in this phase — keeps your save 100% safe while the format matures.
- [ ] Design Pattern Preview (read-only first; full editor to follow) — view, then later import/replace/delete custom designs (inspired by ACNHDesignPatternEditor).
- [ ] Custom Design Slot Management — clear all designs or inject popular design IDs.
- [ ] Collection Progress Tracker (read-only) — fish/bug/fossil/art completion percentages at a glance.

## 🔴 Long-Term — v2.0.0 (Architecture & Community Overhaul)
Target Release: Late 2027

### 🏝️ Island Blueprint Import (Phase B)
- [ ] Blueprint Import — apply community JSON blueprints to reshape your island, gated behind the Dry-Run Diff viewer with conflict validation.

### 🏆 Completion Cheats
- [ ] Museum Completion Flag — mark all fish, bugs, fossils, and art as donated.
- [ ] Villager Friendship Control — max friendship to 10 stars for framed photos.

### 🎨 UI & Graphics
- [ ] Advanced UI Navigation — tree-view or tabbed interface for cleaner feature access.
- [ ] Save File "Diff" Viewer — compare backup and current save side-by-side before writing.

### 🌍 Community & Localization
- [ ] Multi-Language UI — localized items.txt and UI strings (EN, ES, FR, DE, JA, KO) with boot-time selector (Spanish prioritized per community request).
- [ ] Contributing.md — official guide for community devs to submit Pull Requests and translations.

### 🛠️ Quality of Life
- [ ] Modular Plugin System — community devs can write JSON/Lua scripts for new offsets without recompiling.
- [ ] Wi-Fi Cloud Backup — upload backups off-console for true cloud saves.

---
Built with devkitPro/libnx. Educational project — always keep backups!
Responsible use: we ship features that edit only base-game items and values — please never trade unreleased/internal items in online play.
