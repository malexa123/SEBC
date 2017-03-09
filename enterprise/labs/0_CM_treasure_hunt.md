• What is ubertask optimization?
It's a way of running "small jobs" where Map and Reduce tasks are done only on one JVM for simplification purposes. You can edit in CM what is considered as small job based on number of Map, Reduce jobs and size of the data volume.

• Where in CM is the Kerberos Security Realm value displayed?
Administration -> Security -> Kerberos credentials -> Configuration

• Which CDH service(s) host a property for enabling Kerberos authentication?
YARN, HDFS, Zookeeper. Other service use Kerberos principals once configured.

• How do you upgrade the CM agents?
You upgrade CM to latest version, login and upgrade CM agents afterwards.

• Give the tsquery statement used to chart Hue's CPU utilization?
SELECT cpu_user_rate WHERE roleType=HUE_SERVER 

• Name all the roles that make up the Hive service
Hive Metastore, Hive Server2, Gateway

• What steps must be completed before integrating Cloudera Manager with Kerberos?
Install Kerberos server, libs and configure it among all hosts. Kerberos principal to be used by wizard.
