## Package Management ##

### WHAT: ###

### RPM and YUM ###
- DPKG & APT utility
- Working with DPKG:
    - Installation/ Upgrade
    - Uninstalling
    - List
    - Status
    - Verifying

- APT (advanced package managers) / APT-GET:
    - two different package managers
    - APT user friendly & better tool than APT-GET

- APT vs. APT-GET
    - APT: human readable output
    - better for searching; APT-GET needs to use apt=cache search <package> & still not human readable
---

### WHY: ###
- Install, Update, Upgrade and Remove package(s)

---

### HOW: ####
- See below
---

#### Basic Linux Commands ####

```bash
# Install package
[~]$ dpkg -i <package.deb>

# Uninstall package
[~]$ dpkg -r <package.deb>

# List package
[~]$ dpkg -l <package.deb>

# Check package status
[~]$ dpkg -s <package>

# Display package version
[~]$ dpkg -p <path to file> 

```

```bash
# Update package
[~]$ apt update

# Install package upgrade
[~]$ apt upgrade

# Update the repository
[~]$ apt edit-sources

# Install package
[~]$ apt install <package>

# Remove package
[~]$ apt remove <package>

# Search for package
[~]$ apt search <package>

# List all package
[~]$ apt list | grep <package>






```




