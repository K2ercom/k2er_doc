# Frequently Asked Questions

## [Debugging Process](https://docs.qq.com/mind/DVmxYcEpGQWhiRHFL) 

## [Activation-related FAQ](/activation.md)

## How to Connect Gamepad and Keyboards/Mice

K2er supports the vast majority of gamepads and keyboards/mice on the market, including Android handheld devices with built-in gamepad.

* **Bluetooth connection**: If your gamepad or keyboard/mouse supports Bluetooth, go to your phone's Bluetooth settings and pair these devices directly via Bluetooth.

* **Docking station connection**: If your gamepad or keyboard/mouse is wired or only has a USB adapter, use a docking station to connect. Ensure the docking station is powered, or it won’t be able to drive multiple devices.

```bash
[Phone] ----Cable--- [Docking Station] ---Cable---- [Gamepad, Keyboard/Mouse]
```

> **Note 1**: Some gamepads default to `simulating mouse events`. In this case, you need to switch the gamepad's connection mode to `Native Android HID Mode`, `PC Mode (Xbox)`, `PS Mode`, or `NS Mode (Switch)`.

> **Note 2**: Some devices may not be recognized due to `insufficient power supply`. Please use a docking station with power supply function.

> **Note 3**: K2er supports `multiple device mappings simultaneously`: such as gamepad + mouse, keyboard + mouse + gamepad, or gamepad + gamepad.

## Cannot Find the `Floating Window` in the Game

1. Check if the game has been added to K2er.

2. In your phone’s `Game Mode` (sometimes called `Game Space`), remove the game from the `Game List`.

> Add a non-game app to K2er to see if the floating window appears.

## The `Floating window` disappears automatically.

During gameplay, if the `Floating window` disappears, it usually means K2er was terminated by the Android OS.

1. Grant K2er notification permission.

2. Lock K2er in the current task list to reduce the chance of being killed.

3. Battery optimization whitelist: Set K2er to `No restrictions`.

4. Background running permission: Allow K2er to run continuously in the background.

5. Auto start permission

6. Remove the game from the `Game Mode` (sometimes called `Game Space`) game list on your phone.

7. Some phones have a `Game Acceleration` feature during gameplay, such as RedMagic's Turbo Mode. Please disable it.

> In `Game Mode` or `Game Acceleration`, K2er, as a background application, is prioritized for termination by the system.

## Unable to read the Shortcut (Record Key)

When trying to read a shortcut, pressing keyboard, mouse, or gamepad buttons has no effect. Please:

1. Ensure your keyboard, mouse, or gamepad can input on the phone's home screen or in a web browser.

2. In the device management section of the K2er main interface, check your input device.

3. If the gamepad has multiple modes, switch to one of these modes: `Android HID` / `XBOX PC` / `PS` / `NS`.

4. Restart your phone and try again.

## Key Presses Are Not Working, Including Mouse

1. For `Xiaomi`/`Redmi`/`Black Shark`/`POCO` phones, go to `Developer Options` -> `USB Debugging (Security Settings)`.

> Note: Enable `USB Debugging (Security Settings)`. This option must be enabled to simulate finger touches. If it's still not working, restart your phone.

2. For the K2er desktop version: ensure the computer's input method is set to English.

3. In the K2er phone settings, try `Restart Activation Service`.

4. Restart your phone and try again.

5. If none of the above works, it might be due to your phone’s `Game Mode`. Remove the game from `Game Mode` and try again.

## How to Use the PS5 Controller's Touchpad

In the K2er device management section, do not check the `DualSense Touchpad` option. This way, K2er will not hijack your touchpad, and it will continue to function as a mouse. Note that a few games do not support mouse clicks.

## How to Control the Character's View with a Mouse in Shooting Games (Hide Mouse Cursor)

When configuring the key bindings, add an `Aiming Mode`, which simulates the finger controlling the character’s view. The default shortcut is `Middle Mouse Button`.

> Note: Generally, place `Aiming Mode` on the right side of the screen, and avoid placing it in areas with pop-up windows.

## Camera Automatically Moves in One Direction When Aiming with the Gamepad's Right Stick

In the detailed settings for the right stick, increase the `Dead Zone`.

## How to Use Combination Keys

K2er supports two types of combination keys.

* Mod+Key: Hold down the Mod key, then press the Key, for example, `Ctrl+1`, `L1+A`.
   - Keyboard Mod keys: `Ctrl`, `Shift`, `Alt`, `Win`, `↑`, `←`, `↓`, `→`
   - Gamepad Mod keys: `L1`, `L2`, `L3`, `R1`, `R2`, `R3`, `Select`, `Start`, `Mode`
   
* Key1&Key2: Press any two keys simultaneously, for example, `A&B`, `L1&L2`.

## TV Mode Resolution Change Not Effective

**v0.2.141** introduced TV mode, which allows changing the resolution on phones/tablets. However, for OPPO/Realme/OnePlus devices, the "Disable Permission Monitoring" switch needs to be enabled for the changes to take effect.

> Developer Options -> turn on `[Disable Permission Monitoring]`

## Mapper Doc

| Mapper             | Keyboard ⌨️ | Mouse 🖱️ | Gamepad 🎮  |
|------------------|---------|---------|---------|
| [Tap](/mappings/tap.md) |     ✅   |     ✅   |   ✅    |
| [Dpad](/mappings/dpad.md) | ✅       |         | ✅       |
| [Swipe](/mappings/swipe.md) |  ✅      | ✅      | ✅      |
| [Macro](/mappings/macro.md) |  ✅      | ✅      | ✅      |
| [Charge up 4-way swipe](/mappings/fourwayswipe.md)  | ✅      | ✅      | ✅      |
| [Dpad (Stick)](/mappings/dpadstick.md) |      |      | ✅      |
| [Camera stick](/mappings/camerapanstick.md) |      |      | ✅      |
| [FreeLook (Stick)](/mappings/freelookstick.md) |       |      | ✅      |
| [MOBA Skill (Stick)](/mappings/mobastick.md) |      |      | ✅      |
| [Virtual Mouse (Stick)](/mappings/stickmouse.md) |      |      | ✅      |
| [Aiming Mode](/mappings/aiming.md) |  ✅      | ✅      |       |
| [FreeLook (Small Eye)](/mappings/freelook.md) |  ✅      | ✅      |       |
| [Recoil Control](/mappings/recoil.md) |  ✅      | ✅      |       |
| [Right Button Move](/mappings/rightbuttonmove.md) |       | ✅      |       |
| [MOBA Skill](/mappings/moba.md)  | ✅      | ✅      |       |
| [MOBA Skill (Dpad)](/mappings/mobadpad.md)  | ✅      |      |       |
| [MOBA Cancel](/mappings/mobacancel.md) | ✅      | ✅      | ✅      |

