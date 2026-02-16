Part 1: Linux File System Hierarchy

## Core Directories (Must Know):

# / (root) - It is the base directory from where all other directories starts
# /home - User home directory , it gets created whenever any user logs in to the server, user files and data gets stored here. I will use this directory when i want to switch to any other user directory
# /root - Root user's home directory, it has full access to all other filesystems. I can only access this directory if i am perfoming any action as root.
# /etc - Configuration files like network files, host files, access file (sudoers file), ssh files. I will open this directory to see ssh configuration or to see users entries in /etc/passwd file.
# /var/log - Usually a variable directory, Log files of server are stored in this. I will access this dir to see logs
# /tmp - Temporary files, creates cache files on server to reduce run time of any command or process. Usually cleared on reboot of server.

* /bin - Binary files gets stored in the system which are required during initialization of server
* /sbin - System binaries get stored in this directory.
* /usr/bin - User installed software or binaries gets stored in this directory.
* /opt - Other third party softwares gets installed in this directory and there software based directories gets created in the directory.

* ls /
bin                boot  etc   lib                lib64       media  opt   root  sbin                snap  sys  usr
bin.usr-is-merged  dev   home  lib.usr-is-merged  lost+found  mnt    proc  run   sbin.usr-is-merged  srv   tmp  var

* ls /home/
ubuntu   > my home directory

* ls /root/
ls: cannot open directory '/root/': Permission denied   > because it is root directory i cannot see the files inside it

* du -sh /var/log/* 2>/dev/null | sort -h | tail -5
116K    /var/log/sysstat
292K    /var/log/kern.log
556K    /var/log/cloud-init.log
828K    /var/log/syslog
50M     /var/log/journal

* cat /etc/hostname
gitserver   > I have changed my server name :)

* ls /home/ubuntu
TASK-14feb  bollywood  day6  devops-nginx-demo  practise-repo  shell-scripts-git
===============================================================================
# Scenario 1: Service Not Starting

# A web application service called 'myapp' failed to start after a server reboot.
What commands would you run to diagnose the issue?
Write at least 4 commands in order.

* First i will check the service is running or not
* systemctl status myapp.service
* If status shows enabled as enbaled then no issues but if downot show i will try to enable the service using -
  - systemctl enable myapp.service
    journalctl -u myapp -n 50  > it will show last 50 lines log of the service myapp
* systemctl restart myapp.service > i will try to restart the service and will see the recent logs again

=========================================================================================

  # Scenario 2: High CPU Usage

* top command

* top
top - 15:35:47 up  3:10,  1 user,  load average: 0.01, 0.02, 0.00
Tasks: 113 total,   1 running, 112 sleeping,   0 stopped,   0 zombie
%Cpu(s):  0.2 us,  0.0 sy,  0.0 ni, 99.7 id,  0.2 wa,  0.0 hi,  0.0 si,  0.0 st
MiB Mem :    914.2 total,    157.5 free,    383.4 used,    536.6 buff/cache
MiB Swap:      0.0 total,      0.0 free,      0.0 used.    530.8 avail Mem

    PID USER      PR  NI    VIRT    RES    SHR S  %CPU  %MEM     TIME+ COMMAND
   2634 ubuntu    20   0   12360   5900   3672 R   0.7   0.6   0:00.17 top
   1904 root      20   0 1802284  39272  25288 S   0.3   4.2   0:04.16 containerd
      1 root      20   0   22712  13968   9624 S   0.0   1.5   0:02.13 systemd
      2 root      20   0       0      0      0 S   0.0   0.0   0:00.00 kthreadd

1 user is logged in.
top command with process id 2634 is running on server by ubuntu user.
containerd command is running and process id is 1904 as root user
systemd command is running and pid is 1 as root user which initializes the process on server.

* htop is interactive command

* ps aux --sort=-%cpu | head -10
- showing container of docker as process

  ==================================================

  # Scenario 3: Finding Service Logs

  - journalctl -u docker.service
  - it showed the log location of the docker.service > /var/lib/docker
 =======================================

  # Scenario 4: File Permissions Issue

  - I created a file backups.sh and saw permissions of file
 
    ls -la backups.sh
-rw-rw-r-- 1 ubuntu ubuntu 0 Feb 16 15:54 backups.sh

There was no executable permissions on shell script so used chmod to change permissions.

chmod +x backup.sh > the current user and group associated with it can run the script
ls -la backups.sh
-rwxrwxr-x 1 ubuntu ubuntu 0 Feb 16 15:54 backups.sh
