# Dealing with HPLIP

HPLIP (HP Linux Imaging & Printing) is a very unstable utility to print images on HP printers from Linux.

Since this garbage breaks down every time I restart by laptop, and does it to the point of breaking so hard that I only a full reinstall can help, I decided to create a separate repository to deal with this issue. Right now, I'm working around it by doing reinstalls.

## Reinstalling HPLIP

### Uninstalling HPLIP

* `sudo hp-uninstall`

### Installing HPLIP again

* Download an AppImage from their website
* Run the AppImage and go through a tedious process of pressing buttons when prompts appear (this is how babysitting feels like, probably). This can't even be automated with `yes` or similar tools, this stupid darn thing runs some shell of its own if it detects a pipe!
