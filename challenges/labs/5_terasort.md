```
[neymar@ip-172-31-16-183 ~]$ hadoop jar /opt/cloudera/parcels/CDH-5.9.1-1.cdh5.9.1.p0.4/lib/hadoop-mapreduce/hadoop-mapreduce-examples.jar terasort -Dmapreduce.job.maps=4 -Dmapreduce.job.reduces=4 /user/neymar/tgen640 /user/neymar/tsort
17/03/10 09:14:15 INFO terasort.TeraSort: starting
17/03/10 09:14:17 INFO hdfs.DFSClient: Created token for neymar: HDFS_DELEGATION_TOKEN owner=neymar@MALEXA123.ES, renewer=yarn, realUser=, issueDate=1489137257448, maxDate=1489742057448, sequenceNumber=1, masterKeyId=2 on 172.31.16.71:8020
17/03/10 09:14:17 INFO security.TokenCache: Got dt for hdfs://ip-172-31-16-71.eu-central-1.compute.internal:8020; Kind: HDFS_DELEGATION_TOKEN, Service: 172.31.16.71:8020, Ident: (token for neymar: HDFS_DELEGATION_TOKEN owner=neymar@MALEXA123.ES, renewer=yarn, realUser=, issueDate=1489137257448, maxDate=1489742057448, sequenceNumber=1, masterKeyId=2)
17/03/10 09:14:17 INFO input.FileInputFormat: Total input paths to process : 8
Spent 475ms computing base-splits.
Spent 7ms computing TeraScheduler splits.
Computing input splits took 483ms
Sampling 10 splits of 392
Making 4 from 100000 sampled records
Computing parititions took 839ms
Spent 1325ms computing partitions.
17/03/10 09:14:18 INFO client.RMProxy: Connecting to ResourceManager at ip-172-31-22-93.eu-central-1.compute.internal/172.31.22.93:8032
17/03/10 09:14:19 INFO mapreduce.JobSubmitter: number of splits:392
17/03/10 09:14:19 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1489137034771_0001
17/03/10 09:14:19 INFO mapreduce.JobSubmitter: Kind: HDFS_DELEGATION_TOKEN, Service: 172.31.16.71:8020, Ident: (token for neymar: HDFS_DELEGATION_TOKEN owner=neymar@MALEXA123.ES, renewer=yarn, realUser=, issueDate=1489137257448, maxDate=1489742057448, sequenceNumber=1, masterKeyId=2)
17/03/10 09:14:20 INFO impl.YarnClientImpl: Submitted application application_1489137034771_0001
17/03/10 09:14:20 INFO mapreduce.Job: The url to track the job: http://ip-172-31-22-93.eu-central-1.compute.internal:8088/proxy/application_1489137034771_0001/
17/03/10 09:14:20 INFO mapreduce.Job: Running job: job_1489137034771_0001
17/03/10 09:14:29 INFO mapreduce.Job: Job job_1489137034771_0001 running in uber mode : false
17/03/10 09:14:29 INFO mapreduce.Job:  map 0% reduce 0%
17/03/10 09:14:37 INFO mapreduce.Job:  map 1% reduce 0%
17/03/10 09:14:44 INFO mapreduce.Job:  map 3% reduce 0%
17/03/10 09:14:48 INFO mapreduce.Job:  map 4% reduce 0%
17/03/10 09:14:53 INFO mapreduce.Job:  map 5% reduce 0%
17/03/10 09:14:54 INFO mapreduce.Job:  map 6% reduce 0%
17/03/10 09:14:59 INFO mapreduce.Job:  map 7% reduce 0%
17/03/10 09:15:02 INFO mapreduce.Job:  map 8% reduce 0%
17/03/10 09:15:05 INFO mapreduce.Job:  map 9% reduce 0%
17/03/10 09:15:09 INFO mapreduce.Job:  map 10% reduce 0%
17/03/10 09:15:11 INFO mapreduce.Job:  map 11% reduce 0%
17/03/10 09:15:14 INFO mapreduce.Job:  map 12% reduce 0%
17/03/10 09:15:19 INFO mapreduce.Job:  map 13% reduce 0%
17/03/10 09:15:20 INFO mapreduce.Job:  map 14% reduce 0%
17/03/10 09:15:25 INFO mapreduce.Job:  map 15% reduce 0%
17/03/10 09:15:30 INFO mapreduce.Job:  map 17% reduce 0%
17/03/10 09:15:35 INFO mapreduce.Job:  map 18% reduce 0%
17/03/10 09:15:39 INFO mapreduce.Job:  map 19% reduce 0%
17/03/10 09:15:40 INFO mapreduce.Job:  map 20% reduce 0%
17/03/10 09:15:45 INFO mapreduce.Job:  map 21% reduce 0%
17/03/10 09:15:48 INFO mapreduce.Job:  map 22% reduce 0%
17/03/10 09:15:50 INFO mapreduce.Job:  map 23% reduce 0%
17/03/10 09:15:55 INFO mapreduce.Job:  map 24% reduce 0%
17/03/10 09:15:57 INFO mapreduce.Job:  map 25% reduce 0%
17/03/10 09:16:00 INFO mapreduce.Job:  map 26% reduce 0%
17/03/10 09:16:05 INFO mapreduce.Job:  map 28% reduce 0%
17/03/10 09:16:11 INFO mapreduce.Job:  map 29% reduce 0%
17/03/10 09:16:15 INFO mapreduce.Job:  map 30% reduce 0%
17/03/10 09:16:16 INFO mapreduce.Job:  map 31% reduce 0%
17/03/10 09:16:21 INFO mapreduce.Job:  map 32% reduce 0%
17/03/10 09:16:24 INFO mapreduce.Job:  map 33% reduce 0%
17/03/10 09:16:25 INFO mapreduce.Job:  map 34% reduce 0%
17/03/10 09:16:30 INFO mapreduce.Job:  map 35% reduce 0%
17/03/10 09:16:34 INFO mapreduce.Job:  map 36% reduce 0%
17/03/10 09:16:37 INFO mapreduce.Job:  map 37% reduce 0%
17/03/10 09:16:40 INFO mapreduce.Job:  map 38% reduce 0%
17/03/10 09:16:43 INFO mapreduce.Job:  map 39% reduce 0%
17/03/10 09:16:46 INFO mapreduce.Job:  map 40% reduce 0%
17/03/10 09:16:51 INFO mapreduce.Job:  map 42% reduce 0%
17/03/10 09:16:55 INFO mapreduce.Job:  map 43% reduce 0%
17/03/10 09:16:59 INFO mapreduce.Job:  map 44% reduce 0%
17/03/10 09:17:00 INFO mapreduce.Job:  map 45% reduce 0%
17/03/10 09:17:05 INFO mapreduce.Job:  map 46% reduce 0%
17/03/10 09:17:09 INFO mapreduce.Job:  map 47% reduce 0%
17/03/10 09:17:12 INFO mapreduce.Job:  map 48% reduce 0%
17/03/10 09:17:15 INFO mapreduce.Job:  map 49% reduce 0%
17/03/10 09:17:19 INFO mapreduce.Job:  map 50% reduce 0%
17/03/10 09:17:20 INFO mapreduce.Job:  map 51% reduce 0%
17/03/10 09:17:26 INFO mapreduce.Job:  map 52% reduce 0%
17/03/10 09:17:27 INFO mapreduce.Job:  map 53% reduce 0%
17/03/10 09:17:31 INFO mapreduce.Job:  map 54% reduce 0%
17/03/10 09:17:34 INFO mapreduce.Job:  map 55% reduce 0%
17/03/10 09:17:36 INFO mapreduce.Job:  map 56% reduce 0%
17/03/10 09:17:41 INFO mapreduce.Job:  map 57% reduce 0%
17/03/10 09:17:43 INFO mapreduce.Job:  map 58% reduce 0%
17/03/10 09:17:46 INFO mapreduce.Job:  map 59% reduce 0%
17/03/10 09:17:51 INFO mapreduce.Job:  map 60% reduce 0%
17/03/10 09:17:52 INFO mapreduce.Job:  map 61% reduce 0%
17/03/10 09:17:56 INFO mapreduce.Job:  map 62% reduce 0%
17/03/10 09:17:58 INFO mapreduce.Job:  map 63% reduce 0%
17/03/10 09:18:01 INFO mapreduce.Job:  map 64% reduce 0%
17/03/10 09:18:04 INFO mapreduce.Job:  map 65% reduce 0%
17/03/10 09:18:07 INFO mapreduce.Job:  map 66% reduce 0%
17/03/10 09:18:11 INFO mapreduce.Job:  map 67% reduce 0%
17/03/10 09:18:14 INFO mapreduce.Job:  map 68% reduce 0%
17/03/10 09:18:16 INFO mapreduce.Job:  map 69% reduce 0%
17/03/10 09:18:21 INFO mapreduce.Job:  map 70% reduce 0%
17/03/10 09:18:22 INFO mapreduce.Job:  map 71% reduce 0%
17/03/10 09:18:27 INFO mapreduce.Job:  map 72% reduce 0%
17/03/10 09:18:29 INFO mapreduce.Job:  map 73% reduce 0%
17/03/10 09:18:32 INFO mapreduce.Job:  map 74% reduce 0%
17/03/10 09:18:36 INFO mapreduce.Job:  map 75% reduce 0%
17/03/10 09:18:38 INFO mapreduce.Job:  map 76% reduce 0%
17/03/10 09:18:41 INFO mapreduce.Job:  map 77% reduce 0%
17/03/10 09:18:44 INFO mapreduce.Job:  map 78% reduce 0%
17/03/10 09:18:47 INFO mapreduce.Job:  map 79% reduce 0%
17/03/10 09:18:51 INFO mapreduce.Job:  map 80% reduce 0%
17/03/10 09:18:53 INFO mapreduce.Job:  map 81% reduce 0%
17/03/10 09:18:57 INFO mapreduce.Job:  map 82% reduce 0%
17/03/10 09:18:59 INFO mapreduce.Job:  map 83% reduce 0%
17/03/10 09:19:02 INFO mapreduce.Job:  map 84% reduce 0%
17/03/10 09:19:07 INFO mapreduce.Job:  map 84% reduce 7%
17/03/10 09:19:08 INFO mapreduce.Job:  map 84% reduce 11%
17/03/10 09:19:10 INFO mapreduce.Job:  map 84% reduce 18%
17/03/10 09:19:11 INFO mapreduce.Job:  map 85% reduce 19%
17/03/10 09:19:14 INFO mapreduce.Job:  map 85% reduce 21%
17/03/10 09:19:16 INFO mapreduce.Job:  map 85% reduce 25%
17/03/10 09:19:17 INFO mapreduce.Job:  map 86% reduce 26%
17/03/10 09:19:19 INFO mapreduce.Job:  map 86% reduce 27%
17/03/10 09:19:20 INFO mapreduce.Job:  map 86% reduce 28%
17/03/10 09:19:22 INFO mapreduce.Job:  map 87% reduce 28%
17/03/10 09:19:23 INFO mapreduce.Job:  map 87% reduce 29%
17/03/10 09:19:27 INFO mapreduce.Job:  map 88% reduce 29%
17/03/10 09:19:32 INFO mapreduce.Job:  map 89% reduce 29%
17/03/10 09:19:35 INFO mapreduce.Job:  map 89% reduce 30%
17/03/10 09:19:39 INFO mapreduce.Job:  map 90% reduce 30%
17/03/10 09:19:46 INFO mapreduce.Job:  map 91% reduce 30%
17/03/10 09:19:51 INFO mapreduce.Job:  map 92% reduce 30%
17/03/10 09:19:52 INFO mapreduce.Job:  map 92% reduce 31%
17/03/10 09:19:56 INFO mapreduce.Job:  map 93% reduce 31%
17/03/10 09:20:01 INFO mapreduce.Job:  map 94% reduce 31%
17/03/10 09:20:07 INFO mapreduce.Job:  map 95% reduce 31%
17/03/10 09:20:08 INFO mapreduce.Job:  map 95% reduce 32%
17/03/10 09:20:12 INFO mapreduce.Job:  map 96% reduce 32%
17/03/10 09:20:19 INFO mapreduce.Job:  map 97% reduce 32%
17/03/10 09:20:25 INFO mapreduce.Job:  map 98% reduce 32%
17/03/10 09:20:26 INFO mapreduce.Job:  map 98% reduce 33%
17/03/10 09:20:32 INFO mapreduce.Job:  map 99% reduce 33%
17/03/10 09:20:39 INFO mapreduce.Job:  map 100% reduce 33%
17/03/10 09:20:41 INFO mapreduce.Job:  map 100% reduce 37%
17/03/10 09:20:42 INFO mapreduce.Job:  map 100% reduce 61%
17/03/10 09:20:44 INFO mapreduce.Job:  map 100% reduce 66%
17/03/10 09:20:45 INFO mapreduce.Job:  map 100% reduce 70%
17/03/10 09:20:47 INFO mapreduce.Job:  map 100% reduce 72%
17/03/10 09:20:48 INFO mapreduce.Job:  map 100% reduce 75%
17/03/10 09:20:50 INFO mapreduce.Job:  map 100% reduce 77%
17/03/10 09:20:51 INFO mapreduce.Job:  map 100% reduce 80%
17/03/10 09:20:53 INFO mapreduce.Job:  map 100% reduce 82%
17/03/10 09:20:54 INFO mapreduce.Job:  map 100% reduce 83%
17/03/10 09:20:56 INFO mapreduce.Job:  map 100% reduce 84%
17/03/10 09:20:57 INFO mapreduce.Job:  map 100% reduce 85%
17/03/10 09:20:59 INFO mapreduce.Job:  map 100% reduce 89%
17/03/10 09:21:00 INFO mapreduce.Job:  map 100% reduce 90%
17/03/10 09:21:01 INFO mapreduce.Job:  map 100% reduce 91%
17/03/10 09:21:02 INFO mapreduce.Job:  map 100% reduce 92%
17/03/10 09:21:03 INFO mapreduce.Job:  map 100% reduce 94%
17/03/10 09:21:05 INFO mapreduce.Job:  map 100% reduce 95%
17/03/10 09:21:06 INFO mapreduce.Job:  map 100% reduce 96%
17/03/10 09:21:08 INFO mapreduce.Job:  map 100% reduce 97%
17/03/10 09:21:09 INFO mapreduce.Job:  map 100% reduce 98%
17/03/10 09:21:11 INFO mapreduce.Job:  map 100% reduce 100%
17/03/10 09:21:18 INFO mapreduce.Job: Job job_1489137034771_0001 completed successfully
17/03/10 09:21:18 INFO mapreduce.Job: Counters: 50
        File System Counters
                FILE: Number of bytes read=2915256162
                FILE: Number of bytes written=5807933093
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=6553660760
                HDFS: Number of bytes written=6553600000
                HDFS: Number of read operations=1188
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=8
        Job Counters
                Launched map tasks=392
                Launched reduce tasks=4
                Data-local map tasks=391
                Rack-local map tasks=1
                Total time spent by all maps in occupied slots (ms)=2116631
                Total time spent by all reduces in occupied slots (ms)=519944
                Total time spent by all map tasks (ms)=2116631
                Total time spent by all reduce tasks (ms)=519944
                Total vcore-seconds taken by all map tasks=2116631
                Total vcore-seconds taken by all reduce tasks=519944
                Total megabyte-seconds taken by all map tasks=2167430144
                Total megabyte-seconds taken by all reduce tasks=532422656
        Map-Reduce Framework
                Map input records=65536000
                Map output records=65536000
                Map output bytes=6684672000
                Map output materialized bytes=2843108125
                Input split bytes=60760
                Combine input records=0
                Combine output records=0
                Reduce input groups=65536000
                Reduce shuffle bytes=2843108125
                Reduce input records=65536000
                Reduce output records=65536000
                Spilled Records=131072000
                Shuffled Maps =1568
                Failed Shuffles=0
                Merged Map outputs=1568
                GC time elapsed (ms)=21565
                CPU time spent (ms)=1210130
                Physical memory (bytes) snapshot=186966491136
                Virtual memory (bytes) snapshot=626161324032
                Total committed heap usage (bytes)=221910138880
        Shuffle Errors
                BAD_ID=0
                CONNECTION=0
                IO_ERROR=0
                WRONG_LENGTH=0
                WRONG_MAP=0
                WRONG_REDUCE=0
        File Input Format Counters
                Bytes Read=6553600000
        File Output Format Counters
                Bytes Written=6553600000
17/03/10 09:21:18 INFO terasort.TeraSort: done
[neymar@ip-172-31-16-183 ~]$
```
