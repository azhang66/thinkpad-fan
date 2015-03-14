# thinkpad-fan
An automated fan control daemon for ThinkPads

OVERVIEW

 thinkpad-fan controls your ThinkPad's fan. It will set your fan to different levels depending on the temperature of your ThinkPad.
 
INSTALLATION

 1. Download a .zip of thinkpad-fan from GitHub
 2. Unzip it to a directory where only root can modify
 3. Change the owner of all the files to root
 4. Change the files to all be read-only
 5. Add this line to /etc/rc.local:
 
    /bin/bash /path/to/thinkpad-fan/fand &
    
 6. The line after that line should be
 
    exit 0
    
 7. Make sure the "fand" and "settings" files are executable
 8. For thinkpad-fan to work, you will need to create a file in "/etc/modprobe.d/" named "thinkpad_acpi.conf"
 9. Add the following line to "thinkpad_acpi.conf"
 
    options thinkpad_acpi fan_control=1

 10. Reboot to take effect
 
USAGE

 1. Install the program
 2. Configure it as you desire. Configuration information in the "settings" files
 3. Enjoy!
 
TROUBLESHOOTING

 Permission Denied errors:
   This may mean that either the "fand" process isn't running as root, or something else is wrong. Make sure that you are running the script as root.
   
 Cannot find file errors:
   This may mean that either your computer's fan control files or your computer's temperature files do not exist in the place thinkpad-fan looks in.
   Please locate the right file(s) and manually edit the "fand" script.
 
ISSUES

Please report issues to: albertzhang66@outlook.com
Thanks!!