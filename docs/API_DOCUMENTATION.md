# API 文档

## 1. 用户服务

### 1.1 用户注册

- 路径：/user/register
- 方法：POST
- 请求参数：
  ```json
  {
    "username": "string",
    "password": "string",
    "phone": "string"
  }
  ```

### 1.2 用户登录

- 路径：/user/login
- 方法：POST
- 请求参数：
  ```json
  {
    "username": "string",
    "password": "string"
  }
  ```

## 2. 商品服务

### 2.1 查询商品列表

- 路径：/item/list
- 方法：GET
- 请求参数：
  ```json
  {
    "page": 1,
    "size": 10,
    "sortBy": "price",
    "desc": false
  }
  ```

## 3. 订单服务

### 3.1 创建订单

- 路径：/order/create
- 方法：POST
- 请求参数：
  ```json
  {
    "items": [
      {
        "skuId": 123,
        "num": 2
      }
    ],
    "addressId": 1
  }
  ```
