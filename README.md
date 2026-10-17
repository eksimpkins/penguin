# Penguin for Lunar

Penguin is a Windows x64 controller and mod for **Lunar Client with Minecraft 1.21.11, Fabric and Fabric API**. Load or stop Penguin from its controller while Minecraft stays open.

## Download

**[Download Penguin 1.9.13 for Windows](https://github.com/eksimpkins/penguin/releases/download/v1.9.13/Penguin-Lunar-1.9.13-Windows.zip)**

Download `Penguin-Lunar-1.9.13-Windows.zip` from the [latest release](https://github.com/eksimpkins/penguin/releases/latest). GitHub's automatic **Source code** ZIP does not contain the ready-to-run application. Java is included in the Windows download.

## First launch

1. Extract the entire ZIP. Keep `Penguin.exe`, `app` and `runtime` together inside the extracted `Penguin` folder.
2. Fully close Lunar Client, including its tray icon.
3. Open `Penguin.exe`. It enables Lunar's built-in **Enable Attach** setting and saves a backup of the original launcher settings. If Lunar was still open, close it and choose **Prepare Lunar**.
4. Launch Lunar **Fabric 1.21.11** with **Fabric API** available in the profile.
5. Click **Refresh**, select your game, then **Load Penguin**. Keep Minecraft visible while textures reload.

Do not install a second copy of Penguin in the mods folder. When updating from an older Penguin build, restart Minecraft once before loading the new version.

If a previous load reported **FAILED**, restart Minecraft once to clear the old loaded code, then load 1.9.13. Reopening only the controller does not clear that state. Your settings are preserved; no reset is needed.

## Controls

- **K:** open Penguin's menu while in a world. At Minecraft's main menu, use **Open menu** in the controller.
- **J:** toggle all player nametags and tracers, including friends. Friend appearance and label/line choices are preserved.
- **F8:** stop both clickers and aim tracking during gameplay.
- **] / F7:** default left/right clicker toggles; change these in Settings.
- **Stop Penguin:** stop the mod while Minecraft remains open. You can load it again in the same session.

For repeated clicks, enable a clicker, close the menu, then release and hold that mouse button. A fresh press is also required after changing its CPS or returning from a menu or another window. Close any older standalone Penguin Clicker before using this version.

Closing the controller window does not stop the mod. **Stop Penguin** disables its effects and input handling; already loaded Java classes remain until Minecraft exits.

## New in 1.9.13

- **Hold-C zoom compatibility:** while physically holding C in focused gameplay with no screen open, Constant FOV temporarily uses the normal game FOV so your existing zoom can work. Releasing C restores the FOV selected in Minecraft.
- Penguin does not add zoom, consume C or change its binding. This supports existing **hold-to-zoom on C**; remapped and toggle-style zoom are not covered.
- Normal movement and effect FOV changes can apply while C is held, including Trap's zoom effect.

## Retained from 1.9.12

- Fixed a Lunar loading failure caused by its extra FOV accessor, which could prevent Penguin from loading even when Constant FOV was OFF. Penguin now selects Minecraft's exact FOV method and leaves the accessor unchanged.
- The controller preserves the original failure details when a load fails instead of replacing them with a generic repeat-failure message.
- Existing settings and all 1.9.11 features remain included.

## From 1.9.11

- **Live settings sync:** saved settings and module switches update between upgraded windows using the same game/config folder.
- **Show '(behind)' text:** a shared toggle under Nametags and Friend Overlay, OFF by default. Edge labels and tracers continue to work normally.

## From 1.9.10

- Friend additions use consistent account-name matching; adding a saved OFF friend enables it again.
- Friend label and tracer styling is resolved when drawing, and embedded name formatting cannot override the selected text color.

## Also included

- **Settings > Menu scale:** 50–150%, with a reset button and automatic fitting for small windows.
- **Visuals > No Debuff:** one toggle for blindness fog/sky obstruction and nausea distortion/overlay. Actual status effects remain.
- **Visuals > Constant FOV:** keeps the world view at the FOV selected in Minecraft, preventing movement/effect zoom except while holding C during focused gameplay. Hand/item projection is unchanged. Both controls restore normal rendering when switched off.
- **Clues > Clue Scrolls:** chest sorting, optional tier grouping, and collecting matches using hotbar slot 1, with adjustable click delay.
- **Profiles:** export and import shareable settings files, optionally including saved friend names. Import backs up current settings and leaves automation off until enabled.

Profile formats 1 and 2, exported by 1.9.8 through 1.9.10, remain supported; their behind-text setting defaults OFF. New exports use format 3 and require 1.9.11 or newer.

## Included features

- Mining verification, auto-sell and individual alerts with volume controls.
- Block tracers with a searchable block picker and a Vault preset.
- Player nametags and tracers, offscreen indicators, guard/NPC filters, and independent friend appearance settings.
- Saved friends with individual on/off switches.
- Configurable left/right Windows clickers and smooth aim assist with target filters.
- **Aim height:** adjust from legs to head, with **Chest (72%)** as the default and a reset button. Enable **Aim vertically** for height correction.

## Multiple Lunar windows

Restart and load **1.9.13 in every participating window**. Games sharing the same game/config folder sync all saved settings, including module ON/OFF switches, normally within about **0.5 seconds while ticking**. Open menus update too; separate game/config folders remain independent.

Independent simultaneous edits merge, including changes to different friends. When windows change the same setting or friend, the last save wins for that change. Loading/stopping Penguin, selected targets and running operations stay local to each game. Changes to clicker controls require a fresh physical release/press; focused gameplay and a held button are still required.

The shared file is `config/penguin-live-settings.json`, initialized once from existing `namelines.json` and `cluesort.json` settings. It becomes the authoritative settings file. Versions before 1.9.11 do not participate in live sync.

## Compatibility and validation

This is a preview for the tested Lunar Fabric 1.21.11 configuration; later Lunar updates may require changes. Version 1.9.13 passed **220 automated tests**, including holding/releasing C, focus eligibility, unchanged hand projection and preserving the module setting. Live C-key zoom confirmation is still pending. The tests retain coverage for Lunar's duplicate FOV accessor, exact method selection, FOV restoration and retained-error reporting, plus the synchronization, profile and overlay checks. Version 1.9.12 loaded, stopped and loaded again successfully in a fresh Lunar Fabric 1.21.11 session, with the Windows clicker reporting ready. Multi-window sync in Lunar and the reported intermittent friend-color issue still need live confirmation, as does Constant FOV against Trap. Aim smoothing was confirmed in use; adjustable aim placement and click delivery also need normal play testing.

See the included `README.txt` for the full settings and troubleshooting guide. The project uses the [MIT license](LICENSE).
