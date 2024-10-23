# Tap

`Tap` refers to simulating a finger press on a screen location after receiving a `shortcut` event, followed by releasing it. There are four tap modes to choose from: `Sync`, `Interval`, `Single` and `Long Press`.

* **Sync**: When the `shortcut` is pressed, it simulates a finger pressing down on the designated screen location and **holding** it. When the `shortcut` is released, the simulated finger is also released simultaneously.

* **Interval**: When the `shortcut` is pressed, the simulated finger **continuously taps** the screen location at a specified interval until the `shortcut` is released.

* **Single**: When the `shortcut` is pressed, the simulated finger taps the screen location once.

* **Long Press**: When the `shortcut` is **long-pressed**, the simulated finger taps the screen location once.
