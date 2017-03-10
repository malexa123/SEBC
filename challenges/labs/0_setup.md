```
Hi Michael :)

My setup is following:
AWS
Centos 7.1, comunity version, m3.xlarge - hopefully the one working well :)

[root@ip-172-31-22-93 ~]# df -h /
Filesystem      Size  Used Avail Use% Mounted on
/dev/xvda1       50G 1021M   49G   2% /
[root@ip-172-31-22-93 ~]#

[root@ip-172-31-22-93 ~]# yum repolist enabled
Loaded plugins: fastestmirror
Loading mirror speeds from cached hostfile
 * base: ftp.plusline.de
 * epel: mirror.de.leaseweb.net
 * extras: mirror.eu.oneandone.net
 * updates: mirror.23media.de
repo id                                                        repo name                                                                                     status
base/7/x86_64                                                  CentOS-7 - Base                                                                                9,363
epel/x86_64                                                    Extra Packages for Enterprise Linux 7 - x86_64                                                11,310
extras/7/x86_64                                                CentOS-7 - Extras                                                                                311
updates/7/x86_64                                               CentOS-7 - Updates                                                                             1,107
repolist: 22,091
[root@ip-172-31-22-93 ~]#

[root@ip-172-31-22-93 ~]# cat /etc/passwd | grep -e ronaldo -e neymar
neymar:x:2010:2010::/home/neymar:/bin/bash
ronaldo:x:2016:2016::/home/ronaldo:/bin/bash
[root@ip-172-31-22-93 ~]#

Uptime in format:
[root@ip-172-31-22-93 ~]# uptime
 08:01:38 up 22 min,  1 user,  load average: 0.00, 0.01, 0.01
[root@ip-172-31-22-93 ~]#


```
