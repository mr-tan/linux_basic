## Basic Linux Commands ##

### WHAT: ###
- Learning basic linux commands
---

### WHY: ###
- Navigate inside the shell
---

### HOW: ####
- See below
---

#### Basic Linux Commands ####

```bash
# pwd (present working directory)
[~]$ pwd
/home/mark

# ls (list content)
[~]$ ls

# ls -L (long list)
[~]$ ls -l

# ls -a (list all files including hidden)
[~]$ ls -a

# ls -lt (list all files in order created)
[~]$ ls -lt

# ls -ltr (list all files in reverse order)
[~]$ ls -ltr

# mkdir (make a new directory)
[~]$ mkdir folder_01
[~]$ mkdir folder_01/folder_02
[~]$ mkdir -p folder_01/folder_02

# cd (change directory)
[~]$ cd folder
[~]$ cd ..
[~]$ cd 
[~]$ cd folder_02/folder_01

# absolute path
# start from root directory (/)
[~]$ cd /home/mt/documents

# relative path
[~]$ cd downloads
# pushd/popd
[~]$ pushd /home
[~]$ cd /tmp
[~]$ popd

# mv (move file or directory)
[~]$ mv /home/mt/documents /home/mt/other_documents

# cp (copy file)
[~]$ cp /home/mt/file_01.txt /home/mt/chap_01/

# cp -r (copy directory)
[~]$ cp -r /home/mt/documents

# rm (remove file or directory)
[~]$ rm file_01.txt

```

#### Working with Files & Directories ####

```bash
# cat (read file content)
[~]$ cat /home/mt/documents/city.txt

# cat (redirect)
[~]$ cat > /home/mt/documents/city.txt
# ctrl + d

# touch (create new file)
[~]$ touch /home/mt/documents/notes.txt

```

#### Pagers ####

```bash
# more
# [space] - scrolls one screenful of data
# [enter] - scrolls one line
# [b] - scrolls backward
# [/] - search text
[~]$ more new_file.txt

# less 
# [up arrow] - scroll up one line
# [down arrow] - scroll down one line
# [/] - search text
[~]$ less new_file.txt

```


