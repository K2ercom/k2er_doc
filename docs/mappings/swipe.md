# Swipe

The `Swipe` simulates a finger swiping on the screen along a pre-set path after receiving a `shortcut` event. There are 3 `swipe modes` to choose from: `↓: Swipe`, `↓: Swipe & Hold, ↑: Release`, and `↓: Hold down, ↑: Swipe`.

## How to configure?

Simply swipe in the blank area of the expanded floating window interface with your finger. It will record the swipe path, including the points your finger passed through and the time.

## Swipe Modes

* **↓: Swipe**: When the `shortcut` is pressed, the swipe path is executed once.

* **↓: Swipe & Hold, ↑: Release**: When the `shortcut` is pressed, the swipe path is executed once, and the finger holds down at the last point. When the `shortcut` is released, the finger is released simultaneously.

* **↓: Hold down, ↑: Swipe**: When the `shortcut` is pressed, the finger holds down at the first swipe point. When the `shortcut` is released, the swipe path is executed once.
