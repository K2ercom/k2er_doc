# Free Look (Stick)

The `Free Look (Stick)` needs to be used in conjunction with the `Camera stick`, similar to the `Small Eye` feature in TPS games. It is typically used in `FPS/TPS` games and 3D `ARPG` games. When you hold down the `Shortcut`, the joystick that was originally controlling the `Camera stick` will switch to controlling the `Free Look (Stick)`. Releasing the `Shortcut` will return the joystick control to the `Camera stick`.

## Parameters

* **Boundary**: Determines whether the simulated finger is restricted within a range. Some games allow points beyond the screen, and in such cases, disabling the `boundary` can provide smoother control.

* **Radius**: If the `Boundary` is enabled, you need to specify the radius. When the simulated finger moves outside the range, it will return to the center.

* **Re-center Mode**: Determines how to return to the center after crossing the `boundary`.

    * **Default**: The return to the center occurs after an interruption, which may cause a pause.

    * **Nonstop**: Returns to the center without interruption, but not all games support this mode.

* **Re-center Delay**: When in `Default` Re-center Mode, the simulated finger returns to the center after crossing the boundary with a delay of n milliseconds.

* **Sensitivity X**: Sensitivity for horizontal movements. The higher the value, the faster the horizontal movement.

* **Sensitivity Y**: Sensitivity for vertical movements. The higher the value, the faster the vertical movement.

* **Reverse X**: Inverts the X-axis data of the joystick.

* **Reverse Y**: Inverts the Y-axis data of the joystick.

* **Enter Delay**: After the `Shortcut` is triggered, delays by n milliseconds before switching from `Camera stick` to controlling the `Free Look (Stick)`.

* **Exit Delay**: After the `Shortcut` is released, delays by n milliseconds before switching from `Free Look (Stick)` back to `Camera stick`.

* **Dead Zone**: The unresponsive area between the center and the edge of the joystick.
