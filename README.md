# harbor_glusterfs
基于glusterfs实现harbor数据高可用

实现步骤

1，安装glusterfs服务

2，安装keepalive, 实现glusterfs服务高可用（vip）

3，挂载gluterfs到/data/register

df -h

192.168.2.110:gfs0       894G  720G  174G  81% /data/register

4，创建harbor配置文件的目录结构

默认harbor的所有数据都保存在/data/register/

mkdir -pv /data/register/{ca_download,config,data,database,harbor,job_logs,psc,redis,registry}

5，修改harbor中的harbor.cfg和docker-compose.yml配置

这里只提供第4步的2个harbor配置文件(挂载到glusterfs)，以供参考。

6，重启harbor服务


