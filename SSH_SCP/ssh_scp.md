## Basic Linux Commands ##

### WHAT: ###
SSH:
- SSH (port 22) - used for logging into & executing commands on a remote computer

Password-less SSH;
- generate key pairs (eg. private & public)
- copy public key to remote server

SCP:
- SCP - allows to copy files and directories in the file system in linux; copy 
data over SSH

```bash
# Remotely logging into a computer
[~]$ ssh <hostname or IP Address>

# SSH as username to host
[~]$ ssh <user>@<hostname or IP Address>
[~]$ ssh -l <user> <hostname or IP Address>

# Setup password-less SSH
[~]$ ssh-keygen -t rsa

# Copy public key to remote server
[~]$ ssh-copy-id bob@devapp01

# Access w/o password
[~]$ ssh devapp01

# Where the bob's public key in remote server
[~]$ cat /home/bob/.ssh/authorized_keys

```

```bash
# Copying files using SCP
[~]$ scp /home/bob/caleston-code.tar.gz devapp01:/home/bob

# Copying directory using SCP
[~]$ scp -pr /home/bob/media devapp01:/home/bob


```

