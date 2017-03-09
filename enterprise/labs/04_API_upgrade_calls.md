```
#Version
$ curl -u malexa123:cloudera 'http://monkey:7180/api/version'
v15
#API CM version
curl -u malexa123:cloudera 'http://monkey:7180/api/v12/cm/version'
{
  "version" : "5.10.0",
  "buildUser" : "jenkins",
  "buildTimestamp" : "20170120-1037",
  "gitHash" : "aa0b5cd5eceaefe2f971c13ab657020d96bb842a",
  "snapshot" : false
}
#API Users
curl -u malexa123:cloudera 'http://monkey:7180/api/v12/users/'
{
  "items" : [ {
    "name" : "admin",
    "roles" : [ "ROLE_LIMITED" ]
  }, {
    "name" : "malexa123",
    "roles" : [ "ROLE_ADMIN" ]
  }, {
    "name" : "minoatur",
    "roles" : [ "ROLE_CONFIGURATOR" ]
  } ]
}
#DB version used by CM
curl -u malexa123:cloudera 'http://monkey:7180/api/v15/cm/scmDbInfo'
{
  "scmDbType" : "MYSQL",
  "embeddedDbUsed" : false
}
```
