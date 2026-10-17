# Penguin 1.9.13 — Lunar preview

Download **Penguin-Lunar-1.9.13-Windows.zip** below and extract the entire ZIP. It includes Penguin.exe, the mod and Java runtime. GitHub's automatic **Source code** downloads are not the runnable Windows package.

## Changes

- **Hold-C zoom compatibility:** Constant FOV temporarily lets the normal game FOV through while you physically hold C in focused gameplay with no screen open. Your existing C zoom can work; releasing C restores the FOV selected in Minecraft.
- Penguin does not add zoom, consume C, change its binding or toggle Constant FOV. This compatibility rule covers **hold-to-zoom on C**, not remapped or toggle-style zoom.
- Movement and effect FOV changes, including Trap's zoom effect, can apply while C is held.
- Existing settings and features are preserved. No settings reset or new configuration is required.

## Retained from 1.9.12

- **Lunar loading fix:** Lunar's extra FOV accessor shares the same parameters as Minecraft's FOV method. The previous selector treated this as an ambiguous match and failed to load, even with Constant FOV OFF. Penguin now selects the exact Fabric-mapped method and leaves the accessor unchanged.
- **Original error retained:** subsequent controller status/load attempts preserve the first failure details instead of masking them with a generic repeat-failure message.

## Retained from 1.9.11

- **Live settings sync:** all saved settings, including module ON/OFF switches, update across upgraded game windows sharing the same game/config folder, normally within about 0.5 seconds while ticking. Open menus update too.
- **Optional '(behind)' text:** the shared **Show '(behind)' text** switch appears under Nametags and Friend Overlay and defaults OFF. Edge labels, offscreen positions and tracer lines remain unchanged.
- **Merged edits:** simultaneous changes to different settings or friends are retained. For conflicting changes to the same setting or friend, the last save wins for that change.
- **Profile compatibility:** format 1 and 2 profiles still import, with behind text OFF. New exports use format 3 and require 1.9.11 or newer.
- Includes No Debuff, Constant FOV, menu scaling, clue-scroll tools, profiles and all previous features.

**Multiple windows:** restart and load 1.9.13 in every participating game. Settings sync only within the same game/config folder; versions before 1.9.11 do not participate. Loading/stopping Penguin, chosen runtime targets and running operations remain local. A shared ON switch does not copy an active target or operation. Clicker control changes require a fresh physical release/press, and clicks still require focused gameplay with the button held.

**Saved files:** `config/penguin-live-settings.json` becomes the authoritative settings file, initialized once from the existing `namelines.json` and `cluesort.json` files. Later changes made by older versions to those legacy files do not join live sync.

**Validation:** all 220 automated tests passed, including holding/releasing C, focus eligibility, unchanged hand projection and preserving the module setting. Live C-key zoom confirmation is still pending. The tests retain coverage for Lunar's duplicate FOV accessor, exact method selection, FOV restoration and retained-error reporting. Version 1.9.12 loaded, stopped and loaded again successfully in a fresh Lunar Fabric 1.21.11 session, with the Windows clicker reporting ready. Multi-window behavior in Lunar, Constant FOV against Trap and the reported intermittent friend-color issue still need live confirmation.

**Updating:** restart each Minecraft game once, including any game where the previous load reported **FAILED**, then use the new Penguin.exe. Reopening only the controller cannot clear that old loaded code. Existing settings and older profiles are preserved; no settings reset is needed.

Requires **Windows x64, Lunar Fabric 1.21.11 and Fabric API**. On first use, fully close Lunar, including its tray icon, then open Penguin.exe to prepare attachment. Launch the game, click Refresh, select it and Load Penguin.

**Controls:** K opens Penguin; J toggles all player nametags/tracers; F8 stops both clickers and aim tracking. Stop Penguin disables the mod while Minecraft stays open. Loaded Java classes remain until Minecraft exits.

`SHA256SUMS.txt` contains the Windows ZIP checksum.

## Previous release: 1.9.10

- Typed friend names and Nearby selections use the same account-name matching. Adding an existing OFF friend turns it ON again without duplicating it. Nearby entries use the same listed-player and NPC checks as Penguin's overlay.
- Friend styling is resolved when drawing labels and tracers. Formatting codes in account names no longer override the chosen text color.
- All 193 automated tests passed. The exact cause of the reported intermittent color delay remained unconfirmed; the changes addressed concrete identity, add-flow and formatting issues found during investigation. Version 1.9.10 did not support live settings sync.
