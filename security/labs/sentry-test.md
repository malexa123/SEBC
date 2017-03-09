```
[malexa123@ip-172-31-30-231 ~]$ beeline
Beeline version 1.1.0-cdh5.8.3 by Apache Hive
beeline> !connect jdbc:hive2://localhost:10000/default;principal=hive/ip-172-31-30-231.eu-central-1.compute.internal@ZECMA.DOLE
scan complete in 3ms
Connecting to jdbc:hive2://localhost:10000/default;principal=hive/ip-172-31-30-231.eu-central-1.compute.internal@ZECMA.DOLE
Enter username for jdbc:hive2://localhost:10000/default;principal=hive/ip-172-31-30-231.eu-central-1.compute.internal@ZECMA.DOLE: malexa123
Enter password for jdbc:hive2://localhost:10000/default;principal=hive/ip-172-31-30-231.eu-central-1.compute.internal@ZECMA.DOLE: ********
Connected to: Apache Hive (version 1.1.0-cdh5.8.3)
Driver: Hive JDBC (version 1.1.0-cdh5.8.3)
Transaction isolation: TRANSACTION_REPEATABLE_READ
0: jdbc:hive2://localhost:10000/default>
0: jdbc:hive2://localhost:10000/default>
0: jdbc:hive2://localhost:10000/default> show databases;
INFO  : Compiling command(queryId=hive_20170309091111_7bbcd206-6e19-453a-ba8f-236d2a6f64b8): show databases
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:database_name, type:string, comment:from deserializer)], properties:null)
INFO  : Completed compiling command(queryId=hive_20170309091111_7bbcd206-6e19-453a-ba8f-236d2a6f64b8); Time taken: 0.718 seconds
INFO  : Executing command(queryId=hive_20170309091111_7bbcd206-6e19-453a-ba8f-236d2a6f64b8): show databases
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20170309091111_7bbcd206-6e19-453a-ba8f-236d2a6f64b8); Time taken: 0.135 seconds
INFO  : OK
+----------------+--+
| database_name  |
+----------------+--+
| default        |
+----------------+--+
1 row selected (2.101 seconds)
0: jdbc:hive2://localhost:10000/default> show tables;
INFO  : Compiling command(queryId=hive_20170309091111_0f322ab4-3ce7-4c19-ae7a-d960ee9db923): show tables
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, type:string, comment:from deserializer)], properties:null)
INFO  : Completed compiling command(queryId=hive_20170309091111_0f322ab4-3ce7-4c19-ae7a-d960ee9db923); Time taken: 0.061 seconds
INFO  : Executing command(queryId=hive_20170309091111_0f322ab4-3ce7-4c19-ae7a-d960ee9db923): show tables
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20170309091111_0f322ab4-3ce7-4c19-ae7a-d960ee9db923); Time taken: 0.154 seconds
INFO  : OK
+-----------+--+
| tab_name  |
+-----------+--+
+-----------+--+
No rows selected (0.227 seconds)
0: jdbc:hive2://localhost:10000/default>

```
