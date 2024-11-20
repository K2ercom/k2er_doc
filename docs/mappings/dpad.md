# Dpad

The "Dpad" uses 4 `shortcut` to simulate the **virtual joystick** used for movement in games, such as the commonly used `WASD` and `↑←↓→`.

## Parameters

* **Radius**: Adjusts the size of the **virtual joystick**.

* **Release Delay**: After all `shortcut` are released, there is a delay of n milliseconds before movement stops.

* **Change Radius Shortcut**: When the `Change Radius Shortcut` is pressed, the Dpad `radius` will increase or decrease based on the `Radius Offset Value`. This is commonly used for controlling walking and running in games. For example, pressing `Shift` will switch to walking.

* **Hold To Change**: When `Hold To Change` is on, press and hold `Change Radius Shortcut` to change radius, and release to restore. When `Hold To Change` is off, press `Change Radius Shortcut`, the radius will change until you press `Change Radius Shortcut` next time and restore.

* **Angle**: Adjusts the angle between two simultaneously pressed `shortcut`

* **Frequency**: The number of movements per second.

* **Step Length**: The distance moved per step.
