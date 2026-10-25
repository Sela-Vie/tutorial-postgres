### MISC NOTES
- postgres has a `template1` database that is copied every time you make a new database 
- you connect through your machine’s published Docker port, use:
```
extra_hosts:
- "host.docker.internal:host-gateway"

connect using
  Server: host.docker.internal
  Port:   8101
```

### ADMINER
|Label|Definition|
|-|-|
|System|`PosgreSQL`|
|Server|`postgres` <br>uses the container in docker as an ip:port|
|Username|`postgres` <br>defined in the env|
|Password|`postgres` <br>defined in the env|
|Database|can be left empty <br>the database within the database server|

### PG ADMIN
Default Workspace => Server (right-click) => Register => Server
**General**
|Label|Definition|
|-|-|
|Name|can be anything <br> only a local alias fr the connection|

**Connection**
|Label|Definition|
|-|-|
|Host name/address|`postgres` <br>uses the container in docker as an ip|
|Port|`5432` <br>default port of postgres|
|Username|`postgres` <br>defined in the env|
|Password|`postgres` <br>defined in the env|