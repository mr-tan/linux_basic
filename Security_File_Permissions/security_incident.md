## Security and File Permissions ##

### WHAT: ###
- Basic Security & Identifying File Types
- Creating Users & Groups
- Managing file permission & ownership
- Special Directories & Files

Linux Security:
- access control
- PAM
- network security
- SSH Hardening
- SELinux

Linux Accounts:
- user has username, UID, GID, home directory and default shell
- group: group of linux users, GID

Account Types"
- user account eg. bob 
- superuser account eg. root
- system accounts eg. ssh, mail
    - UID < 100 or btw 500 - 1000
- service accounts eg. ngnix

---

```bash
# Information about user account
[~]$ cat /etc/passwd

# Information about group
[~]$ cat /etc/group

# check user id
[~]$ id michael

# check group id
[~]$ grep -i michael /etc/passwd

# user, group information
[~]$ id

# user login
[~]$ who

# records of login users
[~]$ last

# Switching Users
[~]$ su -
root ~#

[~]$ su -c "whoami"

# Alt. switching users
[~]$ sudo

# User privilege specification
[~]$ cat /etc/sudoers

# Restrict root login
[~]$ grep -i ^root /etc/passwd

# Sudo file
# Review contents
[~]$ cat /etc/sudoers

# Access Control Files:
# Use built-in cmd to modify
# not text editor
# username:password:uid:gid:gecos:homedir:shell
[~]$ grep -i ^bob /etc/passwd

# Password file
# hash
# username:password:lastchange:minage:maxage:warn:incative:expdate
[~]$ grep -i ^bob /etc/shadow

# Information all user groups
# name:password:gid:members
[~]$ grep -i ^bob /etc/group

```


