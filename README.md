# Dealing with HPLIP

HPLIP (HP Linux Imaging & Printing) is a very unstable utility to print images on HP printers from Linux.

Since this garbage breaks down every time I restart by laptop, and does it to the point of breaking so hard that only a full reinstall can help, I decided to create a separate repository to deal with this issue. Right now, I'm working around it by doing reinstalls.

## Reinstalling HPLIP

### Uninstalling HPLIP

* `sudo hp-uninstall`

### Installing HPLIP again

* Download an AppImage from their website
* Run the AppImage and go through a tedious process of pressing buttons when prompts appear (this is how babysitting feels like, probably). This can't even be automated with `yes` or similar tools, this stupid darn thing runs some shell of its own if it detects a pipe! Also, their `--auto` mode just crashes with an "UnboundLocalError: local variable 'bClassDriver' referenced before assignment". After running the thing, it will tell you that some darn thing failed and you need to run `hp-setup` *manually*. (You don't, though.) Damn nice *installers* you have here, HP! I'm so fucking tired of this shit... Proceed until it won't be able to find your printer
* After all this, turning the printer off and back on while it is plugged in makes the utility give you a dialogue window upon printer reconnection. That dialogue installs stuff correctly

### Recap

* `yes | sudo hp-uninstall`
* Run the installer AppImage, proceed until it won't be able to find your printer
* Turn the printer off and back on and follow on-screen instructions

## If it still does not work

Literally change the HP printer to a printer from a different manufacturer which will not have a shit ton of issues with its software. HPLIP is literally the buggiest piece of shit I've ever worked with, nothing was worse than that
