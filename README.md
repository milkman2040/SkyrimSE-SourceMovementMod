# SourceMovement

Source-style momentum, air strafing, and bunny hopping for **Skyrim Special Edition — Steam runtime 1.6.1170.0**.

**[Download the mod](https://github.com/ScuffedMilkman/SkyrimSE-SourceMovementMod/releases/latest)** · **[Report an issue](https://github.com/ScuffedMilkman/SkyrimSE-SourceMovementMod/issues)**

Download the `SourceMovement-…-Skyrim-1.6.1170.zip` release asset and install it with your mod manager. GitHub's automatic “Source code” downloads are not the installable mod.

## Features

- Preserve horizontal momentum in the air and gain speed through strafing and mouse turns.
- Hold **Space** to automatically hop.
- Enable **Jump Boost** to add 0–100 speed units per takeoff along your current movement direction.
- Set a maximum horizontal speed from **300 to 2,500 units/sec**.
- Optionally limit jump height to Skyrim's normal height or disable fall damage while SourceMovement is active.
- Customize a speedometer's size, position, font, color, and underline.
- Show a WASD/Space keyboard overlay with adjustable size, opacity, and position.
- Configure everything through **SKSE Menu Framework**, including a master checkbox and rebindable toggle key.

Movement changes and overlays are active only in first person with the mod enabled. Third-person movement remains native. No ESP or replacement HUD is included.

## Requirements

| Dependency | Required version or purpose |
| --- | --- |
| Skyrim Special Edition (Steam) | **1.6.1170.0 only** |
| [SKSE64](https://skse.silverlock.org/) | **2.2.6 for Steam 1.6.1170**; select the matching archived build if necessary |
| [Address Library for SKSE Plugins](https://www.nexusmods.com/skyrimspecialedition/mods/32444) | Anniversary Edition package containing the 1.6.1170 database |
| [SKSE Menu Framework 3](https://www.nexusmods.com/skyrimspecialedition/mods/120352) | Required for the settings pages; integration tested with 3.13-Hotfix2 |
| [ImGui Icons](https://www.nexusmods.com/skyrimspecialedition/mods/114790) | Required by Menu Framework 3.15 and later |

Install each dependency's own requirements. Movement can run with defaults or saved settings without Menu Framework. Other Skyrim runtimes, GOG, and VR are not supported by this build. No additional movement, animation, race, or HUD mod is required.

## Installation

1. Install the dependencies for runtime 1.6.1170.
2. Download the installable ZIP from [Releases](https://github.com/ScuffedMilkman/SkyrimSE-SourceMovementMod/releases/latest).
3. Disable or remove any older SourceMovement installation, then install and enable the new ZIP in your mod manager.
4. Launch Skyrim through SKSE and load a save or start a game.
5. Switch to first person. SourceMovement starts enabled; **F8** toggles it by default.

Use Menu Framework's configured menu key and open **Source Movement** to find **Settings**, **Speedometer**, and **Keyboard Overlay**.

## Defaults and controls

| Setting | Default |
| --- | --- |
| Mod | Enabled after loading a save or starting a game |
| Toggle key | F8 |
| Fall damage | Enabled; checked means damage is enabled |
| Auto hop | Enabled; hold Space |
| Limit jump height | Disabled; existing jump-height effects are allowed |
| Maximum speed | 1,500 units/sec |
| Jump Boost | Enabled, 30 units/sec added per takeoff |
| Speedometer | Disabled; size 70%, X 50%, Y 70%, Console font, size 20, cyan, underline on |
| Keyboard overlay | Disabled; size 60%, opacity 75%, X 30%, Y 75% |

Jump Boost respects the maximum speed and does not propel stationary jumps horizontally. The keyboard overlay displays physical WASD and Space keys, regardless of gameplay bindings. Turning off an overlay stops its display tracking.

## Saved settings and reset

Settings save to `SKSE/Plugins/SourceMovementSettings.ini` beside the installed DLL. The release ZIP contains clean factory defaults. Old settings stored in Documents are not read.

To reset, close Skyrim and reinstall the ZIP, replacing the INI. In MO2, choose **Replace** for the same mod entry. If Overwrite or a higher-priority mod supplies another copy of the INI, remove that specific override as well. Profiles sharing the same installed mod also share its settings.

Reinstalling or updating while replacing the INI resets preferences. Back up that file first if you want to retain your settings.

## Troubleshooting

- Confirm the game executable is **1.6.1170.0**, SKSE matches it, and Address Library includes its database.
- Confirm only one version of SourceMovement is enabled.
- For missing settings pages, check Menu Framework and its dependencies.
- For unexpected settings, reset the INI and check mod-manager file conflicts.
- The log is in your Documents folder at `My Games/Skyrim Special Edition/SKSE/SourceMovement/SourceMovement.log`.

Animation synchronization during auto-hop, including the airborne footstep fix, still needs further in-game validation. The current settings save/reset behavior also needs verification through mod-manager file redirection. Compatibility with every animation or movement mod has not been established.

When reporting an issue, include the mod version, game runtime, steps to reproduce, and relevant log lines. Remove personal paths or other private information before posting.

## Uninstall

Close Skyrim and disable or remove the mod through your mod manager. Optionally remove its remaining log from Documents.

## Package contents

The installable ZIP contains the DLL, factory-default INI, installation guide, and required library license notices. It includes no personal preferences, profile data, diagnostic captures, or development files. This repository provides the download page and documentation; source code is not included.
