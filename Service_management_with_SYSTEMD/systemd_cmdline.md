## SYSTEMD and Service Management ##

### WHAT: ###
Introduction to SYSTEMD:
- 

Create your own SYSTEMD service
- 

SYSTEMD Tools:

- SYSTEMCTL:
    - manage system state
    - start/ stop/ restart
    - enable/ disable
    - list and manage units
    - list and update targets

- JOURNALCTL:
    - query SYSTEMD journal

---

### WHY: ###
- Running service(s) in the background process
---

### HOW: ####
- See below
---

```bash

# Define as a service unit file
# Automatically log 

[~]$ /etc/systemd/system/project-mercury.service

[Unit]
Description=Python Django for Project Mercury
Documentation=http://wiki.caleston-dev.ca/mercury
After=postgresql.service

[Service]
ExecStart= /bin/bash /usr/bin/project-mercury.sh
User=project_mercury
Restart=on-failure
RestartSec=10

[Install]
WantedBy graphical.target
```

```bash

# Service Management with SystemMD
#
# Start
[~]$ sudo systemctl start docker.service

# Stop 
[~]$ sudo systemctl stop docker.service
docker.service# Restart 
[~]$ sudo systemctl restart docker.service

# Reload
[~]$ sudo systemctl reload docker.service

# Enable service and persistent across reboot
[~]$ sudo systemctl enable docker.service

# Disable service at boot
[~]$ sudo systemctl disable docker.service

# Check service status
# Read state
# Active = Service Running
# Inactive = Service Stopped
# Failed = Crashed/Error/Timeout e.t.c
#
[~]$ sudo systemctl status docker.service

# Systemd will notice changes
[~]$ sudo systemctl daemon-reload

# Edit Systemd
[~]$ sudo systemctl edit docker.service --full

# Get current run-level
[~]$ sudo systemctl get-default

# Change target
[~]$ sudo systemctl set-default multi-user.target

# List all units
[~]$ sudo systemctl list-units --all

# Show log error list
[~]$ sudo journalctl -u docker.service

#
[~]$ sudo journalctl -b

#
[~]$ sudo journalctl -u UNIT



```


