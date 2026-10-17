# Penguin 1.9.17 — Lunar preview

Download **Penguin-Lunar-1.9.17-Windows.zip** below and extract the entire ZIP. Keep Penguin.exe, app and runtime together. Java is included.

## Changes

- **Menu memory:** reopening Penguin restores your main menu category, selected module, search and both scroll positions for that game session. This navigation is local to each game, not shared through profiles or live settings. Back from nested pages preserves the parent view.
- **Mining organization:** the Mining tab now contains **Gen Mining** and **Block Tracers**. Gen Mining groups verification, auto-sell and all mining alerts, with their own switches, delays and volume controls. The former Blocks module is named Block Tracers.
- **Preset switches:** Ground Zero, Glass/panes/wool and Vault add their block types when switched ON and remove them when OFF, preserving unrelated selected types. Existing custom colors are kept; Ground Zero supplies yellow, blue and red defaults only when a type has no saved color. Partial presets add missing types. Overlapping presets share the same selected block list.
- **Clearer selection:** selected menu rows have a stronger background/accent, with visible preset switches and separate color swatches.
- **Clue Scrolls:** minimum move delay lowered to **0.05 seconds (50 ms)**. Existing saved/default timing is unchanged until adjusted. The delay applies between moves, not to the whole inventory sort.

Block Tracers keeps the shared outline/tracer list, searchable block names/IDs, RGB color sliders, aimed-block inspector, closest-per-type/all tracing, and **4–512-block horizontal radius**. **O toggles outlines; P toggles tracers.** Enabling a preset while the module is disabled enables both displays; otherwise the display switches and Closest/All choice stay unchanged.

## Updating

Restart Minecraft once to clear the old loaded code, then load this version with Penguin.exe. Existing settings are preserved; no reset is needed. Use the current version in all windows sharing a settings folder. Profile format remains **5**, supported since 1.9.16; older profile formats 1–4 still import.

Requires Windows x64, Lunar Fabric 1.21.11 and Fabric API. On first use, fully close Lunar including its tray icon, open Penguin.exe to prepare attachment, then launch the game and choose Load Penguin. K opens the menu. Stop Penguin disables its effects while Minecraft remains open; loaded classes remain until Minecraft exits.

**Validation:** version 1.9.17 built successfully and passed all 270 automated tests. Live checks are pending. Version 1.9.16 passed 260 tests, loaded successfully in Lunar, and the user confirmed the unified menu and 4-block minimum. In-world rendering and the new menu behavior still need live confirmation.

Other features remain included: hold-C zoom with Constant FOV, No Debuff, friend styling, live settings sync, clue-scroll tools, mining alerts, clickers and aim assist. SHA256SUMS.txt contains the Windows ZIP checksum.
