## Security and File Permissions ##

### WHAT: ###

Permission:
- applied sequentially user then group

Linux File Permissions:
- r = read = 4
- w = write = 2
- x = execute = 1

Directory Permissions:
- r = read = 4
- w = write = 2
- x = execute = 1
- \- = no permission = 0

Modifying File Permissions:
- chmod 775 file
- symbol eg. chmod u+rwx test-file
- numeric mode eg. chmod 775 test-file
---

```bash
# file types:
# d = directory
# - = regular file
# c = character device
# l = link
# s = socket file
# p = pipe
# b = block device

# Determine the type of file
[~]$ ls -l bash-script.sh

[~]$ ls -l <filename>
# owner(u) | group(g) | others(o)
# r = read = 4
# w = write = 2
# x = execute = 1
# -rwx-rwx-r-x

# Modifying File Permissions Symbolic Mode:
# Provide full access to owner
[~]$ chmod u+rwx test-file

# Provide read access to owner, group & others,
# Remove execute access
[~]$ chmod ugo+r-x test-file

# Remove all access for others
[~]$ chmod o-rwx test-files

# Full access for owner, add read, remove
# Execute for group and no access for others
# Provide full access to owner
[~]$ chmod u+rwx, g+r-x, o-rwx test-file

# Modifying File Permissions Numeric Mode:
# Provide full access to owner
[~]$ chmod 777 test-file

# Provide read and execute access to owners,
# groups and others
[~]$ chmod 555 test-file

# Read and write access for owner and group, no
# access for others
[~]$ chmod 660 test-file

# Full access for owner, read and execute for group
# and no access for others
[~]$ chmod 750 test-file

```

```bash
# Modifying File Permissions (Group)

# Changes owner to bob and group developer
[~]$ chown bob:developer test-file

# Changes just the owner of the file to bob. Group
# unchanged
[~]$ chown bob android.apk

# Change the group for the test-file to the group
# called android
[~]$ chgrp android test-file

```




