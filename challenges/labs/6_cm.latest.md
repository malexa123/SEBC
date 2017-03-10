```
[root@ip-172-31-16-183 yum.repos.d]# curl -u malexa123:cloudera 'http://mato:7180/api/version'
v15
[root@ip-172-31-16-183 yum.repos.d]#
[root@ip-172-31-16-183 yum.repos.d]#
[root@ip-172-31-16-183 yum.repos.d]# curl -u malexa123:cloudera 'http://mato:7180/api/v12/cm/version'
{
  "version" : "5.10.0",
  "buildUser" : "jenkins",
  "buildTimestamp" : "20170120-1037",
  "gitHash" : "aa0b5cd5eceaefe2f971c13ab657020d96bb842a",
  "snapshot" : false
}[root@ip-172-31-16-183 yum.repos.d]#
```
