# elk ，可用于实现日志分析的一个工具
- e == > elasticsearch (Elasticsearch 是一个分布式的 RESTful 风格的搜索和数据分析引擎，能够解决不断涌现出的各种用例)
- f == > Filebeat (轻量型数据采集器)
- l == > logstash (能够同时 从多个来源采集数据、转换数据，然后将数据发送到您最喜欢的 “存储库” 中)
- k == > Kibana (Kibana能够可视化 Elasticsearch 中的数据)

--- 

# 各组件间的关系
> filebeat 负责搜集日志信息 ——> logstash 负责过滤日志内容 (如果不过滤可以忽略该步骤) ——> 数据存入 Elasticsearch (也可以保存其他地方) ——> Kibana 对数据进行可视化展示
- 因为我要做过滤的处理,所以就在logstash中进行写入至es中，当然,在filebeat组件中也可以直接写入到库中

# 开始安装 (这里使用linux为物理机,选择tar安装包)

> [FileBeat文档](https://www.elastic.co/guide/en/beats/libbeat/current/index.html)
1. 安装 [Filebeat](https://www.elastic.co/downloads/beats/filebeat)

> [logstash文档](https://www.elastic.co/guide/en/logstash/current/index.html)
1. 安装 [logstash](https://www.elastic.co/cn/downloads/logstash)

> [elasticsearch文档](https://www.elastic.co/guide/en/elasticsearch/reference/current/index.html)
1. 安装 [elasticsearch](https://www.elastic.co/de/downloads/elasticsearch)

> [Kibana文档](https://www.elastic.co/guide/en/kibana/current/index.html)
1. 安装 [Kibana](https://www.elastic.co/cn/downloads/kibana)

还没完成...待续