## File Systems in Linux ##

### WHAT: ###

Linux Filesystem:

EXT2:
- 2 TB file size
- 4 TB volume size
- Supports Compression
- Supports Linux Permissions
- Long Crash Recovery

EXT3:
- 2 TB file size
- 4 TB volume size
- Use journal
- Backwards Compatible

EXT4:
- 16 TB file size
- 1 Exabyte
- Uses journal
- Uses chksum for journal
- Backwards Compatible
---

```bash

# Working with EXT4
# 
# Creating EXT4 filesystem
[~]$ mkfs.ext4 /dev/sdb1

# New directory for filesystem
[~]$ mkdir /mnt/ext4;

# Mount new filesystem
[~]$ mount /dev/sdb1 /mnt/ext4

# Check filesystem is mounted OR
[~]$ mount | grep /dev/sdb1

# Use df to verify filesystem is mounted
[~]$ df -hP | grep /dev/sdb1

# Show type of filesystem
[~]$ sudo blkid /dev/vdc

# filesystem = /dev/vdb1
# mount point = directory to be mounted on "/"
# type = ext2, ext3, ext4
# options = rw = Read-Write, ro = Read Only
# dump = 0 = ignore, 1 = take backup
# pass = 0 = ignore, 1 or 2 = FSCK filesystem check enforced
# Filesystem available after reboot
# add to /etc/fstab
#
[~]$ sudo vi /etc/fstab
# add line in vi "/dev/vdb /mnt/data ext4 rw 00"
# save changes & exit

```


