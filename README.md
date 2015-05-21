# docker-zookeeper
zookeeper的Dockerfiile，使用zookeeper3.4.6和jdk-8u40。

# zookeeper目录结构
```
ZK_HOME /opt/zookeeper
ZK_CONF /opt/zookeeper/conf
ZK_DATA /tmp/zookeeper
```

# 使用方法
1. 拉取jdk-8u40：
```
docker pull dl.dockerpool.com:5000/java:8u40-jdk
```
国内源，速度可观。如出现`v1 ping attempt failed with error: Get https:……`的错误，请在`/etc/sysconfig/docker`中添加``INSECURE_REGISTRY='--insecure-registry dl.dockerpool.com:5000'`,并重启`docker`。

2. 构建镜像：
```
docker build -t xyalan/zookeeper .
```
