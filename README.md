# Installing cassandra on MAC and deep dive into the internal

### install cassandra on MAC
```brew install cassandra```

### starting Cassandra
```cassandra -f```

### To see the internal of cassandra
```cd /usr/local/etc/cassandra```

### Open the configuration and remove # from these two lines
```
data_file_directories:
     - /usr/local/var/lib/cassandra/data

```

### Create a keypace
```
CREATE KEYSPACE ks1 WITH replication={'class':'SimpleStrategy','replication_factor':1};
```

### See the new KEYSPACE

```
select * from system_schema.keyspaces where keyspace_name = 'ks1';
```

### Create table in the keyspaces

```
CREATE TABLE ks1.user_tracking (
  user_id text,
  action_category text,
  action_id text,
  action_detail text,

  PRIMARY KEY(user_id, action_category, action_id)
);
```
