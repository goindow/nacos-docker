# nacos-server-docker
基于 nacos-docker 镜像的 docker-compose 快速部署脚手架，使用内嵌数据库存储，支持单体和集群模式

## 目录说明
- source/，相关项目演进源码（无需关心）
- nacos-docker/，docker-compose 部署模板
- scene/，各场景用例（找到相应场景用例，直接下载使用）

## scene/ 场景用例说明
- /nacos-standalone
> 单机模式
- /nacos-cluster-ecs
> 集群模式，非云平台场景，手动调度容器（n > 1 台 ECS，每台都起一个容器，将这些 ECS 上的容器节点组成集群，使用 n 个 docker-compose.yml 来管理）
- /nacos-cluster-cloud-hostname
> 集群模式，云平台场景，自动调度容器（n >= 1 台 ECS 组成的云平台，使用 1 个 docker-compose.yml 来管理集群）
- /nacos-cluster-cloud-ip
> 同上，如果使用 hostanme 模式，docker 网络有冲突的话，可以使用 ip 版本


  ## 使用
  1. 从 scene/ 中找到相应场景用例，下载到服务器
  2. 修改相关配置
  3. 运行容器
  ```shell
  docker-compose up -d --build
  ```
