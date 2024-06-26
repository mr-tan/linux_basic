## Linux Core Concepts ##

### WHAT: ###
- Introduction to the Linux Kernel:
    1. memory management
    2. process management
    3. device drivers
    4. system calls & security
    5. monolithic
    6. modular

- Kernel Space and User Space
- Working with Hardware
- Linux Boot Sequence
- SYSTEMD TARGETS(RUNLEVELS)
- Filesystems and Hierarchy
---

### WHY: ###
- linux core concepts
---

#### HOW: ####

```bash
# Kernel versions
[~]$ uname

[~]$ uname -r
# 6 = kernel version
# 8 = major version
# 0 = minor version
# 76.00daily = patch release
# generic = distro specific info
6.8.0-76060800daily20240311-generic
```
```bash
# Working with hardware
[~]$ dmesg

# Query device information
[~]$ udevadm info --query=path --name=/dev/sda5

# Info attached/remove device
[~]$ udevadm monitor

# List all pci devices 
[~]$ lspci

# List block devices: eg. sda1
[~]$ lsblk

# Cpu info
[~]$ lscpu

# List memory
[~]$ lsmem --summary

# Free memory
[~]$ free -m

# Detail hardware config
[~]$ lshw 

```


