# Camera stick

The `Camera stick` uses the gamepad's joystick to simulate character view movement in games, commonly used in **FPS** games and 3D **ARPG** games.

## Parameters

* **Boundary**: Determines whether the simulated finger is restricted within a range. Some games allow points beyond the screen, and in such cases, disabling the `boundary` can provide smoother control.

* **Radius**: If the `Boundary` is enabled, you need to specify the radius. When the simulated finger moves outside the range, it will return to the center.

* **Re-center Mode**: Determines how the joystick returns to the center after crossing the `boundary`.

    * **Default**: The return to the center occurs after an interruption, which may cause a pause.

    * **Nonstop**: Returns to the center without interruption, but not all games support this mode.

* **Re-center Delay**: When in Default Re-center Mode, the simulated finger returns to the center after crossing the boundary with a delay of n milliseconds.

* **Release Delay**: After the joystick returns to the center, there is a delay of n milliseconds before stopping.

* **Sensitivity X**: Sensitivity for horizontal movements. The higher the value, the faster the horizontal movement.

* **Sensitivity Y**: Sensitivity for vertical movements. The higher the value, the faster the vertical movement.

* **Main Joystick in Dual-joystick**: K2er supports two gamepads controlling the `Camera stick` simultaneously. If both joysticks are in use, the main gamepad will take priority.

* **Reverse X**: Inverts the X-axis data of the joystick.

* **Reverse Y**: Inverts the Y-axis data of the joystick.

* **Swap X & Y**: Swaps the X-axis and Y-axis data of the joystick.

* **Dead Zone**: The unresponsive area between the center and the edge of the joystick.
