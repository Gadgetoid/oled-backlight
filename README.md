# OLED Backlight

This Python script copies the acpi backlight brightness to the OLED display in the Alienware m15 r2/r3 and other OLED-equipped laptops. It will also work with external displays.

It was originally written by @joel-wright in bash, using inotify - https://gist.github.com/joel-wright/68fc3031cbb3f7cd25db1ed2fe656e60

It was converted to Python and enhanced by @indivisible - https://gist.github.com/indivisible/f643d970bbe362ab1d5cf7c4e604c984

I have probably broken @indivisible's fixes by converting back to inotify but keeping the script as Python. Maybe both methods could be implemented with the config allowing for a choice?

I have also:

* created a systemd unit to start this as a service
* Allowed settings to be configured via /etc/default/oledbacklight
* Allowed configurable gamma... but it's weird on my LCD

# Installing

You'll need these dependencies:

* sudo apt-get install python3-pip libxcb-render0-dev libffi-dev
* sudo pip3 install xcffib inotify configargparse

# Known Issues

* Breaks horribly in conjunction with Night Light