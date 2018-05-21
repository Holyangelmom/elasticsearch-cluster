# Elasticsearch cluster deployment notes

本书讲述如何在centos中部署elasticsearch集群，以及安装相关插件。因为每个人的部署平台都存在差异性，所以本书仅供参考，若有不当之处，还望指出。本文部署的环境如下表所示：

| 组件 | 版本号 | 备注 |
| :--- | :--- | :--- |
| linux | CentOS release 6.8 \(Final\) |  |
| jdk | 1.8.0\_131 |  |
| elasticsearch | 2.3.4 |  |
| elasticsearch-analysis-ik | 1.9.4 | 中文分词插件 |
| elasticsearch-head | 1.x | 图形化集群管理插件 |
| elasticsearch-jdbc | 2.3.4.0 | 关系型数据库数据传输插件 |



