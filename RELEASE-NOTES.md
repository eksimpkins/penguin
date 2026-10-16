# Penguin 1.9.10 — Lunar preview

Download **Penguin-Lunar-1.9.10-Windows.zip** below and extract the entire ZIP. It includes Penguin.exe, the mod and Java runtime. GitHub's automatic **Source code** downloads are not the runnable Windows package.

## Changes

- **Consistent friend additions:** typed names and Nearby selections use the same account-name matching. Adding an existing OFF friend turns it ON again without duplicating it. Nearby entries use the same listed-player and NPC checks as Penguin's overlay.
- **Friend colors:** the overlay resolves current friend settings when drawing labels and tracers. Formatting codes embedded in account names no longer override the chosen label color.
- Includes No Debuff, Constant FOV, menu scaling, clue-scroll tools, profiles and all previous features.

**Validation:** all 193 automated tests passed, including friend additions, re-enabling and actual Minecraft text formatting. The exact cause of the reported intermittent color delay remains unconfirmed; this update addresses the concrete matching, add-flow and formatting issues found during investigation. Live Lunar confirmation is still needed.

**Multiple windows:** games using the same game folder share the saved settings file but keep separate loaded settings. Changes do not currently sync live, and the last window to save can overwrite that file. This update does not add synchronization.

**Updating:** restart Minecraft once to clear older loaded code, then use the new Penguin.exe. Existing settings and profiles are preserved.

Requires **Windows x64, Lunar Fabric 1.21.11 and Fabric API**. On first use, fully close Lunar, including its tray icon, then open Penguin.exe to prepare attachment. Launch the game, click Refresh, select it and Load Penguin.

**Controls:** K opens Penguin; J toggles all player nametags/tracers; F8 stops both clickers and aim tracking. Stop Penguin disables the mod while Minecraft stays open. Loaded Java classes remain until Minecraft exits.

`SHA256SUMS.txt` contains the Windows ZIP checksum.
