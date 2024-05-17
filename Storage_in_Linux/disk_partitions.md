## Storage in Linux ##

### WHAT: ###

Partition Types:
- primary partition
- extended partition
- logical partition

Partition Scheme: MBR
- Four primary
- Local partitions within Extended partition
- Max. disk size is 2 TB per partition

Partition Scheme: GUID partition table (GPT)
- No max size per partition
- Unlimited partitions
---

```bash

# Major Number | Device Type
# 1 = RAM
# 3 = Hard Disk or CD Rom
# 6 = Parallel Printers
# 8 = SCSI Disk
#
# List block storage
[~]$ ls blk

# List in storage
[~]$ ls -l /dev/ | grep "^b"

# List, create & delete partitions
[~]$ sudo fdisk  -l /dev/sda

```

```bash

# List disk partitions
[~]$ lsblk

# Creating partitions
# gdisk improved version of fdisk
# in Gparted
# 
[~] sudo gdisk /dev/sdb

# Inside GDisk
# Command Options
# ? = List all the options
# n = create new partition
# 1 = partition number
# First sector: +20G
# Last sector: accept default
# *Hex code or GUID Enter = 8300 Linux filesystem
# W = Write to the partition table
# Y = to confirm

# Check the status partition
[~]$ sudo fdisk -l /dev/sdb

```


