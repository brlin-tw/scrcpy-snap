# Snap Packaging for scrcpy

**This is a snap for scrcpy**, *"Display and control your Android device"*. It works on Ubuntu, Fedora, Debian, and other major Linux distributions.

![Screenshot of the Snapped Application](https://github.com/Genymobile/scrcpy/blob/master/assets/screenshot-debian-600.jpg "Screenshot of the Snapped Application")

## Installation

([Don't have snapd installed?](https://snapcraft.io/docs/core/install))

### The Graphical Way

[![Get it from the Snap Store](https://snapcraft.io/static/images/badges/en/snap-store-black.svg)](https://snapcraft.io/scrcpy)

### From the Terminal

##### The latest stable version (currently v2.0) is in the stable channel:

    sudo snap install scrcpy

##### Usage:

    scrcpy

##### You can also use the builtin adb tool:

    scrcpy.adb [options]

##### For example:

    scrcpy.adb devices
    scrcpy.adb kill-server

##### For audio playback the alsa plug is needed:

    sudo snap connect scrcpy:alsa

##### In order to use the v4l2loopback feature the camera plug must be connected:

    sudo snap connect scrcpy:camera

##### For physical keyboard simulation you need to connect the raw-usb plug:

    sudo snap connect scrcpy:raw-usb

#### XDG Desktop Entry

The snap comes with an XDG desktop entry that can be called from your desktop environment's application menu. If you would like to customize the command line flags that are called by the desktop environment, edit the `Exec` key value at `/var/lib/snapd/desktop/applications/scrcpy_scrcpy.desktop`. For example:

    Exec=scrcpy

could become:

    Exec=scrcpy -w

to enable the `--stay-awake` flag on scrcpy. See all flags by running `scrcpy --help`.

#### To uninstall the scrcpy snap:

    sudo snap remove scrcpy
