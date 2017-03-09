```
#generate 10GB File my time: 2m23.345s
time hadoop jar /opt/cloudera/parcels/CDH-5.8.3-1.cdh5.8.3.p0.2/lib/hadoop-mapreduce/hadoop-mapreduce-examples.jar teragen -D dfs.block.size=33554432 100000000 /user/malexa123/test_file

#sort the created file time: 5m31.555s
time hadoop jar /opt/cloudera/parcels/CDH-5.8.3-1.cdh5.8.3.p0.2/lib/hadoop-mapreduce/hadoop-mapreduce-examples.jar terasort /user/malexa123/test_file /user/malexa123/test_fileX


#Checks
[malexa123@ip-172-31-24-137 hadoop-mapreduce]$ hdfs dfs -ls /user/malexa123/test_file
Found 3 items
-rw-r--r--   3 malexa123 malexa123          0 2017-03-07 11:16 /user/malexa123/test_file/_SUCCESS
-rw-r--r--   3 malexa123 malexa123 5000000000 2017-03-07 11:16 /user/malexa123/test_file/part-m-00000
-rw-r--r--   3 malexa123 malexa123 5000000000 2017-03-07 11:16 /user/malexa123/test_file/part-m-00001


[malexa123@ip-172-31-24-137 hadoop-mapreduce]$ hdfs dfs -ls /user/malexa123/test_fileX
Found 12 items
-rw-r--r--   1 malexa123 malexa123          0 2017-03-07 11:30 /user/malexa123/test_fileX/_SUCCESS
-rw-r--r--  10 malexa123 malexa123         99 2017-03-07 11:25 /user/malexa123/test_fileX/_partition.lst
-rw-r--r--   1 malexa123 malexa123 1003534200 2017-03-07 11:30 /user/malexa123/test_fileX/part-r-00000
-rw-r--r--   1 malexa123 malexa123  989243200 2017-03-07 11:30 /user/malexa123/test_fileX/part-r-00001
-rw-r--r--   1 malexa123 malexa123 1007354900 2017-03-07 11:30 /user/malexa123/test_fileX/part-r-00002
-rw-r--r--   1 malexa123 malexa123 1003796800 2017-03-07 11:30 /user/malexa123/test_fileX/part-r-00003
-rw-r--r--   1 malexa123 malexa123 1008473700 2017-03-07 11:30 /user/malexa123/test_fileX/part-r-00004
-rw-r--r--   1 malexa123 malexa123 1009595100 2017-03-07 11:30 /user/malexa123/test_fileX/part-r-00005
-rw-r--r--   1 malexa123 malexa123  989770500 2017-03-07 11:30 /user/malexa123/test_fileX/part-r-00006
-rw-r--r--   1 malexa123 malexa123  997992200 2017-03-07 11:30 /user/malexa123/test_fileX/part-r-00007
-rw-r--r--   1 malexa123 malexa123  984587700 2017-03-07 11:30 /user/malexa123/test_fileX/part-r-00008
-rw-r--r--   1 malexa123 malexa123 1005651700 2017-03-07 11:30 /user/malexa123/test_fileX/part-r-00009


[malexa123@ip-172-31-24-137 hadoop-mapreduce]$ hdfs dfs -ls /user/malexa123
Found 4 items
drwx------   - malexa123 malexa123          0 2017-03-07 11:03 /user/malexa123/.Trash
drwx------   - malexa123 malexa123          0 2017-03-07 11:30 /user/malexa123/.staging
drwxr-xr-x   - malexa123 malexa123          0 2017-03-07 11:16 /user/malexa123/test_file
drwxr-xr-x   - malexa123 malexa123          0 2017-03-07 11:30 /user/malexa123/test_fileX
[malexa123@ip-172-31-24-137 hadoop-mapreduce]$
```
