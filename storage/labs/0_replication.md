```
[malexa123@ip-172-31-24-137 ~]$ hadoop distcp hdfs://172.31.24.137:8020/user/malexa123/malexa123_source/data/part-m-00000 hdfs://172.31.24.214:8020/user/malexa123/
17/03/09 13:36:29 ERROR tools.DistCp: Invalid arguments:
java.net.ConnectException: Call From ip-172-31-24-137.eu-central-1.compute.internal/172.31.24.137 to ip-172-31-24-214.eu-central-1.compute.internal:8020 failed on connection exception: java.net.ConnectException: Connection refused; For more details see:  http://wiki.apache.org/hadoop/ConnectionRefused
        at sun.reflect.NativeConstructorAccessorImpl.newInstance0(Native Method)
        at sun.reflect.NativeConstructorAccessorImpl.newInstance(NativeConstructorAccessorImpl.java:57)
        at sun.reflect.DelegatingConstructorAccessorImpl.newInstance(DelegatingConstructorAccessorImpl.java:45)
        at java.lang.reflect.Constructor.newInstance(Constructor.java:526)
        at org.apache.hadoop.net.NetUtils.wrapWithMessage(NetUtils.java:791)
        at org.apache.hadoop.net.NetUtils.wrapException(NetUtils.java:731)
        at org.apache.hadoop.ipc.Client.call(Client.java:1476)
        at org.apache.hadoop.ipc.Client.call(Client.java:1409)
        at org.apache.hadoop.ipc.ProtobufRpcEngine$Invoker.invoke(ProtobufRpcEngine.java:230)
        at com.sun.proxy.$Proxy14.getFileInfo(Unknown Source)
        at org.apache.hadoop.hdfs.protocolPB.ClientNamenodeProtocolTranslatorPB.getFileInfo(ClientNamenodeProtocolTranslatorPB.java:762)
        at sun.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
        at sun.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:57)
        at sun.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
        at java.lang.reflect.Method.invoke(Method.java:606)
        at org.apache.hadoop.io.retry.RetryInvocationHandler.invokeMethod(RetryInvocationHandler.java:256)
        at org.apache.hadoop.io.retry.RetryInvocationHandler.invoke(RetryInvocationHandler.java:104)
        at com.sun.proxy.$Proxy15.getFileInfo(Unknown Source)
        at org.apache.hadoop.hdfs.DFSClient.getFileInfo(DFSClient.java:2121)
        at org.apache.hadoop.hdfs.DistributedFileSystem$19.doCall(DistributedFileSystem.java:1215)
        at org.apache.hadoop.hdfs.DistributedFileSystem$19.doCall(DistributedFileSystem.java:1211)
        at org.apache.hadoop.fs.FileSystemLinkResolver.resolve(FileSystemLinkResolver.java:81)
        at org.apache.hadoop.hdfs.DistributedFileSystem.getFileStatus(DistributedFileSystem.java:1211)
        at org.apache.hadoop.fs.FileSystem.exists(FileSystem.java:1412)
        at org.apache.hadoop.tools.DistCp.setTargetPathExists(DistCp.java:201)
        at org.apache.hadoop.tools.DistCp.run(DistCp.java:113)
        at org.apache.hadoop.util.ToolRunner.run(ToolRunner.java:70)
        at org.apache.hadoop.tools.DistCp.main(DistCp.java:436)
Caused by: java.net.ConnectException: Connection refused
        at sun.nio.ch.SocketChannelImpl.checkConnect(Native Method)
        at sun.nio.ch.SocketChannelImpl.finishConnect(SocketChannelImpl.java:739)
        at org.apache.hadoop.net.SocketIOWithTimeout.connect(SocketIOWithTimeout.java:206)
        at org.apache.hadoop.net.NetUtils.connect(NetUtils.java:530)
        at org.apache.hadoop.net.NetUtils.connect(NetUtils.java:494)
        at org.apache.hadoop.ipc.Client$Connection.setupConnection(Client.java:615)
        at org.apache.hadoop.ipc.Client$Connection.setupIOstreams(Client.java:714)
        at org.apache.hadoop.ipc.Client$Connection.access$2900(Client.java:376)
        at org.apache.hadoop.ipc.Client.getConnection(Client.java:1525)
        at org.apache.hadoop.ipc.Client.call(Client.java:1448)
        ... 21 more
Invalid arguments: Call From ip-172-31-24-137.eu-central-1.compute.internal/172.31.24.137 to ip-172-31-24-214.eu-central-1.compute.internal:8020 failed on connection exception: java.net.ConnectException: Connection refused; For more details see:  http://wiki.apache.org/hadoop/ConnectionRefused
usage: distcp OPTIONS [source_path...] <target_path>
              OPTIONS
 -append                       Reuse existing data in target files and
                               append new data to them if possible
 -async                        Should distcp execution be blocking
 -atomic                       Commit all changes or none
 -bandwidth <arg>              Specify bandwidth per map in MB
 -delete                       Delete from target, files missing in source
 -diff <arg>                   Use snapshot diff report to identify the
                               difference between source and target
 -f <arg>                      List of files that need to be copied
 -filelimit <arg>              (Deprecated!) Limit number of files copied
                               to <= n
 -filters <arg>                The path to a file containing a list of
                               strings for paths to be excluded from the
                               copy.
 -i                            Ignore failures during copy
 -log <arg>                    Folder on DFS where distcp execution logs
                               are saved
 -m <arg>                      Max number of concurrent maps to use for
                               copy
 -mapredSslConf <arg>          Configuration for ssl config file, to use
                               with hftps://
 -numListstatusThreads <arg>   Number of threads to use for building file
                               listing (max 40).
 -overwrite                    Choose to overwrite target files
                               unconditionally, even if they exist.
 -p <arg>                      preserve status (rbugpcaxt)(replication,
                               block-size, user, group, permission,
                               checksum-type, ACL, XATTR, timestamps). If
                               -p is specified with no <arg>, then
                               preserves replication, block size, user,
                               group, permission, checksum type and
                               timestamps. raw.* xattrs are preserved when
                               both the source and destination paths are
                               in the /.reserved/raw hierarchy (HDFS
                               only). raw.* xattrpreservation is
                               independent of the -p flag. Refer to the
                               DistCp documentation for more details.
 -sizelimit <arg>              (Deprecated!) Limit number of files copied
                               to <= n bytes
 -skipcrccheck                 Whether to skip CRC checks between source
                               and target paths.
 -strategy <arg>               Copy strategy to use. Default is dividing
                               work based on file sizes
 -tmp <arg>                    Intermediate work path to be used for
                               atomic commit
 -update                       Update target, copying only missingfiles or
                               directories
[malexa123@ip-172-31-24-137 ~]$
```
