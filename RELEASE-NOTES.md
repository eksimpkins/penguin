# Penguin 1.9.25 — Lunar preview

Download **[Penguin-Lunar-1.9.25-Windows.zip](https://github.com/eksimpkins/penguin/releases/download/v1.9.25/Penguin-Lunar-1.9.25-Windows.zip)** and extract the entire ZIP. Keep Penguin.exe, app and runtime together. Java is included.

Developers can use the attached **Penguin-Lunar-1.9.25-Source.zip** for the buildable Penguin source and tests. GitHub's automatic **Source code** downloads contain only this documentation repository. **SHA256SUMS.txt** covers both release ZIPs.

## Changes

- **CosmicUtilities is included in Prepare Lunar.** Checking CosmicUtilities now selects the tested Minecoin **1.5 experimental-r2 compatibility build for Minecraft 1.21.11**. Friends no longer need to find or select a separate JAR. This unofficial port fixes the G Focus marker crash when a player leaves view and errors while loading saved cooldown settings.
- **Local JAR choices still work.** Choose Utilities JAR… selects a different compatible Minecoin build; Use included build returns to the bundled version. Penguin does not automatically port other 1.21.8 JARs.
- **Installation remains optional.** All companion choices start unchecked. Select the intended Lunar profile, review the files, then install with Lunar fully closed. Required dependencies are checked; previous versions of selected mods are backed up. Unchecked and unrelated mods remain in place. CosmicPings and CosmicTextures continue to use compatible official Modrinth releases.

The included CosmicUtilities build is **not an official Minecoin release**. Original author attribution and **All Rights Reserved** metadata remain intact. Penguin's MIT license does not relicense CosmicUtilities. See the included **THIRD-PARTY-NOTICES.txt** for its identity and attribution.

This release keeps the 1.9.24 mining-start fix, smooth variable-speed turns, background cycles, manual-input cancellation, completion alerts and verification pause/resume. Existing settings and bindings are preserved.

## Installing or updating

1. Extract the new Windows ZIP and open Penguin.exe.
2. Fully close Minecraft and the Lunar launcher, including its tray icon.
3. Open **Prepare Lunar**, choose the intended **Fabric 1.21.11** profile and check **CosmicUtilities**. Review the selected files, then install. The old Utilities JAR is backed up before replacement.
4. Launch Lunar Fabric 1.21.11, then select the game in Penguin and choose **Load Penguin**.

Companion mods load when Minecraft starts. Installing into the normal .minecraft mods folder may not affect Lunar; use the profile shown by Prepare Lunar. Restart Minecraft once when updating Penguin to clear previously loaded code.

Shared settings remain **format 6**, and exported profiles remain **format 8** (compatible with Penguin 1.9.22 and newer). Older profiles still import. Use the current Penguin version in every game window sharing a settings folder.

## Validation

**All 437 automated tests across 51 suites passed.** Eight new tests cover the bundled artifact, integrity checks, dependency handling, local overrides, backups, duplicates and source labels. An isolated installation using the controller JAR and included Java runtime confirmed the exact fixed build without a Utilities download, preserved installed files during review, backed up the old JAR, reused compatible Fabric API and created no duplicates on repeat installation. Independent review found no blockers.

The preceding 1.9.24 release passed **429 automated tests across 50 suites**. Live checks confirmed mining start/stop/restart on the same block, all four manual cancellation methods with normal mining afterward, a full background cycle with three turns and one completion alert, and pause/resume through a real verification prompt.

The exact bundled CosmicUtilities **experimental-r2** JAR previously reached the Lunar Fabric 1.21.11 main menu without saved-settings errors. The G Focus offscreen check passed before r2; that code is unchanged in r2. Item-overlay, damage-indicator and HUD checks remain pending. These results do not claim that every CosmicUtilities feature has been tested.

Requires Windows x64, Lunar Fabric 1.21.11 and Fabric API. K opens the menu. Stop Penguin disables its effects while Minecraft remains open; loaded classes remain until Minecraft exits. Closing only the controller does not stop Penguin.
