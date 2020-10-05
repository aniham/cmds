### sql

##### remove databases starting with SomeString:

```bash
mysql -u usr -ppswd -h host  -e "show databases" -s | egrep "^SomeString" | xargs -I "@@" echo mysql -h host -u usr -ppswd -e "\"drop database @@\""
```

##### can also modify to drop tables:

```bash
mysql -u usr -ppswd -h host  -d database -e "show tables" -s | egrep "^SomeString" | xargs -I "@@" echo mysql -h host -u usr -ppswd -d database -e "\"drop table @@\""
```

[reference](https://stackoverflow.com/questions/456751/drop-mysql-databases-matching-some-wildcard)
