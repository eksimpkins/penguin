# Penguin 1.9.18 — Lunar preview

Download **Penguin-Lunar-1.9.18-Windows.zip** below and extract the entire ZIP. Keep Penguin.exe, app and runtime together. Java is included.

## Changes

- **Clearer navigation:** All, Combat, Mining, Visuals and Clues group the modules. Combat contains clickers and Aim Assist; Mining keeps Gen Mining and Block Tracers separate. Friends, Profiles and Settings are separate utility pages.
- **Smaller settings sections:** Gen Mining has Verify / Auto-sell / Alerts; Aim Assist has Aim / Targets / Advanced; Nametags and Friend Overlay have Display / Style; Block Tracers has Display / Presets. Module ON/OFF controls sit in the settings header where applicable. Gen Mining retains individual switches.
- **Global search:** search across all modules without changing categories first. Clear with ×, or choose a category to clear search and browse its modules.
- **More menu memory:** the category, module, query, scroll positions and each module's selected settings section are remembered for that game session. Navigation remains local, outside settings profiles and live synchronization.
- **Inspector shortcut:** after adding an aimed block to the list, use **Edit selected block color...** to open its RGB editor. Already-selected blocks offer the same shortcut.
- **Block editing:** the picker opens to your selected blocks; typing searches all available blocks. Its footer explains whether outlines and tracers are active or paused. Color reset clearly identifies the standard amber color.
- **Small-screen and keyboard polish:** more room for settings, compact alert controls, clearer help text, and focus fixes for scrolling and changing Friends, Profiles and block lists.

Block Tracers retains one shared selection for outlines and lines, per-block colors, additive preset switches, independent O/P controls, closest-per-type tracing and the 4–512-block horizontal radius. Ground Zero defaults remain yellow wool in yellow, black concrete in blue and raw gold in red. Saved custom colors and unrelated selected types are preserved. Clue Scrolls retains its 0.05-second minimum delay per move and existing saved timing.

## Updating

Restart Minecraft once to clear the old loaded code, then load this version with Penguin.exe. Existing settings are preserved; no reset is needed. Use the current version in every window sharing a settings folder. Profile format remains **5**, supported since 1.9.16; older profile formats 1–4 still import.

Requires Windows x64, Lunar Fabric 1.21.11 and Fabric API. On first use, fully close Lunar including its tray icon, open Penguin.exe to prepare attachment, then launch the game and choose Load Penguin. K opens the menu. Stop Penguin disables its effects while Minecraft remains open; loaded classes remain until Minecraft exits. Closing only the controller does not stop Penguin.

**Validation:** version 1.9.18 built successfully and passed all 272 automated tests. Live confirmation of the reorganized menu is pending.

The included README.txt covers clicker input, profiles, synchronization, removal, compatibility and other features. SHA256SUMS.txt contains the Windows ZIP checksum.
