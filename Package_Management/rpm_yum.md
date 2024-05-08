## Package Management ##

### WHAT: ###

### RPM and YUM ###
- Used in RHEL, CentOS & Fedora
- Red Hat Package Manager (RPM)
    - .rpm
---

### WHY: ###
Used for:
- Installation
- Uninstalling
- Upgrade
- Query
- Verifying
---

### HOW: ####
- See below
---

#### Basic Linux Commands ####

```bash
# Installing package
[~]$ rpm -ivh telnet.rpm

# Uninstalling package
[~]$ rpm -e telnet.rpm

# Upgrading package
[~] rpm -Uvh telnet.rpm

# Query the package
[~]$ rpm -q telnet.rpm

# Verify the package
[~]$ rpm -Vf <path to file>

```


