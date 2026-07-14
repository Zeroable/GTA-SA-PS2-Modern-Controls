# GTA: San Andreas PS2 Modern Controls Patch

A PCSX2 `.pnach` controls patch for **Grand Theft Auto: San Andreas** on PlayStation 2.

This patch modernizes the PS2 control layout by remapping vehicle acceleration/braking and several context-specific controls while keeping the original game ISO untouched.

## Target Version

This patch is for:

- Game: **Grand Theft Auto: San Andreas**
- Platform: **PlayStation 2**
- Region: **NTSC-U**
- Game ID: **SLUS-20946**
- CRC: **399A49CA**
- Emulator: **PCSX2**

Other versions, regions, Greatest Hits/3.00 builds, PAL releases, and modified ISOs are not currently supported.

## What This Is

This is a PCSX2 cheat/patch file that remaps controller inputs at runtime.

It does **not**:

- Modify the game ISO
- Include game files
- Include Rockstar/Take-Two assets
- Require a patched disc image

It does:

- Use PCSX2’s `.pnach` cheat system
- Remap controller inputs while the game is running
- Provide optional modules that can be enabled or disabled from PCSX2’s cheat menu

## Recommended File

Use the one of the two included files:

399A49CA_Basic_Cross_and_R2_and_Square_and_L2_Swap_Plus_Remaps.pnach

or

The first working version that only swaps Cross with R2, and Square with L2 when in any vehicle.
399A49CA_Basic_Cross_and_R2_and_Square_and_L2_Swap_First_Working_Version.pnach

Place it in your PCSX2 cheats folder.

Depending on your PCSX2 setup, the cheats folder is usually found in one of these locations:

Documents\PCSX2\cheats

or inside your portable PCSX2 folder:

PCSX2\cheats

Then enable cheats in PCSX2.

Installation
Download the .pnach file.
Rename it to:
399A49CA.pnach
Place it in your PCSX2 cheats folder.
Start GTA: San Andreas.
In PCSX2, enable cheats.
Open the cheats list and enable the modules you want.
Cheat Modules
1 REQUIRED - Basic vehicle swap core

This module is required for the optional modules to work.

In vehicles, it applies the basic modern-style swap:

Physical R2 -> native Cross
Physical L2 -> native Square
Physical Cross -> native R2
Physical Square -> native L2

This makes R2/L2 behave more like modern accelerate/brake controls.

Leave this enabled while playing.

2 OPTIONAL - Universal in-vehicle D-pad radio/look controls

Applies to vehicles, including the Rhino.

Physical D-pad Up    -> native D-pad Down / next radio station
Physical D-pad Left  -> native L2 / look left
Physical D-pad Right -> native R2 / look right
Physical D-pad Down  -> native L2 + native R2 / look backward
3 OPTIONAL - Bicycle special controls

Applies to:

BMX
Bike
Mountain Bike

Behavior:

Physical R2 -> native Cross
Physical L2 -> native Square
Physical Cross still works
Physical Square still works

This keeps bicycles usable while moving acceleration/braking behavior toward the shoulder buttons.

Enable module 2 separately if you want the universal D-pad look/radio behavior.

4 OPTIONAL - Aircraft special controls

Applies to aircraft and helicopters.

This module remaps aircraft controls so shoulder and face-button behavior is more modernized.

General behavior:

Physical Square -> native L1
Physical Cross  -> native R1
Physical R2     -> native Cross
Physical L2     -> native Square
Physical R1     -> native R2
Physical L1     -> native L2
5 OPTIONAL - Alternate car/motorcycle controls - No Auto Fire

Applies to cars, motorcycles, boats, and other non-bicycle/non-aircraft/non-Rhino vehicles.

This changes the control layout more aggressively than the basic swap.

Do not enable this at the same time as module 6 unless you intentionally want module 6 to win.

6 OPTIONAL - Alternate car/motorcycle controls - With Auto Fire

Same idea as module 5, but adds auto-fire style behavior.

Useful for drive-by style behavior where a shoulder button can output a weapon/fire combo.

Do not enable this at the same time as module 5 unless you intentionally want this module to win.

7 OPTIONAL - On-foot shoulder swap

This module changes only on-foot shoulder behavior.

Current behavior:

Physical L1 -> native L2
Physical R1 -> native R2
Physical L2 -> native L1
Physical R2 -> native R1

The older D-pad remaps were removed from this version.

Suggested Setup

A good default setup is:

Enabled:
1 REQUIRED - Basic vehicle swap core
2 OPTIONAL - Universal in-vehicle D-pad radio/look controls
3 OPTIONAL - Bicycle special controls
4 OPTIONAL - Aircraft special controls
6 OPTIONAL - Alternate car/motorcycle controls - With Auto Fire
7 OPTIONAL - On-foot shoulder swap

Disabled:
5 OPTIONAL - Alternate car/motorcycle controls - No Auto Fire

If you do not want auto-fire behavior, use module 5 instead of module 6.

Known Limitations
Menus are not fully guarded

This version is based on the most stable gameplay build.

Some menu screens may still receive remapped inputs, especially if shoulder buttons are used for menu navigation, zoom, or page switching.

Menu-safe experimental builds were tested, but they could cause side effects such as:

temporary control dropouts while driving
delayed remap activation after entering a vehicle
brake-light/controller-state flicker

Because of that, the stable release does not include the experimental menu guard.

PCSX2 only

This release is currently intended for PCSX2.

Real PS2 hardware / OPL / PS2RD support is not confirmed.

A real-hardware version may be possible later, but it should be considered experimental unless tested on actual PS2 hardware.

Version-specific

This patch is built for:

SLUS-20946
CRC 399A49CA

It will not automatically work on other regions or revisions.

Troubleshooting
The cheat does not appear in PCSX2

Make sure the file is named exactly:

399A49CA.pnach

and that it is in the PCSX2 cheats folder.

Also make sure cheats are enabled in PCSX2.

The controls do not change

Check that module 1 is enabled.

Most optional modules depend on the required core module.

Two modules conflict

Do not enable both alternate car/motorcycle modules unless you intentionally want the later one to override the earlier one.

Recommended:

Use either module 5 or module 6, not both.
Menus behave oddly

This can happen because this patch prioritizes stable gameplay controls over menu-specific guarding.

Disable optional modules temporarily if a menu screen becomes difficult to use.

Credits

Controls design, testing, and project release by Zeroable.

Patch assembly/debugging assistance from ChatGPT.

Portions of the controller hook structure were generated with PS2 Controller Remapper by pelvicthrustman.

Disclaimer

This is an unofficial fan-made controls/accessibility/preservation patch.

This project is not affiliated with, endorsed by, or sponsored by Rockstar Games, Take-Two Interactive, Sony, or the PCSX2 project.

Grand Theft Auto: San Andreas is property of Rockstar Games / Take-Two Interactive.

This repository does not contain any game files, game assets, disc images, BIOS files, or copyrighted Rockstar/Take-Two content.

License

This project is released under the MIT License.

See LICENSE for details.

Credits:
Controls design, testing, and release by Zeroable.
Patch assembly/debugging assistance from ChatGPT.
Portions of the controller hook structure were generated with PS2 Controller Remapper by pelvicthrustman.
