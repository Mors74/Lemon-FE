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

## Supported emulators

| Platform | Emulators and launchers |
| --- | --- |
| Linux, Windows and Android | Azahar, Cemu, Dolphin, DuckStation, Eden, Flycast, melonDS, PPSSPP, RetroArch, Vita3K |
| Additional desktop options | KytyPS5, Lichii, MAME, PCSX2, RPCS3, shadPS4, xemu, Xenia Canary, Xenia Edge, or a custom installed emulator |
| Additional Android options | ARMSX2, ARMSX3, Banana Native, Eden Duo, Eden Duo Dev, HakuX, MAME4droid, melonDS Dev, MelonDualDS / WatermelonDS, WatermelonDS Emufii, MetroidArch, PPSSPP Gold, PPSSPP Duo, XenDroid |
| PC game launchers on Android | GameHub Lite, Winlator Cmod |

On Android, standalone Flycast, HakuX and MAME4droid manage their own saves. Use RetroArch’s Flycast core for Dreamcast save sync. 
