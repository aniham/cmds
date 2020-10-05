##### elasticsearch

a useful tool on npm to import/export an elasticsearch index - [elasticdump](https://www.npmjs.com/package/elasticdump)

```bash
elasticdump --input=http://localhost:9200 --input-index=demo/dump --httpAuthFile=/path/to/your/http_auth_file --output=http://192.168.0.2:9200 --output-index=demo/dump --type=data
```

contents of ```http_auth_file```:

```bash
user=<username>
password=<password>
```

**Note** would only work if both servers use same basic auth or one of them isn't authorized (for example, if you're moving stuff from one server, move to local es index, then put on another remote es index). Elasticdump claims to use a different method of authorization too, but I havent been able to get it to work.
