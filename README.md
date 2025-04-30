# 3.DevSecOps
=================================================================================================================================================================

Linux Cmds

Open Gitbash : 
Goto the path : $ pwd  >> $ ls -l

$ ssh -i daws-84s ec2-user@44.222.158.108

$ ssh -i /c/devops/daws-84s/daws-84s ec2-user@44.22.158.108                  Note :  This is called  Full Path

$ exit 
$ cd                                                                         Note : This is User Directory 
$ ls 

$ cd c/devops/
$ ssh -i daws-84s/daws-84s ec2-user@44.222.158.108                          Note :  This is called  Relative Path


$ sudo su                                                                   Note : $ ==> Normal User
# exit                                                                      Note : # ==> root  /admin   /super user

$ sudo su - 
$ pwd     
        /root ==> root user home directory
# exit 

command <options> <inputs>
/ ==> root directory
$ cd /
$ ls -l                                                                    Note : ls means Long List 


$ ls           ==> help list info about the FILES
 
$ ls -l        ==> long listing format in alphabetical order
$ ls -lr       ==> long li sting format in reverse alphabetical order
$ ls -lt       ==> latest files on top
$ ls -ltr      ==> latest at bottom
$ ls -la       ==> all files including hidden files and folders


touch <file-name> --> creates empty file

cat > <file-name> --> type text, enter and ctrl+d
previous content will be replaced
cat >> <file-name> --> appends text to previous content


> --> usually called as redirection

mkdir <name> --> creates directory
rmdir --> remove empty directory
rm -f --> forcefully removes file
rm -rf --> recursively forcefully delete the files and folders inside too

CRUD --> create read update delete

cp <source> <destination> --> copy files/folders
mv <source> <destination> --> cut and paste

wget <URL> --> downloads the file
curl <URL> --> shows on the screen

cat <file-name> | grep <word-to-search>
grep <word-to-search> <file>

https://raw.githubusercontent.com/daws-84s/notes/refs/heads/main/session-02.txt

echo https://raw.githubusercontent.com/daws-84s/notes/refs/heads/main/session-02.txt | cut -d "/" -f1

awk command
------------
echo https://raw.githubusercontent.com/daws-84s/notes/refs/heads/main/session-02.txt | awk -F "/" '{print $1F}'

log files --> tail -f <log-file>

find <where to search> -name <file-name>

vim --> visually improved

