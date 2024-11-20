# Macro

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

## Examples of Use
### Open and close a backpack in a shooting game

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

### Temporarily Release the Mouse Cursor

Effect: When the Alt key is pressed, Aiming Mode is disabled, and the mouse cursor is displayed. When the Alt key is released, Aiming Mode is enabled, and the mouse cursor is hidden.

> `Macro` Shortcut: Alt
> * Rotation State 1
>   * On Key Down
>       1. [Aiming Mode Command] Off
>   * On Key Up
>       1. [Aiming Mode Command] On

### Use a macro to perform a charge attack

Effect: After pressing the C macro shortcut, the left mouse button is automatically held down for 500 milliseconds and then released.

> `Macro` Shortcut: C
> * Rotation State 1
>   * On Key Down
>       1. [Shortcut Command] Left Mouse Button ↓
>       2. [Delay Command] 500ms
>       3. [Shortcut Command] Left Mouse Button ↑

### Switch weapons in a shooting game

Effect: Pressing the macro shortcut (Mouse Wheel ↓) automatically switches between two weapons. Each time the wheel is scrolled down, it switches to the next weapon.

> `Macro` Shortcut: Mouse Wheel ↓
> * Rotation State 1
>   * On Key Down
>       1. [Click Command] Click position 1 (Weapon 1)
> * Rotation State 2
>   * On Key Down
>       1. [Click Command] Click position 2 (Weapon 2)

### Use a macro for continuous skill casting in MOBA games

Already configured 3 right-stick MOBA buttons: L1, L2, L1&L2. Effect: Holding the Y macro shortcut triggers these 3 skills in a loop. Releasing the Y shortcut stops the loop.

> `Macro` Shortcut: Y
> * Rotation State 1
>   * On Looping `Loop While Held`
>       1. [Shortcut Command] L1 ↓↑
>       2. [Delay Command] 50ms
>       3. [Shortcut Command] L2 ↓↑
>       4. [Delay Command] 50ms
>       5. [Shortcut Command] L1&L2 ↓↑

### Automatically loop skill casting in MOBA games with a macro

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