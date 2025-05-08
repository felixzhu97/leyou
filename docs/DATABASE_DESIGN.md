# 数据库设计文档

## 1. 用户服务数据库

### 1.1 用户表 (tb_user)

```sql
CREATE TABLE `tb_user` (
  `id` bigint NOT NULL AUTO_INCREMENT,
  `username` varchar(32) NOT NULL COMMENT '用户名',
  `password` varchar(32) NOT NULL COMMENT '密码',
  `phone` varchar(11) NOT NULL COMMENT '手机号',
  `created` datetime NOT NULL COMMENT '创建时间',
  PRIMARY KEY (`id`),
  UNIQUE KEY `username` (`username`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4;
```

## 2. 商品服务数据库

### 2.1 商品表 (tb_item)

```sql
CREATE TABLE `tb_item` (
  `id` bigint NOT NULL AUTO_INCREMENT,
  `title` varchar(100) NOT NULL COMMENT '商品标题',
  `price` decimal(10,2) NOT NULL COMMENT '商品价格',
  `stock` int NOT NULL COMMENT '库存',
  `category_id` bigint NOT NULL COMMENT '分类ID',
  PRIMARY KEY (`id`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4;
```

## 3. 订单服务数据库

### 3.1 订单表 (tb_order)

```sql
CREATE TABLE `tb_order` (
  `order_id` bigint NOT NULL COMMENT '订单id',
  `total_pay` decimal(10,2) NOT NULL COMMENT '总金额',
  `user_id` bigint NOT NULL COMMENT '用户id',
  `status` int NOT NULL COMMENT '订单状态',
  `create_time` datetime NOT NULL COMMENT '创建时间',
  PRIMARY KEY (`order_id`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4;
```

## 4. Redis 数据结构

### 4.1 购物车数据

```
Key格式: cart:{userId}
Value类型: Hash
存储内容: {skuId: 商品数量}
```
