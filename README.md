# MOST HUD

MOST HUD is a collection of [Conky](https://github.com/brndnmtthws/conky) configs that gives you almost a complete system monitoring.

![MOST HUD](imgs/most-hud.png?raw=true "Preview")

## Features

-   System info
-   Battery status
-   CPU
-   Nvidia GPU
-   Memory
-   Disk
-   Network
-   Processes
-   Journal log
-   Time / Calendar

## Requirements

-   Linux
-   [conky >= 1.11](https://github.com/brndnmtthws/conky)
-   nvidia-settings
-   Cutive Mono font
    -   [Google fonts](https://fonts.google.com/specimen/Cutive+Mono)
    -   [1001 Free font](https://www.1001freefonts.com/cutive-mono.font)

## Usage

Download compressed files or use git clone.

```shell
git clone https://github.com/VHSgunzo/most-hud.git
```

Go through all .conf files and make sure your own device names are correct like disks / mount points / network interfaces etc. You do need to have some knowledge about how conky works so check out [conky wiki](https://github.com/brndnmtthws/conky/wiki)

Execute the `start_conky` file in your terminal to run all widgets at once, or use `conky -d -c /path/to/configfile.conf` command to only launch the one you want, see the `start_conky` file for how the script loads all conf files.

This collection is developed for a screen resolution of 1920x1080px. So feel free to customize all widgets to fit your screen if they aren't positioned correctly for you.

See [conky wiki](https://github.com/brndnmtthws/conky/wiki) for more information about how to work with conky configurations (widgets)

## FAQ

**Why is all widgets in it's own file?**

Mainly because it's easier to position them on the desktop.  
How ever the bad thing about this is that it requires to run  
multiple conky processes.

**How do I make MOST HUD autostart on boot/login?**

Look up how to create an autostart script on your distribution.  
But most distributions that follows the [FreeDesktop spec](https://www.freedesktop.org/wiki/Specifications/) allows you to create a .desktop file in `~/.config/autostart/` for ex

`~/.config/autostart/mosthud.desktop`

```plaintext
[Desktop Entry]
Name=mosthud
Comment=A complete system monitoring running with conky.
Exec=/path/to/most-hud/start_conky
Terminal=false
Type=Application
```

**How do I customize the widgets in MOST HUD?**

Just edit the conf file you want to customize and save. If conky  
is already running the conf file you edit it should update without  
a restart of conky. See [conky wiki](https://github.com/brndnmtthws/conky/wiki) and `man conky` pages for more information  
on what you can do with conky.
