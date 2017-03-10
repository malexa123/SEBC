```
[root@ip-172-31-16-183 yum.repos.d]# ll
total 36
-rw-r--r--. 1 root root 1664 Mar 31  2015 CentOS-Base.repo
-rw-r--r--. 1 root root 1309 Mar 31  2015 CentOS-CR.repo
-rw-r--r--. 1 root root  649 Mar 31  2015 CentOS-Debuginfo.repo
-rw-r--r--. 1 root root  290 Mar 31  2015 CentOS-fasttrack.repo
-rw-r--r--. 1 root root 1331 Mar 31  2015 CentOS-Sources.repo
-rw-r--r--. 1 root root 1002 Mar 31  2015 CentOS-Vault.repo
-rw-r--r--  1 root root  276 Mar 10 08:10 cloudera-manager.repo
-rw-r--r--. 1 root root  957 Nov 25  2014 epel.repo
-rw-r--r--. 1 root root 1056 Nov 25  2014 epel-testing.repo
[root@ip-172-31-16-183 yum.repos.d]#


[root@ip-172-31-16-183 yum.repos.d]# cat cloudera-manager.repo
[cloudera-manager]
# Packages for Cloudera Manager, Version 5, on RedHat or CentOS 7 x86_64
name=Cloudera Manager
baseurl=https://archive.cloudera.com/cm5/redhat/7/x86_64/cm/5.9.1/
gpgkey =https://archive.cloudera.com/cm5/redhat/7/x86_64/cm/RPM-GPG-KEY-cloudera
gpgcheck = 1

[root@ip-172-31-16-183 yum.repos.d]#

/usr/share/cmf/schema/scm_prepare_database.sh mysql -f -h ip-172-31-22-93.eu-central-1.compute.internal -utemp -ptemp --scm-host ip-172-31-16-183.eu-central-1.compute.internal scm scm scm_password

```
