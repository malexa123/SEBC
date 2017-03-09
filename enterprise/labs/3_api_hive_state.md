```
#Commands:
#Hive status
curl -u malexa123:cloudera 'http://monkey:7180/api/v12/clusters/malexa123/services/hive'
#Hive stop
curl -X POST -u malexa123:cloudera 'http://monkey:7180/api/v12/clusters/malexa123/services/hive/commands/stop'
#Hive start
curl -X POST -u malexa123:cloudera 'http://monkey:7180/api/v12/clusters/malexa123/services/hive/commands/start'

[malexa123@ip-172-31-24-137 ~]$ curl -u malexa123:cloudera 'http://monkey:7180/api/v12/clusters/malexa123/services/hive'
{
  "name" : "hive",
  "type" : "HIVE",
  "clusterRef" : {
    "clusterName" : "cluster"
  },
  "serviceUrl" : "http://ip-172-31-30-231.eu-central-1.compute.internal:7180/cmf/serviceRedirect/hive",
  "roleInstancesUrl" : "http://ip-172-31-30-231.eu-central-1.compute.internal:7180/cmf/serviceRedirect/hive/instances",
  "serviceState" : "STARTED",
  "healthSummary" : "GOOD",
  "healthChecks" : [ {
    "name" : "HIVE_HIVEMETASTORES_HEALTHY",
    "summary" : "GOOD",
    "suppressed" : false
  }, {
    "name" : "HIVE_HIVESERVER2S_HEALTHY",
    "summary" : "GOOD",
    "suppressed" : false
  } ],
  "configStalenessStatus" : "FRESH",
  "clientConfigStalenessStatus" : "FRESH",
  "maintenanceMode" : false,
  "maintenanceOwners" : [ ],
  "displayName" : "Hive",
  "entityStatus" : "GOOD_HEALTH"
}[malexa123@ip-172-31-24-137 ~]$ curl X POST -u malexa123:cloudera 'http://monkey:7180/api/v12/clusters/malexa123/services/hive/commands/stop'
{
  "id" : 699,
  "name" : "Stop",
  "startTime" : "2017-03-08T11:04:47.977Z",
  "active" : true,
  "serviceRef" : {
    "clusterName" : "cluster",
    "serviceName" : "hive"
  }
}[malexa123@ip-172-31-24-137 ~]$ curl u malexa123:cloudera 'http://monkey:7180/api/v12/clusters/malexa123/services/hive''
{
  "name" : "hive",
  "type" : "HIVE",
  "clusterRef" : {
    "clusterName" : "cluster"
  },
  "serviceUrl" : "http://ip-172-31-30-231.eu-central-1.compute.internal:7180/cmf/serviceRedirect/hive",
  "roleInstancesUrl" : "http://ip-172-31-30-231.eu-central-1.compute.internal:7180/cmf/serviceRedirect/hive/instances",
  "serviceState" : "STOPPED",
  "healthSummary" : "DISABLED",
  "healthChecks" : [ {
    "name" : "HIVE_HIVEMETASTORES_HEALTHY",
    "summary" : "DISABLED",
    "suppressed" : false
  }, {
    "name" : "HIVE_HIVESERVER2S_HEALTHY",
    "summary" : "DISABLED",
    "suppressed" : false
  } ],
  "configStalenessStatus" : "FRESH",
  "clientConfigStalenessStatus" : "FRESH",
  "maintenanceMode" : false,
  "maintenanceOwners" : [ ],
  "displayName" : "Hive",
  "entityStatus" : "STOPPED"
}[malexa123@ip-172-31-24-137 ~]$ curl X POST -u malexa123:cloudera 'http://monkey:7180/api/v12/clusters/malexa123/services/hive/commands/start'
{
  "id" : 702,
  "name" : "Start",
  "startTime" : "2017-03-08T11:05:17.131Z",
  "active" : true,
  "serviceRef" : {
    "clusterName" : "cluster",
    "serviceName" : "hive"
  }
}[malexa123@ip-172-31-24-137 ~]$ curl u malexa123:cloudera 'http://monkey:7180/api/v12/clusters/malexa123/services/hive''
{
  "name" : "hive",
  "type" : "HIVE",
  "clusterRef" : {
    "clusterName" : "cluster"
  },
  "serviceUrl" : "http://ip-172-31-30-231.eu-central-1.compute.internal:7180/cmf/serviceRedirect/hive",
  "roleInstancesUrl" : "http://ip-172-31-30-231.eu-central-1.compute.internal:7180/cmf/serviceRedirect/hive/instances",
  "serviceState" : "STARTED",
  "healthSummary" : "GOOD",
  "healthChecks" : [ {
    "name" : "HIVE_HIVEMETASTORES_HEALTHY",
    "summary" : "GOOD",
    "suppressed" : false
  }, {
    "name" : "HIVE_HIVESERVER2S_HEALTHY",
    "summary" : "GOOD",
    "suppressed" : false
  } ],
  "configStalenessStatus" : "FRESH",
  "clientConfigStalenessStatus" : "FRESH",
  "maintenanceMode" : false,
  "maintenanceOwners" : [ ],
  "displayName" : "Hive",
  "entityStatus" : "GOOD_HEALTH"
}[malexa123@ip-172-31-24-137 ~]$
```
