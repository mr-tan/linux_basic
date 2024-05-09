## Linux Core Concepts 02 ##

### WHAT: ###
- Compressing & Archiving Files
---

### WHY: ###
- Manipulating files 
---

```bash
# Viewing file sizes
[~]$ du -sk <filename>

# Viewing file size hunman readable
[~]$ du -sh <filename>

# alternative way to show file size
[~]$ ls -lh <filename>

```

```bash
# Archiving Files
# Compressing files in tar (Tape Archive)
# -c = create the archive
# -f = file name
# -tf = to see the content
# -xf = extract file from tar
# -zcf = compress to reduce size

[~]$ tar -cf test.tar file1 file2 file3

# Alt. to view tar file
[~]$ ls -ltr test.tar

# Compressing file
[~]$ bzip2 test.img
[~]$ du -sh test.img.bz2

# Alt. way_01
[~]$ gzip test1.img
[~]$ du -sh test1.img

# Alt. way 02
[~]$ xz test2.img
[~]$ du -sh test2.img.xz

# Uncoompressing file
[~]$ bunzip2 test.img.bz2
[~]$ du -sh test.img.bz2

[~]$ gunzip test1.img.gz
[~]$ du -sh test1.img.bz2

[~]$ unxz test2.img.xz
[~]$ du -sh test2.img.bz2

# Read files w/o uncompressing them
[~]$ zcat 
[~]$ bzcat
[~]$ xzcat
```

