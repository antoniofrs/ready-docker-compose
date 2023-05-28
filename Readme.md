# Ready docker-compose

> **Warning**
> Not all files are tested
 
&nbsp;
&nbsp;
### :heavy_check_mark: SonarQube

Volumes:
- postgresql
- postgresql-data
- sonarqube-data
- sonarqube-extensions
- sonarqube-logs

Exposed ports:
- 9000

#### Possible errors:

If this error is shown in sonarqube log:
```
max virtual memory areas vm.max_map_count [65530] is too low, increase to at least [262144]
```

Fix it using the following command:

```bash
sudo sysctl -w vm.max_map_count=262144
```

&nbsp;
&nbsp;
### :heavy_check_mark: Jenkins

Volumes:

- jenkins-docker-sock
- jenkins-home


Exposed ports:
- 8080
- 50000


&nbsp;
&nbsp;
### :heavy_check_mark: Redis

Volumes:

- redis-data
- redis-insight

Exposed ports:
- 6379
- 8001 (Redis insight)

&nbsp;
&nbsp;
### :heavy_check_mark: Mongo

Volumes:

- mongo-config-db
- mongo-data

Exposed ports:

- 27017
- 8081 (Mongo express)

&nbsp;
&nbsp;
### :heavy_check_mark: Keycloak

Volumes:

- postgresql-data
- postgresql-preinitdb
- postgresql-initdb
- pgadmin


Exposed ports:

- 5050 (pg-admin)
- 80
