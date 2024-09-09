# Frequently Asked Questions

## [Activation-related FAQ](activation.md)

## How to Connect Gamepad and Keyboards/Mice

K2er supports the vast majority of gamepads and keyboards/mice on the market, including Android handheld devices with built-in gamepad.

* Bluetooth connection: If your gamepad or keyboard/mouse supports Bluetooth, go to your phone's Bluetooth settings and pair these devices directly via Bluetooth.

* Docking station connection: If your gamepad or keyboard/mouse is wired or only has a USB adapter, use a docking station to connect. Ensure the docking station is powered, or it won’t be able to drive multiple devices.

```bash
[Phone] ----Cable--- [Docking Station] ---Cable---- [Gamepad, Keyboard/Mouse]
```

> Note: Some gamepads default to `simulating mouse events`. In this case, you need to switch the gamepad's connection mode to `Native Android Mode`, `PC Mode (Xbox)`, `PS Mode`, or `NS Mode (Switch)`.
> K2er supports multiple device mappings simultaneously: such as gamepad + mouse, keyboard + mouse + gamepad, or gamepad + gamepad.

## Cannot Find the `Floating Window` in the Game

1. Check if the game has been added to K2er.

2. In your phone’s `Game Mode` (sometimes called `Game Space`), remove the game from the `Game List`.

> Add a non-game app to K2er to see if the floating window appears.

## Key Presses Are Not Working, Including Mouse

1. For `Xiaomi`/`Redmi`/`Black Shark`/`POCO` phones, go to `Developer Options` -> `USB Debugging (Security Settings)`.

> Note: Enable `USB Debugging (Security Settings)`. This option must be enabled to simulate finger touches. If it's still not working, restart your phone.

2. For the K2er desktop version: ensure the computer's input method is set to English.

3. In the K2er phone settings, try `Restart Activation Service`.

4. Restart your phone and try again.

5. If none of the above works, it might be due to your phone’s `Game Mode`. Remove the game from `Game Mode` and try again.

## How to Control the Character's View with a Mouse in Shooting Games (Hide Mouse Cursor)

When configuring the key bindings, add an `Aiming Mode`, which simulates the finger controlling the character’s view. The default shortcut is `Middle Mouse Button`.

> Note: Generally, place `Aiming Mode` on the right side of the screen, and avoid placing it in areas with pop-up windows.

## Camera Automatically Moves in One Direction When Aiming with the Gamepad's Right Stick

In the detailed settings for the right stick, increase the `Dead Zone`.

## How to Use Combination Keys

K2er supports two types of combination keys.

* Mod+Key: Hold down the Mod key, then press the Key, for example, `Ctrl+1`, `L1+A`.
   - Keyboard Mod keys: Ctrl, Shift, Alt, Win, ↑←↓→
   - Gamepad Mod keys: L1, L2, L3, R1, R2, R3, Select, Start, Mode
   
* Key1&Key2: Press any two keys simultaneously, for example, `A&B`, `L1&L2`.

## How to Use `Macro`

A `Macro` has at least one `Rotation State`, and for each `Rotation State`, you can configure commands for `On Key Down`, `On Key Up`, and `On Looping`.

* `Rotation State`: Each time the macro’s shortcut is pressed, it automatically switches to the next `Rotation State`. After the last state, it returns to the first state.
    * `On Key Down`: Commands triggered when the macro’s shortcut is pressed.
    * `On Key Up`: Commands triggered when the macro’s shortcut is released.
    * `On Looping`:
        * `Loop While Held`: After the `On Key Down` commands finish, the `On Looping` commands are executed continuously until the shortcut is released.
        * `Loop While Released`: After the `Key Up` commands finish, the `On Looping` commands are executed continuously until the `Interrupt Shortcut` is pressed or an `Interrupt Command` occurs.
* `Commands`:
    * `Click Command`: Simulates a single click at a specified position, with a command duration of 30ms.
    * `Shortcut Command`: Triggers other shortcuts, such as `Right Mouse Button`, `Keyboard A`. Note: For each press (↓), there must be a release (↑).
        * `Press (↓)`: Triggers the shortcut press, command duration 0ms.
        * `Release (↑)`: Triggers the shortcut release, command duration 0ms.
        * `Press and Release (↓↑)`: Triggers the shortcut press and release, command duration 30ms.
    * `Delay Command`: Waits for x milliseconds.
    * `Aiming Mode Command`: Toggles `Aiming Mode` on or off.
    * `Switch Scene Command`: Changes the current `Scene`.
    * `Interrupt Command`: Interrupts all macro commands and sets the `Rotation State` to the first one.

#### Examples of Use
* Open and close a backpack in a shooting game

Effect: Pressing the Tab key simulates clicking the backpack (position 1), disables Aiming Mode, and shows the mouse.
Pressing the Tab key again simulates clicking to close the backpack (position 2), enables Aiming Mode, and hides the mouse.

> `Macro` shortcut: Tab
> * Rotation State 1
>   * On Key Down
>       1. [Click Command] Click position 1
>       2. [Aiming Mode Command] Off
> * Rotation State 2
>   * On Key Down
>       1. [Click Command] Click position 2
>       2. [Delay Command] 300ms
>       3. [Aiming Mode Command] On

* Temporarily Release the Mouse Pointer

Effect: When the Alt key is pressed, Aiming Mode is disabled, and the mouse pointer is displayed. When the Alt key is released, Aiming Mode is enabled, and the mouse pointer is hidden.

> `Macro` Shortcut: Alt
> * Rotation State 1
>   * On Key Down
>       1. [Aiming Mode Command] Off
>   * On Key Up
>       1. [Aiming Mode Command] On

* Use a macro to perform a charge attack

Effect: After pressing the C macro shortcut, the left mouse button is automatically held down for 500 milliseconds and then released.

> `Macro` Shortcut: C
> * Rotation State 1
>   * On Key Down
>       1. [Shortcut Command] Left Mouse Button ↓
>       2. [Delay Command] 500ms
>       3. [Shortcut Command] Left Mouse Button ↑

* Switch weapons in a shooting game

Effect: Pressing the macro shortcut (Mouse Wheel ↓) automatically switches between two weapons. Each time the wheel is scrolled down, it switches to the next weapon.

> `Macro` Shortcut: Mouse Wheel ↓
> * Rotation State 1
>   * On Key Down
>       1. [Click Command] Click position 1 (Weapon 1)
> * Rotation State 2
>   * On Key Down
>       1. [Click Command] Click position 2 (Weapon 2)

* Use a macro for continuous skill casting in MOBA games

Already configured 3 right-stick MOBA buttons: L1, L2, L1&L2. Effect: Holding the Y macro shortcut triggers these 3 skills in a loop. Releasing the Y shortcut stops the loop.

> `Macro` Shortcut: Y
> * Rotation State 1
>   * On Looping `Loop While Held`
>       1. [Shortcut Command] L1 ↓↑
>       2. [Delay Command] 50ms
>       3. [Shortcut Command] L2 ↓↑
>       4. [Delay Command] 50ms
>       5. [Shortcut Command] L1&L2 ↓↑

* Automatically loop skill casting in MOBA games with a macro

Already configured 3 right-stick MOBA buttons: L1, L2, L1&L2. Effect: Pressing the Y macro shortcut once triggers these 3 skills in a loop. Pressing Y again stops the loop.

> `Macro` Shortcut: Y
> * Rotation State 1
>   * On Looping `Loop While Released`
>       1. [Shortcut Command] L1 ↓↑
>       2. [Delay Command] 50ms
>       3. [Shortcut Command] L2 ↓↑
>       4. [Delay Command] 50ms
>       5. [Shortcut Command] L1&L2 ↓↑
> * Rotation State 2
>   * On Key Down
>       1. [Interrupt Command]