# SailfishOS Useful Commands
## Commands that are not so easy to remember
Feel free to add stuff

### Reversing applied patches
devel-su; patch -R -p 1 -d / -i /var/lib/patchmanager/ausmt/patches/{patchname}/unified_diff.patch
ignore "already unapplied" ones

### Battery status
upower -i /org/freedesktop/UPower/devices/battery_battery

### Journalctl (~ Syslog)
as devel-su: 
journalctl
