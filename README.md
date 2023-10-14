# Cyclone's Proxmox VM / LXC Watchdog
~~Release coming soon.~~

_`The public release of Proxmox VM Watchdog is on hold. An alternative is Proxmox VE Monitor-All:`_ https://tteck.github.io/Proxmox/

### Features:
- Monitor VM & LXC
- Auto reboot if VM / LXC fails to respond to ping on specified port(s)

### Options:
- -vm 
- - specify ID of VM / LXC
- -ip 
- - specify VM IP address
- -port 
- - comma separated port(s) to monitor
- -interval 
- - interval in seconds to check VM for uptime
- -checks 
- - how many consecutive checks must be missed before marking VM as offline and issuing reboot command
- -wait 
- - how many seconds to wait after reboot command is issued before restarting watchdog

### Usage Example:
- ./watchdog.bin -vm 100 -ip 10.0.0.100 -port 22
- ./watchdog.bin -vm 100 -ip 10.0.0.100 -port 22,443,8080 -interval 2 -checks 60 -wait 300

Compile from source code info:
- https://github.com/cyclone-github/scripts/blob/main/intro_to_go.txt
