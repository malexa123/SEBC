```
[root@ip-172-31-16-183 cloudera-scm-server]# head -1 cloudera-scm-server.log
2017-03-10 08:23:50,240 INFO main:com.cloudera.server.cmf.Main: Starting SCM Server. JVM Args: [-Dlog4j.configuration=file:/etc/cloudera-scm-server/log4j.properties, -Dfile.encoding=UTF-8, -Dcmf.root.logger=INFO,LOGFILE, -Dcmf.log.dir=/var/log/cloudera-scm-server, -Dcmf.log.file=cloudera-scm-server.log, -Dcmf.jetty.threshhold=WARN, -Dcmf.schema.dir=/usr/share/cmf/schema, -Djava.awt.headless=true, -Djava.net.preferIPv4Stack=true, -Dpython.home=/usr/share/cmf/python, -XX:+UseConcMarkSweepGC, -XX:+UseParNewGC, -XX:+HeapDumpOnOutOfMemoryError, -Xmx2G, -XX:MaxPermSize=256m, -XX:+HeapDumpOnOutOfMemoryError, -XX:HeapDumpPath=/tmp, -XX:OnOutOfMemoryError=kill -9 %p], Args: [], Version: 5.9.1 (#8 built by jenkins on 20170112-1158 git: a66d8bbdbe8bc3ee54235e55423f2f76c7d9f3b1)
[root@ip-172-31-16-183 cloudera-scm-server]#

[root@ip-172-31-16-183 cloudera-scm-server]# cat cloudera-scm-server.log | grep "Started Jetty server"
2017-03-10 08:25:02,896 INFO WebServerImpl:com.cloudera.server.cmf.WebServerImpl: Started Jetty server.
[root@ip-172-31-16-183 cloudera-scm-server]#

[root@ip-172-31-16-183 cloudera-scm-server]# find / -name db.properties
/etc/cloudera-scm-server/db.properties
[root@ip-172-31-16-183 cloudera-scm-server]# cat /etc/cloudera-scm-server/db.properties
# Auto-generated by scm_prepare_database.sh on Fri Mar 10 08:20:54 UTC 2017
#
# For information describing how to configure the Cloudera Manager Server
# to connect to databases, see the "Cloudera Manager Installation Guide."
#
com.cloudera.cmf.db.type=mysql
com.cloudera.cmf.db.host=ip-172-31-22-93.eu-central-1.compute.internal
com.cloudera.cmf.db.name=scm
com.cloudera.cmf.db.user=scm
com.cloudera.cmf.db.password=scm_password
com.cloudera.cmf.db.setupType=EXTERNAL
[root@ip-172-31-16-183 cloudera-scm-server]#
```
