# rocketmq入门安装
[rocketmq文档地址](http://rocketmq.apache.org/docs/quick-start/)

- 下载[rocketmq-all-4.2.0-source-release](https://www.apache.org/dyn/closer.cgi?path=rocketmq/4.2.0/rocketmq-all-4.2.0-source-release.zip)

```
$  unzip rocketmq-all-4.2.0-source-release.zip
```
```
$ cd rocketmq-all-4.2.0/
```
```
$ mvn -Prelease-all -DskipTests clean install -U
```
```
$ cd distribution/target/apache-rocketmq
```
## Start Name Server
```
 $ nohup sh bin/mqnamesrv &
```
```
 $ tail -f /home/${user.name}/logs/rocketmqlogs/namesrv.log
```
```
 The Name Server boot success...
```

## Start Broker
```
 $ nohup sh bin/mqbroker -n localhost:9876 &
```
```
 $ tail -f /home/${user.name}/logs/rocketmqlogs/broker.log 
```
```
The broker[%s, 172.30.30.233:10911] boot success...
```

## 关闭服务
```
 $ sh bin/mqshutdown broker
```
```
The mqbroker(36695) is running...
Send shutdown request to mqbroker(36695) OK
```
```
 $ sh bin/mqshutdown namesrv
```
```
The mqnamesrv(36664) is running...
Send shutdown request to mqnamesrv(36664) OK
```

# rocketmq 控制台
- 下载[rocketmq-console](https://github.com/apache/rocketmq-externals)
```
 $ git clone https://github.com/apache/rocketmq-externals.git
```
```
 $ cd /rocketmq-externals/rocketmq-console
```
```
 $ vim /rocketmq-externals/rocketmq-console/src/main/resources/application.properties
```

- 找到 rocketmq.config.namesrvAddr=
```
rocketmq.config.namesrvAddr=${host:port}
```
- 编译
```
 $ mvn clean package -Dmaven.test.skip=true（注意：不要直接使用mvn package，会提示很多错误）
```
- 启动 rocketmq控制台
```
 $ cd /rocketmq-externals/rocketmq-console/target
```
```
 $ java -jar rocketmq-console-ng-1.0.0.jar
```
- 访问web页面
```
 http://localhost:8080/
```

### 初步安装已经完成
---
