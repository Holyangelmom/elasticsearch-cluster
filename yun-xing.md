1、首先启动协调节点，再启动数据节点

三台机器均以daemon方式运行：

10.194.186.44：sh ${ES\_HOME}/bin/elasticsearch -d

10.194.186.45：sh ${ES\_HOME}/bin/elasticsearch -d

10.194.186.46：sh ${ES\_HOME}/bin/elasticsearch -d

2、若无报错则访问head插件

`http://10.194.186.44:9200/_plugin/head`

_PS：下图只为样例，并非刚安装好的形式。_

![](/assets/head_index.png)

3、至此，elasticsearch的集群安装结束。

