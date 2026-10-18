# Penguin 1.9.27 — Lunar preview

Download **[Penguin-Lunar-1.9.27-Windows.zip](https://github.com/eksimpkins/penguin/releases/download/v1.9.27/Penguin-Lunar-1.9.27-Windows.zip)** and extract the entire ZIP. Keep Penguin.exe, app and runtime together. Java is included.

Developers can use the attached **Penguin-Lunar-1.9.27-Source.zip** for the buildable Penguin source and tests. GitHub's automatic **Source code** downloads contain only this documentation repository. **SHA256SUMS.txt** covers both release ZIPs.

## Changes

- **CosmicUtilities mining correction.** The included Minecoin **1.5 experimental-r3 compatibility build for Minecraft 1.21.11** corrects inherited overrides that could prevent ordinary left-click mining and target changes. Minecraft now makes its normal block-start, target-change and right-click-while-mining decisions. Peaceful Mining stays within normal block reach.
- **Prepare Lunar installs the corrected build.** Check CosmicUtilities to install r3 without a separate download. The old Utilities JAR is backed up before replacement. Choose Utilities JAR… still accepts a different compatible build; Use included build returns to the bundled version.
- **Existing fixes remain.** The G Focus marker and saved-settings corrections are retained. Prepare Lunar still recognizes Lunar's boot log and refreshes Fabric Loader detection on review. Penguin's mining-start fix, smooth turns, background cycles, input cancellation, completion alerts and verification pause/resume are unchanged.

All companion choices start unchecked. CosmicPings and CosmicTextures continue to use compatible official Modrinth releases. Required dependencies are checked; unchecked and unrelated mods remain in place.

The included CosmicUtilities build is **not an official Minecoin release**. Original author attribution and **All Rights Reserved** metadata remain intact. Penguin's MIT license does not relicense CosmicUtilities. See **THIRD-PARTY-NOTICES.txt** for the exact build and attribution.

## Install the mining fix

**Opening or loading the new Penguin alone does not replace an already-installed CosmicUtilities JAR.**

1. Fully close Minecraft and the Lunar launcher, including its tray icon.
2. Download and extract the new Windows ZIP, then open **Penguin 1.9.27**.
3. Open **Prepare Lunar**, select the intended **Fabric 1.21.11** profile and check **CosmicUtilities**. If a local Utilities JAR was selected, choose **Use included build**.
4. Review and install. The previous Utilities JAR is backed up before replacement.
5. Relaunch Lunar Fabric 1.21.11, then select the game in Penguin and choose **Load Penguin**.

Companion mods load when Minecraft starts. Use the profile shown by Prepare Lunar; installing into the normal .minecraft mods folder may not affect Lunar. Update each profile separately if using multiple profiles. Fully restarting Minecraft also clears Penguin's previously loaded code.

Settings and bindings are preserved. Shared settings remain **format 6**; exported profiles remain **format 8** (compatible with Penguin 1.9.22 and newer). Older profiles still import. Use the current Penguin version in every game window sharing a settings folder.

## Validation

**Penguin 1.9.27 passed 458 automated tests across 52 suites, with no failures or errors.** The Utilities regression check passed all **17 checks**, including eight executable targeting cases, with no unresolved Minecraft references or mixin selectors. G Focus and saved-settings code is byte-identical to r2.

An isolated r2-to-r3 installation check used the actual companion JARs and a real Lunar boot log. It verified the bundled SHA256, preserved installed files during review, backed up duplicate old r2 copies, left CosmicPings, CosmicTextures and Fabric API unchanged, and created no duplicates on repeat installation.

**A live mining retest on the affected friend's computer is still pending.** Automated checks do not establish that their exact in-game problem is resolved.

The preceding 1.9.26 release passed **456 automated tests across 52 suites** and an isolated installation check using a real Lunar boot log. The preceding 1.9.24 release passed **429 automated tests across 50 suites**; live checks covered mining starts, manual cancellation, background cycles, the completion alert and pause/resume through verification.

The earlier CosmicUtilities r2 build passed startup without saved-settings errors; G Focus passed an earlier live check. Those fixes remain in r3. Item-overlay, damage-indicator and HUD checks remain pending. These results do not claim that every CosmicUtilities feature has been tested.

Requires Windows x64, Lunar Fabric 1.21.11 and Fabric API. K opens the menu. Stop Penguin disables its effects while Minecraft remains open; loaded classes remain until Minecraft exits. Closing only the controller does not stop Penguin.
