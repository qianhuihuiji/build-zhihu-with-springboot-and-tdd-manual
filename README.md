# SpringZhihu TDD 实战教程

> 从零开始构建仿知乎问答系统，掌握 Spring Boot 测试驱动开发（TDD）技能

[![Spring Boot](https://img.shields.io/badge/Spring%20Boot-3.x-green.svg)](https://spring.io/projects/spring-boot)
[![JUnit 5](https://img.shields.io/badge/JUnit-5.x-orange.svg)](https://junit.org/junit5/)
[![Testcontainers](https://img.shields.io/badge/Testcontainers-latest-blue.svg)](https://www.testcontainers.org/)

---

## 项目介绍

**SpringZhihu** 是一个仿知乎的问答系统，但本项目的核心目标不是构建产品，而是**通过实战教授 TDD 和测试技能**。

课程原始源码见：[build-zhihu-with-springboot-and-tdd](https://github.com/qianhuihuiji/build-zhihu-with-springboot-and-tdd)

### 项目初衷

在多年的开发和教学实践中，我们发现一个普遍存在的问题：**很多开发者会写业务代码，但不会写测试代码**。即使写了测试，也往往是：

- 测试覆盖率为零，或者为了「达标」而凑数
- 测试代码质量低下，维护成本高昂
- 不知道如何测试数据库交互、HTTP 请求、权限控制等常见场景
- 对 TDD（测试驱动开发）有所耳闻，但从未真正实践过

本项目的初衷就是打造一门**兼具实用性和易学性**的测试课程。通过从零开始构建一个仿知乎的问答系统，手把手带你掌握 Spring Boot 应用的测试技能。

---

## 项目特色

### 1. 真实的 TDD 开发流程

本教程严格遵循 TDD 的「红 - 绿 - 重构」循环：

```
编写测试 → 运行测试（失败） → 编写代码 → 运行测试（通过） → 重构 → 重复
```

### 2. 全面的测试场景覆盖

| 测试场景 | 说明 |
|---------|------|
| 数据库测试 | 使用 Testcontainers 创建隔离的测试数据库 |
| 测试表单验证 | 验证用户输入的有效性 |
| 测试文件上传 | 处理头像等文件上传场景 |
| 测试邮件发送 | 模拟邮件发送进行账户验证 |
| 测试远程 API 调用 | 测试第三方 API 集成 |
| 测试「异常」抛出 | 验证业务异常的正确处理 |
| 模拟登录用户 | 使用 Spring Security 测试认证和授权 |
| Contract 测试 | 确保 API 契约的稳定性 |

### 3. 多层次的测试策略

- **单元测试**：测试 Service、Policy 等单一组件的逻辑
- **集成测试**：测试 Controller 层的完整请求处理流程
- **容器化测试**：使用 Testcontainers + Docker 提供干净的测试环境

---

## 你将学到什么

完成本教程后，你将能够：

- ✅ 理解 TDD 的核心思想和实践方法
- ✅ 使用 JUnit 5 + Spring Test 编写单元测试和集成测试
- ✅ 使用 Testcontainers 进行数据库和中间件的隔离测试
- ✅ 测试 Spring Security 保护的受认证接口
- ✅ 测试表单验证、异常处理、文件上传等常见场景
- ✅ 使用 Mock 和 Stub 隔离外部依赖
- ✅ 建立测试驱动开发的信心和习惯

---

## 教程目录

| 章节 | 内容 | 说明 |
|------|------|------|
| 第一章 | [基础信息](docs/1.基础信息) | 项目背景、技术栈、TDD 理念 |
| 第二章 | [舞台布置](docs/2.舞台布置) | 环境准备、产品需求、用例分析 |
| 第三章 | [开始测试](docs/3.开始测试) | TDD 入门，完成第一个测试 |
| 第四章 | [显示问题](docs/4.显示问题) | 学习问题展示功能的 TDD |
| 第五章 | [回答问题](docs/5.回答问题) | 回答功能、单元测试、表单验证、权限控制、最佳答案 |
| 第六章 | [赞成与反对](docs/6.赞成与反对) | 投票功能测试 |
| 第七章 | [添加问题](docs/7.添加问题) | 创建问题功能、表单验证、发布问题、@用户 |
| 第八章 | [问题互动](docs/8.问题互动) | 筛选、关注、推荐、举报、slug 转换 |
| 第九章 | [评论相关](docs/9.评论相关) | 评论功能测试、评论投票、@用户 |
| 第十章 | [用户相关](docs/10.用户相关) | 用户动态、活跃用户、未读消息 |

---

## 技术选型

### 核心框架

| 技术 | 说明 | 官网 |
|------|------|------|
| Spring Boot | 应用框架 | https://spring.io/projects/spring-boot |
| Spring Security | 认证和授权框架 | https://spring.io/projects/spring-security |
| MyBatis | ORM 框架 | http://www.mybatis.org/mybatis-3/zh/index.html |
| Liquibase/Flyway | 数据库版本控制工具 | https://www.liquibase.org/ |
| JWT | Token 认证支持 | https://github.com/jwtk/jjwt |

### 测试工具

| 技术 | 说明 | 官网 |
|------|------|------|
| JUnit 5 | 测试框架 | https://junit.org/junit5/ |
| Mockito | Mock 框架 | https://site.mockito.org/ |
| AssertJ | Fluent 断言库 | https://assertj.github.io/ |
| Testcontainers | 容器化测试工具 | https://www.testcontainers.org/ |
| Spring Test | Spring 测试支持 | https://docs.spring.io/spring-framework/docs/current/reference/html/testing.html |

### 其他技术

| 技术 | 说明 |
|------|------|
| PageHelper | MyBatis 分页插件 |
| Swagger-UI | 文档生产工具 |
| Hibernate Validator | 验证框架 |
| Redis | 分布式缓存 |
| Kafka/RabbitMQ | 消息队列 |
| Druid | 数据库连接池 |
| Lombok | 简化对象封装工具 |

---

## 开发环境

| 工具 | 版本号 | 说明 |
|------|--------|------|
| JDK | 17+ | 推荐使用 LTS 版本 |
| Maven | 3.8+ | 依赖管理和构建工具 |
| MySQL | 8.0 | 通过 Docker 运行 |
| Redis | 最新 | 通过 Docker 运行 |
| Docker | 28+ | 容器化测试环境 |
| IntelliJ IDEA | 最新版 | 社区版或正式版均可 |

> 💡 **注**：MySQL、Redis 等中间件均使用 Docker 运行，无需在本地安装

---

## 快速开始

### 1. 克隆项目

```bash
git clone https://github.com/qianhuihuiji/build-zhihu-with-springboot-and-tdd-manual.git
cd build-zhihu-with-springboot-and-tdd-manual
```

### 2. 安装依赖

```bash
mvn clean install
```

### 3. 运行测试

```bash
# 运行所有测试
mvn test

# 运行特定测试类
mvn test -Dtest=ViewQuestionsTests

# 排除在线测试（需要第三方 API）
mvn test -DexcludedGroups=online
```

### 4. 启动应用

```bash
# 确保 Docker 已启动（用于 Testcontainers）
mvn spring-boot:run
```

---

## 核心功能模块

```
SpringZhihu
├── 问题模块       # 创建、查看、编辑、删除、发布问题
├── 回答模块       # 创建、查看、删除回答，设置最佳答案
├── 评论模块       # 对问题/回答进行评论、评论投票
├── 投票模块       # 赞同/反对问题和回答
├── 互动模块       # 关注问题、推荐、举报、筛选
└── 用户模块       # 用户动态、活跃用户、消息通知
```

### 功能清单

| 功能 | 说明 |
|------|------|
| 问题管理 | 创建、查看、编辑、删除、发布问题 |
| 回答管理 | 创建、查看、删除回答，设置最佳答案 |
| 评论功能 | 对问题/回答进行评论，支持评论投票 |
| 投票功能 | 赞同/反对问题、回答、评论 |
| 互动功能 | 关注问题、推荐、举报、筛选、分类 |
| 用户功能 | 用户动态、活跃用户、未读消息、@用户通知 |

---

## 项目结构

```
src
├── main
│   ├── java
│   │   └── com.nofirst.spring.tdd.zhihu.startup
│   │       ├── controller/      # 控制器层
│   │       ├── service/         # 服务层
│   │       ├── mapper/          # 数据访问层
│   │       ├── model/           # 数据模型
│   │       ├── policy/          # 权限策略
│   │       ├── event/           # 领域事件
│   │       ├── listener/        # 事件监听器
│   │       ├── validator/       # 自定义验证器
│   │       └── exception/       # 业务异常
│   └── resources
│       └── db/migration/        # 数据库迁移脚本
└── test
    └── java
        └── com.nofirst.spring.tdd.zhihu.startup
            ├── integration/     # 集成测试
            ├── unit/            # 单元测试
            └── factory/         # 测试数据工厂
```

---

## 如何阅读本教程

本教程采用**渐进式**的章节结构，建议按顺序阅读：

1. **基础信息**：了解项目背景和技术栈
2. **舞台布置**：准备开发环境和产品需求
3. **开始测试**：TDD 入门，完成第一个测试
4. **显示问题**：学习问题展示功能的 TDD
5. **回答问题**：学习回答功能的实现和测试
6. **赞成与反对**：学习复杂业务逻辑的测试
7. **添加问题**：学习表单验证和权限控制
8. **问题互动**：学习筛选、关注等互动功能
9. **评论相关**：学习评论功能的完整实现
10. **用户相关**：学习用户动态、消息等功能

每个章节都遵循相同的节奏：

```
编写测试 → 运行测试（失败） → 编写代码 → 运行测试（通过） → 小结
```

---

## 相关资源

- **课程原始源码**：[build-zhihu-with-springboot-and-tdd](https://github.com/qianhuihuiji/build-zhihu-with-springboot-and-tdd)
- **本文档源码**：[build-zhihu-with-springboot-and-tdd-manual](https://github.com/qianhuihuiji/build-zhihu-with-springboot-and-tdd-manual)

---

## 关于 TDD

> 测试驱动开发不是关于测试，而是关于设计。— Kent Beck

> 先写测试，后写代码。这听起来很简单，但实际上需要大量的练习。— Martin Fowler

> 好的测试可以让你睡得更好。— 佚名

---

## 许可证

本项目采用 MIT 许可证。

---

**开始这段 TDD 之旅吧！测试不再是负担，而是你最好的编程伙伴。** 
