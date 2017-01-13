# Cassandra learning environment

**Step 1: Starting Cassandra database**

```
docker run -d -p 7000:7000 -p 7001:7001 -p 7199:7199 -p 9042:9042 -p 9160:9160 --name zeppelin_cassandra cassandra
```

**Step 2: Starting Zeppelin**

```
docker run -p 8080:8080 --name zeppelin --link zeppelin_cassandra -d funnyart/zeppelin
```

**Step 3: Zepplain configuration**

- Interpreters config
- Cassandra host: `zeppelin_cassandra`

**Step4: Config test**

- Open a new workbook
- Write and run the following commands

```
%cassandra
HELP;
```
