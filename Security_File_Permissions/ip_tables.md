## Security and File Permissions ##

### WHAT: ###

Network Security

IPTABLES
- filters traffic in the work
- RHEL & CentOS already installed
- Debian have to manually install

Chain INPUT (policy accept)
target prot opt source      destination
- network traffic incoming to the system

Chain FORWARD (policy accept)
target prot opt source      destination
- network router data forwarded to other devices

Chain OUTPUT (policy accept)
target prot opt source      destination
- connection to other servers to other systems

Chain:
- each chain have multiple rules
- accept or drop packet
- implemented from top to bottom


---

```bash
# Install iptables
[~]$ sudo apt install iptables

# List iptable rules
[~]$ sudo iptables -L

# IPTABLES Options
# -A = add rule
# -p = protocol
# -s = source
# -d = destination
# --dport = destination port
# -j = action to take
#
# Accept rule in iptable
[~]$ iptables -A INPUT -p tcp -s 172.16.238.187 --dport 22 -j ACCEPT

# Show IPTABLES rule implemented
[~]$ iptables -L

# Change iptable rules
[~]$ iptables -A INPUT -p tcp --dport 22 -j DROP

# Show IPTABLES rules implemented
[~]$ iptables -L

# Review implemented rules
[~]$ iptables -A OUTPUT -p tcp -d 172.16.238.11 --dport 5432 -j ACCEPT
[~]$ iptables -A OUTPUT -p tcp -d 172.16.238.15 --dport 80 -j ACCEPT
[~]$ iptables -A OUTPUT -p tcp --dport 443 -j DROP
[~]$ iptables -A OUTPUT -p tcp --dport 80 -j DROP
[~]$ iptables -A INPUT -p tcp -s 172.16.238.187 --dport 80 -j DROP

# Show IPTABLES rules implemented
[~]$ iptables -L

# Insert IPTABLES rules
[~]$ iptables -I OUTPUT -p tcp -d 172.16.238.100 --dport 443 -j ACCEPT

# Delete IPTABLES rules:
[~]$ iptables -D OUTPUT 5

# Add IPTABlES rules
# 172.16.238.10 DEVAPP01
[~]$ iptables -A INPUT -p tcp -s 172.16.238.11 --dport 5432 -j ACCEPT

# 172.16.238.11 DBSERVER
[~]$ iptables -A INPUT -p tcp -s 172.16.238.10 --dport 5432 -j ACCEPT

# Drop all other connection
[~]$ iptables -A INPUT -p tcp --dport 5432 -j DROP

# Show IPTABLES rules implemented
[~]$ iptables -L

# Prove communication between DevApp & DbServer
# Show IPTABLES rules implemented
[~]$ netstat -an | grep 5432

# Ephemeral Port Range
# 32768 - 60999

```




