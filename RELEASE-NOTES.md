# Penguin 1.9.21 — Lunar preview

Download **Penguin-Lunar-1.9.21-Windows.zip** below and extract the entire ZIP. Keep Penguin.exe, app and runtime together. Java is included.

## Changes

- **Manual input cancels that game's mining cycle:** key or mouse-button presses, mouse movement and scrolling directed to that game stop its four-block cycle and release its mining input immediately. This also stops an ongoing turn. Manually opening a game menu stops it too.
- **Background mining across windows:** switching apps or game instances does not cancel a running cycle. Start a cycle separately in each game; each continues independently while you use another window. Alt+Tab and other app-switch gestures are exceptions to input cancellation, and input sent to another window does not stop this game's cycle.
- **Starting still works normally:** the initial mining-toggle press, held-toggle repeats and releases alone do not cancel the cycle. Choose the toggle in **Settings**; it remains **Unbound** by default.
- **Existing behavior is preserved:** the cycle holds mining, makes three smooth 90-degree turns, and stops after the fourth distinct finished block. **General > Message Alerts** remains independent of Gen Mining.

Only **plain prismarine** counts as a finished block. Sea lantern (**50 remaining**), dark prismarine (**25**) and prismarine bricks (**10**) are warning stages. The cycle does not require the passive **Tab in at** or **Turn 90 degrees at prismarine** settings. Running progress stays local and is not saved or shared.

## Updating

Restart Minecraft once to clear the old loaded code, then load this version with Penguin.exe. Existing settings and bindings are preserved. Update every window sharing a settings folder together. Shared settings still use **format 5** and profile exports use **format 7**, requiring **1.9.20 or later**. Older shared settings migrate automatically; profile formats **1–6** still import. Profile import stops any running cycle and leaves passive tab-in and turning disabled.

Requires Windows x64, Lunar Fabric 1.21.11 and Fabric API. On first use, fully close Lunar including its tray icon, open Penguin.exe to prepare attachment, then launch the game and choose Load Penguin. K opens the menu. Stop Penguin disables its effects while Minecraft remains open; loaded classes remain until Minecraft exits. Closing only the controller does not stop Penguin.

**Validation:** version 1.9.21 built successfully and passed all 375 automated tests. Live checks of input cancellation, background mining and the full cycle remain pending.

The included README.txt covers controls, profiles, synchronization and troubleshooting. SHA256SUMS.txt contains the Windows ZIP checksum.
