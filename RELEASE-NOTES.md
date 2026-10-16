# Penguin 1.9.8 — Lunar preview

Download **Penguin-Lunar-1.9.8-Windows.zip** below and extract the entire ZIP. It includes Penguin.exe, the mod and Java runtime. GitHub's automatic **Source code** downloads are not the runnable Windows package.

## Changes

- **Scalable menu:** Settings now has a saved 50–150% menu scale and reset button. Text, controls and mouse input scale together; smaller windows fit automatically. Friends, block picker, key capture and profiles follow the same scale.
- **No Blindness / No Nausea:** separate Visuals toggles suppress blindness fog/sky obstruction and nausea distortion/overlay. Effect timers and icons remain; Darkness and portals are unchanged. Turning the controls off or stopping Penguin restores normal rendering.
- **Clue Scrolls:** restored chest sorting, optional tier grouping, and Collect matching using a clue in hotbar slot 1. Collection ignores tier/progress and uses empty inventory slots. Click delay ranges from 250 to 10000 ms. Enable Clues > Clue Scrolls, then open a chest. Remove any old standalone ClueSort copy first.
- **Shareable profiles:** export/import named JSON settings files. Friend names are optional and excluded by default; friend appearance settings are included. Imports preview before confirmation, create a backup and leave automation off until you enable it.
- Includes all previous features, including J toggling friend nametags and tracers.

**Validation:** all 177 automated tests passed, including scale/input coordinates, reversible rendering hooks, clue plans and profile backup/rollback checks. Live Lunar testing of these new features is still pending.

**Updating:** restart Minecraft once to clear older loaded code, then use the new Penguin.exe. Existing settings are preserved.

Requires **Windows x64, Lunar Fabric 1.21.11 and Fabric API**. On first use, fully close Lunar, including its tray icon, then open Penguin.exe to prepare attachment. Launch the game, click Refresh, select it and Load Penguin.

**Controls:** K opens Penguin; J toggles all player nametags/tracers; F8 stops both clickers and aim tracking. Stop Penguin disables the mod while Minecraft stays open. Loaded Java classes remain until Minecraft exits.

`SHA256SUMS.txt` contains the Windows ZIP checksum.
