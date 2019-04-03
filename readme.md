rs.initiate({_id: 'partdio', members: [{_id:0, host: 'mongos1'}, {_id:1, host:'mongos2'}, {_id:2, host:'mongo3'}]})

Rs config:
```
rs.initiate({_id:"partdioConf", configsvr: true, members: [{ _id : 0, host : "mongoCfg1" }]})
```