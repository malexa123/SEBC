* I've changed number of vcores necessary for the OS. 1 should be enough. With memory of 12,8GB (10% of total) it's quite finetuned.
* Rest is left based on recommendation from Cloudera.
* Result is Workload factor of 1.33~ what counts ideal setup for 13MAP and 13Reduce Jobs.

#Criteria for Workload factor
1. Number of CPUs free for Yarn to utilize
2. Number of Disks that are free for HDFS utilization
3. Number of vcores in Task container - size of the container.
* Smaller the number bigger chance of bottleneck on CPU's, higher the number bigger chance of bottleneck on disks I/O's
