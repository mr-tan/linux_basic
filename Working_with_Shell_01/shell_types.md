## Shell Types ##

### WHAT: ###
- Learn Shell Types
---

### WHY: ###
- Shell Types:
    - Bourne Shell (sh)
    - C Shell (csh or tcsh)
    - Korn Shell (ksh)
    - Z Shell (zsh)
    - Bourne again Shell (bash)
        1. auto-completion
        2. alias
        3. history command
        4. environment variables eg. $SHELL

---

### HOW: ####
- See below
---

#### Basic Linux Commands ####

```bash
# display shell type 
[~]$ echo $SHELL 

# change shell type
[~]$ chsh

# display all environment variables
[~]$ env

# set environment variable
[~]$ echo export OFFICE=bob >> /home/bob/.profile

# set alias
[~]$ echo 'alias up=uptime' >> ~bob/.profile

# just in the shell
[~]$ OFFICE=bob

# make perm. variable
[~]$ ~/.profile or ~/.pam_environment

# path variable
[~]$ echo $PATH

# show path of application
[~]$ which git

# add path of application
[~]$ export PATH=$PATH:/opt/<folder>/<application>

# bash prompt
# ~ = present working directory
# $ = user prompt symbol
[~]$

# $PS1 for custom prompt
# \W = present working directory
# $ = prompt symbol
[~]$ echo $PS1
[\W]$

# change bash prompt
[~]$ echo 'PS1="[\d]\u@\h:\w$"' >> ~bob/.profile
[~]$ PS1="ubuntu-server:"







```


