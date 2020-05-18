Until this bug is resolved,
https://bugs.launchpad.net/ubuntu/+source/calamares-settings-ubuntu/+bug/1876950
(which does NOT apply just to Lubuntu) the workaround is to remove the "toram" option from /etc/grub.d/40_custom.
Which *might* cause Calamares to complain, whine and whinge, but do the installation all the same.
:·/

The script will *not* work without the servicemenu...
...unless you edit it and insert the/path/to/the-iso in place of isoentry="$1"

Just copy both files to ~/.local/share/kservices5/ServiceMenus/
Make addiso.sh executable - if it isn't already.
Restart Dolphin.
After which, when you right-click on an ISO, you'll find an "Add ISO to grub" entry.
Choosing that will open the script and guide you through the process.

At boot, you should then find an entry in your grub menu for "whatever your ISO is called".

-------------------------------------------------------------------------------------------

This now checks if your /home is on a separate partition and corrects the entry accordingly.
It still won't work if the ISO is on external media.

NOTE: This works for Ubuntu-based distros, KDE neon and possibly a few others.
For other distros, you can use it to do most of the work, but you have to edit /etc/grub.d/40_custom and correct the location - within the ISO - of whatever /casper/initrd is called there.

To find out what and where it is, open the ISO with Ark (or whatever compression manager you use) and search for it.
