# 部署指南

## 1. 环境要求

- JDK 1.8+
- MySQL 5.7+
- Redis 5.0+
- Maven 3.6+
- Nginx (可选，用于 API 网关)

## 2. 服务部署步骤

### 2.1 数据库准备

```bash
# 创建数据库
mysql -uroot -p -e "CREATE DATABASE leyou_user CHARACTER SET utf8mb4 COLLATE utf8mb4_general_ci"
mysql -uroot -p -e "CREATE DATABASE leyou_item CHARACTER SET utf8mb4 COLLATE utf8mb4_general_ci"
mysql -uroot -p -e "CREATE DATABASE leyou_order CHARACTER SET utf8mb4 COLLATE utf8mb4_general_ci"

# 导入初始数据
mysql -uroot -p leyou_user < leyou.sql
```

### 2.2 服务编译打包

```bash
# 在项目根目录执行
mvn clean package -DskipTests
```

### 2.3 服务启动顺序

1. 启动注册中心 (ly-registry)
2. 启动配置中心 (ly-config)
3. 启动 API 网关 (ly-api-gateway)
4. 启动其他微服务

## 3. 配置文件说明

所有服务的配置文件位于各服务的`src/main/resources/bootstrap.yml`中，主要配置项包括：

- 服务端口
- 数据库连接
- Redis 连接
- 注册中心地址
- 配置中心地址

## 4. 常用运维命令

```bash
# 查看服务日志
tail -f logs/application.log

# 检查服务健康状态
curl http://localhost:服务端口/actuator/health
```
