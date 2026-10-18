# Penguin 1.9.19 — Lunar preview

Download **Penguin-Lunar-1.9.19-Windows.zip** below and extract the entire ZIP. Keep Penguin.exe, app and runtime together. Java is included.

## Changes

- **Mining > Gen Mining > Actions:** **Tab in at** chooses **Not at all** (default), **Sea lantern**, **Prismarine** or **After 4 blocks**. The block choices close Minecraft's Escape pause menu on that type; the four-block choice waits for the full cycle. Sea lantern gives an early return at **50 remaining**; prismarine marks a **finished center block**. This controls the menu inside Minecraft; it does not switch Windows apps.
- **Turn 90 degrees at prismarine** adds a separate switch, **OFF by default**, for a 90-degree right turn when looking at prismarine.
- For a shattercube cycle, choose **Tab in at: After 4 blocks** and enable **Turn 90 degrees at prismarine**. The first three prismarine completions turn right 90 degrees with Escape open; the fourth closes Escape without another turn. Sea lanterns never count. Only different block positions count; revisits are ignored, and a new position already showing prismarine counts without a look-away delay. Closing Escape manually, choosing another tab-in option, disabling the turn switch, or changing worlds resets the count.
- These actions are independent of block alarm switches and sound volumes. Existing alert controls remain available.
- Warning stages remain separate from completion: sea lantern is **50**, dark prismarine **25**, and prismarine bricks **10** remaining. Only **plain prismarine** triggers a completion turn or advances the four-block cycle.
- The new settings save and sync between updated game windows. Settings profiles include them, but importing a profile resets Tab in at to Not at all and leaves turning OFF. The running completion count stays local to each game.

The reorganized menu, session navigation memory, independent Gen Mining controls and separate Block Tracers module remain. Ground Zero presets and saved per-block colors are preserved.

## Updating

Restart Minecraft once to clear the old loaded code, then load this version with Penguin.exe. Existing settings are preserved; no reset is needed. Update every window sharing a settings folder together. This release writes shared settings **format 4** and profile exports **format 6**, which require **1.9.19**. Older shared settings migrate automatically; profile formats **1–5** still import.

Requires Windows x64, Lunar Fabric 1.21.11 and Fabric API. On first use, fully close Lunar including its tray icon, open Penguin.exe to prepare attachment, then launch the game and choose Load Penguin. K opens the menu. Stop Penguin disables its effects while Minecraft remains open; loaded classes remain until Minecraft exits. Closing only the controller does not stop Penguin.

**Validation:** the revised 1.9.19 build passed all 319 automated tests and loaded successfully in Lunar Fabric 1.21.11. The combined selector's four choices and the default OFF turning switch were checked in-game. A full in-world shattercube run remains unverified.

The included README.txt covers clicker input, profiles, synchronization, removal, compatibility and other features. SHA256SUMS.txt contains the Windows ZIP checksum.
