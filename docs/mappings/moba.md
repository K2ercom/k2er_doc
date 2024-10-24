# MOBA Skill Key

The `MOBA Skill Key` operates by using the vector from the `Virtual Center` to the current `Mouse Cursor` position to determine the direction and swipe distance for the skill. It is typically used in `MOBA` games.

## Parameters

* **Offset X**: Adjusts the horizontal offset of the circle's center in the `trigger range` for the finger.

* **Offset Y**: Adjusts the vertical offset of the circle's center in the `trigger range` for the finger.

* **Radius**: Adjusts the size of the **trigger range**.

* **Cast Mode**:

    * Targeted: When you press the `Shortcut`, you can aim by moving the mouse cursor, and the skill is triggered when you release the `Shortcut`.

    * Instant: The skill is triggered immediately based on the current mouse cursor position when the `Shortcut` is pressed.

    * Free: Press the `Shortcut` to trigger the skill directly without aiming.

* **Stop Movement on Skill Cast**: When enabled, movement stops immediately after triggering the skill.

* **Virtual Center**: Set the `Virtual Center` at the character's feet.

* **Virtual X Radius**: The horizontal radius of the `Skill Range`, centered on the `Virtual Center` (the character’s feet).

* **Virtual ↑ Radius**: The vertical upward radius of the `Skill Range`, centered on the `Virtual Center` (the character’s feet).

* **Virtual ↓ Radius**: The vertical downward radius of the `Skill Range`, centered on the `Virtual Center` (the character’s feet).

* **Private Cancel Position**: Set this if the skill cancel position differs from others.
