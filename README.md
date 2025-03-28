# GnomeGlider

Smoothly gliding from one wallpaper to the next.

The script when set up correctly, can periodically change your wallpaper. It will pick from different sets of wallpapers depending on the time of day, so you are not blinded at night by light wallpapers!

This only works on the [Gnome Desktop Environment](http://gnome.org).

---

[Watch the demo](https://files.catbox.moe/kavqen.mp4)


## Installation & setup

Create 3 folders (day, dusk and night) in your Wallpaper folder and populate them with images;

Download the script to a folder and make it executable (right click > Properties > Executable as Program); 

Open the script, **write the path to the folders created (add your username)** and either start using it ([adding its directory to your $PATH](https://www.geeksforgeeks.org/add-directory-to-path-in-linux/) is optional), or configure [cron](https://linuxhandbook.com/crontab/) by running `crontab -e` and adding the code below to run it automatically and periodically.

`*/5 * * * * /bin/bash /home/USERNAME/.scripts/wallpaper -c 2>&1`

Adding this to cron will run the script every 5 minutes with `-c` argument and send any errors/outputs to dev null (digital limbo).
Tweak the time interval to your liking. **Make sure to actually put your username.**

---

### Notes

If you are on Fedora you may need to install cron with `sudo dnf install cronie`.

`$USER` won't work with cron.

The editor I use in the demo to edit cron is called `micro`.

Run `GnomeGlider -h` for help.
