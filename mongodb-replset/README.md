# Dockerfile - tattsun/mongodb-replset
This dockerfile contains mongodb replication set.

## Architecture
Primary - Secondary - Arbiter

## Data Persistency
```
/data/node1 -> Primary Database
/data/node2 -> Secondary Database
/data/node3 -> Arbiter Database
```

## Example
```
$ docker run -p 27017:27017 -p 27018:27018 -d \
    -v /host/primary:/data/node1 -v /host/secondary:/data/node2 \
    --name mongoreplset tattsun/mongodb-replset
```
