# 安装前的准备

在下面的部署中，作者使用三台机器构建集群，IP分别为：10.194.186.44、10.194.186.45、10.194.186.46。关于协调节点及数据节点的解释请参考[elasticsearch文档](http://www.elastic.co/guide/cn/elasticsearch/guide/current/index.html)。注意，作者在完成10.194.186.44节点的部署后，直接将安装好的的elasticsearch文件夹拷贝至10.194.186.45、10.194.186.46节点，以便更快完成部署工作。三台机器的角色划分如下表：

| 节点 | 角色 |
| :--- | :--- |
| 10.194.186.44 | 协调节点 |
| 10.194.186.45 | 数据节点 |
| 10.194.186.46 | 数据节点 |

* 每台机器安装jdk1.8
* 每台机器创建用户elastic
* 从官网或者github下载elasticsearch-2.3.4
* 每台机器环境设置如下：

  ```
  （1）修改内存锁定限制 /etc/security/limits.conf
            panaidan    soft    memlock    unlimited
            panaidan    hard    memlock    unlimited
  （2）修改最大文件打开数
            panaidan    soft    nofile    65536
            panaidan    hard    nofile    65536
  （3）允许其他主机访问9200端口
            第一种做法是直接关闭防火墙，但是不建议：
            sudo service iptables stop
            sudo chkconfig iptables off

            第二种做法是添加规则，允许主机访问9200端口，也可以限制哪些主机可以访问等等：
            sudo vim /etc/sysconfig/iptables
            插入规则：-A INPUT -m state --state NEW -m tcp -p tcp --dport 9200 -j ACCEPT
  ```



