# Useful bash commands
frequently and important bash commnads used on linux machine

## 1. Removing files and directories
	rm [options]
	- Options : -r = recursive,
		    -f = force
	- Ex: rm -rf

## 2. Directory Trees, Disk Usage, and Processes
	tree can help to print formatted dicrctory structure

	- Ex: tree -L 2
	- Output :  .
                ├── cms
                │   └── templates
                └── lms
                    ├── static
                    └── templates

    df -h = system space (h:human-redable)
    du -h dir_name = show directory space
    ps = shows currently running processes (aka. jobs)

## 3. Disk, Memory, and Processor Usage
    ### top / htop
        top displays all currently-running processes and their owners, memory usage, and more. htop is an improved, interactive top. 

## 4. Environment Variables
    env variables are persistent variables that can be created and used withing shell.
    create using = sign
    access using $ sign

    Ex : myvar=hello
    Ex : $myvar
    O/p: hello

## 5. Finding Things
    whereis (1)          - locate the binary, source, and manual page files for a command
    which (1)            - locate a command
    whatis (1)           - display one-line manual page descriptions

    locate  - finds a file anywhere on the system by referring to a semi-regularly-updated cached list of files
    finds   - iterates through the file system to find the file you're looking for.  

## 6. Downloading Things
    ### ping / wget / curl
    ping - attempts to open a line of communication with a network host. Mainly, it's used to check whether or not your Internet connection is down

    wget http://releases.ubuntu.com/18.10/ubuntu-18.10-desktop-amd64.iso
    curl http://releases.ubuntu.com/18.10/ubuntu-18.10-desktop-amd64.iso --output ubuntu.iso

    #### Pros and Cons
    curl supports many more protocols and is more widely available than wget
    curl can also send data, while wget can only receive data
    wget can download files recursively, while curl cannot.

## 7. Superuser
    whoami - your username

## 8. File Permissions
    permissions : r - read, w - write, x - executed
    To see file or dicrectory permissions 
        ls -lh

    ### chmod / chown
    File permissions can be modified with chmod by setting the access bits:
    Ex : chmod 777 test
         chmod +rwx tist
         chmod -w test

    The user who owns a file can be changed with chown:
    Ex : sudo chown marina test
         sudo chgrp hadoop tist && ls -lh

## 9. Pattern Matching
    ### grep - g/re/p (search globally for a regular expression and print it)

    grep is used to find lines of a file which match some pattern:
    Ex : grep -e ".*fi.*" /etc/profile
         grep "andrew" /etc/passwd
    
    deprecated :
    egrep - use of extended regular expressions
    fgrep - matching any one of multiple strings at once
    rgrep - recursively searching files within a directory

## 10. Fun But Mostly Useless Things
    ### w / write / wall / lynx
    w - is a more detailed who, showing who’s logged in and what they’re doing
    write - echo "hello" | write andrew pts/10
    wall is similar to write, but it sends the same message to every logged-in user.


## Reference : https://dev.to/awwsmm/101-bash-commands-and-tips-for-beginners-to-experts-30je
