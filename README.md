# GTA: San Andreas PS2 Modern Controls Patch

A PCSX2 `.pnach` controls patch for **Grand Theft Auto: San Andreas** on PlayStation 2.

This patch modernizes the PS2 control layout by remapping vehicle acceleration/braking and several context-specific controls while keeping the original game ISO untouched.

The patch automatically changes behavior when CJ enters or exits vehicles. You do **not** need to manually switch controller profiles or control schemes in PCSX2.

## Why This Patch Exists

The original PS2 version of *GTA: San Andreas* was designed around the DualShock 2 controller, which had pressure-sensitive face buttons. On original hardware, the Cross and Square buttons could detect how hard they were being pressed, allowing for more gradual acceleration and braking.

Modern controllers usually place analog acceleration and braking on the trigger buttons instead. When playing the PS2 version through PCSX2 with a modern controller, the original Cross/Square vehicle controls can feel awkward. Depending on the controller, adapter, or input setup, driving may behave more like the car is always going “pedal to the metal.”

This patch helps preserve the feel and playability of the PS2 version by moving acceleration and braking-style controls to the shoulder/trigger positions used by modern controllers, while keeping the original game ISO untouched.

## Target Version

This patch is for:

| Item | Value |
|---|---|
| Game | Grand Theft Auto: San Andreas |
| Platform | PlayStation 2 |
| Region | NTSC-U |
| Game ID | SLUS-20946 |
| CRC | 399A49CA |
| Emulators tested | PCSX2, AetherSX2, ARMSX2 |

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
- Automatically change control behavior when entering or exiting vehicles
- Provide optional modules that can be enabled or disabled from PCSX2’s cheat menu

## Included Versions

Choose one of the included `.pnach` files.

| File | Description |
|---|---|
| `399A49CA_Basic_Cross_and_R2_and_Square_and_L2_Swap_Plus_Remaps.pnach` | Recommended version. Includes the basic Cross/R2 and Square/L2 vehicle swap plus optional context-specific modules. |
| `399A49CA_Basic_Cross_and_R2_and_Square_and_L2_Swap_First_Working_Version.pnach` | First working version. Only swaps Cross with R2 and Square with L2 while in a vehicle. Simpler and less invasive. |

## Installation

1. Download the `.pnach` file you want to use.
2. Rename the chosen file to:

```text
399A49CA.pnach
```

3. Place it in your PCSX2 `cheats` folder.

Depending on your PCSX2 setup, the cheats folder is usually found in one of these locations:

```text
Documents\PCSX2\cheats
```

or inside your portable PCSX2 folder:

```text
PCSX2\cheats
```

4. Start GTA: San Andreas.
5. In PCSX2, enable cheats.
6. Open the cheats list and enable the modules you want.

## Cheat Modules

The following modules apply to the recommended “Plus Remaps” version.

### 1 REQUIRED - Basic Vehicle Swap Core

This module is required for the optional modules to work.

In vehicles, it applies the basic modern-style swap:

```text
Physical R2     -> native Cross
Physical L2     -> native Square
Physical Cross  -> native R2
Physical Square -> native L2
```

This makes R2/L2 behave more like modern accelerate/brake controls.

Leave this enabled while playing.

---

### 2 OPTIONAL - Universal In-Vehicle D-pad Radio/Look Controls

Applies to vehicles, including turreted/weaponized vehicles.

```text
Physical D-pad Up    -> native D-pad Down / next radio station
Physical D-pad Left  -> native L2 / look left
Physical D-pad Right -> native R2 / look right
Physical D-pad Down  -> native L2 + native R2 / look backward
```

---

### 3 OPTIONAL - Bicycle Special Controls

Applies to:

```text
BMX
Bike
Mountain Bike
```

Behavior:

```text
Physical R2 -> native Cross
Physical L2 -> native Square
Physical Cross still works
Physical Square still works
```

This keeps bicycles usable while moving acceleration/braking behavior toward the shoulder buttons.

Enable module 2 separately if you want the universal D-pad look/radio behavior.

---

### 4 OPTIONAL - Aircraft Special Controls

Applies to aircraft and helicopters.

This module remaps aircraft controls so shoulder and face-button behavior is more modernized.

General behavior:

```text
Physical Square -> native L1
Physical Cross  -> native R1
Physical R2     -> native Cross
Physical L2     -> native Square
Physical R1     -> native R2
Physical L1     -> native L2
```

---

### 5 OPTIONAL - Alternate Controls for Cars and Normal Ground Vehicles

Applies alternate controls to cars and normal ground vehicles.

Motorcycles, ATV, boats, and hovercraft are not included unless options 6 and/or 7 are also enabled.

Turreted or weaponized vehicles are excluded from this alternate-control group so their vehicle weapon and secondary-fire controls stay closer to the stock/basic layout.

Excluded vehicles:

```text
407 Fire Truck
430 Predator
432 Rhino
544 Fire Truck ladder variant
564 RC Tiger
601 S.W.A.T.
```

---

### 6 OPTIONAL - Include Motorcycles and ATV in Alternate Controls

Requires option 5.

This extends the option 5 alternate controls to motorcycles and ATV-style vehicles.

Leave this disabled to keep motorcycles and ATV on the basic vehicle layout.

---

### 7 OPTIONAL - Include Boats and Hovercraft in Alternate Controls

Requires option 5.

This extends the option 5 alternate controls to boats and the Vortex hovercraft.

The Predator is excluded because it has built-in guns.

---

### 8 OPTIONAL - Auto Fire Add-on for Alternate Controls

Requires option 5.

This is an add-on for the alternate vehicle controls. It is no longer a separate “choose this or that” alternate-control option.

With option 8 enabled, vehicles routed through option 5, 6, and/or 7 use Auto Fire behavior.

Auto Fire behavior:

```text
Physical R1 -> native R2 + Circle
Physical L1 -> native L2 + Circle
```

Use option 5 by itself for alternate controls without Auto Fire.

Use option 5 plus option 8 for alternate controls with Auto Fire.

---

### 9 OPTIONAL - On-Foot Shoulder Swap

This module changes only on-foot shoulder behavior.

Current behavior:

```text
Physical L1 -> native L2
Physical R1 -> native R2
Physical L2 -> native L1
Physical R2 -> native R1
```

## Suggested Setup

A good default setup is:

### Enabled

```text
1 REQUIRED - Basic Vehicle Swap Core
2 OPTIONAL - Universal In-Vehicle D-pad Radio/Look Controls
3 OPTIONAL - Bicycle Special Controls
4 OPTIONAL - Aircraft Special Controls
5 OPTIONAL - Alternate Controls for Cars and Normal Ground Vehicles
6 OPTIONAL - Include Motorcycles and ATV in Alternate Controls
8 OPTIONAL - Auto Fire Add-on for Alternate Controls
9 OPTIONAL - On-Foot Shoulder Swap
```

### Optional

```text
7 OPTIONAL - Include Boats and Hovercraft in Alternate Controls
```

Boats can feel better with either the basic layout or the alternate layout depending on preference.

### Auto Fire

To use alternate controls without Auto Fire:

```text
Enable option 5
Disable option 8
```

To use alternate controls with Auto Fire:

```text
Enable option 5
Enable option 8
```

## Known Limitations

### Menus Are Not Fully Guarded

This version is based on the most stable gameplay build.

Some menu screens may still receive remapped inputs, especially if shoulder buttons are used for menu navigation, zoom, or page switching.

Menu-safe experimental builds were tested, but they could cause side effects such as:

```text
Temporary control dropouts while driving
Delayed remap activation after entering a vehicle
Brake-light/controller-state flicker
```

Because of that, the stable release does not include the experimental menu guard.

## Mod Compatibility Notes

This patch has also been tested with **PS2 Project Kaizo 2.2**, which is based on the same NTSC-U 1.03 version of *GTA: San Andreas*.

Keep in mind that some Project Kaizo shortcuts use the direction buttons. If you are in a vehicle and have **Option 2 - Universal In-Vehicle D-pad Radio/Look Controls** enabled, the D-pad does not behave exactly like stock while driving.

With option 2 enabled, the following inputs are changed while in a vehicle:

- D-pad Left also sends the vehicle look-left input.
- D-pad Right also sends the vehicle look-right input.
- D-pad Down sends both look-left and look-right for rear view.
- D-pad Up is changed for radio station behavior.

Because of this, Project Kaizo shortcuts that rely on the direction buttons may not work correctly while you are in a vehicle.

Workarounds:

- Turn off option 2.
- Get out of the vehicle before using the shortcut.
- Use the shortcut while on foot.

This is not a bug with PS2 Project Kaizo or the base patch. It is a side effect of combining Project Kaizo’s D-pad shortcuts with this patch’s optional in-vehicle D-pad remaps.

### PCSX2 Only

This release is currently intended for PCSX2.

Real PS2 hardware / OPL / PS2RD support is not confirmed.

A real-hardware version may be possible later, but it should be considered experimental unless tested on actual PS2 hardware.

### Version-Specific

This patch is built for:

```text
SLUS-20946
CRC 399A49CA
```

It will not automatically work on other regions or revisions.

## Troubleshooting

### The Cheat Does Not Appear in PCSX2

Make sure the file is named exactly:

```text
399A49CA.pnach
```

and that it is in the PCSX2 `cheats` folder.

Also make sure cheats are enabled in PCSX2.

### The Controls Do Not Change

Check that option 1 is enabled.

Most optional modules depend on the required core module.

### Motorcycles, Boats, or Auto Fire Do Not Change

Options 6, 7, and 8 depend on option 5.

Use this setup:

```text
5 ON  = alternate controls for cars and normal ground vehicles
6 ON  = also include motorcycles and ATV
7 ON  = also include boats and hovercraft
8 ON  = add Auto Fire to the alternate controls
```

### Menus Behave Oddly

This can happen because this patch prioritizes stable gameplay controls over menu-specific guarding.

Disable optional modules temporarily if a menu screen becomes difficult to use.

### Project Kaizo Shortcuts Do Not Work in Vehicles

Turn off option 2 or use the shortcut while on foot.

Option 2 changes D-pad behavior while driving, which can interfere with Project Kaizo shortcuts that use the direction buttons.

## Credits

Controls design, testing, and project release by **Zeroable**.

Patch assembly/debugging assistance from **ChatGPT**.

Portions of the controller hook structure were generated with **PS2 Controller Remapper by pelvicthrustman**.

## Disclaimer

This is an unofficial fan-made controls/accessibility/preservation patch.

This project is not affiliated with, endorsed by, or sponsored by Rockstar Games, Take-Two Interactive, Sony, or the PCSX2 project.

Grand Theft Auto: San Andreas is property of Rockstar Games / Take-Two Interactive.

This repository does not contain any game files, game assets, disc images, BIOS files, or copyrighted Rockstar/Take-Two content.

## License

This project is released under the MIT License.

See `LICENSE` for details.
