# Activation-Related FAQs

## Why is `Wi-Fi` necessary?

`Wi-Fi` is required because enabling `Wireless Debugging` needs a local network environment. The activation process does not consume data but does require a `Wi-Fi (local network)` environment. After activation, `Wi-Fi` is no longer necessary, and you can disable `Wireless Debugging`, but you must keep `USB Debugging` enabled, or the activation will automatically become invalid.

## Cannot find `Wireless Debugging`

* General Android phones: `Wireless Debugging` is supported starting from `Android 11`. Versions before that do not have this feature.

* Honor phones: `Wireless Debugging` is only available from `Android 12`.

* Huawei phones: There is no `Wireless Debugging` feature.

If `Wireless Debugging` is not available, the best activation method is using `Computer Activation`.

## Cannot find `Allow display overlay for settings`

If your phone does not have `Allow display overlay for settings`, mark it as completed and proceed with the following steps. Use `Split-screen pairing` in the final step.

## Prompt: `Pairing failed`

In the last step when entering the `Pairing code`, you must not minimize the `Wireless Debugging` screen. Therefore, you must enter the code in the `floating window` or use `Split-screen pairing`.

If the `Wireless Debugging` screen is minimized, the `Pairing code` will expire, resulting in a pairing failure.

## Stuck on `Activating`

* If stuck on step `[2/3]`, go to `Wireless Debugging` and delete all `Paired devices` at the bottom. Then, under `USB Debugging`, click `Revoke USB Debugging authorizations`. Restart the phone and try again.

* If stuck on `[3/3]`, uninstall `K2er`, restart your phone/tablet, and reinstall the app. If it still fails and your system is Android 11, updating your system might temporarily resolve the issue.

## How to activate via command line

Command line activation must be done using a command line tool that has already been activated (e.g., `Brevent`). This means you need to activate these command line tools first before using them to activate K2er.

## `Computer Activation` not detecting the device

* Ensure the data cable supports data transmission. Most original cables do.

* Your computer needs to have the [Android USB driver](https://developer.android.com/studio/run/oem-usb) installed.

* Software conflict: If both the driver and cable are working but the connection still fails, it may be due to software conflicts. To resolve this, unplug the cable, restart your computer, and close all open software before reconnecting your phone.

## Activation method for `Honor` devices

* `Wireless Activation`: Honor devices do not have `Allow display overlay for settings`, so you need to mark it as completed and use the `Split-screen pairing` button in the final step to activate.

* `Computer Activation`: If there is no `Wireless Debugging`, you need to use `Computer Activation`. Select `Use computer to activate` at the bottom of the activation screen on your phone and follow the instructions. If K2er's `Computer Activation` doesn't detect the device, install the [Honor Suite](https://www.hihonor.com/cn/support/suite/) on your computer, connect your phone successfully, then close the suite and open the K2er desktop app. If it still doesn't work, restart both your computer and phone.

## Activation method for `Huawei` devices

* `Computer Activation`: Huawei devices can only be activated via computer. Select `Use computer to activate` at the bottom of the activation screen on your phone and follow the instructions. If K2er's `Computer Activation` doesn't detect the device, install the [Huawei HiSuite](https://consumer.huawei.com/cn/support/hisuite/) on your computer, connect your phone successfully, then close the suite and open the K2er desktop app. If it still doesn't work, restart both your computer and phone.

## Activation is lost after unplugging during `Computer Activation`

If activation is lost on `Huawei` or `Honor` devices after unplugging, try the following:

1. In Developer Options, set `Allow USB debugging in charging mode only` and reconnect the cable using the `charging only` mode before unplugging.

2. If that doesn't work, try using `MIDI mode` to connect before unplugging.

3. If the issue persists, try disabling your phone's Wi-Fi and attempt again.

4. As a last resort, after `Computer Activation`, unplug the cable (activation will be lost), then on your phone, click `Activate now` on the main screen of K2er and wait for 30 seconds to see if it can `auto-activate`.

Huawei and Honor devices can be complex, so please be patient and keep trying. There are no other alternatives.