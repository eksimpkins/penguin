# Penguin 1.9.15 — Lunar preview

Download **Penguin-Lunar-1.9.15-Windows.zip** below and extract the entire ZIP. It includes Penguin.exe, the mod and Java runtime. GitHub's automatic **Source code** downloads are not the runnable Windows package.

## Changes

- **Visuals > Ground Zero:** a dedicated module with **yellow outlines/tracers for yellow wool**, **blue for black concrete**, and **red for Block of Raw Gold**. It starts OFF; all three types, outlines and tracer lines start ON within it. Closest mode draws up to three lines, one to the closest match of each enabled type; **All** traces every discovered match.
- Ground Zero has separate type toggles and colors, plus line-width and radius controls. It matches only `minecraft:yellow_wool`, `minecraft:black_concrete` and `minecraft:raw_gold_block`. While enabled, it owns rendering for those three IDs so generic Block Outlines and Block Tracers do not paint over its chosen colors. Other block types are unaffected.
- **Block Outlines preset:** in **Visuals > Block Tracers** and **Choose blocks**, select the block types used by your enabled **Glass blocks**, **Glass panes** and **Wool** categories. This includes clear/tinted/all 16 colored glass blocks, clear/all 16 colored panes, and all 16 wool colors, as enabled.
- Applying the preset replaces the selected tracer block types, enables Block Tracers and tracer lines, and chooses **Closest**. It takes a snapshot of the category switches, so apply it again after changing them. Existing colored Block Outlines rendering and settings are preserved.

## Retained block tools

- **Trace closest block:** in **Visuals > Block Tracers**, one button enables the finder and tracer lines and selects the closest target. **Tracer target: Closest / All** replaces the old Trace all switch. Fresh settings default to Closest; existing saved All selections are preserved.
- Closest mode follows the nearest valid highlighted match, rechecked each frame by distance from you to the block's center. A mined or removed match no longer holds the line. Lines still work for behind and offscreen blocks.
- **Identify aimed block:** aim at an unfamiliar block from within **8 blocks**, then open **K > Visuals > Block Tracers > Identify aimed block**. The inspector shows its exact client block registry ID and coordinates. **Copy block ID** copies its ID; **Add to highlighted blocks** retains the existing selected blocks, including preset selections. Adding a type does not enable the module.

The inspector ignores entity displays and colored entity overlays, but a real block in front can still be hit. It cannot reveal a different block type known only to the server. Tracers use loaded chunks and a bounded sampled cache; Closest means the nearest currently highlighted discovered match, not every block in the world.

## Retained behavior

- **Hold-C zoom** still works with Constant FOV. Holding C in focused gameplay lets normal FOV through; releasing C restores the selected FOV. This covers existing hold-C zoom, not remapped or toggle zoom, and other movement/effect FOV changes can apply during the hold.
- Includes the **Lunar FOV loading fix**, original-error reporting, live settings sync, optional behind text, friend appearance controls, No Debuff, menu scaling, clue-scroll tools and profiles.
- Existing settings and older profiles are preserved. No settings reset is needed. Profile formats 1 through 3 still import, with Ground Zero starting OFF. New exports use **profile format 4**, include Ground Zero settings, and require **Penguin 1.9.15**.

**Updating:** restart each Minecraft game once, then use the new Penguin.exe. This also clears any previous FAILED initialization; reopening only the controller cannot clear old loaded game code. **Upgrade all windows sharing a settings folder to 1.9.15 together.** Existing settings migrate automatically; older Penguin versions cannot read the updated shared settings after a save. Upgraded games using the same config folder sync saved settings and module switches; active targets and running operations remain local.

**Validation:** version 1.9.15 built successfully and passed 238 automated tests. Ground Zero and the new Block Outlines preset still need live Lunar testing. Version 1.9.14 built successfully, passed 228 automated tests, loaded in Lunar, and its inspector correctly identified black concrete; tracer behavior still needs live confirmation. Version 1.9.13 passed 220 automated tests, loaded successfully in Lunar, and the user confirmed hold-C zoom with Constant FOV. Version 1.9.12 passed a live load/stop/reload check. Multi-window sync, Constant FOV against Trap and the reported intermittent friend-color issue still need live confirmation.

Requires **Windows x64, Lunar Fabric 1.21.11 and Fabric API**. On first use, fully close Lunar, including its tray icon, then open Penguin.exe to prepare attachment. Launch the game, click Refresh, select it and Load Penguin.

**Controls:** K opens Penguin; J toggles all player nametags/tracers; O toggles block outlines; P toggles block tracers; F8 stops both clickers and aim tracking. Stop Penguin disables the mod while Minecraft stays open. Loaded Java classes remain until Minecraft exits.

`SHA256SUMS.txt` contains the Windows ZIP checksum.
