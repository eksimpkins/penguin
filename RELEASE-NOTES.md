# Penguin 1.9.9 — Lunar preview

Download **Penguin-Lunar-1.9.9-Windows.zip** below and extract the entire ZIP. It includes Penguin.exe, the mod and Java runtime. GitHub's automatic **Source code** downloads are not the runnable Windows package.

## Changes

- **Visuals > No Debuff:** blindness and nausea visual suppression now share one toggle. If either old setting was enabled, No Debuff stays enabled after upgrading. Actual status effects, timers and icons remain; this does not remove server-side debuffs.
- **Visuals > Constant FOV:** keeps your world view at the FOV selected in Minecraft's settings, preventing movement and effect multipliers from zooming it in or out. Hand/item projection is unchanged. Defaults off; turning it off or stopping Penguin restores normal FOV changes.
- **Profile compatibility:** imports existing 1.9.8 profiles and migrates the old blindness/nausea switches. New exports include both new controls and require 1.9.9 or newer.
- Includes menu scaling, clue-scroll tools, shareable profiles and all previous features.

**Validation:** 188 automated tests passed, including renderer compatibility, FOV restoration and settings/profile migration. Live Lunar testing against the enchantment is still pending.

**Updating:** restart Minecraft once to clear older loaded code, then use the new Penguin.exe. Existing settings are preserved. Press K, open Visuals, and enable Constant FOV to use the new control.

Requires **Windows x64, Lunar Fabric 1.21.11 and Fabric API**. On first use, fully close Lunar, including its tray icon, then open Penguin.exe to prepare attachment. Launch the game, click Refresh, select it and Load Penguin.

**Controls:** K opens Penguin; J toggles all player nametags/tracers; F8 stops both clickers and aim tracking. Stop Penguin disables the mod while Minecraft stays open. Loaded Java classes remain until Minecraft exits.

`SHA256SUMS.txt` contains the Windows ZIP checksum.
