# Penguin 1.9.24 — Lunar preview

Download **[Penguin-Lunar-1.9.24-Windows.zip](https://github.com/eksimpkins/penguin/releases/download/v1.9.24/Penguin-Lunar-1.9.24-Windows.zip)** and extract the entire ZIP. Keep Penguin.exe, app and runtime together. Java is included.

Developers can use the attached **Penguin-Lunar-1.9.24-Source.zip** for the buildable source and tests. GitHub's automatic **Source code** downloads contain only this documentation repository. **SHA256SUMS.txt** covers both release ZIPs.

## Changes

- **Mining starts and restarts correctly:** fixed cycles that swung the pickaxe without mining, including with CosmicUtilities installed. Each new or resumed block gets a normal attack press before held mining continues. Turning, verification waits and cancellation release mining input and clear pending cycle presses.
- **Smoother mining turns with variable speed:** each 90-degree turn starts immediately and takes a randomly selected **1.6–2.1 seconds** in foreground gameplay. The pace follows one smooth curve rather than changing abruptly from frame to frame. Fixed conflicting tick/render updates that could make foreground turns hitch. Background instances continue through game ticks; throttling can lengthen their turns. There is **no added delay** before turning.
- **Optional mods in Prepare Lunar:** choose a Lunar profile and select companion mods, all initially unchecked. Review/download first, then install with Lunar fully closed. Official compatible releases come from Modrinth with file-size, SHA-512 and Fabric metadata checks. Required dependencies are included. Existing versions of selected mods are backed up; unrelated and unchecked mods remain untouched. These companion mods load on the next game launch.
- **Verification during a mining cycle:** with **Mining > Gen Mining > Verify** enabled, a verification prompt pauses mining and turning. Penguin resumes the same cycle position and finished-block count only after the server confirms successful verification; sending the command alone does not resume it. Verify must remain enabled. A blocked command, a 45-second timeout or manual cancellation stops the cycle instead.

The optional chooser supports CosmicPings, CosmicTextures and **CosmicUtilities by Minecoin**. If CosmicUtilities has no official Fabric 1.21.11 release available, leave it unchecked or use **Choose Utilities JAR…** to select a compatible Minecoin build you already have. Penguin does not automatically port a 1.21.8 JAR. The separate experimental compatibility build used for local testing is **not included in this release**.

The completion alert remains under **Mining > Gen Mining > Alerts > Cycle finished**, with its own toggle, 0–200% volume and Test button. Background mining and manual-input cancellation remain supported. Choose the mining-cycle toggle in Settings; it starts Unbound. Only plain prismarine means a block is finished. Sea lantern (50), dark prismarine (25) and prismarine bricks (10) are warning stages.

## Updating

Restart Minecraft to clear previously loaded Penguin code, then load this version. Installing companion mods requires fully closing Lunar, including its tray icon, first. Select the correct profile in Prepare Lunar; the normal .minecraft mods folder is not always Lunar's mod location.

Shared settings remain **format 6**, and exported profiles remain **format 8** (compatible with Penguin 1.9.22 and newer). Existing settings and bindings are preserved. Older profiles still import. Use the current Penguin version in every game window sharing a settings folder.

**Validation:** all **429 automated tests across 50 suites** passed. Live testing confirmed mining start/stop/restart on the same block, all four manual cancellation methods with normal mining afterward, a full background cycle with three turns and one completion alert, and pause/resume through a real verification prompt. Companion downloads, dependency staging and installation of a locally supplied CosmicUtilities build passed. That separate build passed startup and Gang Focus checks; this is not a full validation of every CosmicUtilities feature.

Requires Windows x64, Lunar Fabric 1.21.11 and Fabric API. K opens the menu. Stop Penguin disables its effects while Minecraft remains open; loaded classes remain until Minecraft exits. Closing only the controller does not stop Penguin.
