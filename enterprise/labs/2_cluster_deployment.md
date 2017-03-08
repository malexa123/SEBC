```
{
  "timestamp" : "2017-03-08T10:26:21.375Z",
  "clusters" : [ {
    "name" : "malexa123",
    "version" : "CDH5",
    "services" : [ {
      "name" : "hive",
      "type" : "HIVE",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "HIVEMETASTORE",
          "items" : [ {
            "name" : "hive_metastore_java_heapsize",
            "value" : "677380096"
          } ]
        }, {
          "roleType" : "HIVESERVER2",
          "items" : [ {
            "name" : "hiveserver2_java_heapsize",
            "value" : "677380096"
          }, {
            "name" : "hiveserver2_spark_driver_memory",
            "value" : "966367641"
          }, {
            "name" : "hiveserver2_spark_executor_cores",
            "value" : "4"
          }, {
            "name" : "hiveserver2_spark_executor_memory",
            "value" : "912680550"
          }, {
            "name" : "hiveserver2_spark_yarn_driver_memory_overhead",
            "value" : "102"
          }, {
            "name" : "hiveserver2_spark_yarn_executor_memory_overhead",
            "value" : "153"
          } ]
        } ],
        "items" : [ {
          "name" : "hive_metastore_database_host",
          "value" : "ip-172-31-30-231.eu-central-1.compute.internal"
        }, {
          "name" : "hive_metastore_database_password",
          "value" : "hive_password"
        }, {
          "name" : "mapreduce_yarn_service",
          "value" : "yarn"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "hive-GATEWAY-2214dd35fd06504385c5cdb9f4ed11ef",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "i-05168cffced92b968"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-GATEWAY-2f468a89d547d0233efc40fafaea4df8",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "i-056395f4fff5d2bed"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-GATEWAY-4d7a6710819bf008aa58ed552fcf2f4a",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "i-0234c2e87a5cc1853"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-GATEWAY-92105f3c08b8afb56e66bab05fa2c017",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "i-09f327713be816103"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-GATEWAY-f72d16a31d61399b80a772f6fb05ef4d",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "i-04c071ab02aaf6e1a"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-HIVEMETASTORE-f72d16a31d61399b80a772f6fb05ef4d",
        "type" : "HIVEMETASTORE",
        "hostRef" : {
          "hostId" : "i-04c071ab02aaf6e1a"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "4mtbre5purkc4ggivmohp25no"
          } ]
        }
      }, {
        "name" : "hive-HIVESERVER2-f72d16a31d61399b80a772f6fb05ef4d",
        "type" : "HIVESERVER2",
        "hostRef" : {
          "hostId" : "i-04c071ab02aaf6e1a"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "5djk1sdihoaw0utym0d20tnv3"
          } ]
        }
      } ],
      "displayName" : "Hive"
    }, {
      "name" : "zookeeper",
      "type" : "ZOOKEEPER",
      "config" : {
        "roleTypeConfigs" : [ ],
        "items" : [ ]
      },
      "roles" : [ {
        "name" : "zookeeper-SERVER-2214dd35fd06504385c5cdb9f4ed11ef",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "i-05168cffced92b968"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "7aj1ggbdkulsecyse3f7ysvw1"
          }, {
            "name" : "serverId",
            "value" : "2"
          } ]
        }
      }, {
        "name" : "zookeeper-SERVER-4d7a6710819bf008aa58ed552fcf2f4a",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "i-0234c2e87a5cc1853"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "d975eum5n9hpj7tg8olhutpnx"
          }, {
            "name" : "serverId",
            "value" : "1"
          } ]
        }
      }, {
        "name" : "zookeeper-SERVER-92105f3c08b8afb56e66bab05fa2c017",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "i-09f327713be816103"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "5hr2aazl0nxgfjestu7gh8ofi"
          }, {
            "name" : "serverId",
            "value" : "3"
          } ]
        }
      } ],
      "displayName" : "ZooKeeper"
    }, {
      "name" : "hue",
      "type" : "HUE",
      "config" : {
        "roleTypeConfigs" : [ ],
        "items" : [ {
          "name" : "database_host",
          "value" : "ip-172-31-30-231.eu-central-1.compute.internal"
        }, {
          "name" : "database_password",
          "value" : "hue_password"
        }, {
          "name" : "database_type",
          "value" : "mysql"
        }, {
          "name" : "hive_service",
          "value" : "hive"
        }, {
          "name" : "hue_webhdfs",
          "value" : "hdfs-HTTPFS-f72d16a31d61399b80a772f6fb05ef4d"
        }, {
          "name" : "oozie_service",
          "value" : "oozie"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "hue-HUE_SERVER-f72d16a31d61399b80a772f6fb05ef4d",
        "type" : "HUE_SERVER",
        "hostRef" : {
          "hostId" : "i-04c071ab02aaf6e1a"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "5q6cy757794t0tyebg5c0rwmc"
          }, {
            "name" : "secret_key",
            "value" : "krtXb9gWaMYYriFXgSri7OYUu8hAJ0"
          } ]
        }
      } ],
      "displayName" : "Hue"
    }, {
      "name" : "oozie",
      "type" : "OOZIE",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "OOZIE_SERVER",
          "items" : [ {
            "name" : "oozie_database_host",
            "value" : "ip-172-31-30-231.eu-central-1.compute.internal"
          }, {
            "name" : "oozie_database_password",
            "value" : "oozie"
          }, {
            "name" : "oozie_database_type",
            "value" : "mysql"
          }, {
            "name" : "oozie_database_user",
            "value" : "oozie"
          }, {
            "name" : "oozie_java_heapsize",
            "value" : "677380096"
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
        "name" : "oozie-OOZIE_SERVER-f72d16a31d61399b80a772f6fb05ef4d",
        "type" : "OOZIE_SERVER",
        "hostRef" : {
          "hostId" : "i-04c071ab02aaf6e1a"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "clh8glynzhxwkxlsoerpspnro"
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
            "value" : "10"
          }, {
            "name" : "mapred_submit_replication",
            "value" : "2"
          } ]
        }, {
          "roleType" : "JOBHISTORY",
          "items" : [ {
            "name" : "mr2_jobhistory_java_heapsize",
            "value" : "1047527424"
          } ]
        }, {
          "roleType" : "NODEMANAGER",
          "items" : [ {
            "name" : "rm_cpu_shares",
            "value" : "1800"
          }, {
            "name" : "rm_io_weight",
            "value" : "900"
          }, {
            "name" : "yarn_nodemanager_heartbeat_interval_ms",
            "value" : "100"
          }, {
            "name" : "yarn_nodemanager_local_dirs",
            "value" : "/yarn/nm"
          }, {
            "name" : "yarn_nodemanager_log_dirs",
            "value" : "/yarn/container-logs"
          }, {
            "name" : "yarn_nodemanager_resource_cpu_vcores",
            "value" : "3"
          }, {
            "name" : "yarn_nodemanager_resource_memory_mb",
            "value" : "2942"
          } ]
        }, {
          "roleType" : "RESOURCEMANAGER",
          "items" : [ {
            "name" : "resource_manager_java_heapsize",
            "value" : "1047527424"
          }, {
            "name" : "yarn_scheduler_maximum_allocation_mb",
            "value" : "2942"
          }, {
            "name" : "yarn_scheduler_maximum_allocation_vcores",
            "value" : "3"
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
          "value" : "90"
        }, {
          "name" : "yarn_service_cgroups",
          "value" : "false"
        }, {
          "name" : "yarn_service_lce_always",
          "value" : "false"
        }, {
          "name" : "zk_authorization_secret_key",
          "value" : "717tqCVzu6ihXfCgivFnBR0RhfMXe0"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "yarn-JOBHISTORY-2f468a89d547d0233efc40fafaea4df8",
        "type" : "JOBHISTORY",
        "hostRef" : {
          "hostId" : "i-056395f4fff5d2bed"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "75xasj5t5ht9f377dc2cv0xtv"
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-2214dd35fd06504385c5cdb9f4ed11ef",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "i-05168cffced92b968"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "9v7g15zgtgyi6owzpnkk893s2"
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-2f468a89d547d0233efc40fafaea4df8",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "i-056395f4fff5d2bed"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "brv8fhwh2uc4w42xk0inc7km1"
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-4d7a6710819bf008aa58ed552fcf2f4a",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "i-0234c2e87a5cc1853"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "609il2lduoe0mrys8drju12xr"
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-92105f3c08b8afb56e66bab05fa2c017",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "i-09f327713be816103"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "4kbc7ozet4479ihgvr8qha0ua"
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-f72d16a31d61399b80a772f6fb05ef4d",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "i-04c071ab02aaf6e1a"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "1g8l45zdqnp8x7dishk988gm9"
          } ]
        }
      }, {
        "name" : "yarn-RESOURCEMANAGER-2f468a89d547d0233efc40fafaea4df8",
        "type" : "RESOURCEMANAGER",
        "hostRef" : {
          "hostId" : "i-056395f4fff5d2bed"
        },
        "config" : {
          "items" : [ {
            "name" : "rm_id",
            "value" : "56"
          }, {
            "name" : "role_jceks_password",
            "value" : "7jzhkka53gva3h6n4ft5mri67"
          } ]
        }
      } ],
      "displayName" : "YARN (MR2 Included)"
    }, {
      "name" : "hdfs",
      "type" : "HDFS",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "BALANCER",
          "items" : [ {
            "name" : "balancer_java_heapsize",
            "value" : "1047527424"
          } ]
        }, {
          "roleType" : "DATANODE",
          "items" : [ {
            "name" : "datanode_java_heapsize",
            "value" : "1073741824"
          }, {
            "name" : "dfs_data_dir_list",
            "value" : "/dfs/dn"
          }, {
            "name" : "dfs_datanode_du_reserved",
            "value" : "5367503257"
          }, {
            "name" : "dfs_datanode_max_locked_memory",
            "value" : "4294967296"
          }, {
            "name" : "rm_cpu_shares",
            "value" : "200"
          }, {
            "name" : "rm_io_weight",
            "value" : "100"
          } ]
        }, {
          "roleType" : "GATEWAY",
          "items" : [ {
            "name" : "role_config_suppression_hdfs_trash_disabled_validator",
            "value" : "true"
          } ]
        }, {
          "roleType" : "JOURNALNODE",
          "items" : [ {
            "name" : "dfs_journalnode_edits_dir",
            "value" : "/dfs/jn"
          } ]
        }, {
          "roleType" : "NAMENODE",
          "items" : [ {
            "name" : "dfs_name_dir_list",
            "value" : "/dfs/nn"
          }, {
            "name" : "dfs_namenode_handler_count",
            "value" : "32"
          }, {
            "name" : "dfs_namenode_service_handler_count",
            "value" : "32"
          }, {
            "name" : "dfs_namenode_servicerpc_address",
            "value" : "8022"
          }, {
            "name" : "fs_trash_interval",
            "value" : "0"
          }, {
            "name" : "namenode_java_heapsize",
            "value" : "1073741824"
          }, {
            "name" : "role_config_suppression_fs_trash_interval_minimum_validator",
            "value" : "true"
          } ]
        }, {
          "roleType" : "SECONDARYNAMENODE",
          "items" : [ {
            "name" : "fs_checkpoint_dir_list",
            "value" : "/dfs/snn"
          }, {
            "name" : "secondary_namenode_java_heapsize",
            "value" : "1073741824"
          } ]
        } ],
        "items" : [ {
          "name" : "dfs_ha_fencing_cloudera_manager_secret_key",
          "value" : "s00HryPL5APOC6NXBVpWGEbtwql4dm"
        }, {
          "name" : "dfs_ha_fencing_methods",
          "value" : "shell(true)"
        }, {
          "name" : "fc_authorization_secret_key",
          "value" : "gOxKB2MhHgrGcQq3T2adLs6DrFpfm9"
        }, {
          "name" : "http_auth_signature_secret",
          "value" : "sE6rogi3bBBMzLwckxMnlKX3cFSOoy"
        }, {
          "name" : "rm_dirty",
          "value" : "false"
        }, {
          "name" : "rm_last_allocation_percentage",
          "value" : "10"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "hdfs-BALANCER-2f468a89d547d0233efc40fafaea4df8",
        "type" : "BALANCER",
        "hostRef" : {
          "hostId" : "i-056395f4fff5d2bed"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hdfs-DATANODE-2214dd35fd06504385c5cdb9f4ed11ef",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "i-05168cffced92b968"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "9xj7dsldxzpjybx3mw9nki4x8"
          } ]
        }
      }, {
        "name" : "hdfs-DATANODE-2f468a89d547d0233efc40fafaea4df8",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "i-056395f4fff5d2bed"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "5s0zqjpya73aphetkhu8fk3mb"
          } ]
        }
      }, {
        "name" : "hdfs-DATANODE-4d7a6710819bf008aa58ed552fcf2f4a",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "i-0234c2e87a5cc1853"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "6hkwc8xpu1a7l8sap8t9cn8tp"
          } ]
        }
      }, {
        "name" : "hdfs-DATANODE-92105f3c08b8afb56e66bab05fa2c017",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "i-09f327713be816103"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "2katkyxxkmhylqi5vfx9zclo8"
          } ]
        }
      }, {
        "name" : "hdfs-DATANODE-f72d16a31d61399b80a772f6fb05ef4d",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "i-04c071ab02aaf6e1a"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "cdx8t0ppml9axcem8xx3iwc"
          } ]
        }
      }, {
        "name" : "hdfs-FAILOVERCONTROLLER-2f468a89d547d0233efc40fafaea4df8",
        "type" : "FAILOVERCONTROLLER",
        "hostRef" : {
          "hostId" : "i-056395f4fff5d2bed"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "8kofjextsresidt032ra33jyw"
          } ]
        }
      }, {
        "name" : "hdfs-FAILOVERCONTROLLER-f72d16a31d61399b80a772f6fb05ef4d",
        "type" : "FAILOVERCONTROLLER",
        "hostRef" : {
          "hostId" : "i-04c071ab02aaf6e1a"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "cvh0uionxqo7lsdn2bvya47kp"
          } ]
        }
      }, {
        "name" : "hdfs-HTTPFS-f72d16a31d61399b80a772f6fb05ef4d",
        "type" : "HTTPFS",
        "hostRef" : {
          "hostId" : "i-04c071ab02aaf6e1a"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "5aiqhl2oejojfa13v2z5bnk7u"
          } ]
        }
      }, {
        "name" : "hdfs-JOURNALNODE-2214dd35fd06504385c5cdb9f4ed11ef",
        "type" : "JOURNALNODE",
        "hostRef" : {
          "hostId" : "i-05168cffced92b968"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "drrlhsovdp8lz0yfnpz47547b"
          } ]
        }
      }, {
        "name" : "hdfs-JOURNALNODE-4d7a6710819bf008aa58ed552fcf2f4a",
        "type" : "JOURNALNODE",
        "hostRef" : {
          "hostId" : "i-0234c2e87a5cc1853"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "txu9a2uhrlru8lqx18epcn2s"
          } ]
        }
      }, {
        "name" : "hdfs-JOURNALNODE-92105f3c08b8afb56e66bab05fa2c017",
        "type" : "JOURNALNODE",
        "hostRef" : {
          "hostId" : "i-09f327713be816103"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "7ke4ul4krj53lhbsrm1s8vbf4"
          } ]
        }
      }, {
        "name" : "hdfs-NAMENODE-2f468a89d547d0233efc40fafaea4df8",
        "type" : "NAMENODE",
        "hostRef" : {
          "hostId" : "i-056395f4fff5d2bed"
        },
        "config" : {
          "items" : [ {
            "name" : "autofailover_enabled",
            "value" : "true"
          }, {
            "name" : "dfs_federation_namenode_nameservice",
            "value" : "nameservice1"
          }, {
            "name" : "dfs_namenode_quorum_journal_name",
            "value" : "nameservice1"
          }, {
            "name" : "namenode_id",
            "value" : "58"
          }, {
            "name" : "role_jceks_password",
            "value" : "45z8zf2k9r7lt5f4i2kgb9jdh"
          } ]
        }
      }, {
        "name" : "hdfs-NAMENODE-f72d16a31d61399b80a772f6fb05ef4d",
        "type" : "NAMENODE",
        "hostRef" : {
          "hostId" : "i-04c071ab02aaf6e1a"
        },
        "config" : {
          "items" : [ {
            "name" : "autofailover_enabled",
            "value" : "true"
          }, {
            "name" : "dfs_federation_namenode_nameservice",
            "value" : "nameservice1"
          }, {
            "name" : "dfs_namenode_quorum_journal_name",
            "value" : "nameservice1"
          }, {
            "name" : "namenode_id",
            "value" : "65"
          }, {
            "name" : "role_jceks_password",
            "value" : "c4hfkr7txomlk59gwo2ujcfy9"
          } ]
        }
      } ],
      "displayName" : "HDFS"
    } ]
  } ],
  "hosts" : [ {
    "hostId" : "i-09f327713be816103",
    "ipAddress" : "172.31.17.193",
    "hostname" : "ip-172-31-17-193.eu-central-1.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "i-056395f4fff5d2bed",
    "ipAddress" : "172.31.24.137",
    "hostname" : "ip-172-31-24-137.eu-central-1.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "i-0234c2e87a5cc1853",
    "ipAddress" : "172.31.24.214",
    "hostname" : "ip-172-31-24-214.eu-central-1.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "i-05168cffced92b968",
    "ipAddress" : "172.31.25.165",
    "hostname" : "ip-172-31-25-165.eu-central-1.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "i-04c071ab02aaf6e1a",
    "ipAddress" : "172.31.30.231",
    "hostname" : "ip-172-31-30-231.eu-central-1.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  } ],
  "users" : [ {
    "name" : "__cloudera_internal_user__mgmt-EVENTSERVER-f72d16a31d61399b80a772f6fb05ef4d",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "2a318bbc1c06c1d63d520233b24832ac9cdc1e3402316963aa760dd52e268f83",
    "pwSalt" : -8290479377039557767,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-HOSTMONITOR-f72d16a31d61399b80a772f6fb05ef4d",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "e90c8a0b38f0e6c7bfd7f5905c6601a261495cfcd147682beaadb2d0addeda95",
    "pwSalt" : 3891575888446456037,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-REPORTSMANAGER-f72d16a31d61399b80a772f6fb05ef4d",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "53f0afb942a7c85cc121c16bd6062e40e6fde1a3d0e84fa01905e1a32d74e9a6",
    "pwSalt" : -6186700860768685534,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-SERVICEMONITOR-f72d16a31d61399b80a772f6fb05ef4d",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "8438e38fefccfe7d536d4f7970d5b51121a932d0ac1aee3533756bb09c0540c7",
    "pwSalt" : 6900268413729054756,
    "pwLogin" : true
  }, {
    "name" : "admin",
    "roles" : [ "ROLE_LIMITED" ],
    "pwHash" : "f886cd417b59b8479d02187de5a9bf6f9565315426250494f4e987f3dfb79345",
    "pwSalt" : -401687275629834803,
    "pwLogin" : true
  }, {
    "name" : "malexa123",
    "roles" : [ "ROLE_ADMIN" ],
    "pwHash" : "1a65d7c0cf5907af058271533acfe7285650a7abd93b663995f0333ad23c9cdb",
    "pwSalt" : -5391087403634390960,
    "pwLogin" : true
  }, {
    "name" : "minoatur",
    "roles" : [ "ROLE_CONFIGURATOR" ],
    "pwHash" : "0925108e5fdbb3252a6b614dfb1b91830d078f1315a042cb65d3cbdc12ce645f",
    "pwSalt" : -3189334353967346030,
    "pwLogin" : true
  } ],
  "versionInfo" : {
    "version" : "5.8.3",
    "buildUser" : "jenkins",
    "buildTimestamp" : "20161019-1013",
    "gitHash" : "518f0d6d44abc87bc392646e4369a20c8192b7cf",
    "snapshot" : false
  },
  "managementService" : {
    "name" : "mgmt",
    "type" : "MGMT",
    "config" : {
      "roleTypeConfigs" : [ {
        "roleType" : "EVENTSERVER",
        "items" : [ {
          "name" : "event_server_heapsize",
          "value" : "677380096"
        } ]
      }, {
        "roleType" : "HOSTMONITOR",
        "items" : [ {
          "name" : "firehose_heapsize",
          "value" : "677380096"
        }, {
          "name" : "firehose_non_java_memory_bytes",
          "value" : "880803840"
        } ]
      }, {
        "roleType" : "REPORTSMANAGER",
        "items" : [ {
          "name" : "headlamp_database_host",
          "value" : "ip-172-31-30-231.eu-central-1.compute.internal"
        }, {
          "name" : "headlamp_database_name",
          "value" : "rman"
        }, {
          "name" : "headlamp_database_password",
          "value" : "rman_password"
        }, {
          "name" : "headlamp_database_user",
          "value" : "rman"
        }, {
          "name" : "headlamp_heapsize",
          "value" : "677380096"
        } ]
      }, {
        "roleType" : "SERVICEMONITOR",
        "items" : [ {
          "name" : "firehose_heapsize",
          "value" : "677380096"
        }, {
          "name" : "firehose_non_java_memory_bytes",
          "value" : "880803840"
        } ]
      } ],
      "items" : [ ]
    },
    "roles" : [ {
      "name" : "mgmt-ALERTPUBLISHER-f72d16a31d61399b80a772f6fb05ef4d",
      "type" : "ALERTPUBLISHER",
      "hostRef" : {
        "hostId" : "i-04c071ab02aaf6e1a"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "bul46xda0h1l24bq1m24fcn7r"
        } ]
      }
    }, {
      "name" : "mgmt-EVENTSERVER-f72d16a31d61399b80a772f6fb05ef4d",
      "type" : "EVENTSERVER",
      "hostRef" : {
        "hostId" : "i-04c071ab02aaf6e1a"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "87q5083o0pmhhkbh8ed85kg9y"
        } ]
      }
    }, {
      "name" : "mgmt-HOSTMONITOR-f72d16a31d61399b80a772f6fb05ef4d",
      "type" : "HOSTMONITOR",
      "hostRef" : {
        "hostId" : "i-04c071ab02aaf6e1a"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "90oivx8ald3qeia96bnhimu96"
        } ]
      }
    }, {
      "name" : "mgmt-REPORTSMANAGER-f72d16a31d61399b80a772f6fb05ef4d",
      "type" : "REPORTSMANAGER",
      "hostRef" : {
        "hostId" : "i-04c071ab02aaf6e1a"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "5ooh0vyc6wonnpk16ui6ak3tc"
        } ]
      }
    }, {
      "name" : "mgmt-SERVICEMONITOR-f72d16a31d61399b80a772f6fb05ef4d",
      "type" : "SERVICEMONITOR",
      "hostRef" : {
        "hostId" : "i-04c071ab02aaf6e1a"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "8citf0xfmr1iah8lszy5pvisj"
        } ]
      }
    } ],
    "displayName" : "Cloudera Management Service"
  },
  "managerSettings" : {
    "items" : [ {
      "name" : "CLUSTER_STATS_START",
      "value" : "10/27/2012 17:50"
    }, {
      "name" : "PUBLIC_CLOUD_STATUS",
      "value" : "ON_PUBLIC_CLOUD"
    }, {
      "name" : "REMOTE_PARCEL_REPO_URLS",
      "value" : "https://archive.cloudera.com/cdh5/parcels/5.8.3/,https://archive.cloudera.com/cdh4/parcels/latest/,https://archive.cloudera.com/impala/parcels/latest/,https://archive.cloudera.com/search/parcels/latest/,https://archive.cloudera.com/accumulo/parcels/1.4/,https://archive.cloudera.com/accumulo-c5/parcels/latest/,https://archive.cloudera.com/kafka/parcels/latest/,https://archive.cloudera.com/navigator-keytrustee5/parcels/latest/,https://archive.cloudera.com/spark/parcels/latest/,https://archive.cloudera.com/sqoop-connectors/parcels/latest/"
    } ]
  }
}
```
