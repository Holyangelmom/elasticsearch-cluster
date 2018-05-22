# 安装前的准备

* 安装jdk1.8
* 创建用户elastic
* 从官网或者github下载elasticsearch-2.3.4
* 环境设置如下：
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

   第二种做法是添加规则，允许主机访问9200端口，也可以限制哪些主机可以访问等等，不懂赶紧脑补防火墙知识：

   sudo vim /etc/sysconfig/iptables

   插入规则：-A INPUT -m state --state NEW -m tcp -p tcp --dport 9200 -j ACCEPT

```



