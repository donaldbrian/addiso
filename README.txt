The script will *not* work without the servicemenu...
...unless you edit it and insert the/path/to/the-iso in place of isoentry="$1"

Just copy both files to ~/.local/share/kservices5/ServiceMenus/
Make addiso.sh executeble (if it isn't already).
Restart Dolphin.
After which, when you right-click on an ISO, you'll find an "Add ISO to grub" entry.
Choosing that will open the script and guide you through the process.

At boot, you should then find an entry in your grub menu for "<whatever your ISO is called>".

