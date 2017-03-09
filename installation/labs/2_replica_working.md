#Database Install and configuration
#monkey CMS server
yum install mariadb-server
#copy old config file
cp /etc/my.cnf /etc/my.cnf_old1
#add config from Cloudera recommendation
vi /etc/mv.cnf

yum install mariadb-libs.x86_64

#start service and add to automaticaly start
systemctl start mariadb.service
systemctl enable mariadb.service

#secure installation
/usr/bin/mysql_secure_installation

#root password mariadb

#JDBC connector
cd /tmp && tar zxvf mysql-connector-java-5.1.41.tar.gz && mkdir /usr/share/java && cp ./mysql-connector-java-5.1.41/mysql-connector-java-5.1.41-bin.jar /usr/share/java/mysql-connector-java.jar && ls -la /usr/share/java

#GALERA MariadDB

#database setup
mysql -u root -p
Enter password:

create database amon DEFAULT CHARACTER SET utf8;
create database rman DEFAULT CHARACTER SET utf8;
create database metastore DEFAULT CHARACTER SET utf8;
create database sentry DEFAULT CHARACTER SET utf8;
create database nav DEFAULT CHARACTER SET utf8;
create database navms DEFAULT CHARACTER SET utf8;

grant all on amon.* TO 'amon'@'%' IDENTIFIED BY 'amon_password';
grant all on rman.* TO 'rman'@'%' IDENTIFIED BY 'rman_password';
grant all on metastore.* TO 'hive'@'%' IDENTIFIED BY 'hive_password';
grant all on sentry.* TO 'sentry'@'%' IDENTIFIED BY 'sentry_password';
grant all on nav.* TO 'nav'@'%' IDENTIFIED BY 'nav_password';
grant all on navms.* TO 'navms'@'%' IDENTIFIED BY 'navms_password';

create database oozie;
grant all privileges on oozie.* to 'oozie'@'localhost' identified by 'oozie';
grant all privileges on oozie.* to 'oozie'@'%' identified by 'oozie';

#Replication setup: MASTER
systemctl stop mariadb.service
systemctl status mariadb.service
vi /etc/my.cnf
systemctl start mariadb.service
mysql -u root -p
#check for skip-networking=1 (pruser); bind-address 127.0.0.1 (pruser)
show variables;
GRANT REPLICATION SLAVE ON *.* TO replication_user;
systemctl restart mariadb.service

#Replication setup: SLAVE
yum install mariadb-server
systemctl stop mariadb.service
cp /etc/my.cnf /etc/my.cnf_old1
#same config as on master  change server_id=2 and log-basename=slave1
vi /my.cnf
#secure installation
/usr/bin/mysql_secure_installation
systemctl restart mariadb.service

#MASTER
# you need two sessions
#1
mysql -u root -p
> FLUSH TABLES WITH READ LOCK
>
#2
mysql -u root -p
> show master status;
+--------------------+----------+--------------+------------------+
| File               | Position | Binlog_Do_DB | Binlog_Ignore_DB |
+--------------------+----------+--------------+------------------+
| master1-bin.000002 |      245 |              |                  |
+--------------------+----------+--------------+------------------+
1 row in set (0.00 sec)

mysqldump -u root -p --all-databases > all.databases.sql

#SLAVE
mysql -u root -p < all.databases.sql

#MASTER
>unlock tables;

#SLAVE
>CHANGE MASTER TO
  MASTER_HOST='ip-172-31-24-214.eu-central-1.compute.internal',
  MASTER_USER='replication_user',
  MASTER_PORT=3306,
  MASTER_LOG_FILE='master1-bin.000002',
  MASTER_LOG_POS=245,
  MASTER_CONNECT_RETRY=10;

>START SLAVE;
>SHOW SLAVE STATUS;
MariaDB [(none)]> SHOW SLAVE STATUS;
+----------------------------------+------------------------------------------------+------------------+-------------+---------------+--------------------+---------------------+-------------------------+---------------+-----------------------+------------------+-------------------+-----------------+---------------------+--------------------+------------------------+-------------------------+-----------------------------+------------+------------+--------------+---------------------+-----------------+-----------------+----------------+---------------+--------------------+--------------------+--------------------+-----------------+-------------------+----------------+-----------------------+-------------------------------+---------------+---------------+----------------+----------------+-----------------------------+------------------+
| Slave_IO_State                   | Master_Host                                    | Master_User      | Master_Port | Connect_Retry | Master_Log_File    | Read_Master_Log_Pos | Relay_Log_File          | Relay_Log_Pos | Relay_Master_Log_File | Slave_IO_Running | Slave_SQL_Running | Replicate_Do_DB | Replicate_Ignore_DB | Replicate_Do_Table | Replicate_Ignore_Table | Replicate_Wild_Do_Table | Replicate_Wild_Ignore_Table | Last_Errno | Last_Error | Skip_Counter | Exec_Master_Log_Pos | Relay_Log_Space | Until_Condition | Until_Log_File | Until_Log_Pos | Master_SSL_Allowed | Master_SSL_CA_File | Master_SSL_CA_Path | Master_SSL_Cert | Master_SSL_Cipher | Master_SSL_Key | Seconds_Behind_Master | Master_SSL_Verify_Server_Cert | Last_IO_Errno | Last_IO_Error | Last_SQL_Errno | Last_SQL_Error | Replicate_Ignore_Server_Ids | Master_Server_Id |
+----------------------------------+------------------------------------------------+------------------+-------------+---------------+--------------------+---------------------+-------------------------+---------------+-----------------------+------------------+-------------------+-----------------+---------------------+--------------------+------------------------+-------------------------+-----------------------------+------------+------------+--------------+---------------------+-----------------+-----------------+----------------+---------------+--------------------+--------------------+--------------------+-----------------+-------------------+----------------+-----------------------+-------------------------------+---------------+---------------+----------------+----------------+-----------------------------+------------------+
| Waiting for master to send event | ip-172-31-24-214.eu-central-1.compute.internal | replication_user |        3306 |            10 | master1-bin.000002 |                 245 | slave1-relay-bin.000002 |           531 | master1-bin.000002    | Yes              | Yes               |                 |                     |                    |                        |                         |                             |          0 |            |            0 |                 245 |             826 | None            |                |             0 | No                 |                    |                    |                 |                   |                |                     0 | No                            |             0 |               |              0 |                |                             |                1 |
+----------------------------------+------------------------------------------------+------------------+-------------+---------------+--------------------+---------------------+-------------------------+---------------+-----------------------+------------------+-------------------+-----------------+---------------------+--------------------+------------------------+-------------------------+-----------------------------+------------+------------+--------------+---------------------+-----------------+-----------------+----------------+---------------+--------------------+--------------------+--------------------+-----------------+-------------------+----------------+-----------------------+-------------------------------+---------------+---------------+----------------+----------------+-----------------------------+------------------+
1 row in set (0.00 sec)


#MASTER
>create database test DEFAULT CHARACTER SET utf8;

#SLAVE
>show databases;
MariaDB [(none)]> show databases;
+--------------------+
| Database           |
+--------------------+
| information_schema |
| amon               |
| metastore          |
| mysql              |
| nav                |
| navms              |
| oozie              |
| performance_schema |
| rman               |
| sentry             |
| test               |
+--------------------+
11 rows in set (0.00 sec)

MariaDB [(none)]>

MariaDB [(none)]> show slave status;
+----------------------------------+------------------------------------------------+------------------+-------------+---------------+--------------------+---------------------+-------------------------+---------------+-----------------------+------------------+-------------------+-----------------+---------------------+--------------------+------------------------+-------------------------+-----------------------------+------------+------------+--------------+---------------------+-----------------+-----------------+----------------+---------------+--------------------+--------------------+--------------------+-----------------+-------------------+----------------+-----------------------+-------------------------------+---------------+---------------+----------------+----------------+-----------------------------+------------------+
| Slave_IO_State                   | Master_Host                                    | Master_User      | Master_Port | Connect_Retry | Master_Log_File    | Read_Master_Log_Pos | Relay_Log_File          | Relay_Log_Pos | Relay_Master_Log_File | Slave_IO_Running | Slave_SQL_Running | Replicate_Do_DB | Replicate_Ignore_DB | Replicate_Do_Table | Replicate_Ignore_Table | Replicate_Wild_Do_Table | Replicate_Wild_Ignore_Table | Last_Errno | Last_Error | Skip_Counter | Exec_Master_Log_Pos | Relay_Log_Space | Until_Condition | Until_Log_File | Until_Log_Pos | Master_SSL_Allowed | Master_SSL_CA_File | Master_SSL_CA_Path | Master_SSL_Cert | Master_SSL_Cipher | Master_SSL_Key | Seconds_Behind_Master | Master_SSL_Verify_Server_Cert | Last_IO_Errno | Last_IO_Error | Last_SQL_Errno | Last_SQL_Error | Replicate_Ignore_Server_Ids | Master_Server_Id |
+----------------------------------+------------------------------------------------+------------------+-------------+---------------+--------------------+---------------------+-------------------------+---------------+-----------------------+------------------+-------------------+-----------------+---------------------+--------------------+------------------------+-------------------------+-----------------------------+------------+------------+--------------+---------------------+-----------------+-----------------+----------------+---------------+--------------------+--------------------+--------------------+-----------------+-------------------+----------------+-----------------------+-------------------------------+---------------+---------------+----------------+----------------+-----------------------------+------------------+
| Waiting for master to send event | ip-172-31-24-214.eu-central-1.compute.internal | replication_user |        3306 |            10 | master1-bin.000002 |                 355 | slave1-relay-bin.000002 |           641 | master1-bin.000002    | Yes              | Yes               |                 |                     |                    |                        |                         |                             |          0 |            |            0 |                 355 |             936 | None            |                |             0 | No                 |                    |                    |                 |                   |                |                     0 | No                            |             0 |               |              0 |                |                             |                1 |
+----------------------------------+------------------------------------------------+------------------+-------------+---------------+--------------------+---------------------+-------------------------+---------------+-----------------------+------------------+-------------------+-----------------+---------------------+--------------------+------------------------+-------------------------+-----------------------------+------------+------------+--------------+---------------------+-----------------+-----------------+----------------+---------------+--------------------+--------------------+--------------------+-----------------+-------------------+----------------+-----------------------+-------------------------------+---------------+---------------+----------------+----------------+-----------------------------+------------------+
1 row in set (0.00 sec)

MariaDB [(none)]>
