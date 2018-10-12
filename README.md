# harbor_glusterfs
基于glusterfs实现harbor数据高可用

实现步骤

1，安装glusterfs服务

2，安装keepalive, 实现glusterfs服务高可用（vip）

3，docker方式运行harbor

4，修改harbor中的harbor.cfg和docker-compose.yml配置

数据目录挂载到glusterfs中

5，重启harbor服务

这里只提供第4步的2个harbor配置文件，以供参考。
