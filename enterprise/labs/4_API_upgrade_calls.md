# Upgrade Cloudera Manager

## API Version
```
https://52.91.154.108:7183/api/version
v18
```
## Version
```
https://52.91.154.108:7183/api/v1/cm/version
{
  "version" : "5.13.0",
  "buildUser" : "jenkins",
  "buildTimestamp" : "20171002-1719",
  "gitHash" : "bd657e597e6743c458ee2c9aabe808b7c972981c",
  "snapshot" : false
}
```

## Users
```
https://52.91.154.108:7183/api/v1/users
{
  "items" : [ {
    "name" : "admin",
    "roles" : [ "ROLE_LIMITED" ]
  }, {
    "name" : "jlusancheza",
    "roles" : [ "ROLE_ADMIN" ]
  }, {
    "name" : "minotaur",
    "roles" : [ "ROLE_CONFIGURATOR" ]
  } ]
}

```

## Database Information
```
https://52.91.154.108:7183/api/v18/cm/scmDbInfo
{
  "scmDbType" : "MYSQL",
  "embeddedDbUsed" : false
}
```


