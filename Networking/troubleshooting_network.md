## Troubleshooting Network ##

### WHAT: ###

- Networking connection troubleshooting steps
---

### WHY: ###
- Troubleshooting networking communication
---

```bash
# Check local primary interface
[~]$ ip link

# check host name (dns) resolution
[~]$ nslookup caleston-repo-01

# check connectivity with remote server
[~]$ping caleston-repo-01

# check route
[~]$ traceroute 192.168.2.5

# check services
[~]$ netstat -an | grep 80 | greip -i LISTEN

# check the interface
[~]$ ip link

# interface is down in server & bring back up
[~]$ ip link set dev enp1s0f1 up

```


