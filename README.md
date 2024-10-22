# Accessibility Pack for Splatoon 3

### About this project

This project is aimed at providing additional accessibility options for the Splatoon 3 game.

### Current features

- A [Flick Stick](https://www.youtube.com/watch?v=C5L_Px3dFtE) implementation
- Deactivating controller rumble
- Turbo "Booyah!" as well as remapping "Booyah!"

### Planned features

- Adjustable gyro sensitivity on the natural sensitivity scale (where N on that scale means that for every 1º of controller movement, Nº of camera movement will happen in game)
- A more expansive gyro modifier button (Gyro off, Gyro on, Gyro toggle, Native reset camera, reset camera pitch only, invert gyro) similar to Fortnite's gyro options
- Expanded sensitivity options like acceleration and vertical/horizontal ratio
- An option for regular horizontal+vertical stick *while* gyro is enabled (normally vertical stick is disabled while gyro is enabled)
- Expanded joystick sensitivity curves for stick players

### What you need

This project is built for a [Titan Two](https://www.consoletuner.com/products/titan-two/) adapter.

Controllers tested so far:

- Dualsense

### Setup

Make sure your switch has wired communication enabled (system settings -> Controllers and Sensors -> Pro Controller Wired Communication)

You will need to install [Gtuner IV](https://www.consoletuner.com/titan-two-downloads/)

In Gtuner go to `Device Configuration` (located in the bottom right) and make sure the `Output Protocol` is set to `USB Nintendo Switch`

 Download the scripts hosted here into a directory and load that directory.

 Open `s3accessibility.gpc`

 Make sure `Device Memory Slots` is selected in the bottom right.

 Click the `install active work to memory slot` button in the top bar and choose a memory slot.

 Click the configuration gear icon for the memory slot you chose above.

 Configure your options (more info below)

 Click `Save and Run`


### Configuration

Enable Rumble - I would recommend disabling this if you find that rumble is messing with your gyro aim or if you just don't like rumble

Booyah options - You may find it helpful to swap L and Dpad down so that it's easier to press the booyah button for booyah bombs. There is also a turbo option if you have trouble mashing buttons.

Flick Stick
  - Enable Flick Stick will replace the right stick behavior with a flick stick behavior (all other options don't matter if this is disabled).
    **For this to work properly your gyro (motion controls) must be enabled and set to +5 Sensitivity.** Stick sensitivity can be set to anything and has no effect.
  - Forward snap angle. Often to turn more slowly you'll want to press forward on the stick (resulting in no flick) and then sweep the stick in a direction for one-to-one horizontal camera movement. A forward snap angle means that anything within this angle (in degrees) of up will count as if it was pressed perfectly up in other words there will be no flick.
  - Flick Threshold. This is the percentage the stick must travel before a flick is registered. Smaller values mean flicks occur sooner; larger values mean the angle of the flick will be more accurate.
  - Special Flick Stick Disable window. Sometimes when using a special you will accidentally push the stick enough to cause an unintended flick. This window in milliseconds is how long after pressing special flicks will be disabled.
  - Flick Stick sensitivity. Most users should not need to mess with this; **make sure your gyro (motion control) sensitivity is set to +5**. If you still find that flick stick angles are consistently wrong, you may need to tweak this value.

