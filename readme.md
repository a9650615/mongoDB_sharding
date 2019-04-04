docker-compose up -d --force-recreate

rs.initiate({_id: 'partdio', members: [{_id:0, host: 'mongoS1'}, {_id:1, host:'mongoS2'}]})

rs.initiate({_id: 'partdio1', members: [{_id: 0, host:'mongoS3'}, {_id:1, host:'mongoS4'}]})

Rs config1:
```
rs.initiate({_id:"partdioConf", configsvr: true, members: [{ _id : 0, host : "mongoCfg1" }, { _id : 1, host : "mongoCfg2" }]})
```

Rs Router:
```
sh.addShard("partdio/mongoS1,mongoS2")
sh.addShard("partdio1/mongoS3,mongoS4")
```
Refrerence:
[For build sharding](https://dzone.com/articles/composing-a-sharded-mongodb-on-docker)
[For test sharding](http://bboymars.coding.me/2018/04/01/mongodb_sharding_inDocker/)