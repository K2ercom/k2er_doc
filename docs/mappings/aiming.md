# Aiming Mode

`Aiming Mode` uses the mouse to simulate the movement of the character's view in games, commonly used in **FPS** games and 3D **ARPG** games. When `Aiming Mode` is enabled, the mouse cursor is hidden, and moving the mouse simulates a finger swiping on the touchscreen to control the view. When `Aiming Mode` is disabled, the mouse cursor reappears.

## Parameters

* **Boundary**: Determines whether the simulated finger is restricted within a range. Some games allow points beyond the screen, and in such cases, disabling the `boundary` can provide smoother control.

* **Radius**: If the `Boundary` is enabled, you need to specify the radius. When the simulated finger moves outside the range, it will return to the center.

* **Re-center Mode**: Determines how to return to the center after crossing the `boundary`.

    * **Default**: The return to the center occurs after an interruption, which may cause a pause.

    * **Nonstop**: Returns to the center without interruption, but not all games support this mode.

* **Re-center Delay**: When in `Default` Re-center Mode, the simulated finger returns to the center after crossing the boundary with a delay of n milliseconds.

* **Release Delay**: After the returns to the center, there is a delay of n milliseconds before movement stops.

* **Sensitivity X**: Sensitivity for horizontal movements. The higher the value, the faster the horizontal movement.

* **Sensitivity Y**: Sensitivity for vertical movements. The higher the value, the faster the vertical movement.

* **Auto Release**: If the mouse remains still for n milliseconds, the simulated touchscreen finger is automatically released.

* **Offset Correction**: In some games (such as Free Fire), view movement may become unstable when boundary mode is disabled. In such cases, enable this option. Otherwise, keep it disabled.
