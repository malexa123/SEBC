
## Sorry for the command :) I just like to have it all, below in more readable format
/* cat /etc/sysconfig/selinux && cat /etc/rc.local && cat /sys/kernel/mm/transparent_hugepage/defrag
* && service ntpd status && ntpq -p && service nscd status && cat /etc/fstab && df -h && ifconfig -a 
* && cat /etc/hosts && nslookup 172.31.30.231 && nslookup 172.31.24.214 && nslookup 172.31.17.193 && nslookup 172.31.24.137 
* && nslookup 172.31.25.165 && nslookup ec2-52-59-230-23.eu-central-1.compute.amazonaws.com 
* && nslookup ec2-52-59-229-83.eu-central-1.compute.amazonaws.com && nslookup ec2-52-59-210-102.eu-central-1.compute.amazonaws.com 
* && nslookup ec2-52-59-203-32.eu-central-1.compute.amazonaws.com && nslookup ec2-52-59-205-120.eu-central-1.compute.amazonaws.com
*/

[root@ip-172-31-25-55 ~]# cat /etc/sysconfig/selinux && cat /etc/rc.local && cat /sys/kernel/mm/transparent_hugepage/defrag && service ntpd status && ntpq -p && service nscd status && cat /etc/fstab && df -h && ifconfig -a && cat /etc/hosts && nslookup 172.31.30.231 && nslookup 172.31.24.214 && nslookup 172.31.17.193 && nslookup 172.31.24.137 && nslookup 172.31.25.165 && nslookup ec2-52-59-230-23.eu-central-1.compute.amazonaws.com && nslookup ec2-52-59-229-83.eu-central-1.compute.amazonaws.com && nslookup ec2-52-59-210-102.eu-central-1.compute.amazonaws.com && nslookup ec2-52-59-203-32.eu-central-1.compute.amazonaws.com && nslookup ec2-52-59-205-120.eu-central-1.compute.amazonaws.com

# This file controls the state of SELinux on the system.
# SELINUX= can take one of these three values:
#     enforcing - SELinux security policy is enforced.
#     permissive - SELinux prints warnings instead of enforcing.
#     disabled - No SELinux policy is loaded.
SELINUX=disabled
# SELINUXTYPE= can take one of three two values:
#     targeted - Targeted processes are protected,
#     minimum - Modification of targeted policy. Only selected processes are protected.
#     mls - Multi Level Security protection.
SELINUXTYPE=targeted


#!/bin/bash
# THIS FILE IS ADDED FOR COMPATIBILITY PURPOSES
#
# It is highly advisable to create own systemd services or udev rules
# to run scripts during boot instead of using this file.
#
# In contrast to previous versions due to parallel execution during boot
# this script will NOT be run after all other services.
#
# Please note that you must run 'chmod +x /etc/rc.d/rc.local' to ensure
# that this script will be executed during boot.

touch /var/lock/subsys/local
echo never > /sys/kernel/mm/transparent_hugepage/defrag
always madvise [never]
Redirecting to /bin/systemctl status  ntpd.service
ntpd.service - Network Time Service
   Loaded: loaded (/usr/lib/systemd/system/ntpd.service; disabled)
   Active: active (running) since Mon 2017-03-06 14:37:17 UTC; 41min ago
  Process: 8816 ExecStart=/usr/sbin/ntpd -u ntp:ntp $OPTIONS (code=exited, status=0/SUCCESS)
 Main PID: 8817 (ntpd)
   CGroup: /system.slice/ntpd.service
           └─8817 /usr/sbin/ntpd -u ntp:ntp -g

Mar 06 14:37:17 ip-172-31-25-55.eu-central-1.compute.internal ntpd[8817]: Listen normally on 3 eth0 172.31.24.137 UDP 123
Mar 06 14:37:17 ip-172-31-25-55.eu-central-1.compute.internal ntpd[8817]: Listen normally on 4 lo ::1 UDP 123
Mar 06 14:37:17 ip-172-31-25-55.eu-central-1.compute.internal ntpd[8817]: Listen normally on 5 eth0 fe80::410:9dff:fe3d:e259 UDP 123
Mar 06 14:37:17 ip-172-31-25-55.eu-central-1.compute.internal ntpd[8817]: Listening on routing socket on fd #22 for interface updates
Mar 06 14:37:17 ip-172-31-25-55.eu-central-1.compute.internal ntpd[8817]: 0.0.0.0 c016 06 restart
Mar 06 14:37:17 ip-172-31-25-55.eu-central-1.compute.internal ntpd[8817]: 0.0.0.0 c012 02 freq_set kernel 0.000 PPM
Mar 06 14:37:17 ip-172-31-25-55.eu-central-1.compute.internal ntpd[8817]: 0.0.0.0 c011 01 freq_not_set
Mar 06 14:37:24 ip-172-31-25-55.eu-central-1.compute.internal ntpd[8817]: 0.0.0.0 c614 04 freq_mode
Mar 06 14:58:36 ip-172-31-25-55.eu-central-1.compute.internal ntpd[8817]: 0.0.0.0 0612 02 freq_set kernel -17.296 PPM
Mar 06 14:58:36 ip-172-31-25-55.eu-central-1.compute.internal ntpd[8817]: 0.0.0.0 0615 05 clock_sync
     remote           refid      st t when poll reach   delay   offset  jitter
==============================================================================
*re.uni-paderbor .DCF.            1 u   21   64  377   13.429    6.988  10.408
-de.danzuck.eu   192.53.103.104   2 u   27   64  377    1.183   -9.579  12.687
+46.101.140.169  131.188.3.220    2 u   12   64  377    1.233    4.514   7.566
+smtp.johdiehl.d 192.53.103.103   2 u   13   64  377    8.118   -6.539   6.605
Redirecting to /bin/systemctl status  nscd.service
nscd.service - Name Service Cache Daemon
   Loaded: loaded (/usr/lib/systemd/system/nscd.service; disabled)
   Active: active (running) since Mon 2017-03-06 14:37:16 UTC; 41min ago
  Process: 8790 ExecStart=/usr/sbin/nscd $NSCD_OPTIONS (code=exited, status=0/SUCCESS)
 Main PID: 8791 (nscd)
   CGroup: /system.slice/nscd.service
           └─8791 /usr/sbin/nscd

Mar 06 14:37:11 ip-172-31-25-55.eu-central-1.compute.internal nscd[8791]: 8791 stat failed for file `/etc/netgroup'; will try aga...tory
Mar 06 14:37:16 ip-172-31-25-55.eu-central-1.compute.internal nscd[8791]: 8791 Access Vector Cache (AVC) started
Mar 06 14:37:16 ip-172-31-25-55.eu-central-1.compute.internal systemd[1]: Started Name Service Cache Daemon.
Mar 06 14:37:35 ip-172-31-25-55.eu-central-1.compute.internal nscd[8791]: 8791 checking for monitored file `/etc/netgroup': No su...tory
Mar 06 14:52:38 ip-172-31-25-55.eu-central-1.compute.internal nscd[8791]: 8791 monitored file `/etc/hosts` was moved, removing watch
Mar 06 14:52:38 ip-172-31-25-55.eu-central-1.compute.internal nscd[8791]: 8791 monitored file `/etc/hosts` was created, adding watch
Mar 06 14:52:38 ip-172-31-25-55.eu-central-1.compute.internal nscd[8791]: 8791 monitored file `/etc/hosts` was written to
Mar 06 15:10:07 ip-172-31-25-55.eu-central-1.compute.internal nscd[8791]: 8791 monitored file `/etc/hosts` was moved, removing watch
Mar 06 15:10:07 ip-172-31-25-55.eu-central-1.compute.internal nscd[8791]: 8791 monitored file `/etc/hosts` was created, adding watch
Mar 06 15:10:07 ip-172-31-25-55.eu-central-1.compute.internal nscd[8791]: 8791 monitored file `/etc/hosts` was written to
Hint: Some lines were ellipsized, use -l to show in full.
=======
   Active: active (running) since Mon 2017-03-06 14:37:28 UTC; 1h 3min ago
  Process: 15935 ExecStart=/usr/sbin/ntpd -u ntp:ntp $OPTIONS (code=exited, status=0/SUCCESS)
 Main PID: 15936 (ntpd)
   CGroup: /system.slice/ntpd.service
           └─15936 /usr/sbin/ntpd -u ntp:ntp -g

Mar 06 14:37:28 ip-172-31-30-231 ntpd[15936]: Listen normally on 3 eth0 172.31.30.231 UDP 123
Mar 06 14:37:28 ip-172-31-30-231 ntpd[15936]: Listen normally on 4 lo ::1 UDP 123
Mar 06 14:37:28 ip-172-31-30-231 ntpd[15936]: Listen normally on 5 eth0 fe80::4af:e7ff:fee5:befd UDP 123
Mar 06 14:37:28 ip-172-31-30-231 ntpd[15936]: Listening on routing socket on fd #22 for interface updates
Mar 06 14:37:28 ip-172-31-30-231 ntpd[15936]: 0.0.0.0 c016 06 restart
Mar 06 14:37:28 ip-172-31-30-231 ntpd[15936]: 0.0.0.0 c012 02 freq_set kernel 0.000 PPM
Mar 06 14:37:28 ip-172-31-30-231 ntpd[15936]: 0.0.0.0 c011 01 freq_not_set
Mar 06 14:37:35 ip-172-31-30-231 ntpd[15936]: 0.0.0.0 c614 04 freq_mode
Mar 06 14:55:34 ip-172-31-30-231 ntpd[15936]: 0.0.0.0 0612 02 freq_set kernel -25.587 PPM
Mar 06 14:55:34 ip-172-31-30-231 ntpd[15936]: 0.0.0.0 0615 05 clock_sync
     remote           refid      st t when poll reach   delay   offset  jitter
==============================================================================
-char-ntp-pool.c 130.149.17.8     2 u  103  128  377   14.357    2.625   2.561
+138.68.126.106  130.149.17.8     2 u  125  128  157    1.475    4.105   0.625
*ptbtime1.ptb.de .PTB.            1 u   55  128  377   11.234    8.400   1.325
+vm06.hv03.nebie 131.188.3.221    2 u   36  128  377    6.623    4.685   0.789
Redirecting to /bin/systemctl status  nscd.service
nscd.service - Name Service Cache Daemon
   Loaded: loaded (/usr/lib/systemd/system/nscd.service; disabled)
   Active: active (running) since Mon 2017-03-06 14:37:28 UTC; 1h 3min ago
  Process: 15909 ExecStart=/usr/sbin/nscd $NSCD_OPTIONS (code=exited, status=0/SUCCESS)
 Main PID: 15910 (nscd)
   CGroup: /system.slice/nscd.service
           └─15910 /usr/sbin/nscd

Mar 06 14:59:39 ip-172-31-30-231 nscd[15910]: 15910 monitored file `/etc/hosts` was written to
Mar 06 15:00:22 ip-172-31-30-231 nscd[15910]: 15910 monitored file `/etc/hosts` was moved, removing watch
Mar 06 15:00:22 ip-172-31-30-231 nscd[15910]: 15910 monitored file `/etc/hosts` was created, adding watch
Mar 06 15:00:22 ip-172-31-30-231 nscd[15910]: 15910 monitored file `/etc/hosts` was written to
Mar 06 15:07:59 ip-172-31-30-231 nscd[15910]: 15910 monitored file `/etc/hosts` was moved, removing watch
Mar 06 15:07:59 ip-172-31-30-231 nscd[15910]: 15910 monitored file `/etc/hosts` was created, adding watch
Mar 06 15:07:59 ip-172-31-30-231 nscd[15910]: 15910 monitored file `/etc/hosts` was written to
Mar 06 15:39:34 ip-172-31-30-231 nscd[15910]: 15910 monitored file `/etc/hosts` was moved, removing watch
Mar 06 15:39:34 ip-172-31-30-231 nscd[15910]: 15910 monitored file `/etc/hosts` was created, adding watch
Mar 06 15:39:34 ip-172-31-30-231 nscd[15910]: 15910 monitored file `/etc/hosts` was written to

#
# /etc/fstab
# Created by anaconda on Wed Jun 17 12:49:40 2015
#
# Accessible filesystems, by reference, are maintained under '/dev/disk'
# See man pages fstab(5), findfs(8), mount(8) and/or blkid(8) for more info
#
UUID=335af179-4d0b-4449-a3fe-8ab2991dab2e /                       xfs     defaults        0 0
Filesystem      Size  Used Avail Use% Mounted on
/dev/xvda1       50G  1.1G   49G   3% /
devtmpfs        7.3G     0  7.3G   0% /dev
tmpfs           7.2G     0  7.2G   0% /dev/shm
tmpfs           7.2G  8.3M  7.2G   1% /run
tmpfs           7.2G     0  7.2G   0% /sys/fs/cgroup
eth0: flags=4163<UP,BROADCAST,RUNNING,MULTICAST>  mtu 9001
        inet 172.31.24.137  netmask 255.255.240.0  broadcast 172.31.31.255
        inet6 fe80::410:9dff:fe3d:e259  prefixlen 64  scopeid 0x20<link>
        ether 06:10:9d:3d:e2:59  txqueuelen 1000  (Ethernet)
        RX packets 17897  bytes 21680457 (20.6 MiB)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 6173  bytes 813446 (794.3 KiB)
=======
tmpfs           7.2G  8.4M  7.2G   1% /run
tmpfs           7.2G     0  7.2G   0% /sys/fs/cgroup
eth0: flags=4163<UP,BROADCAST,RUNNING,MULTICAST>  mtu 9001
        inet 172.31.30.231  netmask 255.255.240.0  broadcast 172.31.31.255
        inet6 fe80::4af:e7ff:fee5:befd  prefixlen 64  scopeid 0x20<link>
        ether 06:af:e7:e5:be:fd  txqueuelen 1000  (Ethernet)
        RX packets 33117  bytes 38535297 (36.7 MiB)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 17386  bytes 1985720 (1.8 MiB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0

lo: flags=73<UP,LOOPBACK,RUNNING>  mtu 65536
        inet 127.0.0.1  netmask 255.0.0.0
        inet6 ::1  prefixlen 128  scopeid 0x10<host>
        loop  txqueuelen 0  (Local Loopback)
        RX packets 160  bytes 18852 (18.4 KiB)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 160  bytes 18852 (18.4 KiB)
        RX packets 32  bytes 6492 (6.3 KiB)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 32  bytes 6492 (6.3 KiB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0

127.0.0.1   localhost localhost.localdomain localhost4 localhost4.localdomain4
::1         localhost localhost.localdomain localhost6 localhost6.localdomain6

172.31.30.231   monkey  ec2-52-59-230-23.eu-central-1.compute.amazonaws.com
172.31.24.214   lion    ec2-52-59-229-83.eu-central-1.compute.amazonaws.com
172.31.17.193   horse   ec2-52-59-210-102.eu-central-1.compute.amazonaws.com
172.31.24.137   elephant        ec2-52-59-203-32.eu-central-1.compute.amazonaws.com
172.31.25.165   tiger   ec2-52-59-205-120.eu-central-1.compute.amazonaws.com

172.31.30.231   monkey  ip-172-31-24-214        ip-172-31-24-214.eu-central-1.compute.internal
172.31.24.214   lion    ip-172-31-30-231        ip-172-31-30-231.eu-central-1.compute.internal
172.31.17.193   horse   ip-172-31-17-193        ip-172-31-17-193.eu-central-1.compute.internal
172.31.24.137   elephant        ip-172-31-24-137        ip-172-31-24-137.eu-central-1.compute.internal
172.31.25.165   tiger   ip-172-31-25-165        ip-172-31-25-165.eu-central-1.compute.internal

Server:         172.31.0.2
Address:        172.31.0.2#53

Non-authoritative answer:
231.30.31.172.in-addr.arpa      name = ip-172-31-30-231.eu-central-1.compute.internal.

Authoritative answers can be found from:

Server:         172.31.0.2
Address:        172.31.0.2#53

Non-authoritative answer:
214.24.31.172.in-addr.arpa      name = ip-172-31-24-214.eu-central-1.compute.internal.

Authoritative answers can be found from:

Server:         172.31.0.2
Address:        172.31.0.2#53

Non-authoritative answer:
193.17.31.172.in-addr.arpa      name = ip-172-31-17-193.eu-central-1.compute.internal.

Authoritative answers can be found from:

Server:         172.31.0.2
Address:        172.31.0.2#53

Non-authoritative answer:
137.24.31.172.in-addr.arpa      name = ip-172-31-24-137.eu-central-1.compute.internal.

Authoritative answers can be found from:

Server:         172.31.0.2
Address:        172.31.0.2#53

Non-authoritative answer:
165.25.31.172.in-addr.arpa      name = ip-172-31-25-165.eu-central-1.compute.internal.

Authoritative answers can be found from:

Server:         172.31.0.2
Address:        172.31.0.2#53

Non-authoritative answer:
Name:   ec2-52-59-230-23.eu-central-1.compute.amazonaws.com
Address: 172.31.30.231

Name:   ip-172-31-24-214.eu-central-1.compute.internal
Address: 172.31.24.214

Server:         172.31.0.2
Address:        172.31.0.2#53

Non-authoritative answer:
Name:   ec2-52-59-229-83.eu-central-1.compute.amazonaws.com
Address: 172.31.24.214

Name:   ip-172-31-30-231.eu-central-1.compute.internal
Address: 172.31.30.231

Server:         172.31.0.2
Address:        172.31.0.2#53

Non-authoritative answer:
Name:   ec2-52-59-210-102.eu-central-1.compute.amazonaws.com
Name:   ip-172-31-17-193.eu-central-1.compute.internal

Address: 172.31.17.193

Server:         172.31.0.2
Address:        172.31.0.2#53

Non-authoritative answer:
Name:   ec2-52-59-203-32.eu-central-1.compute.amazonaws.com
Name:   ip-172-31-24-137.eu-central-1.compute.internal

Address: 172.31.24.137

Server:         172.31.0.2
Address:        172.31.0.2#53

Non-authoritative answer:
Name:   ec2-52-59-205-120.eu-central-1.compute.amazonaws.com
Address: 172.31.25.165

[root@ip-172-31-25-55 ~]#

Name:   ip-172-31-25-165.eu-central-1.compute.internal
Address: 172.31.25.165

[root@ip-172-31-30-231 ~]#

