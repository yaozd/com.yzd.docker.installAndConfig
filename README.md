# com.yzd.docker.installAndConfig
docker 安装与配置

## 当前系统环境
```
CentOS 7.4.1708 (Core)
docker-ce-17.09.0.ce-1.el7.centos.x86_64.rpm
```

## docker-install
```
1.
直接下载rpm安装:
wget https://download.docker.com/linux/centos/7/x86_64/stable/Packages/docker-ce-17.09.0.ce-1.el7.centos.x86_64.rpm
yum localinstall docker-ce-17.09.0.ce-1.el7.centos.x86_64.rpm
==
2.
启动docker，然后将docker服务设置成开机自启动
systemctl start docker //启动
systemctl status docker  //状态
systemctl enable docker  //开机自启动
systemctl restart docker  //重新启动
==
3.
运行docker hello world示例：
docker pull hello-world //
docker images //列出镜像列表
docker run hello-world //
docker ps
docker ps -a为查看所有的容器，包括已经停止的。
==

参考：
moby、docker-ce与docker-ee的区别
https://blog.csdn.net/yk20091201/article/details/80016135
centos7安装docker总结
https://blog.csdn.net/leo881205/article/details/79463880
```
## docker的常用命令汇总

1. [docker的常用命令汇总](https://blog.csdn.net/yufei_java/article/details/78739667)
2. [常用docker命令，及一些坑](https://blog.csdn.net/wsscy2004/article/details/25878363)
3. [Docker常用命令、超实用、讲解清晰明了-推荐](https://blog.csdn.net/jiangyu1013/article/details/79894762)

## moby、docker-ce与docker-ee的区别
```
https://blog.csdn.net/yk20091201/article/details/80016135
moby、docker-ce与docker-ee
最早的时候docker就是一个开源项目，主要由docker公司维护。
2017年年初，docker公司将原先的docker项目改名为moby，并创建了docker-ce和docker-ee。
这三者的关系是：
moby是继承了原先的docker的项目，是社区维护的的开源项目，谁都可以在moby的基础打造自己的容器产品
docker-ce是docker公司维护的开源项目，是一个基于moby项目的免费的容器产品
docker-ee是docker公司维护的闭源产品，是docker公司的商业产品。
moby project由社区维护，docker-ce project是docker公司维护，docker-ee是闭源的。
要使用免费的docker，从网页docker-ce上获取。
```
## Docker版本分为CE和EE|Docker Engine和Docker Data Center
```
https://blog.csdn.net/zhengmx100/article/details/71698509
http://dockone.io/article/2128
2017年年初
Docker Engine改为Docker CE（社区版） 
它包含了CLI客户端、后台进程/服务以及API。用户像以前以同样的方式获取。
Docker Data Center改为Docker EE（企业版） 
在Docker三个定价层增加了额外的支付产品和支持
这些修改并不影响Docker Compose以及Docker Machine
Docker版本现在基于YY.MM 
使用基于月份的发行版本，17.03 的第一版就指向17.03.0，如果有bug/安全修复需要发布，那么将会指向17.03.1等等。
"Edge"与"Stable"两个版本发行
Edge版本每月发布，提供一个月支持。
Stable版本每季度发布，提供4个月支持。
你可以通过Docker EE订阅 延长Stable版本支持以及补丁修复。
```