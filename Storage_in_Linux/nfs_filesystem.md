## Storage in Linux ##

### WHAT: ###

Network Filesystem (NFS):

- saving data in files
- server-client model
- exporting: term for directory sharing in NFS
---

```bash
# Export Config File
# /software/repos 10.61.35.201 16.61.35.202
#
[~]$ /etc/exports


# Exports all the mounts defined
# /etc/exports
[~]$ exportfs -a 

# Manually export a directory
[~]$ exportfs -o 10.61.35.201:/software/repos

# After export, mounting to local directory
[~]$ mount 10.61.112.101:/software/repos /mnt/software/repos

```


