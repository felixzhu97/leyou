# 开发者指南

## 1. 开发环境配置

### 1.1 开发工具

- IDE: IntelliJ IDEA 或 Eclipse
- 数据库工具: Navicat 或 DBeaver
- API 测试工具: Postman 或 Insomnia

### 1.2 本地环境搭建

```bash
# 克隆项目
git clone https://github.com/your-repo/leyou.git

# 安装依赖
mvn clean install
```

## 2. 代码规范

### 2.1 命名规范

- 类名: 大驼峰式 (如 UserService)
- 方法名: 小驼峰式 (如 getUserById)
- 变量名: 小驼峰式
- 常量: 全大写加下划线 (如 MAX_COUNT)

### 2.2 包结构规范

```
com.leyou.[服务名]
├── config       # 配置类
├── controller   # 控制器
├── service      # 服务层
├── mapper       # 数据访问层
└── pojo         # 实体类
```

## 3. 测试规范

### 3.1 单元测试

- 测试类命名: 被测试类名 + Test (如 UserServiceTest)
- 测试方法命名: test + 被测试方法名 + 测试场景 (如 testGetUserByIdWhenUserExists)

### 3.2 集成测试

- 使用@SpringBootTest 注解
- 测试数据使用 H2 内存数据库

## 4. 提交规范

- 提交信息格式: [类型] 简要描述
  - 示例: [FEATURE] 添加用户登录功能
  - 类型包括: FEATURE, FIX, DOCS, STYLE, REFACTOR, TEST
