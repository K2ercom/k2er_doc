# Free Look (Small Eye)

The `Free Look (Small Eye)` needs to be used in conjunction with the `Aiming Mode`, similar to the `Small Eye` feature in TPS games. It is typically used in `FPS/TPS` games and 3D `ARPG` games. When you hold down the `Shortcut`, the mouse movement, which was originally controlling the `Aiming Mode`, will switch to control the `Free Look (Small Eye)`. Releasing the `Shortcut` will return the mouse control to the `Aiming Mode`.

## Parameters

* **Boundary**: Determines whether the simulated finger is restricted within a range. Some games allow points beyond the screen, and in such cases, disabling the `boundary` can provide smoother control.

* **Radius**: If the `Boundary` is enabled, you need to specify the radius. When the simulated finger moves outside the range, it will return to the center.

* **Re-center Mode**: Determines how to return to the center after crossing the `boundary`.

    * **Default**: The return to the center occurs after an interruption, which may cause a pause.

    * **Nonstop**: Returns to the center without interruption, but not all games support this mode.

* **Re-center Delay**: When in `Default` Re-center Mode, the simulated finger returns to the center after crossing the boundary with a delay of n milliseconds.

* **Sensitivity X**: Sensitivity for horizontal movements. The higher the value, the faster the horizontal movement.

* **Sensitivity Y**: Sensitivity for vertical movements. The higher the value, the faster the vertical movement.

* **Enter Delay**: After the `Shortcut` is triggered, delays by n milliseconds before switching from `Aiming Mode` to controlling the `Free Look (Small Eye)`.

* **Exit Delay**: After the `Shortcut` is released, delays by n milliseconds before switching from `Free Look (Small Eye)` back to `Aiming Mode`.
