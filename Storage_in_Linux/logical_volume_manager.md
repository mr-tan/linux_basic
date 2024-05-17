## Storage in Linux ##

### WHAT: ###

Logical Volume Manager (LVM)

- allows grouping of multiple physical volume (partitions)
- can resize dynamically with extra space available
-

---

```bash
# Need to setup LVM
[~]$ sudo apt-get install lvm2

# Physical Volume (PV)
[~]$ pvcreate /dev/sdb

# Volume Group (VG)
[~]$ vgcreate caleston_vg /dev/sdb

# Display Physical Volume Group
[~]$ pvdisplay

# Display Volume Group
[~]$ vgdisplay

# Create Logical Volume
[~]$ lvcreate -L 1G -n vol1 caleston_vg

# Display Logical Volume
[~]$ lvdisplay

# Display Logical Volume 
[~]$ lvs

# Create Filesystem
[~]$ mkfs.ext4 /dev/caleston_vg/vol1

# Mounting Volume
[~]$ mount -t ext4 /dev/caleston_vg/vol1 /mnt/vol1
```
```bash

# Resize mnt/vol1
#
# Display Volume Group 
# check for enough space
#
[~]$ vgs 

# Resizing Logical Volume
[~]$ lvresize -L +1G -n /dev/caleston_vg/vol1

# View filesystem
[~]$ df -hP /mnt/vol1

# Resize file system
[~]$ resize2fs /dev/caleston_vg/vol1

# View updated filesystem
# vol1 /dev/caleston_vg/vol1
# vol1 /dev/mapper/caleston_vg-vol1
# both filesystem are the same
#
[~]$ df -hP /mnt/vol1






```


