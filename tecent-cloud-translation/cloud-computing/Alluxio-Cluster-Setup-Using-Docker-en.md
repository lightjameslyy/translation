# Alluxio Cluster Setup Using Docker

author: Balaji Kandregula  

address: https://dzone.com/articles/alluxio-cluster-setup-using-docker

In our previous post, we introduced you to the world of Docker. This post will take you through setting up an Alluxio cluster.


The first step is to create a base image with the required software packages, as well as exposing the SSH port (22). Additionally, create Hadoop user required to by the Alluxio master to SSH to workers for starting the processes.


Image title


The next step is to create a Docker file with the steps required to install Alluxio:


Image title


After that, create the Docker-Compose file with cluster information (Master and workers). In our example, we have one master and two workers.


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




Next, start the containers with the “docker-compose up -d” command. Connect to the master container, sudo to Hadoop (sudo su - hadoop), generate SSH keys (ssh-keygen), and copy the keys (ssh-copy-id) to workers (/opt/apache/alluxio/workers)


The last step is to create the configuration files required by Alluxio, and start the cluster.


cd /opt/apache/alluxio/bin.


./alluxio bootstrapConf master1


./alluxio copyDir ../conf


./alluxio format


./alluxio-start.sh all NoMount



Here is a screenshot of the cluster.


Image title
