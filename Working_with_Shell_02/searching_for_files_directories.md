## Linux Core Concepts 02 ##

### WHAT: ###
- Searching for files & directories
---

### WHY: ###
- Locating files & directories
---

```bash
# update file location database
[~]$ updatedb

# Searching for file_01
[~]$ locate filename

# Searching for file_02
[~]$ find /home/bob -name <filename>

# Searching for keyword
[~] grep keyword <filename>

# cmd case insensitive
[~]$ grep -i keyword <filename>

# cmd searching recursive in directory
[~]$ grep -r "keyword" /home/bob

# cmd print that does not match pattern
[~]$ grep -v "keyword" <filename>

# cmd searching whole word
[~]$ grep -w keyword <filename>

# combine cmd
[~]$ grep -wv

# view content after keyword
[~]$ grep -A1 keyword <filename>

# view content before keyword
[~]$ grep -B1 keyword <filename>

# view content before/after keyword
[~]$ grep -A1 -B1 keyword <filename>




```
