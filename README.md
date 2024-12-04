# Accessibility Pack for Splatoon 3

### About this project

This project is aimed at providing additional accessibility options for the Splatoon 3 game. This project is not affiliated with Nintendo or ConsoleTuner in any way.

### Current features

- A [Flick Stick](https://www.youtube.com/watch?v=C5L_Px3dFtE) implementation
- Selectable Gyro Axis (adaptive, yaw, roll)
- A Gyro off ratcheting button (holding y, quick presses still act as normal, or by touching the PS touchpad)
- Adjustable gyro sensitivity on the natural sensitivity scale (where N on that scale means that for every 1º of controller rotation, Nº of camera rotation will happen in game)
- Adjustable vertical : horizontal sensitivity ratio
- Deactivating controller rumble
- Turbo "Booyah!" as well as remapping "Booyah!"
- Quick Super Jump To Base on Left Stick Press

### Planned features (some may not be possible based on gtuner limitations)

- A more expansive gyro modifier button (Gyro on, Gyro toggle, Native reset camera, reset camera pitch only, invert gyro) similar to Fortnite's gyro options
- Expanded sensitivity options like acceleration
- An option for regular horizontal+vertical stick *while* gyro is enabled (normally vertical stick is disabled while gyro is enabled)
- Expanded joystick sensitivity curves for stick players

### Known issues

- Flick Stick sweep is a bit crunchy with the Pro Controller (I think this is due to the slow polling rate)
- Flicks may not be 100% accurate due to how the hardware works (even the exact same gyro/accelerometer inputs will produce slightly different results)

### What you need

This project is built for a [Titan Two](https://www.consoletuner.com/products/titan-two/) adapter.

A Switch and copy of the game.

A controller. Controllers tested so far:

- ✅⭐ Dualsense (Works best, has a sensitivity preset, high polling rate gives excellent results)
- ✅  Pro Controller (Works well, has a sensitivity preset, low polling rate gives a bit more jank with the flick stick sweep)
- ❌  Dualsense Edge (Doesn't work; will probably need some sort of firmware fix on ConsoleTuner's side of things since things like gyro/accel aren't even detected)
- ❌  8bitdo Bluetooth Ultimate (seems like it's defaulting to xinput when wired, might work with the bluetooth adapter or with the beta firmware)

### Setup

Make sure your switch has wired communication enabled (system settings -> Controllers and Sensors -> Pro Controller Wired Communication)

For most options to work properly you should set your in-game gyro sensitivity to +5. Don't worry if this is higher than what you normall play with, you can modify the effective sensitivity in the configuration step later.

You will need to install [Gtuner IV](https://www.consoletuner.com/titan-two-downloads/)

In Gtuner go to `Device Configuration` (located in the bottom right) and make sure the `Output Protocol` is set to `USB Nintendo Switch`

Install method 1: 

- In Gtuner search for 'splatoon accessibility', look for the one titled `Accessibility Pack for Splatoon 3`

- Make sure `Device Memory Slots` is selected in the bottom right.

- Drag the `DRAG DROP` icon over to an open memory slot.

- Configure your options (more info below)

- Click `Save and Run`

Install method 2:

 - Download the scripts hosted here into a directory and load that directory.

 - Open `s3accessibility.gpc`

 - Make sure `Device Memory Slots` is selected in the bottom right.

 - Click the `install active work to memory slot` button in the top bar and choose a memory slot.

 - Click the configuration gear icon for the memory slot you chose above.

 - Configure your options (more info below)

 - Click `Save and Run`


### Configuration

Gyro Options

 - Sensitivity Presets - Select which controller you're using first. This will configure the gyro and accelerometer sensitivities so you don't have to fiddle with those.

- Natural Sensitivity Multiplier - Adjust your sensitivity preference here. Note that this is based on the natural sensitivity scale

If you don't know what your natural sensitivity preference is here is a table of conversions for Splatoon 3:

| Splatoon Sensitivity | Natural Sensitivity |
| -------------------- | ------------------- |
| +5                   | 3.37                |
| +4.5                 | 3.19                |
| +4                   | 3.14                |
| +3.5                 | 3.07                |
| +3                   | 3.02                |
| +2.5                 | 2.97                |
| +2                   | 2.92                |
| +1.5                 | 2.87                |
| +1                   | 2.82                |
| +0.5                 | 2.78                |
| 0                    | 2.73                |
| -0.5                 | 2.60                |
| -1                   | 2.44                |
| -1.5                 | 2.28                |
| -2                   | 2.13                |
| -2.5                 | 2.00                |
| -3                   | 1.89                |
| -3.5                 | 1.75                |
| -4                   | 1.60                |
| -4.5                 | 1.47                |
| -5                   | 1.35                |

Enable Rumble - I would recommend disabling this if you find that rumble is messing with your gyro aim or if you just don't like rumble

Booyah options - You may find it helpful to swap L and Dpad down so that it's easier to press the booyah button for booyah bombs. There is also a turbo option if you have trouble mashing buttons.

Super Jump To Base - pressing the left stick can be used to automatically super jump to base (map + booyah + a)

Flick Stick
  - Enable Flick Stick will replace the right stick behavior with a flick stick behavior (all other options don't matter if this is disabled).
    **For this to work properly your gyro (motion controls) must be enabled and set to +5 Sensitivity.** Stick sensitivity can be set to anything and has no effect.
  - Forward snap angle. Often to turn more slowly you'll want to press forward on the stick (resulting in no flick) and then sweep the stick in a direction for one-to-one horizontal camera movement. A forward snap angle means that anything within this angle (in degrees) of up will count as if it was pressed perfectly up in other words there will be no flick.
  - Flick Threshold. This is the percentage the stick must travel before a flick is registered. Smaller values mean flicks occur sooner; larger values mean the angle of the flick will be more accurate.
  - Special Flick Stick Disable window. Sometimes when using a special you will accidentally push the stick enough to cause an unintended flick. This window in milliseconds is how long after pressing special flicks will be disabled.
  - Flick Stick sensitivity. Most users should not need to mess with this; **make sure your gyro (motion control) sensitivity is set to +5**. If you still find that flick stick angles are consistently wrong, you may need to tweak this value.


Gyro Off Button
 - Enable if you wish to hold y to disable gyro (ratcheting), y will still work normally if you press and release it within a certain window.
 - The length of the window in ms can be set (defaults to 200).
 - If using a playstation controller, you may wish to have touchpad touches disable gyro instead.

Gyro Axis
- Adaptive (yaw + roll based on how you hold the controller, this is most similar to how Splatoon handles gyro natively)
- Yaw (only the yaw axis for gyro affects yaw in game, good if you mostly hold the controller flat (charge port forward))
- Roll (only the roll axis for gyro affects yaw in game, good if you mostly hold the controller vertically (charge port up))
