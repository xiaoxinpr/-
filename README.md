# 闲鱼二手交易平台

一个基于微信小程序的二手交易平台，提供完整的买卖闲置物品功能。
可以当作毕业设计，价格600元，包含微信小程序、Spring Boot 后端、Vue.js 管理后台、Python 脚本打包工具。
联系qq:2446912757
微信:13633093820

## 📱 项目概述

本项目是一个完整的二手交易平台解决方案，包含：
- **微信小程序**：用户端交易平台
- **Spring Boot 后端**：API 服务和业务逻辑
- **Vue.js 管理后台**：平台管理系统
- **实用工具**：Python 脚本打包工具

## 🏗️ 项目架构

```
闲鱼项目/
├── xianyuqianduan/           # 微信小程序前端
│   ├── miniprogram/          # 小程序源码
│   ├── backend/              # Spring Boot 后端
│   └── admin/                # Vue.js 管理后台

```

## ✨ 主要功能

### 🛒 用户功能
- **商品浏览**：首页商品展示、分类浏览、搜索功能
- **商品发布**：发布闲置物品、图片上传、商品管理
- **交易功能**：下单购买、订单管理、支付集成
- **聊天系统**：买卖双方实时沟通
- **用户中心**：个人信息、收藏夹、地址管理
- **微信登录**：一键登录、用户认证

### 🔧 管理功能
- **用户管理**：用户信息、权限控制
- **商品管理**：商品审核、分类管理
- **订单管理**：订单监控、交易统计
- **数据分析**：交易数据、用户行为分析

## 🛠️ 技术栈

### 前端技术
- **微信小程序**：原生小程序开发
- **Vue.js 3**：管理后台前端框架
- **Element Plus**：UI 组件库
- **TypeScript**：类型安全的 JavaScript
- **Vite**：现代化构建工具

### 后端技术
- **Spring Boot 3.2.0**：Java 后端框架
- **MyBatis Plus**：ORM 框架
- **MySQL 8.0**：关系型数据库
- **Redis**：缓存和会话存储
- **Spring Security**：安全认证框架
- **JWT**：用户认证令牌
- **阿里云 OSS**：文件存储服务

### 开发工具
- **Maven**：Java 项目构建工具
- **微信开发者工具**：小程序开发调试
- **PyInstaller**：Python 脚本打包工具

## 🚀 快速开始

### 环境要求
- **Java 17+**
- **Node.js 16+**
- **MySQL 8.0+**
- **Redis 6.0+**
- **微信开发者工具**

### 1. 克隆项目
```bash
git clone [项目地址]
cd xianyu
```

### 2. 数据库配置
```sql
-- 创建数据库
CREATE DATABASE xianyu DEFAULT CHARACTER SET utf8mb4;

-- 导入初始化脚本
source xianyuqianduan/backend/src/main/resources/sql/init.sql
```

### 3. 后端启动
```bash
cd xianyuqianduan/backend

# 修改配置文件
vim src/main/resources/application.yml

# 启动后端服务
mvn spring-boot:run
```

### 4. 管理后台启动
```bash
cd xianyuqianduan/admin

# 安装依赖
npm install

# 启动开发服务器
npm run dev
```

### 5. 小程序配置
1. 使用微信开发者工具打开 `xianyuqianduan/miniprogram` 目录
2. 配置小程序 AppID 和 AppSecret
3. 修改 `utils/request.js` 中的服务器地址
4. 编译并预览小程序


## 🔒 安全特性

- **JWT 认证**：无状态用户认证
- **Spring Security**：接口权限控制
- **数据验证**：输入参数校验
- **SQL 注入防护**：MyBatis 参数化查询
- **XSS 防护**：输出内容转义
- **HTTPS 支持**：生产环境加密传输

## 📈 性能优化

- **Redis 缓存**：热点数据缓存
- **数据库索引**：查询性能优化
- **图片压缩**：OSS 图片处理
- **长轮询**：实时消息推送
- **分页查询**：大数据量处理
- **懒加载**：小程序性能优化

## 🐛 常见问题

### 1. 数据库连接失败
```
错误：Public Key Retrieval is not allowed
解决：在数据库连接 URL 中添加 &allowPublicKeyRetrieval=true
```

### 2. 微信登录失败
```
错误：微信登录失败，请检查登录凭证
解决：检查 AppID 和 AppSecret 配置是否正确
```

### 3. 文件上传失败
```
错误：OSS 上传失败
解决：检查阿里云 OSS 配置和网络连接
```

