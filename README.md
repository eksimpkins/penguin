# Penguin for Lunar

Penguin is a Windows x64 controller and mod for **Lunar Client with Minecraft 1.21.11, Fabric and Fabric API**. Load or stop Penguin from its controller while Minecraft stays open.

## Download

**[Download Penguin 1.9.10 for Windows](https://github.com/eksimpkins/penguin/releases/download/v1.9.10/Penguin-Lunar-1.9.10-Windows.zip)**

Download `Penguin-Lunar-1.9.10-Windows.zip` from the [latest release](https://github.com/eksimpkins/penguin/releases/latest). GitHub's automatic **Source code** ZIP does not contain the ready-to-run application. Java is included in the Windows download.

## First launch

1. Extract the entire ZIP. Keep `Penguin.exe`, `app` and `runtime` together inside the extracted `Penguin` folder.
2. Fully close Lunar Client, including its tray icon.
3. Open `Penguin.exe`. It enables Lunar's built-in **Enable Attach** setting and saves a backup of the original launcher settings. If Lunar was still open, close it and choose **Prepare Lunar**.
4. Launch Lunar **Fabric 1.21.11** with **Fabric API** available in the profile.
5. Click **Refresh**, select your game, then **Load Penguin**. Keep Minecraft visible while textures reload.

Do not install a second copy of Penguin in the mods folder. When updating from an older Penguin build, restart Minecraft once before loading the new version.

## Controls

- **K:** open Penguin's menu while in a world. At Minecraft's main menu, use **Open menu** in the controller.
- **J:** toggle all player nametags and tracers, including friends. Friend appearance and label/line choices are preserved.
- **F8:** stop both clickers and aim tracking during gameplay.
- **] / F7:** default left/right clicker toggles; change these in Settings.
- **Stop Penguin:** stop the mod while Minecraft remains open. You can load it again in the same session.

For repeated clicks, enable a clicker, close the menu, then release and hold that mouse button. A fresh press is also required after changing its CPS or returning from a menu or another window. Close any older standalone Penguin Clicker before using this version.

Closing the controller window does not stop the mod. **Stop Penguin** disables its effects and input handling; already loaded Java classes remain until Minecraft exits.

## New in 1.9.10

- Friend additions use consistent account-name matching; adding a saved OFF friend enables it again.
- Friend label and tracer styling is resolved when drawing, and embedded name formatting cannot override the selected text color.

## Also included

- **Settings > Menu scale:** 50–150%, with a reset button and automatic fitting for small windows.
- **Visuals > No Debuff:** one toggle for blindness fog/sky obstruction and nausea distortion/overlay. Actual status effects remain.
- **Visuals > Constant FOV:** keeps the world view at the FOV selected in Minecraft, preventing movement/effect zoom. Hand/item projection is unchanged. Both controls restore normal rendering when switched off.
- **Clues > Clue Scrolls:** chest sorting, optional tier grouping, and collecting matches using hotbar slot 1, with adjustable click delay.
- **Profiles:** export and import shareable settings files, optionally including saved friend names. Import backs up current settings and leaves automation off until enabled.

Profiles from 1.9.8 still import correctly. New profiles include both visual toggles and require 1.9.9 or newer.

## Included features

- Mining verification, auto-sell and individual alerts with volume controls.
- Block tracers with a searchable block picker and a Vault preset.
- Player nametags and tracers, offscreen indicators, guard/NPC filters, and independent friend appearance settings.
- Saved friends with individual on/off switches.
- Configurable left/right Windows clickers and smooth aim assist with target filters.
- **Aim height:** adjust from legs to head, with **Chest (72%)** as the default and a reset button. Enable **Aim vertically** for height correction.

## Multiple Lunar windows

Windows using the same game folder share the saved settings file, but each keeps its own loaded settings. Changes do not currently sync live; the last window to save can overwrite the file. This update does not add synchronization.

## Compatibility and validation

This is a preview for the tested Lunar Fabric 1.21.11 configuration; later Lunar updates may require changes. The release passed **193 automated tests**, and clicker startup was checked in Lunar. Aim smoothing was confirmed in use; the reported intermittent friend-color issue still needs live confirmation, as does Constant FOV against Trap. Adjustable aim placement and click delivery also need normal play testing.

See the included `README.txt` for the full settings and troubleshooting guide. The project uses the [MIT license](LICENSE).
