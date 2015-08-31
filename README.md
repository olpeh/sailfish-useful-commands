SailfishOS Useful Commands
==========================

Commands that are not so easy to remember

Feel free to add stuff

## PLEASE BE AWARE WHEN RUNNING THESE COMMANDS! THEY MIGHT BRICK YOUR PHONE! ONLY USE THEM IF YOU KNOW WHAT YOU ARE DOING!

### Open
xdg-open

### Reversing applied patches
devel-su

patch -R -p 1 -d / -i /var/lib/patchmanager/ausmt/patches/{patchname}/unified_diff.patch
- ignore "already unapplied" ones

### Restart android VM
devel-su

systemctl restart aliendalvik.service

### Send SMS from command line
For example sending and SMS to +358500000000:

dbus-send --system --print-reply --dest=org.ofono /ril_0 org.ofono.MessageManager.SendMessage string:"+358500000000" string:"test sms" 

HARBOUR-proof version: 

dbus-send --type=method_call --dest=org.nemomobile.qmlmessages / org.nemomobile.qmlmessages.startSMS array:string:"+358123456" string:"Hello world" 

### Manually run BTRFS balance
??? btrfs fi balance /home ??? 

### Battery status
upower -i /org/freedesktop/UPower/devices/battery_battery

upower -d

### Journalctl (~ Syslog)
devel-su 

journalctl

### Media player from CLI
gst-launch-0.10 playbin2 uri=file:///path/to/file/music.mp3
