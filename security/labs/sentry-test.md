```
[malexa123@ip-172-31-30-231 ~]$ kinit george
Password for george@ZECMA.DOLE:
[malexa123@ip-172-31-30-231 ~]$ beeline
Beeline version 1.1.0-cdh5.8.3 by Apache Hive
beeline> !connect jdbc:hive2://localhost:10000/default;principal=hive/ip-172-31-30-231.eu-central-1.compute.internal@ZECMA.DOLE
scan complete in 2ms
Connecting to jdbc:hive2://localhost:10000/default;principal=hive/ip-172-31-30-231.eu-central-1.compute.internal@ZECMA.DOLE
Enter username for jdbc:hive2://localhost:10000/default;principal=hive/ip-172-31-30-231.eu-central-1.compute.internal@ZECMA.DOLE: george
Enter password for jdbc:hive2://localhost:10000/default;principal=hive/ip-172-31-30-231.eu-central-1.compute.internal@ZECMA.DOLE: ********
Connected to: Apache Hive (version 1.1.0-cdh5.8.3)
Driver: Hive JDBC (version 1.1.0-cdh5.8.3)
Transaction isolation: TRANSACTION_REPEATABLE_READ
0: jdbc:hive2://localhost:10000/default> show tables;
INFO  : Compiling command(queryId=hive_20170309094646_b13c7aa0-5d8f-4b68-be0a-37fdba54eea0): show tables
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, type:string, comment:from deserializer)], properties:null)
INFO  : Completed compiling command(queryId=hive_20170309094646_b13c7aa0-5d8f-4b68-be0a-37fdba54eea0); Time taken: 0.053 seconds
INFO  : Executing command(queryId=hive_20170309094646_b13c7aa0-5d8f-4b68-be0a-37fdba54eea0): show tables
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20170309094646_b13c7aa0-5d8f-4b68-be0a-37fdba54eea0); Time taken: 0.108 seconds
INFO  : OK
+------------+--+
|  tab_name  |
+------------+--+
| customers  |
| sample_07  |
| sample_08  |
| web_logs   |
+------------+--+
4 rows selected (0.276 seconds)
0: jdbc:hive2://localhost:10000/default> show current roles;
INFO  : Compiling command(queryId=hive_20170309094646_72589261-a282-4d03-8b01-2f984f720fa3): show current roles
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:role, type:string, comment:from deserializer)], properties:null)
INFO  : Completed compiling command(queryId=hive_20170309094646_72589261-a282-4d03-8b01-2f984f720fa3); Time taken: 0.051 seconds
INFO  : Executing command(queryId=hive_20170309094646_72589261-a282-4d03-8b01-2f984f720fa3): show current roles
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20170309094646_72589261-a282-4d03-8b01-2f984f720fa3); Time taken: 0.018 seconds
INFO  : OK
+--------+--+
|  role  |
+--------+--+
| reads  |
+--------+--+
1 row selected (0.081 seconds)
0: jdbc:hive2://localhost:10000/default> [malexa123@ip-172-31-30-231 ~]$ kinit ferdinand
Password for ferdinand@ZECMA.DOLE:
[malexa123@ip-172-31-30-231 ~]$ beeline
Beeline version 1.1.0-cdh5.8.3 by Apache Hive
beeline> !connect jdbc:hive2://localhost:10000/default;principal=hive/ip-172-31-30-231.eu-central-1.compute.internal@ZECMA.DOLE
scan complete in 3ms
Connecting to jdbc:hive2://localhost:10000/default;principal=hive/ip-172-31-30-231.eu-central-1.compute.internal@ZECMA.DOLE
Enter username for jdbc:hive2://localhost:10000/default;principal=hive/ip-172-31-30-231.eu-central-1.compute.internal@ZECMA.DOLE: ferdinadn
Enter password for jdbc:hive2://localhost:10000/default;principal=hive/ip-172-31-30-231.eu-central-1.compute.internal@ZECMA.DOLE: *[malexa123@ip-172-31-30-231 ~]$ beeline
Beeline version 1.1.0-cdh5.8.3 by Apache Hive
beeline> !connect jdbc:hive2://localhost:10000/default;principal=hive/ip-172-31-30-231.eu-central-1.compute.internal@ZECMA.DOLE
scan complete in 3ms
Connecting to jdbc:hive2://localhost:10000/default;principal=hive/ip-172-31-30-231.eu-central-1.compute.internal@ZECMA.DOLE
Enter username for jdbc:hive2://localhost:10000/default;principal=hive/ip-172-31-30-231.eu-central-1.compute.internal@ZECMA.DOLE: ferdinand
Enter password for jdbc:hive2://localhost:10000/default;principal=hive/ip-172-31-30-231.eu-central-1.compute.internal@ZECMA.DOLE: ********
Connected to: Apache Hive (version 1.1.0-cdh5.8.3)
Driver: Hive JDBC (version 1.1.0-cdh5.8.3)
Transaction isolation: TRANSACTION_REPEATABLE_READ
0: jdbc:hive2://localhost:10000/default> show tables;
INFO  : Compiling command(queryId=hive_20170309094747_2034c692-32d4-424a-92c7-577b3cd3cefb): show tables
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, type:string, comment:from deserializer)], properties:null)
INFO  : Completed compiling command(queryId=hive_20170309094747_2034c692-32d4-424a-92c7-577b3cd3cefb); Time taken: 0.08 seconds
INFO  : Executing command(queryId=hive_20170309094747_2034c692-32d4-424a-92c7-577b3cd3cefb): show tables
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20170309094747_2034c692-32d4-424a-92c7-577b3cd3cefb); Time taken: 0.113 seconds
INFO  : OK
+------------+--+
|  tab_name  |
+------------+--+
| sample_07  |
+------------+--+
1 row selected (0.309 seconds)
0: jdbc:hive2://localhost:10000/default> show current roles;
INFO  : Compiling command(queryId=hive_20170309094747_2bb67489-ac2b-4f08-b838-21ff35c14095): show current roles
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:role, type:string, comment:from deserializer)], properties:null)
INFO  : Completed compiling command(queryId=hive_20170309094747_2bb67489-ac2b-4f08-b838-21ff35c14095); Time taken: 0.051 seconds
INFO  : Executing command(queryId=hive_20170309094747_2bb67489-ac2b-4f08-b838-21ff35c14095): show current roles
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20170309094747_2bb67489-ac2b-4f08-b838-21ff35c14095); Time taken: 0.023 seconds
INFO  : OK
+---------+--+
|  role   |
+---------+--+
| writes  |
+---------+--+
1 row selected (0.085 seconds)
0: jdbc:hive2://localhost:10000/default>


```
