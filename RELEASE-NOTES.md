# Penguin 1.9.6 — Lunar preview

Download **Penguin-Lunar-1.9.6-Windows.zip** below and extract the entire ZIP. It includes the controller, mod and Java runtime. GitHub's automatic **Source code** downloads are not the runnable Windows package.

Requires **Windows x64, Lunar Fabric 1.21.11 and Fabric API**. On first use, fully close Lunar, including its tray icon, then open `Penguin.exe` to enable attachment and back up the launcher settings. Launch the game, click **Refresh**, select it, then **Load Penguin**.

## Changes

- Replaced the Chest/Head selector with an **Aim height** slider from 10% to 95% of the player's current pose height.
- Default aim height is **Chest (72%)**, with a reset button and automatic saving. Enable **Aim vertically** for height correction.
- Preserves smoother aim, friend on/off switches, friend styling and target exclusions, and the sword exception to the naked-player filter.
- Includes the Lunar clicker startup fix, clicker readiness status, and filters for common lobby NPCs and blank-name tracers.

**Validation:** 135 automated tests passed. Clicker threads were verified running in Lunar, and aim smoothing was confirmed in use. Adjustable aim placement and click delivery still need normal play testing.

**Updating:** restart Minecraft once to clear older loaded code. Existing settings are preserved.

**Stopping:** use **Stop Penguin** to disable the mod while Minecraft stays open. Loaded Java classes remain until Minecraft exits. **K** opens the in-game menu; **F8** stops both clickers and aim tracking during gameplay.
