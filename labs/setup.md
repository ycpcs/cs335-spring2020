---
layout: default
course_number: CS335
title: Lab Setup
---

Labs
-----------------------------------
- Hands-on [Labs](http://www.cis.syr.edu/~wedu/seed/Labs_16.04/) for Security Education.

Lab Setup
-----------------------------------
- [Oracle® VM VirtualBox](https://www.virtualbox.org/wiki/Downloads) is a general-purpose full virtualizer for x86 hardware, targeted at server, desktop and embedded use. User Manual can be found [here](https://www.virtualbox.org/manual/).

-  Pre-built Virtual Machine [SEED Ubuntu 16.04 VM](https://drive.google.com/file/d/12l8OO3PXHjUsf9vfjkAf7-I6bsixvMUa/view?usp=sharing).

- Follow [Run SEED VM on VirtualBox](http://www.cis.syr.edu/~wedu/seed/Labs_16.04/Documents/SEEDVM_VirtualBoxManual.pdf) to load the image into VirtualBox.

- [User Manual](http://www.cis.syr.edu/~wedu/seed/Documentation/Ubuntu16_04_VM/Ubuntu16_04_VM_Manual.pdf) includes the account and password information, list of software and servers installed, and configuration.

Troubleshooting
-----------------------------------
- The first thing you should do after creating your SEED VM is to update your packages; to do that, run the following two commands from your VM:
  - ```sudo apt update```
  - ```sudo apt upgrade```
- If the guest screen is too small:
  - With VirtualBox 6.0.0 you need to go to the VirtualBox Preferences » Display » Scale Factor = 200%.
- When you clone your VM's, make sure the MAC Address Policy is set to __Generate new MAC addresses for all network adapters__.

Cheat Sheets
-----------------------------------
#### Networking
- ```ifconfig -a``` displays all network interfaces and IP address.
- ```hostname -I``` displays the IP addresses of the host (all local IP addresses).
- ```host domain``` displays IP address for _domain_.
- ```ping host``` sends ICMP echo request to _host_.
- ```whois domain``` displays whois records for _domain_.
- ```dig domain``` displays DNS information for _domain_.
- ```dig -x IP``` does reverse lookup of _IP_ address.  

#### User Management
- Local user information is stored in the /_etc/passwd_ file. Get the list of all users using ```cat /etc/passwd```. The fields are delimited by colons and contain the following:
  - User name
  - Encrypted password (x means that the password is stored in the ```/etc/shadow``` file)
  - User ID number (UID)
  - User's group ID number (GID)
  - Full name of the user (GECOS)
  - User home directory
  - Login shell (defaults to /bin/bash)
- ```id``` display the user and group ids of your current user.
- ```groupadd attacker``` created a group named _attacker_
- ```useradd -c "John Doe" -m john``` creates an account names _john_ with a comment of _John Doe_.
- ```userdel john``` deletes the _john_ account.
  - ```rm -r /home/john``` will delete the home directory of the _john_ account
  - ```su``` temporarily become the superuser.

#### File and Directory
- ```cd``` go to _$HOME_ directory.
- ```cd ...``` go one level up the directory tree.
- ```cd /etc``` to change to the _/etc_ directory.  
- ```ls``` list all files.
  - Use the ```-al``` argument to view details.
- ```pwd``` lists the present working directory.
- ```mkdir directory``` created a _directory_.
- ```rm -r directory``` removes the _directory_ and its contents recursively. Use the ```f``` argument to forcefully remove, re: ```rm -rf directory```.
- ```touch file``` will create an empty _file_.
- ```rm file``` removes a _flle_.
- ```copy file file2``` will copy _file_ to _file2_.
- ```mv file file2``` renames or moves _file_ to _file2_.
- ```cat file``` will display the contests of _file_.
- _chmod_ command is used to change the permissions of a file or directory.

#### Permissions
![](images/file_permissions.png "File Permissions")

- Legend
  - User or Owner ```U```
  - Group ```G```
  - World (Other Users) ```W```
- Permission Classes
  - Read ```r```
  - Write ```w```
  - Execute ```x```
- File Type
  - ```-``` regular file
  - ```d``` directory
- Examples
  - file _desktop.ini_: ```-rwxrwxrwx 1 seed seed 282 Dec 27 10:10 desktop.ini```
  - directory _host_: ```drwxrwxrwx 1 seed seed 4096 Jan 20 13:22 host```

  Number | Permission Type | Symbol |
  -------|-----------------|--------|
  0	     | No Permission   | ---     |
  1	     | Execute         | --x
  2      | Write	         | -w-
  3	     | Execute + Write | -wx
  4 	   | Read	           | r--
  5	     | Read + Execute	 | r-x
  6	     | Read +Write  	 | rw-
  7	     | Read + Write +Execute	| rwx
- Permission Examples  
  - ```chmod 777 filename```: _rwx rwx rwx_
  - ```chmod 775 filename```: _rwx rwx r-x_
  - ```chmod 755 filename```: _rwx r-x r-x_
  - ```chmod 664 filename```: _rw- rw- r--_
  - ```chmod 644 filename```: _rw- r-- r--_
