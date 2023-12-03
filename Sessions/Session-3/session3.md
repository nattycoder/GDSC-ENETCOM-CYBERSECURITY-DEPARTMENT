# Linux Essentials Session Documentation

## Introduction

Welcome to the Linux Essentials session! In this session, we covered fundamental Linux commands that are essential for navigating and managing files and directories in a Linux environment.
You will also find commands related to user management, processes, etc.

## Basic Commands

The `ls` command is used to list files and directories in the current directory.
```bash
$ ls
Alaa  Ranim  Adam  Wissem  Omar  Ilef  Khemais
```

`cat` command is used to concatenate and display the content of files.
```bash
$ cat passwords.txt
User: Alaa / Password: securepassword
User: Ranim / Password: strongpassword
```

The grep command is used to search for a specific pattern in a file.
```bash
$ grep "mayssa" students.txt
```

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
```

The cut command is used to remove sections from each line of a file.
```bash
$ cut -d" " -f1,2 cybersecurityEnthusiasts.txt
```

The `tr`command is used to translate or delete characters.
```bash
$ echo "yessin" | tr 'a-z' 'A-Z'
YESSIN
```

The `wc`command is used to count lines, words, and characters in a file.
```bash
$ wc welovecybersecurity.txt
```

The echo command is used to display a message on the screen.
```bash
$ echo "Hello, Ahmed!"
```

The mkdir command is used to create a new directory.
```bash
$ mkdir CybersecurityLinuxEssentials
```

The rmdir command is used to remove an empty directory.
```bash
$ rmdir empty_directory
```

The rm command is used to remove files or directories.
```bash
$ rm filename.txt
$ rm  -r not_an_empty_directory
```

The pwd command is used to print the current working directory.
```bash
$ pwd
/home/houda/Desktop
```

The cd command is used to change the current working directory.
```bash
$ cd /home/sarra/Documents
```

The touch command is used to create an empty file.
```bash
$ touch reasonstohatealaa.txt
```

The nano (or any other text editor) command is a simple text editor in the terminal.
```bash
$ nano why.txt
$ gedit you.txt
$ vi should.txt
$ vim love.txt
$ subl ranim.txt
$ pluma ourCo-lead.txt
etc...
```

The shred command is used to securely delete files.
```bash
$ shred -u sensitive_document.txt
```

The sudo command is used to execute a command as a superuser.
```bash
$ sudo apt-get update
$ sudo su Wael
etc...
```

The whatis command is used to display one-line manual page descriptions. (or use man, or --help)
```bash
$ whatis ls
$ ls man
```

The whereis command is used to locate the binary, source, and manual page files for a command.
```bash
$ whereis ls
```

The zip command is used to compress files, and unzip is used to decompress them.
```bash
$ zip riddles.zip riddle1 riddle2
$ unzip riddles.zip
```

The head command is used to display the first part of files.
```bash
$ head -n 5 filename.txt
```

The tail command is used to display the last part of files.
```bash
$ tail -n 5 filename.txt
```

The find command is used to search for files in a directory hierarchy.
```bash
$ find /path/to/search -name "file.txt"
```

## User Management and System Configuration Commands

The `useradd` command is used to add a new user to the system.
The adduser command is an interactive way to add a new user.
```bash
$ sudo useradd newuser
$ sudo adduser newuser
```

```bash
The usermod command is used to modify user information.
$ sudo usermod -c "New User" newuser
```

Managing user groups involves creating, modifying, and deleting groups.
```bash
$ sudo addgroup newsgroup
$ sudo usermod -aG newgroup username
$ sudo deluser username newgroup
```

The sudo group is used to grant superuser privileges to a user.
```bash
$ sudo usermod -aG sudo username
```

The visudo command is used to safely edit the sudoers file.
```bash
$ sudo visudo /etc/sudoers
```

The /etc/passwd file contains user account information.
```bash
$ cat /etc/passwd
```

The /etc/shadow file contains password information.
```bash
$ sudo cat /etc/shadow
```

The chmod command is used to change file permissions.
```bash
$ chmod +x filename
```

The chown command is used to change file or directory ownership.
```bash
$ sudo chown newuser:newgroup filename
```

The chsh command is used to change a user's login shell.
```bash
$ chsh -s /bin/bash username
```

Adding ALL = ALL in the sudoers file grants a user all privileges.
```bash
$ sudo visudo
# Add the following line:
username ALL = ALL
```

The groups command displays group memberships for a user.
```bash
$ groups username
```

****************************************************************

### Daemons, Services, Processes

A daemon is a background process that runs continuously. It is often initiated at the system boot and performs specific tasks.

`systemd` is the master daemon and the first process in the process tree. It is responsible for initializing the system.
```bash
$ sudo systemctl status systemd
```

The pstree command is used to display the process tree, including daemons, services, and processes.
```bash
$ pstree
```

The systemctl command is used to start, stop, restart, and check the status of services.
```bash
$ sudo systemctl start servicename
$ sudo systemctl stop servicename
$ sudo systemctl restart servicename
$ sudo systemctl status servicename
```








