# 3.DevSecOps.4
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

>> Goto Github   >> Note Open file.txt (only)   >> Click on RAW    >> Copy URL
$ wget <URL>       ==> Downloads the File
$ ls -l
$ cat file name    ==> You can see the Output here

$ curl <URL>       ==> Shows on the Screen

==========================

$ grep --help 
[ec2-user@ip-172-31-6-251 ~] $ cat session-02.txt | grep linux                      Note : cat <file-name> | grep <word-to-search>
[ec2-user@ip-172-31-6-251 ~] $ grep linux session-02.txt                            Note : grep <word-to-search> <file>


==========================

https://raw.githubusercontent.com/daws-84s/notes/refs/heads/main/session-02.txt      Note : session-02.txt is File Name its a Example

[ec2-user@ip-172-31-6-251 ~] $ echo "hello world"
hello world

echo https://raw.githubusercontent.com/daws-84s/notes/refs/heads/main/session-02.txt | cut -d "/" -f1            
Note : session-02.txt is File Name its a Example

[ec2-user@ip-172-31-6-251 ~] $ echo https://raw.githubusercontent.com/daws-84s/note
https:
[ec2-user@ip-172-31-6-251 ~] $ echo https://raw.githubusercontent.com/daws-84s/notes/refs/heads/main/session-02.txt | cut -d "/" -f7           
heads
[ec2-user@ip-172-31-6-251 ~] $ echo https://raw.githubusercontent.com/daws-84s/notes/refs/heads/main/session-02.txt | cut -d "/" -f1-6      Note : 1/6 Here to show
https://raw.githubusercontent.com/daws-84s/notes/refs


==========================

awk command ====== echo https://raw.githubusercontent.com/daws-84s/notes/refs/heads/main/session-02.txt | awk -F "/" '{print $1F}'        
Note : session-02.txt is File Name its a Example

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

============================================================================================================================================================================================================================================================================================================================================================================================================================================================

Command Mode ==> :q ==> quit the file, :wq ==> write and quit, :q! ==> exit without saving, wq! ==> Force write and quit

Goto Gitbash
vim editor ==> 3 modes - Esc mode, Command mode, Insect mode

$ vim devops.txt  
  press "i" , press "Esc" , ":q!"      Note : WithOut Saving 

$ vim devops.txt 
  press "i" 
  This is joindevops session
  press "Esc" , ":wq!"                 Note : Its Saving 

==========================

cp /etc/passwd  users
vim users

:/ec2-user                             Note : Now ec2-user  pop display 
:/sbin                                 ==> Search for the word from Top
:?/sbin                                ==> Search for the word from Bottom

:noh                                   ==> No Highlight
:set nu                                ==> Numbers 
:set nonu                              ==> No Number 

:27d                                   ==> Deleted particular 27th row
:%d                                    ==> Total data deleted
:q!                                    ==> Exit without saving

:4s/sbin/SBIN                          ==> Replace sbin place SBIN  Note: 1st occurence 
:7s/sbin/SBIN

:8s/sbin/SBIN/g                        ==> All occurance in that line  will be Captial letters
:%s/sbin/SBIN/g                        ==> All occurance in the file will be Capital letters

U                                      ==> Escmode

==========================

yy                                    ==> Copy
p                                     ==> Paste
10yy                                  ==> Copy
dd                                    ==> Delete
gg                                    ==> Top
Shift + g                             ==> Bottom

==========================

Linux Administration       
1. User Management                   How to user // CRUD ==> Create, Read, Update, Delete
                                     Note : Doing these i will be Administrator // gautham is a User // & Goto root 

$ sudo su -
# Clear
# Useradd  gautham
# id gautham

In linux two types of groups - Primary group & Secondary group    // 1 Primary group & atleast  1 Secondary group 
group ==> List of Similar Users
devops team have 15 members
create devops group, add team members to the group
In Linux wen you create user, By default group also will be created with the same name

# cat /etc/passwd 
# cat /etc/group

# groupadd devops                    Note : Now groupadd devops // devops group will be created
# cat /etc/group

# usermod -g devops grk              Note : usermod -g devops grk   // Here small -g is a primary group
# id grk 

# groupadd testers 
# usermod -aG testers grk            Note : usermod -aG testers grk  // Here Captial G is a Secondary group 
# id grk

# userdel grk                       ==> Deleted User
# id grk
# cat /etc/group 

# groupdel grk                      ==> Delete Group also
# cd /home/grk                      ==> Dekete Directory also
# cd
# id grk 

# useradd grk 
# id grk

# usermod -g devops grk
# usermod -aG devops grk grk
# usermod -aG testers grk
# id grk

# gpasswd -d grk testers
# id grk                         ==> Compulsory One group must 


# usermod -g grk grk
# id grk 
# userdel grk
# cat /etc/group 

   
How to login User ?

# useradd grk
# passwd  grk                 ==> Give password

>> Goto new Duplicate window
$ ssh grk@3.231.56.105                Note : Permission are Denied 

>> Goto old Gitbash Window            Note : In Linux by Default Login to Keys only // Don't use passwords

# vim/etc/ssh/sshd_config             Note : If you change any Behaviour you need to changes Config files // default process
:?Password = xxxx                  
                                     Note : " Password Authencation no " 
 >>  i                               Note :  Now change " yes "

 >> esc   >> :wq!   >> enter


# sshd -t                            Note : Check for testing any changes here done or not

# systemctl restart sshd 

>> Goto new Duplicate window
# ssh grk@3.231.56.105 
:password = xxxx         
                  

























  
  







