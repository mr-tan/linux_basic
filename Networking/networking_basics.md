## Networking ##

### WHAT: ###
Linux Networking Basic

Switching:
- communicating on the network  

Router/ Routing:
- connection two different system on the same network

Gateway:
- doorway to section the network
---

### WHY: ###
- Troubleshooting network communication
---

```bash
# Switching
[~]$ ip link

# Setup computers to talk to
# each other thru a switch
# compu_01
[~]$ ip addr add 192.168.1.10/24 dev eth0

# ping compu_02
[~]$ ping 192.168.1.11

# compu_02
[~]$ ip addr add 192.168.1.11/24 dev eth0

# Router
# ip addresses:
# 192.168.1.1
# 192.168.2.1

# Internet 
# 172.217.194.0

# Gateway/ Door
[~]$ route

# Add a Gateway
[~]$ ip route add 192.168.2.0/24 via 192.168.1.1

# Add a route
[~]$ ip route add 192.168.1.0/24 via 192.162.2.1

# Delete a route
[~]$ sudo ip r del default

# default router
[~]$ ip route add default via 192.168.2.1

# Commands
# list interface on the host
[~]$ ip link

# list ip address assist to the interfaces
[~]$ ip addr

# set ip address to the interfaces
[~]$ ip addr add 192.168.1.0/24 dev eth0

# view routing table
[~]$ route

# add ip to the ip route table
[~]$ ip route

# Review bring up eth0
[~]$ sudo ip link set dev eth0 up

```


