This repository contains a Marlin firmware for the Sovol SV06.

This is an attempt at cleaning up branches from various other firmwares while
providing a working Marlin 2.1.2 firmware with X-Twist compensation support.

The rebase over Marlin 2.1.2 does not tweak the configuration, except for the
following small changes:

- Enable X-Twist Compensation
- Disable beeps (I hate beeps)
- Enable watchdog (Marlin warns that it should be enabled)

There is no Unified Bed Leveling build because I couldn't make it work on my
printer. When it is enabled, for some reason motors spin more slowly and
sensorless homing is broken (it keeps grinding). My uneducated guess is that the
board is not fast enough for the UBL calculations.

## How to download the rebased firmware

You can download the released firmware [here](https://github.com/blastrock/Marlin-sv06/releases).

## How to explore this repository

You'll find here the following branches:

- [rebase-sovol-2.0.9.2](https://github.com/blastrock/Marlin-sv06/tree/rebase-sovol-2.0.9.2): The original [Sovol SV06 firmware](https://github.com/Sovol3d/Sv06-Source-Code/commits/main)
- [rebase-sovol-2.0.9.2-bare](https://github.com/blastrock/Marlin-sv06/tree/rebase-sovol-2.0.9.2-bare): The sovol fork but a little bit cleaned up (file permissions were fixed)
- [rebase-sovol-2.1.2-xtwist](https://github.com/blastrock/Marlin-sv06/tree/rebase-sovol-2.1.2-xtwist): The sovol fork, rebased over [Marlin 2.1.2](https://github.com/MarlinFirmware/Marlin/releases/tag/2.1.2)
- [rebase-hillsoftware](https://github.com/blastrock/Marlin-sv06/tree/rebase-hillsoftware): The [hillsoftware fork](https://github.com/hillsoftware/sv06) based on the actual commit from Marlin's bugfix-2.1.2 branch
