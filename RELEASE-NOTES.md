# Penguin 1.9.20 — Lunar preview

Download **Penguin-Lunar-1.9.20-Windows.zip** below and extract the entire ZIP. Keep Penguin.exe, app and runtime together. Java is included.

## Changes

- **Independent Message Alerts:** the new **General > Message Alerts** module has its own toggle, volume and Test button. It works with Gen Mining disabled; existing message-alert settings are preserved.
- **Configurable mining-circle toggle:** choose a key in **Settings**; it defaults to **Unbound**. Aim at the first shattercube center block during focused gameplay and press your chosen toggle. Penguin holds mining until plain prismarine marks completion, releases mining for an eased 90-degree right turn, then holds mining on the next block. It stops after four distinct finished blocks, with three turns.
- **Immediate stop controls:** the toggle again, F8, Escape, any open menu, or loss of game focus stops the circle and releases its mining input. The cycle never opens or closes Escape to keep mining.
- **Smoother passive turns:** the separate automatic 90-degree setting now eases in and out over about a second, preserving pitch.
- **Stable block detection:** blocks crossed during the turn do not trigger an alarm or advance the mining cycle. Detection resumes after the turn settles.
- **Existing controls stay together:** open **Mining > Gen Mining > Actions**. **Tab in at** offers **Not at all**, **Sea lantern**, **Prismarine** and **After 4 blocks** for the existing Escape-menu behavior. Passive turning remains a separate switch and defaults **OFF**. Neither setting is required for the mining circle.

Only **plain prismarine** counts as a finished block. Sea lantern (**50 remaining**), dark prismarine (**25**) and prismarine bricks (**10**) are warning stages. Actions remain independent of alarm switches and volumes. Running progress stays local and is not saved or shared in profiles.

## Updating

Restart Minecraft once to clear the old loaded code, then load this version with Penguin.exe. Existing settings are preserved. Update every window sharing a settings folder together. Shared settings use **format 5** and profile exports use **format 7**, requiring **1.9.20**. Older shared settings migrate automatically; profile formats **1–6** still import. Existing installs start with the mining-cycle key unbound. Profile import stops any running cycle and leaves passive tab-in and turning disabled.

Requires Windows x64, Lunar Fabric 1.21.11 and Fabric API. On first use, fully close Lunar including its tray icon, open Penguin.exe to prepare attachment, then launch the game and choose Load Penguin. K opens the menu. Stop Penguin disables its effects while Minecraft remains open; loaded classes remain until Minecraft exits. Closing only the controller does not stop Penguin.

**Validation:** version 1.9.20 built successfully and passed all 358 automated tests. Live in-game checks of the new cycle and configurable key remain pending.

The included README.txt covers controls, profiles, synchronization and troubleshooting. SHA256SUMS.txt contains the Windows ZIP checksum.

