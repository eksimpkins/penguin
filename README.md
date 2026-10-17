# Penguin for Lunar

Penguin is a Windows x64 controller and mod for **Lunar Client, Minecraft 1.21.11, Fabric and Fabric API**. Load or stop it while Minecraft stays open.

## Download

**[Download Penguin 1.9.16 for Windows](https://github.com/eksimpkins/penguin/releases/download/v1.9.16/Penguin-Lunar-1.9.16-Windows.zip)**

Extract the entire ZIP and keep Penguin.exe, app and runtime together. Java is included. GitHub's automatic Source code downloads are not the ready-to-run application.

## First launch and updates

1. Fully close Lunar, including its tray icon, then open Penguin.exe. It enables Lunar's built-in Enable Attach setting and backs up the launcher settings. If needed, close Lunar and choose Prepare Lunar.
2. Launch Lunar **Fabric 1.21.11** with Fabric API available in the profile.
3. In Penguin, click Refresh, select the game and choose Load Penguin. Keep Minecraft visible while textures reload.

Do not install another Penguin copy in the mods folder. Restart Minecraft once when updating; closing only the controller does not clear old loaded code or a previous FAILED initialization.

**Upgrade every window sharing a game/config folder to 1.9.16 together.** Existing settings migrate automatically. Older Penguin versions cannot read the updated shared settings after a save.

## Blocks: one list for outlines and tracers

Open **K > Visuals > Blocks**. Search block names or registry IDs, add types to the list, or show only selected types. Each selected type has its own color editor with **Red, Green and Blue sliders**, a preview and reset. Changes save automatically.

Outlines and tracer lines always use that same block list and the same per-type colors. Their switches are independent. **O toggles outlines; P toggles tracers.** Turning either on also enables the Blocks module. They operate during gameplay, not while typing in menus.

**Closest of each type** draws one line to the nearest valid discovered match of every selected type. **All** traces all retained matches. Radius and line width are adjustable. Offscreen and behind targets still receive lines. Only loaded chunks are scanned, using bounded per-type samples; this is not a search of the entire world.

Presets:

- **Ground Zero:** yellow wool in yellow, black concrete in blue, and Block of Raw Gold in red. Enables outlines and lines with closest-per-type targeting.
- **Glass, panes & wool:** clear/tinted/colored glass, clear/colored panes, and all wool colors.
- **Vault:** pale oak logs and wood, including stripped variants.

The horizontal radius goes from **4 to 512 blocks** for any selection, including Ground Zero.

The old separate Ground Zero and Block Outlines menus are replaced by Blocks. Active Ground Zero types and colors migrate automatically. If only legacy Block Outlines was active, its enabled categories become an outlines-only shared list. If tracing was active, the tracer selection takes priority over broad legacy outline categories.

**Identify aimed block:** aim within 8 blocks, then open the inspector from Blocks. It displays the client-known ID, with Copy block ID and Add to highlighted blocks. Entity decorations do not obscure the block-only check; a real block in front can still be hit, and a server-only original identity cannot be recovered.

## Other controls and features

- **K:** open Penguin in a world. At the main menu, use Open menu in the controller.
- **J:** toggle all player nametags/tracers, including friends, preserving their appearance settings.
- **F8:** stop both clickers and aim tracking. Default clicker toggles are ] and F7; change them in Settings.
- **Stop Penguin:** disable the mod while Minecraft stays open. Closing only the controller does not stop it. Java classes remain loaded until Minecraft exits.
- Mining verification, auto-sell and separate alerts with volume controls.
- Friend lists with individual on/off switches, custom labels/tracers, guard/NPC filtering and offscreen indicators.
- Windows clickers and smooth aim assist with target filters and adjustable aim height. Clickers require focused gameplay and a fresh physical release/press after settings or focus changes.
- Menu scaling from 50–150%, No Debuff, Constant FOV, and clue-scroll sorting/collection.
- Constant FOV allows normal hold-C zoom while C is physically held during focused gameplay, restoring configured FOV on release. Remapped/toggle zoom is not covered. Server-side effects remain unchanged.

## Profiles and multiple windows

Export/import settings through Profiles. Friend names are optional on export and import. Imports preview the change, create a backup and leave automation off until enabled. Profile formats **1–4** still import; new exports use **format 5** and require **1.9.16**. Per-block colors and line width are included.

Updated windows sharing the same config folder sync saved settings, normally within about half a second while ticking. Different folders remain independent. Simultaneous independent changes merge; competing edits to the same setting use the last save. Loading/stopping, selected live targets and running operations remain local. The shared file is config/penguin-live-settings.json.

## Validation

Version 1.9.16 built successfully and passed all 260 automated tests. Live checks are pending. Version 1.9.15 passed 238 automated tests and loaded successfully in Lunar. The inspector identified black concrete and raw gold in the user's screenshots. New unified menu/rendering still needs live confirmation. Previous tests cover profiles, synchronization, reversible hooks, FOV, overlays and input; hold-C zoom was confirmed in use.

See the included README.txt for additional features and troubleshooting. [MIT license](LICENSE).
