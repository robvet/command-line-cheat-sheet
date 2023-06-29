# Azure Redis Cache Command Line Cheat-Sheet

## Redis Console Command Line

### Search Key/Vaule Pairs
```
Keys *
Scan 0 count 1000 Match *
```

### Check Status of Redis Cache
#### Azure Cache for Redis uses the db0 database by default. If you switch to another database (for example, db1) and try to read keys from it, Azure Cache for Redis won't find them there. Every database is a logically separate unit and holds a different dataset.
```
Info
```

### Check Status of Redis Cache
```
select <database number - zero based>
```

### Blah
```
Blah
```
