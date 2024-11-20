# Dpad (Stick)

The `Dpad (Stick)` uses the gamepad's **joystick** to simulate the **virtual joystick** for movement in games.

## Parameters

* **Radius**: Adjusts the size of the **virtual joystick**.

* **Release Delay**: After the joystick returns to the center, there is a delay of n milliseconds before movement stops.

* **Change Radius Shortcut**: When the `Change Radius Shortcut` is pressed, the Dpad `radius` will increase or decrease based on the `Radius Offset Value`. This is commonly used for controlling walking and running in games. For example, pressing `R1` will switch to walking.

* **Hold To Change**: When `Hold To Change` is on, press and hold `Change Radius Shortcut` to change radius, and release to restore. When `Hold To Change` is off, press `Change Radius Shortcut`, the radius will change until you press `Change Radius Shortcut` next time and restore.

* **Reverse X**: Inverts the X-axis data of the joystick.

* **Reverse Y**: Inverts the Y-axis data of the joystick.

* **Switch X & Y**: Swaps the X-axis and Y-axis data of the joystick.

* **Frequency**: The number of movements per second.

* **Step Length**: The distance moved per step.

* **Dead Zone**: The unresponsive area between the center and the edge of the joystick.
