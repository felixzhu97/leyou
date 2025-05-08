# 乐优商城项目 (leyou)

基于 SpringBoot 和 Spring Cloud 实现的分布式电商系统

## 技术栈

- 后端框架: Spring Boot 2.x, Spring Cloud
- 注册中心: Eureka
- 配置中心: Spring Cloud Config
- 网关: Spring Cloud Gateway
- 数据库: MySQL
- 缓存: Redis
- 搜索: Elasticsearch
- 消息队列: RabbitMQ
- 文件存储: FastDFS

## 项目结构

```
ly-api-gateway/        - API网关服务
ly-auth-center/        - 认证中心
ly-cart/              - 购物车服务
ly-common/            - 公共模块
ly-config/            - 配置中心
ly-item/              - 商品服务
ly-order/             - 订单服务
ly-page/              - 静态页面服务
ly-registry/          - 注册中心
ly-search/            - 搜索服务
ly-sms-service/       - 短信服务
ly-upload/            - 文件上传服务
ly-user-service/      - 用户服务
```

## 模块功能

- **ly-api-gateway**: 统一 API 入口，路由转发，权限控制
- **ly-auth-center**: 用户认证与授权
- **ly-cart**: 购物车管理
- **ly-item**: 商品管理
- **ly-order**: 订单管理
- **ly-search**: 商品搜索
- **ly-user-service**: 用户管理

## 快速开始

1. 启动注册中心: `cd ly-registry && mvn spring-boot:run`
2. 启动配置中心: `cd ly-config && mvn spring-boot:run`
3. 启动其他微服务

## 数据库

数据库脚本位于项目根目录: `leyou.sql`

## 配置说明

各服务配置文件位于对应模块的`src/main/resources/bootstrap.yml`
