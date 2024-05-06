## Linux Core Concepts ##

### WHAT: ###
Linux Boot Sequence Overview:

    1. BIOS Post
    2. Boot Loader (GRUB2)
    3. Kernel Initialization
    4. INIT process (systemd)

Systemd Targets: Runlevels

    1. 0 - poweroff.target
    2. 1 - rescue.target
    3. 2 - multi-user.target
    4. 3 - multi-user.target
    5. 4 - multi-user.target
    6. 5 - graphical.target
    7. 6 - reboot.target
---

### WHY: ###
- Learn Linux environment
---

### HOW: ####
- See below
---

#### Basic Linux Commands ####

```bash
# INIT Process
[~]$ ls -l /sbin/init
lrwxrwxrwx ... /sbin/init -> /lib/systemd/systemd

# Display Runlevel
# 5 - boots into a gui graphical.target
# 3 - boots into a cli multi-user.target 
[~]$ runlevel

# Viewing & Changing Systemd target
[~]$ systemctl get-default

# Display Systemd target
[~]$ ls -ltr /etc/systemd/system/default.target

# Switching Systemd target
[~]$ systemctl get-default multi-user.target

```


