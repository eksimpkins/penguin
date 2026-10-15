# Penguin 1.9.7 — Lunar preview

Download **Penguin-Lunar-1.9.7-Windows.zip** below and extract the entire ZIP. It includes the controller, mod and Java runtime. GitHub's automatic **Source code** downloads are not the runnable Windows package.

Requires **Windows x64, Lunar Fabric 1.21.11 and Fabric API**. On first use, fully close Lunar, including its tray icon, then open `Penguin.exe` to enable attachment and back up the launcher settings. Launch the game, click **Refresh**, select it, then **Load Penguin**.

## Changes

- **J now toggles all player nametags and tracers, including friends.** The Nametags switch in the menu follows the same behavior.
- Friend colors, sizes, label/line visibility and other appearance choices are preserved when toggling off and on. Friend Overlay remains an additional friend-only switch.
- Updated the menu descriptions and controls guide to explain the shared toggle.
- Includes all features from 1.9.6, including the aim-height slider with Chest (72%) as the default.

**Validation:** build succeeded and all 135 existing automated tests passed. The new J behavior has been reviewed in code; live gameplay confirmation is still pending.

**Updating:** restart Minecraft once to clear older loaded code, then use the new Penguin.exe. Existing settings are preserved.

**Stopping:** use **Stop Penguin** to disable the mod while Minecraft stays open. Loaded Java classes remain until Minecraft exits. **K** opens the in-game menu; **F8** stops both clickers and aim tracking during gameplay.

`SHA256SUMS.txt` contains the Windows ZIP checksum.
