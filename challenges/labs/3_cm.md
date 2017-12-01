# Install CDH 5.9
## User´s folders
```
[centos@ip-10-0-3-201 ~]$ sudo -u hdfs hdfs dfs -ls /user/
Found 7 items
drwxr-xr-x   - haley  comets           0 2017-12-01 18:50 /user/haley
drwxrwxrwx   - mapred hadoop           0 2017-12-01 18:45 /user/history
drwxrwxr-t   - hive   hive             0 2017-12-01 18:46 /user/hive
drwxrwxr-x   - hue    hue              0 2017-12-01 18:46 /user/hue
drwxrwxr-x   - oozie  oozie            0 2017-12-01 18:47 /user/oozie
drwxr-xr-x   - saturn  planets          0 2017-12-01 18:50 /user/saturn
drwxr-x--x   - spark  spark            0 2017-12-01 18:45 /user/spark

```
## Hosts
```
[centos@ip-10-0-3-17 ~]$ curl -X GET -u admin:admin http://52.203.21.69:7180/api/v14/hosts
{
  "items" : [ {
    "hostId" : "fc12f7db-83e9-4b56-a83e-ee549b585899",
    "ipAddress" : "10.0.3.17",
    "hostname" : "ip-10-0-3-17.ec2.internal",
    "rackId" : "/default",
    "hostUrl" : "http://ip-10-0-3-35.ec2.internal:7180/cmf/hostRedirect/fc12f7db-                                                                                       83e9-4b56-a83e-ee549b585899",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 8,
    "numPhysicalCores" : 4,
    "totalPhysMemBytes" : 31549353984
  }, {
    "hostId" : "f1b68fd2-5402-423b-98f5-20fe83f9c694",
    "ipAddress" : "10.0.3.201",
    "hostname" : "ip-10-0-3-201.ec2.internal",
    "rackId" : "/default",
    "hostUrl" : "http://ip-10-0-3-35.ec2.internal:7180/cmf/hostRedirect/f1b68fd2-                                                                                       5402-423b-98f5-20fe83f9c694",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 8,
    "numPhysicalCores" : 4,
    "totalPhysMemBytes" : 31549353984
  }, {
    "hostId" : "70efd194-550b-4255-af27-382cf5e8a0e7",
    "ipAddress" : "10.0.3.219",
    "hostname" : "ip-10-0-3-219.ec2.internal",
    "rackId" : "/default",
    "hostUrl" : "http://ip-10-0-3-35.ec2.internal:7180/cmf/hostRedirect/70efd194-                                                                                       550b-4255-af27-382cf5e8a0e7",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 8,
    "numPhysicalCores" : 4,
    "totalPhysMemBytes" : 31549353984
  }, {
    "hostId" : "9a917a20-ab33-4323-b44a-90c6eb909417",
    "ipAddress" : "10.0.3.35",
    "hostname" : "ip-10-0-3-35.ec2.internal",
    "rackId" : "/default",
    "hostUrl" : "http://ip-10-0-3-35.ec2.internal:7180/cmf/hostRedirect/9a917a20-                                                                                       ab33-4323-b44a-90c6eb909417",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 8,
    "numPhysicalCores" : 4,
    "totalPhysMemBytes" : 31549353984
  } ]
}
```
## Services
```
[centos@ip-10-0-3-17 ~]$
[centos@ip-10-0-3-17 ~]$ curl -X GET -u admin:admin http://52.203.21.69:7180/api/v8/clusters/jlusancheza/services
{
  "items" : [ {
    "name" : "hive",
    "type" : "HIVE",
    "clusterRef" : {
      "clusterName" : "cluster"
    },
    "serviceUrl" : "http://ip-10-0-3-35.ec2.internal:7180/cmf/serviceRedirect/hiv                                                                                       e",
    "serviceState" : "STARTED",
    "healthSummary" : "GOOD",
    "healthChecks" : [ {
      "name" : "HIVE_HIVEMETASTORES_HEALTHY",
      "summary" : "GOOD"
    }, {
      "name" : "HIVE_HIVESERVER2S_HEALTHY",
      "summary" : "GOOD"
    } ],
    "configStalenessStatus" : "FRESH",
    "clientConfigStalenessStatus" : "FRESH",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "displayName" : "Hive"
  }, {
    "name" : "zookeeper",
    "type" : "ZOOKEEPER",
    "clusterRef" : {
      "clusterName" : "cluster"
    },
    "serviceUrl" : "http://ip-10-0-3-35.ec2.internal:7180/cmf/serviceRedirect/zoo                                                                                       keeper",
    "serviceState" : "STARTED",
    "healthSummary" : "GOOD",
    "healthChecks" : [ {
      "name" : "ZOOKEEPER_CANARY_HEALTH",
      "summary" : "GOOD"
    }, {
      "name" : "ZOOKEEPER_SERVERS_HEALTHY",
      "summary" : "GOOD"
    } ],
    "configStalenessStatus" : "FRESH",
    "clientConfigStalenessStatus" : "FRESH",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "displayName" : "ZooKeeper"
  }, {
    "name" : "hue",
    "type" : "HUE",
    "clusterRef" : {
      "clusterName" : "cluster"
    },
    "serviceUrl" : "http://ip-10-0-3-35.ec2.internal:7180/cmf/serviceRedirect/hue                                                                                       ",
    "serviceState" : "STARTED",
    "healthSummary" : "GOOD",
    "healthChecks" : [ {
      "name" : "HUE_HUE_SERVERS_HEALTHY",
      "summary" : "GOOD"
    } ],
    "configStalenessStatus" : "FRESH",
    "clientConfigStalenessStatus" : "FRESH",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "displayName" : "Hue"
  }, {
    "name" : "oozie",
    "type" : "OOZIE",
    "clusterRef" : {
      "clusterName" : "cluster"
    },
    "serviceUrl" : "http://ip-10-0-3-35.ec2.internal:7180/cmf/serviceRedirect/ooz                                                                                       ie",
    "serviceState" : "STARTED",
    "healthSummary" : "GOOD",
    "healthChecks" : [ {
      "name" : "OOZIE_OOZIE_SERVERS_HEALTHY",
      "summary" : "GOOD"
    } ],
    "configStalenessStatus" : "FRESH",
    "clientConfigStalenessStatus" : "FRESH",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "displayName" : "Oozie"
  }, {
    "name" : "yarn",
    "type" : "YARN",
    "clusterRef" : {
      "clusterName" : "cluster"
    },
    "serviceUrl" : "http://ip-10-0-3-35.ec2.internal:7180/cmf/serviceRedirect/yar                                                                                       n",
    "serviceState" : "STARTED",
    "healthSummary" : "GOOD",
    "healthChecks" : [ {
      "name" : "YARN_JOBHISTORY_HEALTH",
      "summary" : "GOOD"
    }, {
      "name" : "YARN_NODE_MANAGERS_HEALTHY",
      "summary" : "GOOD"
    }, {
      "name" : "YARN_RESOURCEMANAGERS_HEALTH",
      "summary" : "GOOD"
    }, {
      "name" : "YARN_USAGE_AGGREGATION_HEALTH",
      "summary" : "DISABLED"
    } ],
    "configStalenessStatus" : "FRESH",
    "clientConfigStalenessStatus" : "FRESH",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "displayName" : "YARN (MR2 Included)"
  }, {
    "name" : "spark_on_yarn",
    "type" : "SPARK_ON_YARN",
    "clusterRef" : {
      "clusterName" : "cluster"
    },
    "serviceUrl" : "http://ip-10-0-3-35.ec2.internal:7180/cmf/serviceRedirect/spa                                                                                       rk_on_yarn",
    "serviceState" : "STARTED",
    "healthSummary" : "GOOD",
    "healthChecks" : [ ],
    "configStalenessStatus" : "FRESH",
    "clientConfigStalenessStatus" : "FRESH",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "displayName" : "Spark"
  }, {
    "name" : "hdfs",
    "type" : "HDFS",
    "clusterRef" : {
      "clusterName" : "cluster"
    },
    "serviceUrl" : "http://ip-10-0-3-35.ec2.internal:7180/cmf/serviceRedirect/hdf                                                                                       s",
    "serviceState" : "STARTED",
    "healthSummary" : "GOOD",
    "healthChecks" : [ {
      "name" : "HDFS_BLOCKS_WITH_CORRUPT_REPLICAS",
      "summary" : "GOOD"
    }, {
      "name" : "HDFS_CANARY_HEALTH",
      "summary" : "GOOD"
    }, {
      "name" : "HDFS_DATA_NODES_HEALTHY",
      "summary" : "GOOD"
    }, {
      "name" : "HDFS_FREE_SPACE_REMAINING",
      "summary" : "GOOD"
    }, {
      "name" : "HDFS_HA_NAMENODE_HEALTH",
      "summary" : "GOOD"
    }, {
      "name" : "HDFS_MISSING_BLOCKS",
      "summary" : "GOOD"
    }, {
      "name" : "HDFS_UNDER_REPLICATED_BLOCKS",
      "summary" : "GOOD"
    } ],
    "configStalenessStatus" : "FRESH",
    "clientConfigStalenessStatus" : "FRESH",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "displayName" : "HDFS"
  } ]

```