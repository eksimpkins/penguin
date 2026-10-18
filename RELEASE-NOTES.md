# Penguin 1.9.22 — Lunar preview

Download **Penguin-Lunar-1.9.22-Windows.zip** below and extract the entire ZIP. Keep Penguin.exe, app and runtime together. Java is included.

## Changes

- **Mining-cycle completion alert:** open **Mining > Gen Mining > Alerts > Cycle finished**. The alert defaults **ON at 100%** and has its own toggle, **0–200% volume** and **Test** button. It sounds once after the fourth distinct block finishes, including while tabbed out. It does not require verification or other alerts. Cancelling or interrupting a cycle does not play the completion sound.
- **Slower, smoother 90-degree turns:** both the mining cycle and passive prismarine turn use a gradual start and gentle stop over about **1.8 seconds in foreground gameplay**. Pitch stays unchanged and the turn finishes at exactly 90 degrees. Background timing can vary if game ticks are throttled.
- **Background behavior is preserved:** start a cycle separately in each game window. Switching apps or game instances does not cancel a cycle. Manual key/button presses, mouse movement or scrolling directed to that game cancel its cycle; manually opening a game menu stops it too. Initial-toggle presses, held-toggle repeats, releases alone and app-switch gestures such as Alt+Tab remain exceptions.

Choose the mining-cycle toggle in **Settings**; it starts **Unbound**. Only **plain prismarine** counts as a finished block. Sea lantern (**50 remaining**), dark prismarine (**25**) and prismarine bricks (**10**) are warning stages. Four distinct completions produce three turns. The cycle does not require the passive **Tab in at** or **Turn 90 degrees at prismarine** settings. **General > Message Alerts** remains independent of Gen Mining.

## Updating

Restart Minecraft once to clear the old loaded code, then load this version with Penguin.exe. Existing settings and bindings are preserved. Update every window sharing a settings folder together. Shared settings use **format 6** and profile exports use **format 8**, requiring **1.9.22**. Older shared settings migrate automatically; profile formats **1–7** still import. Older settings and profiles default the completion alert to ON at 100%. Profile import stops any running cycle and leaves passive tab-in and turning disabled.

Requires Windows x64, Lunar Fabric 1.21.11 and Fabric API. On first use, fully close Lunar including its tray icon, open Penguin.exe to prepare attachment, then launch the game and choose Load Penguin. K opens the menu. Stop Penguin disables its effects while Minecraft remains open; loaded classes remain until Minecraft exits. Closing only the controller does not stop Penguin.

**Validation:** version 1.9.22 built successfully; all 382 automated tests passed. Live checks of the completion alert and slower turns remain pending.

The included README.txt covers controls, profiles, synchronization and troubleshooting. SHA256SUMS.txt contains the Windows ZIP checksum.
