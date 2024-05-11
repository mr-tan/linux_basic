## Networking ##

### WHAT: ###
Linux Networking Basics
- DNS
- Domain Names:
    - .com - commercial or general purpose
    - .net - network or general purpose
    - .edu - education
    - .org - non-profit
- Domain:
    - root
    - sub-domain
    - domain

- Networking Basics
- Troubleshooting
---

### WHY: ###
- Understanding network architecture
---

### HOW: ####
- See below
---

```bash
# Test connection
[~]$ ping 192.168.1.11

# Using name (db) instead 
# ip address
[~]$ cat >> /etc/hosts
192.168.1.11    db
192.168.1.11    www.google.com

# Name resolution
# ping dns
[~]$ ping db
[~]$ ssh db
[~]$ curl http://www.google.com

# DNS resolution file
[~]$ cat /etc/resolv.conf
nameserver  192.168.1.100   #dns server

# Review DNS logic
[~]$ cat >> /etc/hosts
192.168.1.115   test

[~]$ cat /etc/nsswitch.conf
hosts:  files dns

# nslookup
[~]$ nslookup www.google.com
[~]$ dig www.google.com

```


