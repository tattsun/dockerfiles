# Dockerfile - tattsun/mongodb-replset
This dockerfile contains mongodb replication set.

## Architecture
Primary - Secondary - Arbiter

## Data Presistency
```
/data/node1 -> Primary Database
/data/node2 -> Secondary Database
/data/node3 -> Arbiter Database
```

## Example
```
$ docker run -p 27017:27017 -p 27018:27018 -d -v /data/node1:/host/primary -v /data/node2:/host/secondary --name mongoreplset tattsun/mongodb-replset
```
