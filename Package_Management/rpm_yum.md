## Package Management ##

### WHAT: ###

### RPM and YUM ###
- Used in RHEL, CentOS & Fedora
- Red Hat Package Manager (RPM)
    - .rpm
- YUM Package Manager (yellowdog updater, modified)
    - works w/ RPM based distro
    - software repositories
    - /etc/yum.repos.d .repo extension
    - high level package manager
    - automatic dependency resolution
    
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
# Installing RPM package
[~]$ rpm -ivh telnet.rpm

# Uninstalling package
[~]$ rpm -e telnet.rpm

# Upgrading package
[~] rpm -Uvh telnet.rpm

# Query the package
[~]$ rpm -q telnet.rpm

# Verify the package
[~]$ rpm -Vf <path to file>

# search
[~]$ rpm -qa | grep wget

```

```bash
# Repo list
[~]$ yum repolist

# package need to install for specific cmd to work
[~]$ yum provides <cmd>

# Remove package
[~]$ yum remove <package>

# Update single package
[~]$ yum update <package>

# Update all package in the system
[~]$ yum update

# Identify the package which provide
# particular library file
[~]$ yum whatprovides [file_name]


```


