# Cluster Deployment
```
{
  "timestamp" : "2017-11-30T17:19:30.609Z",
  "clusters" : [ {
    "name" : "jlusancheza",
    "version" : "CDH5",
    "services" : [ {
      "name" : "hive",
      "type" : "HIVE",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "HIVEMETASTORE",
          "items" : [ {
            "name" : "hive_metastore_server_max_message_size",
            "value" : "858993459"
          } ]
        }, {
          "roleType" : "HIVESERVER2",
          "items" : [ {
            "name" : "hiveserver2_enable_impersonation",
            "value" : "false"
          }, {
            "name" : "hiveserver2_java_heapsize",
            "value" : "4080218931"
          }, {
            "name" : "hiveserver2_spark_driver_memory",
            "value" : "966367641"
          }, {
            "name" : "hiveserver2_spark_executor_cores",
            "value" : "4"
          }, {
            "name" : "hiveserver2_spark_executor_memory",
            "value" : "2335624396"
          }, {
            "name" : "hiveserver2_spark_yarn_driver_memory_overhead",
            "value" : "102"
          }, {
            "name" : "hiveserver2_spark_yarn_executor_memory_overhead",
            "value" : "393"
          } ]
        } ],
        "items" : [ {
          "name" : "hive_metastore_database_host",
          "value" : "ip-10-0-3-96.ec2.internal"
        }, {
          "name" : "hive_metastore_database_password",
          "value" : "password"
        }, {
          "name" : "mapreduce_yarn_service",
          "value" : "yarn"
        }, {
          "name" : "sentry_service",
          "value" : "sentry"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "hive-GATEWAY-ea85d7631ccd062a61118c35975177f9",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "e0fccfa2-3dde-4159-9675-920b43a8a17a"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-HIVEMETASTORE-4b651c7ae701fccc378d431d0f4803e6",
        "type" : "HIVEMETASTORE",
        "hostRef" : {
          "hostId" : "864c120e-55b2-4dff-ba1f-ee41c90361ef"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "95ywsg95mrv955pil2xou66j1"
          } ]
        }
      }, {
        "name" : "hive-HIVESERVER2-d8e636f263e9a814802f441b53b3fb29",
        "type" : "HIVESERVER2",
        "hostRef" : {
          "hostId" : "907b0099-5930-42ab-bf6d-a2a6796d3c50"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "3fnmqkvriravt1idc8ukwaen2"
          } ]
        }
      }, {
        "name" : "hive-HIVESERVER2-ea85d7631ccd062a61118c35975177f9",
        "type" : "HIVESERVER2",
        "hostRef" : {
          "hostId" : "e0fccfa2-3dde-4159-9675-920b43a8a17a"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "za0zpe0dng8ib1wnke9ag647"
          } ]
        }
      } ],
      "displayName" : "Hive"
    }, {
      "name" : "zookeeper",
      "type" : "ZOOKEEPER",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "SERVER",
          "items" : [ {
            "name" : "dataDir",
            "value" : "/var/log/zookeeper"
          }, {
            "name" : "dataLogDir",
            "value" : "/var/log/zookeeper"
          } ]
        } ],
        "items" : [ {
          "name" : "enableSecurity",
          "value" : "true"
        } ]
      },
      "roles" : [ {
        "name" : "zookeeper-SERVER-3df3e7656abb08cfa5c50885c0ecbb75",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "926254b5-a026-49dc-9889-c60925552df4"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "7l7i5uefhqefbsaatvgff91y9"
          }, {
            "name" : "serverId",
            "value" : "1"
          } ]
        }
      }, {
        "name" : "zookeeper-SERVER-d8e636f263e9a814802f441b53b3fb29",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "907b0099-5930-42ab-bf6d-a2a6796d3c50"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "clgf2uf3br0iuyfuwkbxcwowd"
          }, {
            "name" : "serverId",
            "value" : "2"
          } ]
        }
      }, {
        "name" : "zookeeper-SERVER-ea85d7631ccd062a61118c35975177f9",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "e0fccfa2-3dde-4159-9675-920b43a8a17a"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "c2uzjqoxicmq14rx493qsjqzn"
          }, {
            "name" : "serverId",
            "value" : "3"
          } ]
        }
      } ],
      "displayName" : "ZooKeeper"
    }, {
      "name" : "oozie",
      "type" : "OOZIE",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "OOZIE_SERVER",
          "items" : [ {
            "name" : "oozie_database_host",
            "value" : "ip-10-0-3-96.ec2.internal"
          }, {
            "name" : "oozie_database_password",
            "value" : "password"
          }, {
            "name" : "oozie_database_type",
            "value" : "mysql"
          }, {
            "name" : "oozie_database_user",
            "value" : "oozie"
          } ]
        } ],
        "items" : [ {
          "name" : "hive_service",
          "value" : "hive"
        }, {
          "name" : "mapreduce_yarn_service",
          "value" : "yarn"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "oozie-OOZIE_SERVER-3df3e7656abb08cfa5c50885c0ecbb75",
        "type" : "OOZIE_SERVER",
        "hostRef" : {
          "hostId" : "926254b5-a026-49dc-9889-c60925552df4"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "lviclz1qf14fmfgmcd9rbi1t"
          } ]
        }
      } ],
      "displayName" : "Oozie"
    }, {
      "name" : "yarn",
      "type" : "YARN",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "GATEWAY",
          "items" : [ {
            "name" : "mapred_reduce_tasks",
            "value" : "12"
          }, {
            "name" : "mapred_submit_replication",
            "value" : "3"
          } ]
        }, {
          "roleType" : "NODEMANAGER",
          "items" : [ {
            "name" : "container_executor_allowed_system_users",
            "value" : "nobody,impala,hive,llama,hbase,hue"
          }, {
            "name" : "yarn_nodemanager_heartbeat_interval_ms",
            "value" : "100"
          }, {
            "name" : "yarn_nodemanager_local_dirs",
            "value" : "/yarn/nm,/yarn/nm"
          }, {
            "name" : "yarn_nodemanager_log_dirs",
            "value" : "/vol1/yarn/container-logs,/vol2/yarn/container-logs"
          }, {
            "name" : "yarn_nodemanager_resource_memory_mb",
            "value" : "6662"
          } ]
        }, {
          "roleType" : "RESOURCEMANAGER",
          "items" : [ {
            "name" : "yarn_scheduler_maximum_allocation_mb",
            "value" : "7338"
          }, {
            "name" : "yarn_scheduler_maximum_allocation_vcores",
            "value" : "6"
          } ]
        } ],
        "items" : [ {
          "name" : "hdfs_service",
          "value" : "hdfs"
        }, {
          "name" : "rm_dirty",
          "value" : "false"
        }, {
          "name" : "rm_last_allocation_percentage",
          "value" : "80"
        }, {
          "name" : "yarn_service_cgroups",
          "value" : "false"
        }, {
          "name" : "yarn_service_lce_always",
          "value" : "false"
        }, {
          "name" : "zk_authorization_secret_key",
          "value" : "9GEINoyGme1QSrWpcyhXM0pjs0N4B7"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "yarn-JOBHISTORY-d8e636f263e9a814802f441b53b3fb29",
        "type" : "JOBHISTORY",
        "hostRef" : {
          "hostId" : "907b0099-5930-42ab-bf6d-a2a6796d3c50"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "j18nocmzxidumi80x5fv2xq9"
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-3df3e7656abb08cfa5c50885c0ecbb75",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "926254b5-a026-49dc-9889-c60925552df4"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "987nq8tpzigvgg4332xncw3kw"
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-d8e636f263e9a814802f441b53b3fb29",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "907b0099-5930-42ab-bf6d-a2a6796d3c50"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "a529qny3kg1r83u8j6ozow44c"
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-ea85d7631ccd062a61118c35975177f9",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "e0fccfa2-3dde-4159-9675-920b43a8a17a"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "bdh0zufazr9uetyg6nuy5ases"
          } ]
        }
      }, {
        "name" : "yarn-RESOURCEMANAGER-3df3e7656abb08cfa5c50885c0ecbb75",
        "type" : "RESOURCEMANAGER",
        "hostRef" : {
          "hostId" : "926254b5-a026-49dc-9889-c60925552df4"
        },
        "config" : {
          "items" : [ {
            "name" : "rm_id",
            "value" : "81"
          }, {
            "name" : "role_jceks_password",
            "value" : "3xwugbb81j8mndvsyr8cdumhh"
          } ]
        }
      } ],
      "displayName" : "YARN (MR2 Included)"
    }, {
      "name" : "hdfs",
      "type" : "HDFS",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "DATANODE",
          "items" : [ {
            "name" : "datanode_java_heapsize",
            "value" : "1073741824"
          }, {
            "name" : "dfs_data_dir_list",
            "value" : "/vol1/dfs/dn,/vol2/dfs/dn"
          }, {
            "name" : "dfs_datanode_data_dir_perm",
            "value" : "700"
          }, {
            "name" : "dfs_datanode_du_reserved",
            "value" : "8455158169"
          }, {
            "name" : "dfs_datanode_http_port",
            "value" : "1006"
          }, {
            "name" : "dfs_datanode_max_locked_memory",
            "value" : "4294967296"
          }, {
            "name" : "dfs_datanode_port",
            "value" : "1004"
          }, {
            "name" : "rm_cpu_shares",
            "value" : "400"
          }, {
            "name" : "rm_io_weight",
            "value" : "200"
          } ]
        }, {
          "roleType" : "GATEWAY",
          "items" : [ {
            "name" : "dfs_client_use_trash",
            "value" : "true"
          } ]
        }, {
          "roleType" : "JOURNALNODE",
          "items" : [ {
            "name" : "dfs_journalnode_edits_dir",
            "value" : "/vol1/dfs/jn"
          } ]
        }, {
          "roleType" : "NAMENODE",
          "items" : [ {
            "name" : "dfs_name_dir_list",
            "value" : "/vol1/dfs/nn,/vol2/dfs/nn"
          }, {
            "name" : "dfs_namenode_servicerpc_address",
            "value" : "8022"
          } ]
        }, {
          "roleType" : "SECONDARYNAMENODE",
          "items" : [ {
            "name" : "fs_checkpoint_dir_list",
            "value" : "/vol1/dfs/snn"
          } ]
        } ],
        "items" : [ {
          "name" : "dfs_encrypt_data_transfer_algorithm",
          "value" : "AES/CTR/NoPadding"
        }, {
          "name" : "dfs_ha_fencing_cloudera_manager_secret_key",
          "value" : "BxYn3Sar5vJquCPxglsixedfRYM82d"
        }, {
          "name" : "fc_authorization_secret_key",
          "value" : "co5Z9xHHdO09HivHYlfaNGT7qY1iut"
        }, {
          "name" : "hadoop_security_authentication",
          "value" : "kerberos"
        }, {
          "name" : "hadoop_security_authorization",
          "value" : "true"
        }, {
          "name" : "http_auth_signature_secret",
          "value" : "ISq4nBbmBSZy2kHtOxpxRKN4nlOTLy"
        }, {
          "name" : "rm_dirty",
          "value" : "false"
        }, {
          "name" : "rm_last_allocation_percentage",
          "value" : "20"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "hdfs-BALANCER-d8e636f263e9a814802f441b53b3fb29",
        "type" : "BALANCER",
        "hostRef" : {
          "hostId" : "907b0099-5930-42ab-bf6d-a2a6796d3c50"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hdfs-DATANODE-3df3e7656abb08cfa5c50885c0ecbb75",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "926254b5-a026-49dc-9889-c60925552df4"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "2efn8yc14ju2c5ja4h66g1639"
          } ]
        }
      }, {
        "name" : "hdfs-DATANODE-d8e636f263e9a814802f441b53b3fb29",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "907b0099-5930-42ab-bf6d-a2a6796d3c50"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "9hl5wmnd3o5ewwzrs13boh260"
          } ]
        }
      }, {
        "name" : "hdfs-DATANODE-ea85d7631ccd062a61118c35975177f9",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "e0fccfa2-3dde-4159-9675-920b43a8a17a"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "e66lqu0hh6lt5g98yb9gybx7j"
          } ]
        }
      }, {
        "name" : "hdfs-GATEWAY-4b651c7ae701fccc378d431d0f4803e6",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "864c120e-55b2-4dff-ba1f-ee41c90361ef"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hdfs-NAMENODE-ea85d7631ccd062a61118c35975177f9",
        "type" : "NAMENODE",
        "hostRef" : {
          "hostId" : "e0fccfa2-3dde-4159-9675-920b43a8a17a"
        },
        "config" : {
          "items" : [ {
            "name" : "namenode_id",
            "value" : "56"
          }, {
            "name" : "role_jceks_password",
            "value" : "1adq2x6j223ehzhawop0ge1tj"
          } ]
        }
      }, {
        "name" : "hdfs-SECONDARYNAMENODE-d8e636f263e9a814802f441b53b3fb29",
        "type" : "SECONDARYNAMENODE",
        "hostRef" : {
          "hostId" : "907b0099-5930-42ab-bf6d-a2a6796d3c50"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "booymgz1vws2i4oalmb4bnygo"
          } ]
        }
      } ],
      "displayName" : "HDFS"
    }, {
      "name" : "sentry",
      "type" : "SENTRY",
      "config" : {
        "roleTypeConfigs" : [ ],
        "items" : [ {
          "name" : "hdfs_service",
          "value" : "hdfs"
        }, {
          "name" : "sentry_server_database_host",
          "value" : "ip-10-0-3-96.ec2.internal"
        }, {
          "name" : "sentry_server_database_password",
          "value" : "password"
        }, {
          "name" : "sentry_service_admin_group",
          "value" : "hive,impala,hue,solr,kafka,jlusancheza"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "sentry-GATEWAY-3df3e7656abb08cfa5c50885c0ecbb75",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "926254b5-a026-49dc-9889-c60925552df4"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "sentry-GATEWAY-d8e636f263e9a814802f441b53b3fb29",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "907b0099-5930-42ab-bf6d-a2a6796d3c50"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "sentry-GATEWAY-ea85d7631ccd062a61118c35975177f9",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "e0fccfa2-3dde-4159-9675-920b43a8a17a"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "sentry-SENTRY_SERVER-4b651c7ae701fccc378d431d0f4803e6",
        "type" : "SENTRY_SERVER",
        "hostRef" : {
          "hostId" : "864c120e-55b2-4dff-ba1f-ee41c90361ef"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "8tvr28o0vvpzpxitjf0pq1qq9"
          } ]
        }
      } ],
      "displayName" : "Sentry"
    }, {
      "name" : "hue",
      "type" : "HUE",
      "config" : {
        "roleTypeConfigs" : [ ],
        "items" : [ {
          "name" : "database_host",
          "value" : "ip-10-0-3-96.ec2.internal"
        }, {
          "name" : "database_password",
          "value" : "password"
        }, {
          "name" : "database_type",
          "value" : "mysql"
        }, {
          "name" : "hive_service",
          "value" : "hive"
        }, {
          "name" : "hue_webhdfs",
          "value" : "hdfs-NAMENODE-ea85d7631ccd062a61118c35975177f9"
        }, {
          "name" : "oozie_service",
          "value" : "oozie"
        }, {
          "name" : "sentry_service",
          "value" : "sentry"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "hue-HUE_LOAD_BALANCER-ea85d7631ccd062a61118c35975177f9",
        "type" : "HUE_LOAD_BALANCER",
        "hostRef" : {
          "hostId" : "e0fccfa2-3dde-4159-9675-920b43a8a17a"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "89f2z4qbjyanbqclhijvlzk2a"
          } ]
        }
      }, {
        "name" : "hue-HUE_SERVER-ea85d7631ccd062a61118c35975177f9",
        "type" : "HUE_SERVER",
        "hostRef" : {
          "hostId" : "e0fccfa2-3dde-4159-9675-920b43a8a17a"
        },
        "config" : {
          "items" : [ {
            "name" : "navmetadataserver_cmdb_password",
            "value" : "3f59ded1-6b0a-4cae-be8d-d146ef429137"
          }, {
            "name" : "role_jceks_password",
            "value" : "euxvwq1znt6o61qlxyvbcqxv1"
          }, {
            "name" : "secret_key",
            "value" : "7B2QSR4nwYe91QPv8anSw0K6spOcxT"
          } ]
        }
      }, {
        "name" : "hue-KT_RENEWER-ea85d7631ccd062a61118c35975177f9",
        "type" : "KT_RENEWER",
        "hostRef" : {
          "hostId" : "e0fccfa2-3dde-4159-9675-920b43a8a17a"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "aduun54sz09bh3li94mynay8c"
          } ]
        }
      } ],
      "displayName" : "Hue"
    } ]
  } ],
  "hosts" : [ {
    "hostId" : "e0fccfa2-3dde-4159-9675-920b43a8a17a",
    "ipAddress" : "10.0.3.144",
    "hostname" : "ip-10-0-3-144.ec2.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ {
        "name" : "host_config_suppression_memory_overcommitted_validator",
        "value" : "true"
      } ]
    }
  }, {
    "hostId" : "926254b5-a026-49dc-9889-c60925552df4",
    "ipAddress" : "10.0.3.187",
    "hostname" : "ip-10-0-3-187.ec2.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "907b0099-5930-42ab-bf6d-a2a6796d3c50",
    "ipAddress" : "10.0.3.79",
    "hostname" : "ip-10-0-3-79.ec2.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "864c120e-55b2-4dff-ba1f-ee41c90361ef",
    "ipAddress" : "10.0.3.96",
    "hostname" : "ip-10-0-3-96.ec2.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  } ],
  "users" : [ {
    "name" : "__cloudera_internal_user__hue-HUE_SERVER-ea85d7631ccd062a61118c35975177f9",
    "roles" : [ "ROLE_NAVIGATOR_ADMIN" ],
    "pwHash" : "008650d066f17467a50d94b85b7804ae36bb95040117c00999b652ff06ba1a03",
    "pwSalt" : -8882213671263045912,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-ACTIVITYMONITOR-4b651c7ae701fccc378d431d0f4803e6",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "917297c1637f78dd4ca19963fb961002f551c49708fc6cdf4331645533bfb6ea",
    "pwSalt" : 311595378085487065,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-EVENTSERVER-4b651c7ae701fccc378d431d0f4803e6",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "43f4312b1f94c9f54f1b9233c75d1e53d904ff4488cc7f9a65da48494f413cf0",
    "pwSalt" : 9105096918263294783,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-HOSTMONITOR-4b651c7ae701fccc378d431d0f4803e6",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "5b47967c908f17efb93011be8f896267d5f7dc0b76a0bfafd02fab206a2bdb31",
    "pwSalt" : -6445625724528029323,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-REPORTSMANAGER-4b651c7ae701fccc378d431d0f4803e6",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "7f43e4d71e1d0db22bafa8d769873f60ec4e4c72b3c2880494c3724d1b7392a8",
    "pwSalt" : -2568438634624736233,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-SERVICEMONITOR-4b651c7ae701fccc378d431d0f4803e6",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "6053a2a4bd8894a9422f49c489dc73bb8e3d1b3af259b1a06346005155589dda",
    "pwSalt" : 670405150816565953,
    "pwLogin" : true
  }, {
    "name" : "admin",
    "roles" : [ "ROLE_LIMITED" ],
    "pwHash" : "9b140017a35e0c0166723c4e47c76a9d7340663fbae79a602e39a840a26369a8",
    "pwSalt" : -599915577890841675,
    "pwLogin" : true
  }, {
    "name" : "jlusancheza",
    "roles" : [ "ROLE_ADMIN" ],
    "pwHash" : "e30e824d5db0408f3e68124f1f840b06bb4d0db22bd0bba634b1440ace47b54e",
    "pwSalt" : 1007657085220512545,
    "pwLogin" : true
  }, {
    "name" : "minotaur",
    "roles" : [ "ROLE_CONFIGURATOR" ],
    "pwHash" : "d875126ba771394e06f5a0412461d7e25950e9d1cf4707425d75b1a294d427a2",
    "pwSalt" : 6428616827500724045,
    "pwLogin" : true
  } ],
  "versionInfo" : {
    "version" : "5.12.1",
    "buildUser" : "jenkins",
    "buildTimestamp" : "20170818-0807",
    "gitHash" : "9bdee611802535491d400e03c98ef694a2c77d0a",
    "snapshot" : false
  },
  "managementService" : {
    "name" : "mgmt",
    "type" : "MGMT",
    "config" : {
      "roleTypeConfigs" : [ {
        "roleType" : "ACTIVITYMONITOR",
        "items" : [ {
          "name" : "firehose_database_host",
          "value" : "ip-10-0-3-96.ec2.internal"
        }, {
          "name" : "firehose_database_name",
          "value" : "amon"
        }, {
          "name" : "firehose_database_password",
          "value" : "password"
        }, {
          "name" : "firehose_database_user",
          "value" : "amon"
        } ]
      }, {
        "roleType" : "HOSTMONITOR",
        "items" : [ {
          "name" : "firehose_non_java_memory_bytes",
          "value" : "1610612736"
        } ]
      }, {
        "roleType" : "REPORTSMANAGER",
        "items" : [ {
          "name" : "headlamp_database_host",
          "value" : "ip-10-0-3-96.ec2.internal"
        }, {
          "name" : "headlamp_database_name",
          "value" : "rman"
        }, {
          "name" : "headlamp_database_password",
          "value" : "password"
        }, {
          "name" : "headlamp_database_user",
          "value" : "rman"
        } ]
      }, {
        "roleType" : "SERVICEMONITOR",
        "items" : [ {
          "name" : "firehose_non_java_memory_bytes",
          "value" : "1610612736"
        } ]
      } ],
      "items" : [ {
        "name" : "ssl_client_truststore_location",
        "value" : "/usr/java/jdk1.7.0_67-cloudera/jre/lib/security/jssecacerts"
      }, {
        "name" : "ssl_client_truststore_password",
        "value" : "changeit"
      } ]
    },
    "roles" : [ {
      "name" : "mgmt-ACTIVITYMONITOR-4b651c7ae701fccc378d431d0f4803e6",
      "type" : "ACTIVITYMONITOR",
      "hostRef" : {
        "hostId" : "864c120e-55b2-4dff-ba1f-ee41c90361ef"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "14u0ilih1gsd7vvc47qx53ko7"
        } ]
      }
    }, {
      "name" : "mgmt-ALERTPUBLISHER-4b651c7ae701fccc378d431d0f4803e6",
      "type" : "ALERTPUBLISHER",
      "hostRef" : {
        "hostId" : "864c120e-55b2-4dff-ba1f-ee41c90361ef"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "eua5sfm55jou0w0sbzp7spiej"
        } ]
      }
    }, {
      "name" : "mgmt-EVENTSERVER-4b651c7ae701fccc378d431d0f4803e6",
      "type" : "EVENTSERVER",
      "hostRef" : {
        "hostId" : "864c120e-55b2-4dff-ba1f-ee41c90361ef"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "apv90leup53lzyika67mefdk1"
        } ]
      }
    }, {
      "name" : "mgmt-HOSTMONITOR-4b651c7ae701fccc378d431d0f4803e6",
      "type" : "HOSTMONITOR",
      "hostRef" : {
        "hostId" : "864c120e-55b2-4dff-ba1f-ee41c90361ef"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "dbvc80qvd1bmuqiooa5jwf0c0"
        } ]
      }
    }, {
      "name" : "mgmt-REPORTSMANAGER-4b651c7ae701fccc378d431d0f4803e6",
      "type" : "REPORTSMANAGER",
      "hostRef" : {
        "hostId" : "864c120e-55b2-4dff-ba1f-ee41c90361ef"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "6n3cdma755bvd5xd56kwvr909"
        } ]
      }
    }, {
      "name" : "mgmt-SERVICEMONITOR-4b651c7ae701fccc378d431d0f4803e6",
      "type" : "SERVICEMONITOR",
      "hostRef" : {
        "hostId" : "864c120e-55b2-4dff-ba1f-ee41c90361ef"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "a9g1ag4z75crlr9csfucg97h5"
        } ]
      }
    } ],
    "displayName" : "Cloudera Management Service"
  },
  "managerSettings" : {
    "items" : [ {
      "name" : "AD_USE_SIMPLE_AUTH",
      "value" : "false"
    }, {
      "name" : "AGENT_TLS",
      "value" : "true"
    }, {
      "name" : "CLUSTER_STATS_START",
      "value" : "10/22/2012 21:20"
    }, {
      "name" : "KDC_ADMIN_HOST",
      "value" : "ip-10-0-3-96.ec2.internal:749"
    }, {
      "name" : "KDC_ADMIN_PASSWORD",
      "value" : "BQIAAABCAAIADEVDMi5JTlRFUk5BTAAMY2xvdWRlcmEtc2NtAAVhZG1pbgAAAAFaHuxTAQAXABDXI8g+AKhgt+kFgBXnDI1P"
    }, {
      "name" : "KDC_ADMIN_USER",
      "value" : "cloudera-scm/admin@EC2.INTERNAL"
    }, {
      "name" : "KDC_HOST",
      "value" : "ip-10-0-3-96.ec2.internal:88"
    }, {
      "name" : "KEYSTORE_PASSWORD",
      "value" : "password"
    }, {
      "name" : "KEYSTORE_PATH",
      "value" : "/opt/cloudera/security/pki/ip-10-0-3-96.ec2.internal-server.jks"
    }, {
      "name" : "KRB_DNS_LOOKUP_KDC",
      "value" : "true"
    }, {
      "name" : "KRB_MANAGE_KRB5_CONF",
      "value" : "true"
    }, {
      "name" : "MAX_RENEW_LIFE",
      "value" : "604800"
    }, {
      "name" : "PUBLIC_CLOUD_STATUS",
      "value" : "ON_PUBLIC_CLOUD"
    }, {
      "name" : "REMOTE_PARCEL_REPO_URLS",
      "value" : "https://archive.cloudera.com/cdh5/parcels/{latest_supported}/,https://archive.cloudera.com/cdh4/parcels/latest/,https://archive.cloudera.com/search/parcels/latest/,http://10.0.3.96/ACCUMULO/,https://archive.cloudera.com/spark/parcels/latest/,https://archive.cloudera.com/sqoop-connectors/parcels/latest/,https://archive.cloudera.com/kafka/parcels/latest/,http://10.0.3.96/GPLExtras/,https://archive.cloudera.com/accumulo/parcels/1.4/,https://archive.cloudera.com/accumulo-c5/parcels/latest/,http://archive.cloudera.com/kudu/parcels/latest/"
    }, {
      "name" : "SECURITY_REALM",
      "value" : "EC2.INTERNAL"
    }, {
      "name" : "WEB_TLS",
      "value" : "true"
    } ]
  }
}

```