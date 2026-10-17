# Penguin for Lunar

Penguin is a Windows x64 controller and mod for **Lunar Client with Minecraft 1.21.11, Fabric and Fabric API**. Load or stop Penguin from its controller while Minecraft stays open.

## Download

**[Download Penguin 1.9.15 for Windows](https://github.com/eksimpkins/penguin/releases/download/v1.9.15/Penguin-Lunar-1.9.15-Windows.zip)**

Download `Penguin-Lunar-1.9.15-Windows.zip` from the [latest release](https://github.com/eksimpkins/penguin/releases/latest). GitHub's automatic **Source code** ZIP does not contain the ready-to-run application. Java is included in the Windows download.

## First launch

1. Extract the entire ZIP. Keep `Penguin.exe`, `app` and `runtime` together inside the extracted `Penguin` folder.
2. Fully close Lunar Client, including its tray icon.
3. Open `Penguin.exe`. It enables Lunar's built-in **Enable Attach** setting and saves a backup of the original launcher settings. If Lunar was still open, close it and choose **Prepare Lunar**.
4. Launch Lunar **Fabric 1.21.11** with **Fabric API** available in the profile.
5. Click **Refresh**, select your game, then **Load Penguin**. Keep Minecraft visible while textures reload.

Do not install a second copy of Penguin in the mods folder. When updating from an older Penguin build, restart Minecraft once before loading the new version.

If a previous load reported **FAILED**, restart Minecraft once to clear the old loaded code, then load 1.9.15. Reopening only the controller does not clear that state. Your settings are preserved; no reset is needed.

## Controls

- **K:** open Penguin's menu while in a world. At Minecraft's main menu, use **Open menu** in the controller.
- **J:** toggle all player nametags and tracers, including friends. Friend appearance and label/line choices are preserved.
- **F8:** stop both clickers and aim tracking during gameplay.
- **] / F7:** default left/right clicker toggles; change these in Settings.
- **Stop Penguin:** stop the mod while Minecraft remains open. You can load it again in the same session.

For repeated clicks, enable a clicker, close the menu, then release and hold that mouse button. A fresh press is also required after changing its CPS or returning from a menu or another window. Close any older standalone Penguin Clicker before using this version.

Closing the controller window does not stop the mod. **Stop Penguin** disables its effects and input handling; already loaded Java classes remain until Minecraft exits.

## New in 1.9.15

**Visuals > Ground Zero** gives **yellow wool yellow outlines/tracers**, **black concrete blue outlines/tracers**, and **Block of Raw Gold red outlines/tracers**. The module starts OFF, with all three block types, outlines and tracer lines enabled inside it. Turn it on to draw a line to the **closest block of each type** (up to three lines), or choose **All**.

Ground Zero has separate type toggles and colors, plus line-width and radius controls. It matches exactly `minecraft:yellow_wool`, `minecraft:black_concrete` and `minecraft:raw_gold_block`. While enabled, it owns these three types so generic Block Outlines and Block Tracers do not paint over the selected colors; other types are unaffected. Restart Minecraft and load the new version to use this module.

**Visuals > Block Tracers > Block Outlines preset** makes the outlined block categories your tracer targets. It uses the current **Glass blocks**, **Glass panes** and **Wool** switches under Block Outlines: clear/tinted/all 16 colored glass blocks, clear/all 16 colored panes, and all 16 wool colors, as enabled.

The preset replaces the selected tracer block types, enables Block Tracers and tracer lines, and chooses **Closest**. It is also available in **Choose blocks**. Apply it again after changing the Block Outlines categories; the selection is a snapshot. Existing colored outlines and their settings are unchanged.

## Block tools

- **Trace closest block:** under **Visuals > Block Tracers**, this button enables the finder and tracer lines and selects the closest target. **Tracer target: Closest / All** clearly selects one line or lines to all matches. Fresh settings start with Closest; saved All selections are retained.
- Closest mode reselects the nearest valid highlighted match each frame, measured from you to the block's center. A mined or removed match no longer holds the line. Behind and offscreen lines still work.
- **Identify aimed block:** aim at a block from within **8 blocks**, then open **K > Visuals > Block Tracers > Identify aimed block**. See its exact client block registry ID and coordinates, choose **Copy block ID**, or **Add to highlighted blocks** while retaining the existing selected blocks. Adding a block does not turn on the module.

Block inspection ignores entity displays and colored entity overlays; a real block in front can still be selected. It reports what Minecraft knows and cannot reveal a different server-only block type. Tracers scan loaded chunks using a bounded cache, so Closest means the nearest currently highlighted discovered match, not a search of the whole world.

## Retained fixes and controls

- **Hold-C zoom compatibility:** Constant FOV lets the normal game FOV through while physically holding C in focused gameplay with no screen open; releasing C restores the selected FOV. This supports existing hold-C zoom, not remapped or toggle zoom. Movement and effect FOV changes can also apply during the hold.
- **Lunar loading fix:** Penguin selects Minecraft's exact FOV method despite Lunar's extra accessor. Original error details are preserved after a failed load.
- **Show '(behind)' text:** a shared Nametags/Friend Overlay switch, OFF by default. Edge labels and tracers keep working.
- Friend additions consistently match account names, re-enable saved OFF friends, and apply the chosen label/tracer styling when drawing.

## Also included

- **Settings > Menu scale:** 50–150%, with a reset button and automatic fitting for small windows.
- **Visuals > No Debuff:** one toggle for blindness fog/sky obstruction and nausea distortion/overlay. Actual status effects remain.
- **Visuals > Constant FOV:** keeps the world view at the FOV selected in Minecraft, preventing movement/effect zoom except while holding C during focused gameplay. Hand/item projection is unchanged. Both controls restore normal rendering when switched off.
- **Clues > Clue Scrolls:** chest sorting, optional tier grouping, and collecting matches using hotbar slot 1, with adjustable click delay.
- **Profiles:** export and import shareable settings files, optionally including saved friend names. Import backs up current settings and leaves automation off until enabled.

Profile formats 1 through 3 remain supported, with Ground Zero starting OFF for older profiles. Formats 1 and 2 also default behind text to OFF. New exports use **profile format 4**, include Ground Zero settings, and require **Penguin 1.9.15**.

## Included features

- Mining verification, auto-sell and individual alerts with volume controls.
- Ground Zero: independent outlines/tracers for yellow wool (yellow), black concrete (blue) and Block of Raw Gold (red), with closest-per-type or all targeting.
- Block tracers with closest/all targeting, a searchable block picker, Block Outlines and Vault presets, and aimed-block identification.
- Player nametags and tracers, offscreen indicators, guard/NPC filters, and independent friend appearance settings.
- Saved friends with individual on/off switches.
- Configurable left/right Windows clickers and smooth aim assist with target filters.
- **Aim height:** adjust from legs to head, with **Chest (72%)** as the default and a reset button. Enable **Aim vertically** for height correction.

## Multiple Lunar windows

Restart and upgrade **every window sharing the same game/config folder to 1.9.15 together**. Existing settings migrate automatically; older Penguin versions cannot read the updated shared settings after a save. Upgraded windows sync all saved settings, including module ON/OFF switches, normally within about **0.5 seconds while ticking**. Open menus update too; separate game/config folders remain independent.

Independent simultaneous edits merge, including changes to different friends. When windows change the same setting or friend, the last save wins for that change. Loading/stopping Penguin, selected targets and running operations stay local to each game. Changes to clicker controls require a fresh physical release/press; focused gameplay and a held button are still required.

The shared file is `config/penguin-live-settings.json`, initialized once from existing `namelines.json` and `cluesort.json` settings. It becomes the authoritative settings file. Use 1.9.15 in all windows sharing it.

## Compatibility and validation

This is a preview for the tested Lunar Fabric 1.21.11 configuration; later Lunar updates may require changes. **Version 1.9.15 built successfully and passed 238 automated tests.** Ground Zero and the new Block Outlines preset still need live Lunar testing. Version 1.9.14 built successfully, passed **228 automated tests**, loaded in Lunar, and its inspector correctly identified black concrete; tracer behavior still needs live confirmation. Version 1.9.13 passed **220 automated tests**, loaded successfully in Lunar, and the user confirmed hold-C zoom with Constant FOV. Version 1.9.12 passed a live load/stop/reload check with the Windows clicker ready. Existing automated coverage includes FOV restoration, retained errors, settings synchronization, profile migration and overlays. Multi-window sync, Constant FOV against Trap and the reported intermittent friend-color issue still need live confirmation. Aim smoothing was confirmed in use; adjustable aim placement and click delivery also need normal play testing.

See the included `README.txt` for the full settings and troubleshooting guide. The project uses the [MIT license](LICENSE).
