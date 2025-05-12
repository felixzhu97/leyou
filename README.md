# 乐优商城项目

## 项目概述

乐优商城是一个基于 Spring Cloud 的分布式电商系统，包含用户服务、商品服务、订单服务等核心模块。

## 提示

仓库中有配套项目
https://github.com/felixzhu97/leyou-portal   门户网站
https://github.com/felixzhu97/leyou-manage-web   后台管理系统

## 功能特性

- 用户注册登录
- 商品浏览搜索
- 购物车管理
- 订单创建支付
- 后台管理系统

## 技术栈

- 后端：Spring Boot + Spring Cloud
- 数据库：MySQL + Redis
- 搜索：Elasticsearch
- 消息队列：RabbitMQ
- 配置中心：Spring Cloud Config
- 服务注册中心：Eureka

## 快速开始

1. 克隆项目

```bash
git clone https://github.com/your-repo/leyou.git
```

2. 导入数据库

```bash
mysql -uroot -p < leyou.sql
```

3. 启动服务

```bash
mvn spring-boot:run
```

## 文档

- [架构设计](docs/ARCHITECTURE.md)
- [API 文档](docs/API_DOCUMENTATION.md)
- [数据库设计](docs/DATABASE_DESIGN.md)
- [部署指南](docs/DEPLOYMENT_GUIDE.md)
- [开发者指南](docs/DEVELOPER_GUIDE.md)
- [C4 架构图](docs/C4_ARCHITECTURE.puml)
- [ER 图](docs/ER_DIAGRAM.puml)

## 许可证

MIT License
