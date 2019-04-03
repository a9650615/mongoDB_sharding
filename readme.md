rs.initiate({_id: 'partdio', members: [{_id:0, host: 'mongoS1'}, {_id:1, host:'mongoS2'}, {_id:2, host:'mongoS3'}]})

Rs config:
```
rs.initiate({_id:"partdioConf", configsvr: true, members: [{ _id : 0, host : "mongoCfg1" }]})
```

Rs Router:
```
sh.addShard("partdio/mongos")
```