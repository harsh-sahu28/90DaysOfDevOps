Include at least 20 commands with one‑line usage notes

Navigation commands

* whoami - tells who are logged in as
* pwd - present working directory
* ls - lists file and details included like permissions, size, date created, file name
* ls -la - lists files including hidden files
* cd - change directory
* cd .. - change directory from working directory to one directory back

- File or directory management -

* mkdir <name> - make directory
* mkdir -p <a/b/c> - makes multiple directory
* touch <file name> - creates an empty file
* vi file_name - creates and allows to edit the file
* cat file_name - display file on the page

Crontab manage -
* crontab -l = lists all cron entries
  -e to edit cron entries , -r to remove cron entries

Disk management -

* df -hP = define hard disk partitioning
* du -sh /path/to/directory = disk utilisation

User management - 

* useradd -m = creates user with home directory
* useradd -s = creates user with login shell

Group management

* groupadd = creates group
* passwd "username" = change password of any user
* date/timedatectl = to check timezone of server
* grep abc /etc/file = it will fetch abc from "/etc/file" file and is case sensitive
* grep -i = case insensitive

CPU and RAM related 

* lscpu = to see number of cpus
* free -g = to see ram usage in gb (-m in mb)

--------
Add 3 networking commands

- ifconfig -a (to see network adaptors) ip addr will show ip of system
- chronyc sources/ntpq -p = to see network related services like chronyd service and ntp service.
- ping "ip/hostname" = to ping any ip or hostname
- telnet <port_number> <host> = to check port connectivity
- curl "url"
- ifup/ifdown = to bring up or down any network adaptor.




