# 系统架构设计文档

## 1. 系统概述

乐优商城是一个基于 Spring Cloud 的分布式电商系统，包含多个微服务模块。

## 2. 架构图

```mermaid
graph TD
    A[用户] --> B[API Gateway]
    B --> C[用户服务]
    B --> D[商品服务]
    B --> E[订单服务]
    B --> F[购物车服务]
    B --> G[搜索服务]
    C --> H[MySQL]
    D --> I[MySQL]
    E --> J[MySQL]
    F --> K[Redis]
    G --> L[Elasticsearch]
```

## 3. 技术栈

- 后端：Spring Boot + Spring Cloud
- 数据库：MySQL + Redis
- 搜索：Elasticsearch
- 消息队列：RabbitMQ
- 配置中心：Spring Cloud Config
- 服务注册中心：Eureka
