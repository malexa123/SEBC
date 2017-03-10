```
[ronaldo@ip-172-31-16-183 ~]$ hadoop jar /opt/cloudera/parcels/CDH-5.9.1-1.cdh5.9.1.p0.4/lib/hadoop-mapreduce/hadoop-mapreduce-examples.jar pi 5 5
Number of Maps  = 5
Samples per Map = 5
Wrote input for Map #0
Wrote input for Map #1
Wrote input for Map #2
Wrote input for Map #3
Wrote input for Map #4
Starting Job
17/03/10 09:24:57 INFO client.RMProxy: Connecting to ResourceManager at ip-172-31-22-93.eu-central-1.compute.internal/172.31.22.93:8032
17/03/10 09:24:57 INFO hdfs.DFSClient: Created token for ronaldo: HDFS_DELEGATION_TOKEN owner=ronaldo@MALEXA123.ES, renewer=yarn, realUser=, issueDate=1489137897991, maxDate=1489742697991, sequenceNumber=2, masterKeyId=2 on 172.31.16.71:8020
17/03/10 09:24:58 INFO security.TokenCache: Got dt for hdfs://ip-172-31-16-71.eu-central-1.compute.internal:8020; Kind: HDFS_DELEGATION_TOKEN, Service: 172.31.16.71:8020, Ident: (token for ronaldo: HDFS_DELEGATION_TOKEN owner=ronaldo@MALEXA123.ES, renewer=yarn, realUser=, issueDate=1489137897991, maxDate=1489742697991, sequenceNumber=2, masterKeyId=2)
17/03/10 09:24:58 INFO input.FileInputFormat: Total input paths to process : 5
17/03/10 09:24:58 INFO mapreduce.JobSubmitter: number of splits:5
17/03/10 09:24:58 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1489137034771_0002
17/03/10 09:24:58 INFO mapreduce.JobSubmitter: Kind: HDFS_DELEGATION_TOKEN, Service: 172.31.16.71:8020, Ident: (token for ronaldo: HDFS_DELEGATION_TOKEN owner=ronaldo@MALEXA123.ES, renewer=yarn, realUser=, issueDate=1489137897991, maxDate=1489742697991, sequenceNumber=2, masterKeyId=2)
17/03/10 09:24:58 INFO impl.YarnClientImpl: Submitted application application_1489137034771_0002
17/03/10 09:24:58 INFO mapreduce.Job: The url to track the job: http://ip-172-31-22-93.eu-central-1.compute.internal:8088/proxy/application_1489137034771_0002/
17/03/10 09:24:58 INFO mapreduce.Job: Running job: job_1489137034771_0002
17/03/10 09:25:07 INFO mapreduce.Job: Job job_1489137034771_0002 running in uber mode : false
17/03/10 09:25:07 INFO mapreduce.Job:  map 0% reduce 0%
17/03/10 09:25:15 INFO mapreduce.Job:  map 20% reduce 0%
17/03/10 09:25:16 INFO mapreduce.Job:  map 60% reduce 0%
17/03/10 09:25:17 INFO mapreduce.Job:  map 100% reduce 0%
17/03/10 09:25:23 INFO mapreduce.Job:  map 100% reduce 100%
17/03/10 09:25:23 INFO mapreduce.Job: Job job_1489137034771_0002 completed successfully
17/03/10 09:25:23 INFO mapreduce.Job: Counters: 50
        File System Counters
                FILE: Number of bytes read=64
                FILE: Number of bytes written=746698
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=1515
                HDFS: Number of bytes written=215
                HDFS: Number of read operations=23
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=3
        Job Counters
                Launched map tasks=5
                Launched reduce tasks=1
                Data-local map tasks=4
                Rack-local map tasks=1
                Total time spent by all maps in occupied slots (ms)=37097
                Total time spent by all reduces in occupied slots (ms)=3181
                Total time spent by all map tasks (ms)=37097
                Total time spent by all reduce tasks (ms)=3181
                Total vcore-seconds taken by all map tasks=37097
                Total vcore-seconds taken by all reduce tasks=3181
                Total megabyte-seconds taken by all map tasks=37987328
                Total megabyte-seconds taken by all reduce tasks=3257344
        Map-Reduce Framework
                Map input records=5
                Map output records=10
                Map output bytes=90
                Map output materialized bytes=167
                Input split bytes=925
                Combine input records=0
                Combine output records=0
                Reduce input groups=2
                Reduce shuffle bytes=167
                Reduce input records=10
                Reduce output records=0
                Spilled Records=20
                Shuffled Maps =5
                Failed Shuffles=0
                Merged Map outputs=5
                GC time elapsed (ms)=171
                CPU time spent (ms)=3610
                Physical memory (bytes) snapshot=2483314688
                Virtual memory (bytes) snapshot=9509117952
                Total committed heap usage (bytes)=2782920704
        Shuffle Errors
                BAD_ID=0
                CONNECTION=0
                IO_ERROR=0
                WRONG_LENGTH=0
                WRONG_MAP=0
                WRONG_REDUCE=0
        File Input Format Counters
                Bytes Read=590
        File Output Format Counters
                Bytes Written=97
Job Finished in 25.512 seconds
Estimated value of Pi is 3.68000000000000000000
[ronaldo@ip-172-31-16-183 ~]$
```
