## SYSTEMD and Service Management ##

### WHAT: ###
Introduction to SYSTEMD:
- 

Create your own SYSTEMD service
- 

SYSTEMD Tools
- 
---

### WHY: ###
- Navigate inside the shell
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

# Start systemd
[~]$ sudo systemctl start project-mercury.service

# Check project status
[~]$ sudo systemctl status project-mercury.service

# Stop systemd
[~]$ sudo systemctl stop project-mercury.service

# Enable systemd
[~]$ sudo systemctl enable project-mercury.service

# Systemd will notice changes
[~]$ sudo systemctl daemon-reload

# Show log error list
[~]$ sudo journalctl -u project-mercury.service


```


