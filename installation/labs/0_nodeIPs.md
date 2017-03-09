```
## I like automating things in case it's possible :)
cat /etc/sysconfig/selinux && cat /etc/rc.local && cat /sys/kernel/mm/transparent_hugepage/defrag && service nscd status 
&& cat /etc/fstab && df -h && ifconfig -a && cat /etc/hosts && nslookup 172.31.30.231 && nslookup 172.31.24.214 
&& nslookup 172.31.17.193 && nslookup 172.31.24.137 && nslookup 172.31.25.165 && nslookup ip-172-31-24-214 
&& nslookup ip-172-31-30-231 && nslookup ip-172-31-17-193 && nslookup ip-172-31-24-137 && nslookup ip-172-31-25-165

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
Redirecting to /bin/systemctl status  nscd.service
● nscd.service - Name Service Cache Daemon
   Loaded: loaded (/usr/lib/systemd/system/nscd.service; enabled; vendor preset: disabled)
   Active: active (running) since Wed 2017-03-08 20:47:30 UTC; 16h ago
  Process: 467 ExecStart=/usr/sbin/nscd $NSCD_OPTIONS (code=exited, status=0/SUCCESS)
 Main PID: 468 (nscd)
   CGroup: /system.slice/nscd.service
           └─468 /usr/sbin/nscd

Mar 09 10:01:18 ip-172-31-30-231.eu-central-1.compute.internal nscd[468]: 468 monitored file `/etc/group` was written to
Mar 09 10:01:18 ip-172-31-30-231.eu-central-1.compute.internal nscd[468]: 468 monitored file `/etc/group` was moved into place, adding watch
Mar 09 10:01:18 ip-172-31-30-231.eu-central-1.compute.internal nscd[468]: 468 monitoring file `/etc/passwd` (11)
Mar 09 10:01:18 ip-172-31-30-231.eu-central-1.compute.internal nscd[468]: 468 monitoring directory `/etc` (2)
Mar 09 10:01:18 ip-172-31-30-231.eu-central-1.compute.internal nscd[468]: 468 monitoring file `/etc/group` (13)
Mar 09 10:01:18 ip-172-31-30-231.eu-central-1.compute.internal nscd[468]: 468 monitoring directory `/etc` (2)
Mar 09 10:01:18 ip-172-31-30-231.eu-central-1.compute.internal nscd[468]: 468 monitoring file `/etc/passwd` (11)
Mar 09 10:01:18 ip-172-31-30-231.eu-central-1.compute.internal nscd[468]: 468 monitoring directory `/etc` (2)
Mar 09 10:01:18 ip-172-31-30-231.eu-central-1.compute.internal nscd[468]: 468 monitoring file `/etc/group` (13)
Mar 09 10:01:18 ip-172-31-30-231.eu-central-1.compute.internal nscd[468]: 468 monitoring directory `/etc` (2)

#
# /etc/fstab
# Created by anaconda on Wed Jun 17 12:49:40 2015
#
# Accessible filesystems, by reference, are maintained under '/dev/disk'
# See man pages fstab(5), findfs(8), mount(8) and/or blkid(8) for more info
#
UUID=335af179-4d0b-4449-a3fe-8ab2991dab2e /                       xfs     defaults        0 0
Filesystem      Size  Used Avail Use% Mounted on
/dev/xvda1       50G   27G   24G  54% /
devtmpfs        7.3G     0  7.3G   0% /dev
tmpfs           7.2G     0  7.2G   0% /dev/shm
tmpfs           7.2G   73M  7.1G   1% /run
tmpfs           7.2G     0  7.2G   0% /sys/fs/cgroup
tmpfs           1.5G     0  1.5G   0% /run/user/0
cm_processes    7.2G   23M  7.2G   1% /run/cloudera-scm-agent/process
tmpfs           1.5G     0  1.5G   0% /run/user/997
tmpfs           1.5G     0  1.5G   0% /run/user/1000
eth0: flags=4163<UP,BROADCAST,RUNNING,MULTICAST>  mtu 9001
        inet 172.31.30.231  netmask 255.255.240.0  broadcast 172.31.31.255
        inet6 fe80::4af:e7ff:fee5:befd  prefixlen 64  scopeid 0x20<link>
        ether 06:af:e7:e5:be:fd  txqueuelen 1000  (Ethernet)
        RX packets 1145056  bytes 367495860 (350.4 MiB)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 1219861  bytes 293878908 (280.2 MiB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0

lo: flags=73<UP,LOOPBACK,RUNNING>  mtu 65536
        inet 127.0.0.1  netmask 255.0.0.0
        inet6 ::1  prefixlen 128  scopeid 0x10<host>
        loop  txqueuelen 0  (Local Loopback)
        RX packets 8795055  bytes 8782600820 (8.1 GiB)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 8795055  bytes 8782600820 (8.1 GiB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0

127.0.0.1   localhost localhost.localdomain localhost4 localhost4.localdomain4
::1         localhost localhost.localdomain localhost6 localhost6.localdomain6

172.31.30.231   ip-172-31-30-231.eu-central-1.compute.internal  monkey  ip-172-31-30-231
172.31.24.214   ip-172-31-24-214.eu-central-1.compute.internal  lion    ip-172-31-24-214
172.31.17.193   ip-172-31-17-193.eu-central-1.compute.internal  horse   ip-172-31-17-193
172.31.24.137   ip-172-31-24-137.eu-central-1.compute.internal  elephant        ip-172-31-24-137
172.31.25.165   ip-172-31-25-165.eu-central-1.compute.internal  tiger   ip-172-31-25-165

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
Name:   ip-172-31-24-214.eu-central-1.compute.internal
Address: 172.31.24.214

Server:         172.31.0.2
Address:        172.31.0.2#53

Non-authoritative answer:
Name:   ip-172-31-30-231.eu-central-1.compute.internal
Address: 172.31.30.231

Server:         172.31.0.2
Address:        172.31.0.2#53

Non-authoritative answer:
Name:   ip-172-31-17-193.eu-central-1.compute.internal
Address: 172.31.17.193

Server:         172.31.0.2
Address:        172.31.0.2#53

Non-authoritative answer:
Name:   ip-172-31-24-137.eu-central-1.compute.internal
Address: 172.31.24.137

Server:         172.31.0.2
Address:        172.31.0.2#53

Non-authoritative answer:
Name:   ip-172-31-25-165.eu-central-1.compute.internal
Address: 172.31.25.165

[malexa123@ip-172-31-30-231 ~]$
```
