## Security and File Permissions ##

### WHAT: ###

Managing Users
- Add user(s)
- Remove user(s)

---

```bash
# Add new user
[~]$ useradd bob

# Show detail about bob
[~]$ grep -i bob /etc/pwd

# Show password for bob
[~]$ grep -i bob /etc/shadow

# Set bob password
[~]$ passwd bob

# Example with options
# -c = custom comments
# -d = custom home directory
# -e = expiry date
# -g = specifi GID
# -G = create user with multiple secondary groups
# -s = specify login shells
# -u specific UID
[~]$ useradd -u 1009 -g 1009 -d /home/robert -s /bin/bash -c "Mercury Project member" bob

# View custom field
[~]$ id bob

# View bob's custom field
[~]$ grep -i bob /etc/passwd

```

```bash
# Delete user
[~]$ userdel bob

# Add new group
[~]$ groupadd -g 1011 developer

# Delete group
[~]$ groupdel developer

```


