# Dealing with HPLIP

HPLIP (HP Linux Imaging & Printing) is a very unstable utility to print images on HP printers from Linux.

Since this garbage breaks down every time I restart by laptop, and does it to the point of breaking so hard that I only a full reinstall can help, I decided to create a separate repository to deal with this issue. Right now, I'm working around it by doing reinstalls.

## Reinstalling HPLIP

### Uninstalling HPLIP

* `sudo hp-uninstall`

### Installing HPLIP again

* Download an AppImage from their website
* Run the AppImage and go through a tedious process of pressing buttons when prompts appear (this is how babysitting feels like, probably). This can't even be automated with `yes` or similar tools, this stupid darn thing runs some shell of its own if it detects a pipe! Also, their `--auto` mode just crashes with a "UnboundLocalError: local variable 'bClassDriver' referenced before assignment"
* After running the thing, it will tell you that some darn thing failed and you need to run `hp-setup` *manually*. Damn nice *installers* you have here, HP! I'm so fucking tired of this shit...
* IDK what exactly makes it work, but it seems like either running `hp-setup` once (and seeing it fail as well) or not running it at all (maybe it's not required) makes the utility give you a dialogue window upon printer reconnection. That dialogue installs stuff correctly

### Recap

* `sudo hp-uninstall`
* Run the installer AppImage
* Run `hp-setup`?
* Replug the printer and follow on-screen instructions
