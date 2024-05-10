## Working with Shell 02 ##

### WHAT: ###
- IO redirection
- data stream:
    - standard input 
    - standard output
    - standard error
---

### WHY: ###
- Redirect input & output
---

### HOW: ####
- See below
---

```bash
# Redirect Standard Output
[~]$ echo $SHELL > shell.txt

# Append 
[~]$ echo "This is a Bash shell" >> shell.txt

# Redirect Standard Error
[~]$ cat missing_file 2> error.txt

# Append Standard Error
[~]$ cat missing_file >> shell.txt

# Do not print Standard Error
[~]$ cat missing_file 2> /dev/null

```

```bash
# Command Line Pipes
[~]$ grep Hello sample.txt | less

[~]$ echo "This is the bash shell" | tee -a shell.txt

```


