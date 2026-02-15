#DAY2 Today’s goal is to understand how Linux works under the hood.

LINUX is an open source ready to user kernel. Which manages hardware resources, system processes, memory and security.

What is kernel ?
Kernel is a bridge between hardware (ram, cpu) and software applications.

When Linux is an Operating system.
The linux is OS when combined with system utilities, libraries and application of different distributions. Just like an engine is kernel and it can be a car or bike based on gears and chasis of it.

Linux core components -
1. Kernel
2. Utilities
3. Binaries / system binaries
4. Filesystem
5. Processes

Why Linux ?
1. Open source and free to use.
2. Stability and security
3. Efficient performance and process management.
4. Scalable
5. Ecosystem is designed in such as way that mostly used in DEVops, cloud services and automations.


How processes are created and managed ?
A process is a programm run by the operating system after any command is executed.
Each process has its own process ID (PID).
First process in linux is #init (initialisation).

The process are managed by set of commands
ps lists current process running.
ps -aux
ps -ef | grep "process name"
top (realtime processes using cpu percentage)
systemd (system daemon)
kill "PID" will kill the mentioned process.

There are some kinds of processes.
Parent - New process started when any application or command runs on system.
Child - This gets created from parent process.
Zombie - Process not running on system but there is history of the process.
Running - Process is running on system
Sleeping - Process not running on system.
Enabled - Process is enabled on system (after reboot of server the process automatically starts).

What systemd does and why it matters
Systemd is a system manager and it is very important in managing the background process and new processes using "systemctl".
systemctl start stop and enable can be used to manage the services.

=================================

Some daily commands which needs to be used.

uptime - machine uptime check
systemctl status network - to check status of network service.
free -g - check available ram in gb
sudo su - super user switch to root


