在下面的部署中，作者使用三台机器构建集群，IP分别为：10.194.186.44、10.194.186.45、10.194.186.46。角色划分如下表：

| 节点 | 角色 |
| :--- | :--- |
| 10.194.186.44 | 协调节点 |
| 10.194.186.45 | 数据节点 |
| 10.194.186.46 | 数据节点 |

关于协调节点及数据节点的解释请参考elasticsearch文档[http://www.elastic.co/guide/cn/elasticsearch/guide/current/index.html](http://www.elastic.co/guide/cn/elasticsearch/guide/current/index.html)。注意，作者在完成10.194.186.44节点的部署后，直接将安装好的的elasticsearch文件夹拷贝至10.194.186.45、10.194.186.46节点，以便更快完成部署工作。

