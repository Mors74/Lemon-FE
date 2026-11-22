# Lemon-FE
A multiplatform emulation frontend

## Features

- **Player profiles.** Everyone has separate saves, favorites, collections and play time. Lemon loads saves before launch, collects them on exit and recovers interrupted transfers.
- **Save sync.** Continue on another device using a shared network folder (SMB). Sync manually or automatically, with optional SMB 3 encryption. After offline play, choose a save per game and keep the other as a backup. The NAS keeps a full save archive for every synced profile change.
- **Profile ZIPs.** Move names, pictures, favorites and game saves, optionally with appearance settings and custom names. Save states, collections, hidden games and play time stay on each device.
- **Light library.** Supported ROMs can live on a NAS. Games download on launch and temporary copies are removed on exit. Favorites stay downloaded for offline play. You can free local space after Lemon verifies the NAS copies.
- **Library.** Scan, search, rename and hide games. Sort by title, recency or play time, build collections and choose an emulator per system or per game.
- **Artwork and appearance.** Get covers, backgrounds, logos and icons from SteamGridDB with your own key, or import local covers and icons. Customize the theme, colors, wallpaper, size and animations.
- **Steam and Android.** Import installed Steam games on desktop. Android can launch PC games and installed apps, serve as the home screen and show game artwork on a second display. PC games manage their own saves.

## Supported emulators and saves

| Platform | Emulators and launchers |
| --- | --- |
| Linux, Windows and Android | Azahar, Cemu, Dolphin, DuckStation, Eden, Flycast, melonDS, PPSSPP, RetroArch, Vita3K |
| Additional desktop options | KytyPS5, Lichii, MAME, PCSX2, RPCS3, shadPS4, xemu, Xenia Canary, Xenia Edge, or a custom installed emulator |
| Additional Android options | ARMSX2, ARMSX3, Eden Duo, Eden Duo Dev, HakuX, Hokkaido, MAME4droid, melonDS Dev, MelonDualDS / WatermelonDS, WatermelonDS Emufii, MetroidArch, PPSSPP Gold, PPSSPP Duo, XenDroid |
| PC game launchers on Android | GameHub Lite, Winlator Cmod |

Hokkaido, Lichii’s Android port, plays Switch and Switch 2 games; Eden stays the first Switch choice on Android.

Saves sync between a PC emulator and the Android apps that keep the same files. Point the Android app at the shared folder below, then press **Check for save locations** in the setup wizard (**Suggest locations** in Settings → Saves) and enable the locations it finds.

| PC emulator | Android apps | Android setting |
| --- | --- | --- |
| RetroArch | RetroArch, MetroidArch | Save Files = `/storage/emulated/0/RetroArch/saves` |
| Lichii | Hokkaido (Switch and Switch 2) | Settings › Advanced settings › Custom Paths › Save Data Directory = `/storage/emulated/0/Hokkaido` |
| Eden | Eden, Eden Duo, Eden Duo Dev (one per device) | Save Data Directory = `/storage/emulated/0/Eden` (`EdenDuo`, `EdenDuoDev`) |
| Azahar | Azahar | User folder `/storage/emulated/0/Azahar` |
| Vita3K | Vita3K | Emulated System Storage Folder = `/storage/emulated/0/Vita3K` |
| melonDS | melonDS, melonDS Dev, MelonDualDS / WatermelonDS, WatermelonDS Emufii | Save folder `/storage/emulated/0/melonDS/saves` |
| PPSSPP | PPSSPP, PPSSPP Gold, PPSSPP Duo | PSP folder `/storage/emulated/0/PSP` |
| PCSX2 | ARMSX2 | App Data Folder `/storage/emulated/0/ARMSX2` |
| RPCS3 | ARMSX3 | Custom data folder `/storage/emulated/0/ARMSX3` |
| DuckStation | DuckStation | Memory Cards = `/storage/emulated/0/DuckStation/memcards` |
| Xenia Canary, Xenia Edge | XenDroid | `content_root = '/storage/emulated/0/XenDroid/content'` |
| Dolphin, Cemu | Dolphin, Cemu | Allow access to the app’s saves when asked |
| Flycast | RetroArch’s Flycast core | Its memory cards in RetroArch’s system folder |

On Android, standalone Flycast, HakuX and MAME4droid manage their own saves. Use RetroArch’s Flycast core for Dreamcast save sync.

## Get started

Install your emulator and supply your games and any required firmware. Create a profile or choose **Sync with NAS**, then follow the wizard: choose your games folder and an emulator per system, set up each emulator and its save locations, and set the Restricted password (or set it later in Settings → Classes). On desktop, `--root <folder>` selects a portable data folder. Android asks you to choose one.

## Restricted games: what the password does

Restricted is a household filter, not encryption. The game files stay readable, and anyone who can open the data folder can remove the password: close Lemon Frontend and delete `data/restricted.json`. Until a new password is set in Settings → Classes, games in Restricted stay hidden from every profile. With NAS sync, the removal reaches the other devices with the next sync. Lemon Frontend keeps only a salted PBKDF2-SHA256 hash of the password.

Builds before classes ignore them: they show every game and take profile access away when they sync a profile. Update every device that shares the NAS folder.
