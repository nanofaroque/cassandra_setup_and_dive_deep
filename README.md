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
