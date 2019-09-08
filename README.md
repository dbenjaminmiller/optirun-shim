# `optirun` shim

## What's this?

This is a shim which replaces Bumblebee's `optirun`, a program which allows users with dual-graphics laptops (integrated + Nvidia graphics) to run programs selectively with their more powerful dGPU. Bumblebee, however, suffered from terrible performance: in most cases, it meant that the program would run better on the integrated graphics card than on the dGPU.

This program was written for my own setup, using Fedora 30 (as of writing) with the Cinnamon desktop environment. Cinnamon detects whether or not `optirun` is intalled by checking `/usr/bin/optirun`; if it is present, it will add a right-click option to applications in its start menu, allowing them to be launched with the dGPU in one click. This shim allows you to do this with better performance tan Bumblebee enabled using Nvidia's support in their latest beta drivers.

## Use

1. Install Nvidia driver 435.17 or later. As of writing, this is the beta version; follow the [instructions on RPM Fusion's wiki](https://rpmfusion.org/Howto/NVIDIA#Latest.2FBeta_driver).
2. Follow the [Optimus instructions](https://rpmfusion.org/Howto/Optimus); as of writing, a COPR repository must be enabled to install a particular version of X.
3. Copy the `optirun` file to `/usr/bin/optirun` and make sure it is set to executable.

## Note

To adjust render offload settings, modify the script in accordance with the documentation in the Optimus instructions page
