# Linux Essentials Session Documentation

## Introduction

Welcome to the Linux Essentials session! In this session, we covered fundamental Linux commands that are essential for navigating and managing files and directories in a Linux environment.
You will also find commands related to user management, processes, etc.

## Basic Commands

### 1. `ls` - List Directory Contents

The `ls` command is used to list files and directories in the current directory.

```bash
$ ls
Alaa  Ranim  Adam  Wissem  Omar  Ilef  Khemais

`cat` command is used to concatenate and display the content of files.
```bash
$ cat passwords.txt
User: Alaa / Password: securepassword
User: Ranim / Password: strongpassword

The grep command is used to search for a specific pattern in a file.
```bash
$ grep "mayssa" students.txt

The sort command is used to sort lines of text.
```bash
$ sort cybersecurityStudents.txt
Adam
Emna
Fourat
Ismail
Lamis
Youssef
Zaineb

The cut command is used to remove sections from each line of a file.
```bash
$ cut -d" " -f1,2 cybersecurityEnthusiasts.txt

The `tr`command is used to translate or delete characters.
```bash
$ echo "yessin" | tr 'a-z' 'A-Z'
YESSIN

The `wc`command is used to count lines, words, and characters in a file.
```bash
$ wc welovecybersecurity.txt

The echo command is used to display a message on the screen.
```bash
$ echo "Hello, Ahmed!"

The mkdir command is used to create a new directory.
```bash
$ mkdir CybersecurityLinuxEssentials

The rmdir command is used to remove an empty directory.
```bash
$ rmdir empty_directory

The rm command is used to remove files or directories.
```bash
$ rm filename.txt
$ rm  -r not_an_empty_directory

The pwd command is used to print the current working directory.
```bash
$ pwd
/home/houda/Desktop

The cd command is used to change the current working directory.
```bash
$ cd /home/sarra/Documents

The touch command is used to create an empty file.
```bash
$ touch reasonstohatealaa.txt

The nano (or any other text editor) command is a simple text editor in the terminal.
```bash
$ nano why.txt
$ gedit you.txt
$ vi should.txt
$ vim love.txt
$ subl ranim.txt
$ pluma ourCo-lead.txt
etc...

The shred command is used to securely delete files.
```bash
$ shred -u sensitive_document.txt

The sudo command is used to execute a command as a superuser.
```bash
$ sudo apt-get update
$ sudo su Wael
etc...

The whatis command is used to display one-line manual page descriptions. (or use man, or --help)
```bash
$ whatis ls
$ ls man

The whereis command is used to locate the binary, source, and manual page files for a command.
```bash
$ whereis ls

The zip command is used to compress files, and unzip is used to decompress them.
```bash
$ zip riddles.zip riddle1 riddle2
$ unzip riddles.zip

The head command is used to display the first part of files.
```bash
$ head -n 5 filename.txt

The tail command is used to display the last part of files.
```bash
$ tail -n 5 filename.txt


The find command is used to search for files in a directory hierarchy.
```bash
$ find /path/to/search -name "file.txt"

**************************************************************

## User Management and System Configuration Commands

### 26. `useradd` - Add a User

The `useradd` command is used to add a new user to the system.

```bash
$ sudo useradd newuser
$ sudo adduser newuser

$ sudo usermod -c "New User" newuser

$ sudo addgroup newgroup
$ sudo usermod -aG newgroup username
$ sudo deluser username newgroup

$ sudo usermod -aG sudo username

$ sudo visudo /etc/sudoers

$ cat /etc/passwd

$ sudo cat /etc/shadow

$ chmod +x filename

$ sudo chown newuser:newgroup filename

$ chsh -s /bin/bash username

$ sudo visudo
# Add the following line:
username ALL = ALL

$ groups username

****************************************************************

### 39. Daemons

A daemon is a background process that runs continuously. It is often initiated at the system boot and performs specific tasks.

### 40. `systemd` - Master Daemon

`systemd` is the master daemon and the first process in the process tree. It is responsible for initializing the system.

```bash
$ sudo systemctl status systemd

$ pstree

$ sudo systemctl start servicename
$ sudo systemctl stop servicename
$ sudo systemctl restart servicename
$ sudo systemctl status servicename








