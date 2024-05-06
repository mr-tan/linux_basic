## Linux Core Concepts ##

### WHAT: ###
- File Types in Linux:
    1. Regular file (eg. images, scripts, configuration/ data files)
    2. Directory (eg. /home/bob)
    3. Special Files (eg. character files, block files, links, socket, named pipes)
---

### WHY: ###
- Learn about environment
---

### HOW: ####
- See below
---

#### Basic Linux Commands ####

```bash
# Id file types
[~]$ file /home/bob

[~]$ file bash-script.sh

[~]$ file insync1000.sock

# Symbolic link
[~]$ file /home/bob/bash-script

# d -directory, - regular file, c - character
# l - link, s - socket file, p - pipe, b - block device
[~]$ ls -ld /home/bob

drwxrwxr-x 2 mt mt 4096 May  6 01:59


```


