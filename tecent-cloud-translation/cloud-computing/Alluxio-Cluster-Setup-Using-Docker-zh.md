# 使用Docker搭建Alluxio群集

在[之前的文章](https://dzone.com/articles/diving-into-docker)中，我们向您介绍了Docker。这篇文章将带你一起搭建Alluxio集群。

第一步是使用所需的软件包创建一个基本映像，并公开SSH端口（22）。另外，创建Alluxio master所需的Hadoop用户，以便SSH到workers并启动进程。

![img1](https://dzone.com/storage/temp/2769913-1.png)

下一步是按照安装Alluxio所需的步骤创建一个Docker文件：

![img2](https://dzone.com/storage/temp/2769938-2.png)

之后，创建包含集群信息（Master和Worker）的Docker-Compose文件。在本文的例子中，我们有一个master和两个worker。

```
version: '2'
services:
#############################
# Master1
#############################
    master1:
        container_name: master1
        domainname: master1.dev
        hostname: master1
        image: alluxio_base
        working_dir: /opt/apache/
        restart: always
        ports:
            - "32000:22"
            - "32001:19999"
        volumes:
            - ./master1:/apacheapps/data/alluxio/master1
#            - ./master1/conf:/opt/apache/alluxio/conf
#            - ./master1/logs:/opt/apache/alluxio/logs:rw
        mem_limit: 1000000000
#############################
# worker1
#############################
    worker1:
        container_name: worker1
        domainname: worker1.dev
        hostname: worker1
        image: alluxio_base
        working_dir: /opt/apache/
        restart: always
        ports:
            - "32002:22"
            - "32003:30000"
            - "32004:19999"
        volumes:
            - ./worker1:/apacheapps/data/alluxio/worker1
#            - ./worker1/conf:/opt/apache/alluxio/conf
#            - ./worker1/logs:/opt/apache/alluxio/logs:rw
            - ./worker1/ramdisk:/mnt/ramdisk
        mem_limit: 1000000000  
#############################
# worker2
#############################
    worker2:
        container_name: worker2
        domainname: worker2.dev
        hostname: worker2
        image: alluxio_base
        working_dir: /opt/apache/
        restart: always
        ports:
            - "32005:22"
            - "32006:30000"
            - "32007:19999"
        volumes:
            - ./worker2:/apacheapps/data/alluxio/worker2
#            - ./worker2/conf:/opt/apache/alluxio/conf
#            - ./worker2/logs:/opt/apache/alluxio/logs:rw
            - ./worker1/ramdisk:/mnt/ramdisk            
        mem_limit: 1000000000
```

接下来，用`docker-compose up -d`命令启动容器。

连接到主容器，sudo到Hadoop（`sudo su - hadoop`），生成SSH密钥（`ssh-keygen`），并将密钥复制（`ssh-copy-id`）到worker节点（`/opt/apache/alluxio/workers`）。（这一步是为了配置ssh免密登录。）

最后一步是创建Alluxio所需的配置文件，并启动集群。

```shell
cd /opt/apache/alluxio/bin.

./alluxio bootstrapConf master1

./alluxio copyDir ../conf

./alluxio format

./alluxio-start.sh all NoMount
```

这是群集的屏幕截图：

![img3](https://dzone.com/storage/temp/2769958-4.png)
