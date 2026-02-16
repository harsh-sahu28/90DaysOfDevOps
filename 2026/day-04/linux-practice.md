Check running processes
- ps
  

ps
    PID TTY          TIME CMD
   1078 pts/0    00:00:00 bash
   1249 pts/0    00:00:00 ps

- ps aux
USER         PID %CPU %MEM    VSZ   RSS TTY      STAT START   TIME COMMAND
root           1  0.0  1.4  22140 13508 ?        Ss   12:25   0:01 /sbin/init
root           2  0.0  0.0      0     0 ?        S    12:25   0:00 [kthreadd]
root           3  0.0  0.0      0     0 ?        S    12:25   0:00 [pool_workqueue_release]
root           4  0.0  0.0      0     0 ?        I<   12:25   0:00 [kworker/R-rcu_gp]
root           5  0.0  0.0      0     0 ?        I<   12:25   0:00 [kworker/R-sync_wq]
root           6  0.0  0.0      0     0 ?        I<   12:25   0:00 [kworker/R-kvfree_rcu_reclaim]
root           7  0.0  0.0      0     0 ?        I<   12:25   0:00 [kworker/R-slub_flushwq]
root           8  0.0  0.0      0     0 ?        I<   12:25   0:00 [kworker/R-netns]
root          11  0.0  0.0      0     0 ?        I<   12:25   0:00 [kworker/0:0H-events_highpri]

=============================================
- Checking chronyd service which is basically a network service to sync server clock
systemctl status chronyd.service
● chrony.service - chrony, an NTP client/server
     Loaded: loaded (/usr/lib/systemd/system/chrony.service; enabled; preset: enabled)
     Active: active (running) since Mon 2026-02-16 12:25:25 UTC; 32min ago
       Docs: man:chronyd(8)
             man:chronyc(1)
             man:chrony.conf(5)

========================================
top
top - 12:59:43 up 34 min,  1 user,  load average: 0.00, 0.00, 0.00
Tasks: 112 total,   1 running, 111 sleeping,   0 stopped,   0 zombie
%Cpu(s):  0.0 us,  0.0 sy,  0.0 ni,100.0 id,  0.0 wa,  0.0 hi,  0.0 si,  0.0 st
MiB Mem :    914.2 total,    276.1 free,    349.7 used,    446.1 buff/cache
MiB Swap:      0.0 total,      0.0 free,      0.0 used.    564.5 avail Mem

    PID USER      PR  NI    VIRT    RES    SHR S  %CPU  %MEM     TIME+ COMMAND
      1 root      20   0   22140  13508   9624 S   0.0   1.4   0:01.25 systemd
      2 root      20   0       0      0      0 S   0.0   0.0   0:00.00 kthreadd

--------

Checking ram usage in mb
free -m
               total        used        free      shared  buff/cache   available
Mem:             914         350         273           2         447         563

=================================

tail -n 10 /etc/ssh/sshd_config     (Fetching last 10 line from /etc/ssh/sshd_config file)

# override default of no subsystems
Subsystem       sftp    /usr/lib/openssh/sftp-server

# Example of overriding settings on a per-user basis
#Match User anoncvs
#       X11Forwarding no
#       AllowTcpForwarding no
#       PermitTTY no
#       ForceCommand cvs server

  
