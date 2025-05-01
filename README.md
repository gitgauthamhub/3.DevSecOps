# 3.DevSecOps
==========================

Linux Cmds

Open Gitbash : 
Goto the path : $ pwd  >> $ ls -l

$ ssh -i daws-84s ec2-user@44.222.158.108

$ ssh -i /c/devops/daws-84s/daws-84s ec2-user@44.22.158.108                  Note :  This is called  Full Path

$ exit 
$ cd                                                                         Note : This is User Directory 
$ ls 

$ cd /c/devops/
$ ssh -i daws-84s/daws-84s ec2-user@44.222.158.108                          Note :  This is called  Relative Path


$ sudo su -                                                                 Note : $ ==> Normal User                                       
$ pwd                                                                       Note : # ==> root  /admin   /super user
        /root ==> root user home directory
# exit 

==========================

command <options> <inputs>
/ ==> root directory
$ cd /
$ ls -l                                                                    Note : ls means Long List 


==========================

$ ls           ==> help list info about the FILES
$ ls -l        ==> long listing format in alphabetical order
$ ls -lr       ==> long li sting format in reverse alphabetical order
$ ls -lt       ==> latest files on top
$ ls -ltr      ==> latest at bottom
$ ls -la       ==> all files including hidden files and folders


==========================

Note : $ ssh -i /c/devops/daws-84s/daws-84s ec2-user@44.22.158.108 

$ touch devops.txt    ==> creates empty file                              Note : touch <file-name>   ==> creates empty file  
  
$ cat > devops.txt   ==> type text, enter and ctrl+d                      Note : cat > <file-name> --> type text, enter and  ==> ctrl+d
$ cat devops.txt                                                          previous content will be replaced


$ cat >> devops.txt 
$ cat devops.txt                                                          Note : >   ==> usually called as redirection


==========================

$ mkdir  daws84s                                                         mkdir <name> ==> Creates Directory
$ ls -l

$ rmdir     ==> Remove empty directory
$ rm -f     ==> Forcefully removes file
$ rm -rf    ==> Recursively forcefully delete the files and folders inside too


==========================

CRUD ==> Create Read Update Delete

[ec2-user@ip-172-31-6-251 ~] $ touch devops.txt
[ec2-user@ip-172-31-6-251 ~] $ mkdir joindevops
[ec2-user@ip-172-31-6-251 ~] $ ls -l

                                                                 -rw-r--r--. 1 ec2-user ec2-user 0 Apr 30 14:39 devops.txt
                                                                 drwxr-xr-x. 2 ec2-user ec2-user 6 Apr 30 14:39 joindevops
                                                                 
$ cp <source> <destination>   ==> copy files/folders

[ec2-user@ip-172-31-6-251 ~] $ cp devops.txt joindevops/
[ec2-user@ip-172-31-6-251 ~] $ cd joindevops/
[ec2-user@ip-172-31-6-251 joindevops] $ ls -l
total 0
-rw-r--r--. 1 ec2-user ec2-user 0 Apr 30 14:41 devops.txt

                                                                 


$ mv <source> <destination>   ==> cut and paste

==========================

>> Goto Github   >> Open file    >> Click on RAW    >> Copy URL
$ wget <URL>       ==> Downloads the File
$ ls -l
$ cat file name    ==> You can see the Output here

$ curl <URL>       ==> Shows on the Screen

==========================

$ grep --help 
[ec2-user@ip-172-31-6-251 ~] $ cat session-02.txt | grep linux                      Note : cat <file-name> | grep <word-to-search>
[ec2-user@ip-172-31-6-251 ~] $ grep linux session-02.txt                            Note : grep <word-to-search> <file>


==========================

https://raw.githubusercontent.com/daws-84s/notes/refs/heads/main/session-02.txt

[ec2-user@ip-172-31-6-251 ~] $ echo "hello world"
hello world

echo https://raw.githubusercontent.com/daws-84s/notes/refs/heads/main/session-02.txt | cut -d "/" -f1

[ec2-user@ip-172-31-6-251 ~] $ echo https://raw.githubusercontent.com/daws-84s/note
https:
[ec2-user@ip-172-31-6-251 ~] $ echo https://raw.githubusercontent.com/daws-84s/notes/refs/heads/main/session-02.txt | cut -d "/" -f7
heads
[ec2-user@ip-172-31-6-251 ~] $ echo https://raw.githubusercontent.com/daws-84s/notes/refs/heads/main/session-02.txt | cut -d "/" -f1-6      Note : 1/6 Here to show
https://raw.githubusercontent.com/daws-84s/notes/refs


==========================

awk command ====== echo https://raw.githubusercontent.com/daws-84s/notes/refs/heads/main/session-02.txt | awk -F "/" '{print $1F}'

[ec2-user@ip-172-31-6-251 ~] $ echo https://raw.githubusercontent.com/daws-84s/notes/refs/heads/main/session-02.txt | awk -F "/" '{print $1F}'
https:
[ec2-user@ip-172-31-6-251 ~] $ echo https://raw.githubusercontent.com/daws-84s/notes/refs/heads/main/session-02.txt | awk -F "/" '{print $NF}'
session-02.txt


==========================

log files ==> head -f <log-file>
log files ==> tail -f <log-file>
find <where to search> -name <file-name>

$ find . -name "users"
$ find . -name "*se*"

vim ==> visually improved

