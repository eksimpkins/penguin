# Penguin 1.9.16 — Lunar preview

Download **Penguin-Lunar-1.9.16-Windows.zip** below and extract the entire ZIP. It includes Penguin.exe, the mod and Java runtime. GitHub's automatic Source code downloads are not the runnable Windows package.

## Changes

- **Visuals > Blocks** combines block outlines and tracer lines into one module. Both use the same selected block types and per-block colors; switch **Outlines** and **Tracers** independently.
- **Search and manage blocks:** search registered block names or IDs, add/remove types, and view the selected list. Each selected block has a color editor with **Red, Green and Blue sliders**, a preview, reset and automatic saving. The chosen color applies to its outlines and lines.
- **Ground Zero preset:** selects yellow wool in yellow, black concrete in blue and Block of Raw Gold in red. It enables outlines and tracers with **Closest of each type**. Glass, panes & wool and Vault presets remain available.
- **Horizontal radius: 4–512 blocks**, including Ground Zero, so the highlight range can focus on nearby blocks.
- **O** toggles outlines; **P** toggles tracer lines. Turning either on also enables Blocks. Turning one off leaves the other unchanged. These keys operate during gameplay, not while typing in menus.
- Closest mode draws a separate line to the nearest discovered valid block of each selected type. **All** traces all retained matches. Scanning uses loaded chunks and bounded per-type caches; a dense field of one type cannot consume another type's entire allocation.
- Existing active Ground Zero selections and colors migrate into Blocks. The old separate Block Outlines and Ground Zero menus are replaced. When only legacy Block Outlines was active, its categories become an outlines-only shared list. When tracing was active, its selected types take priority over the old broad outline categories.

## Updating

Restart Minecraft once, then use the new Penguin.exe. **Upgrade all windows sharing a settings folder to 1.9.16 together.** Old settings migrate automatically; older versions cannot read the updated shared settings after a save. No settings reset is needed.

Profile formats **1–4** remain supported. New exports use **format 5**, include per-block colors and line width, and require **1.9.16**. Active Ground Zero settings in older profiles migrate into the shared block list.

The aimed-block inspector remains under **K > Visuals > Blocks > Identify aimed block**. Aim within 8 blocks before opening it. It reads the client-known registry ID beneath entity decorations, and can copy the ID or add the type. It cannot reveal a different server-only block identity.

**Validation:** version 1.9.16 built successfully and passed all 260 automated tests. Live checks are pending. Version 1.9.15 passed 238 automated tests and loaded successfully in Lunar with the Windows clicker ready. Version 1.9.14's inspector identified black concrete and raw gold from the user's screenshots. Actual world rendering of the new unified controls still needs live confirmation.

Requires **Windows x64, Lunar Fabric 1.21.11 and Fabric API**. On first use, fully close Lunar including its tray icon, open Penguin.exe to prepare attachment, launch the game, select it and choose Load Penguin. K opens the menu, J toggles player labels/tracers, and F8 stops both clickers and aim tracking. Stop Penguin disables the mod while Minecraft remains open; loaded classes remain until Minecraft exits.

Other features and fixes remain included: hold-C zoom with Constant FOV, No Debuff, friend styling, live settings sync, clue-scroll tools, mining alerts, clickers and aim assist. SHA256SUMS.txt contains the Windows ZIP checksum.
