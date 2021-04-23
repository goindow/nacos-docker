## demo 说明
* /nacos-standalone                
  * 单机模式
* /nacos-cluster-ecs-ip
  * 集群模式，非云平台场景，手动调度容器（n > 1 台 ECS，每台都起一个容器，将这些 ECS 上的容器节点组成集群，使用 n 个 docker-compose.yml 来管理）
* /nacos-cluster-cloud-hostname    
  * 集群模式，云平台场景，自动调度容器（n >= 1 台 ECS 组成的云平台，使用 1 个 docker-compose.yml 来管理集群）
* /nacos-cluster-cloud-ip          
  * 同上，如果使用 hostanme 模式，docker 网络有冲突的话，可以使用 ip 版本
