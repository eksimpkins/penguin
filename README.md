# Penguin for Lunar

Penguin is a Windows x64 controller and mod for **Lunar Client, Minecraft 1.21.11, Fabric and Fabric API**. Load or stop it while Minecraft stays open.

## Download

**[Download Penguin 1.9.22 for Windows](https://github.com/eksimpkins/penguin/releases/download/v1.9.22/Penguin-Lunar-1.9.22-Windows.zip)**

Extract the entire ZIP and keep Penguin.exe, app and runtime together. Java is included. GitHub's automatic Source code downloads are not the ready-to-run application.

## First launch and updates

1. Fully close Lunar, including its tray icon, then open Penguin.exe. It enables Lunar's built-in Enable Attach setting and backs up the launcher settings. If needed, close Lunar and choose Prepare Lunar.
2. Launch Lunar **Fabric 1.21.11** with Fabric API available in the profile.
3. In Penguin, click Refresh, select the game and choose Load Penguin. Keep Minecraft visible while textures reload.

Do not install another Penguin copy in the mods folder. Restart Minecraft once when updating; closing only the controller does not clear old loaded code or a previous FAILED initialization.

Use the current version in every game window sharing a settings folder. Existing settings are preserved. Versions before 1.9.22 cannot read the current shared settings format 6 after it is saved.

## Menu organization

**All** shows every module. **General** contains Message Alerts; **Combat** groups the clickers and Aim Assist; **Mining** contains Gen Mining and Block Tracers; **Visuals** contains player overlays and visual controls; **Clues** contains Clue Scrolls. **Friends, Profiles and Settings** are separate utility pages.

Search checks all modules, including those outside the current category. Clear it with the × button, or choose a category to clear the search and browse that category. Module ON/OFF controls sit in the settings-panel header where applicable; Gen Mining keeps individual feature switches.

Settings are split into smaller sections:

- **Gen Mining:** Verify, Auto-sell, Alerts, Actions.
- **Aim Assist:** Aim, Targets, Advanced.
- **Nametags and Friend Overlay:** Display, Style.
- **Block Tracers:** Display, Presets.

Reopening the menu restores the category, module, search, scroll positions and each module's selected section for that game session. Navigation stays local to each game and is not exported or synced. Back from a nested page preserves the parent view; explicit Friend Overlay links open that page directly.

**General > Message Alerts** has its own enabled switch, volume and Test button. Incoming private-message alerts work with Gen Mining and its mining cycle disabled. Your existing message-alert settings are preserved.

## Mining: Gen Mining and Block Tracers

Open **K > Mining**. **Gen Mining** contains verification, auto-sell and all mining alerts, with independent switches, delays and volume controls. **Block Tracers** contains the shared block list for outlines and tracer lines.

**Choose a mining-circle toggle in Settings; it defaults to Unbound.** During focused gameplay, aim at the first shattercube center block and press your chosen toggle. Penguin holds mining until plain prismarine marks completion, releases mining while smoothly turning right 90 degrees, then holds mining on the next center block. Each turn takes about **1.8 seconds in foreground gameplay**, with a gradual start and gentle stop; background timing can vary with game tick rate. After the fourth distinct finished block it releases mining and stops without a fourth turn. Blocks crossed during a turn do not advance the cycle.

**Mining > Gen Mining > Alerts > Cycle finished** plays a sound once after the fourth distinct block finishes. It defaults **ON at 100%**, with its own toggle, **0–200% volume** and **Test** button. It works in the background, independently of verification and other alerts. Cancelling or interrupting a cycle does not play this completion sound.

**Manual key or mouse-button presses, mouse movement or scrolling directed to that game stop its cycle and release its mining input.** The initial toggle press, held-toggle repeats and releases alone do not cancel it. Manually opening a game menu also stops it. The circle does not require either passive control below.

**Mining can continue while tabbed out.** Switching apps or game instances does not cancel the cycle; app-switch gestures such as Alt+Tab are exceptions to input cancellation. Start a cycle separately in each game window. Each runs independently, and input sent to another window does not stop it.

The existing controls under **Mining > Gen Mining > Actions** remain separate. **Tab in at** chooses **Not at all** (default), **Sea lantern**, **Prismarine** or **After 4 blocks**. The block choices close Minecraft's Escape pause menu when you aim at that type; **After 4 blocks** waits for the passive sequence below. Sea lantern is the early warning at **50 remaining**; prismarine means the center block is **finished**. This does not change which Windows app is in front. The selected action is independent of alarm switches and volumes.

**Turn 90 degrees at prismarine** is a separate switch, **OFF by default**. It uses the same slower turn, taking about **1.8 seconds in foreground gameplay** with a gradual start and gentle stop, preserving pitch. Blocks crossed during the turn do not trigger alerts or another action; observation resumes after the turn settles. The action is independent of alarm sound. Outside the four-block cycle, look away for one second before it can turn again.

The shattercube warning stages are sea lantern at **50**, dark prismarine at **25**, and prismarine bricks at **10** remaining. Only **plain prismarine** counts as finished.

For the passive Escape-menu sequence, choose **Tab in at: After 4 blocks** and enable **Turn 90 degrees at prismarine**. These controls do not hold mining. The first three prismarine completions turn right 90 degrees; the fourth closes Escape without another turn. Only distinct positions while Escape is open count; revisits are ignored. A new prismarine position can count after the turn settles without a look-away delay. Closing the menu manually, changing the tab-in choice, turning the switch off, or changing worlds resets the count. Both passive and mining-circle progress stay local to that game.

Search block names or registry IDs, add types to the list, or show only selected types. Each selected type has its own color editor with **Red, Green and Blue sliders**, a preview and reset. Selected rows now have a clearer background and accent. Changes save automatically.

Outlines and tracer lines always use that same block list and the same per-type colors. Their switches are independent. **O toggles outlines; P toggles tracers.** Turning either on also enables Block Tracers. They operate during gameplay, not while typing in menus.

**Closest of each type** draws one line to the nearest valid discovered match of every selected type. **All** traces all retained matches. Radius and line width are adjustable. Offscreen and behind targets still receive lines. Only loaded chunks are scanned, using bounded per-type samples; this is not a search of the entire world.

Presets are switches. ON adds the preset's blocks; OFF removes those blocks. Your other selected types and saved colors remain. A preset is ON when all of its types are selected; enabling a partial preset adds the missing types. Presets can overlap, so removing shared types also updates other preset switches.

- **Ground Zero:** yellow wool in yellow, black concrete in blue, and Block of Raw Gold in red. These colors are defaults; your saved custom colors are kept.
- **Glass, panes & wool:** clear/tinted/colored glass, clear/colored panes, and all wool colors.
- **Vault:** pale oak logs and wood, including stripped variants.

The horizontal radius goes from **4 to 512 blocks** for any selection, including Ground Zero.

Enabling a preset while Block Tracers is disabled enables its outlines and lines. Otherwise it keeps your display switches and Closest/All choice. Existing Ground Zero and outline settings still migrate into the shared list.

**Identify aimed block:** aim within 8 blocks, then open the inspector from Block Tracers. It displays the client-known ID, with **Copy block ID**, **Add to block list** and **Edit selected block color...** for a selected type. Entity decorations do not obscure the block-only check; a real block in front can still be hit, and a server-only original identity cannot be recovered.

## Clue-scroll timing

Clue Scrolls now allows a **0.05-second minimum delay per move**. Your saved delay stays unchanged until you adjust it; this is not a promise that an entire inventory sorts in 0.05 seconds.

## Other controls and features

- **K:** open Penguin in a world. At the main menu, use Open menu in the controller.
- **J:** toggle all player nametags/tracers, including friends, preserving their appearance settings.
- **Mining-circle toggle:** choose it in Settings; Unbound by default. It starts/stops the four-block circle during focused gameplay.
- **F8:** stop both clickers, aim tracking and the mining circle. Default clicker toggles are ] and F7; change them in Settings.
- **Stop Penguin:** disable the mod while Minecraft stays open. Closing only the controller does not stop it. Java classes remain loaded until Minecraft exits.
- Mining > Gen Mining: verification, auto-sell and separate alerts with volume controls.
- Friend lists with individual on/off switches, custom labels/tracers, guard/NPC filtering and offscreen indicators.
- Windows clickers and smooth aim assist with target filters and adjustable aim height. Clickers require focused gameplay and a fresh physical release/press after settings or focus changes.
- Menu scaling from 50–150%, No Debuff, Constant FOV, and clue-scroll sorting/collection.
- Constant FOV allows normal hold-C zoom while C is physically held during focused gameplay, restoring configured FOV on release. Remapped/toggle zoom is not covered. Server-side effects remain unchanged.

## Profiles and multiple windows

Export/import settings through Profiles. Friend names are optional on export and import. Imports preview the change, create a backup, stop the running mining cycle and leave automation off until enabled, including Gen Mining's passive tab-in and turning actions. Profile formats **1–7** still import; new exports use **format 8** and require **1.9.22**. Per-block colors, line width, Gen Mining controls, the mining-cycle binding and completion-alert settings are included. Older settings and profiles default the new completion alert to ON at 100%.

Updated windows sharing the same config folder sync saved settings, normally within about half a second while ticking. Different folders remain independent. Simultaneous independent changes merge; competing edits to the same setting use the last save. Loading/stopping, selected live targets and running operations remain local. The shared file is config/penguin-live-settings.json.

## Validation

Version 1.9.22 built successfully; all 382 automated tests passed. Live checks of the completion alert and slower turns remain pending.

See the included README.txt for additional features and troubleshooting. [MIT license](LICENSE).

