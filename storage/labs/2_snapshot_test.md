# Test snapshot

## Commands

```
[centos@ip-10-0-3-126 ~]$ sudo -u hdfs hdfs dfs -mkdir /precious
[centos@ip-10-0-3-126 ~]$ sudo -u hdfs dfs -put SEBC.zip /precious
sudo: dfs: command not found
[centos@ip-10-0-3-126 ~]$ sudo -u hdfs hdfs dfs -put SEBC.zip /precious


[centos@ip-10-0-3-126 ~]$ sudo -u hdfs hdfs dfsadmin -allowSnapshot /precious
Allowing snaphot on /precious succeeded
[centos@ip-10-0-3-126 ~]$ sudo -u hdfs hdfs dfs -createSnapshot /precious sebc-hdfs-test
Created snapshot /precious/.snapshot/sebc-hdfs-test


[centos@ip-10-0-3-126 ~]$ sudo -u hdfs hdfs dfs -rm -R /precious
rm: Failed to move to trash: hdfs://ip-10-0-3-126.ec2.internal:8020/precious: The directory          /precious cannot be deleted since /precious is snapshottable and already has snapshots


[centos@ip-10-0-3-126 ~]$ sudo -u hdfs hdfs dfs -rm  /precious/SEBC.zip
17/11/28 17:45:50 INFO fs.TrashPolicyDefault: Moved: 'hdfs://ip-10-0-3-126.ec2.internal:8020/precious/SEBC.zip' to trash at: hdfs://ip-10-0-3-126.ec2.internal:8020/user/hdfs/.Trash/Current/precious/SEBC.zip1511891150738


[centos@ip-10-0-3-126 ~]$ sudo -u hdfs hdfs dfs -ls /precious/.snapshot
Found 1 items
drwxr-xr-x   - hdfs supergroup          0 2017-11-28 17:44 /precious/.snapshot/sebc-hdfs-test
[centos@ip-10-0-3-126 ~]$ sudo -u hdfs hdfs dfs -ls /precious/.snapshot/sebc-hdfs-test
Found 1 items
-rw-r--r--   3 hdfs supergroup     474833 2017-11-28 17:42 /precious/.snapshot/sebc-hdfs-test/SEBC.zip


[centos@ip-10-0-3-126 ~]$ sudo -u hdfs hdfs dfs -cp /precious/.snapshot/sebc-hdfs-test/SEBC.zip /precious/SEBC.zip
[centos@ip-10-0-3-126 ~]$ sudo -u hdfs hdfs dfs -ls /precious
Found 1 items
-rw-r--r--   3 hdfs supergroup     474833 2017-11-28 17:48 /precious/SEBC.zip

```