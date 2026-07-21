# Easy-4-Java

<p align="center">
  <img alt="Easy-4-Java" src="./assets/banner.svg" width="800">
</p>

<p align="center">
  <strong>面向 Java 的易用工具集 —— 文档处理、安全鉴权、通用工具箱等高频场景的一站式解决方案</strong>
</p>

<p align="center">
  <a href="https://github.com/easy-4-java"><img alt="Repos" src="https://img.shields.io/badge/Repos-TBD-blue?style=flat-square"></a>
  <a href="https://github.com/easy-4-rust"><img alt="Rust Counterpart" src="https://img.shields.io/badge/Counterpart-easy--4--rust-orange?style=flat-square&logo=rust"></a>
  <a href="https://github.com/ddd-4-java"><img alt="Architecture" src="https://img.shields.io/badge/Architecture-ddd--4--java-blue?style=flat-square&logo=openjdk"></a>
  <a href="https://github.com/partme-ai"><img alt="Ecosystem" src="https://img.shields.io/badge/Ecosystem-partme--ai-6366f1?style=flat-square"></a>
  <a href="https://github.com/easy-4-java/.github/blob/main/profile/LICENSE"><img alt="License" src="https://img.shields.io/badge/License-Apache_2.0-green?style=flat-square"></a>
</p>

---

## 关于我们

**Easy-4-Java** 是 partme-ai 开源生态旗下的**易用工具集**组织，专注于为 Java 生态提供文档处理、安全鉴权、通用工具等高频场景的工程化、规范化、可复用解决方案。

我们的核心理念是：

> **让 Java 开发者不再重复造轮子，把高频场景沉淀为标准构件。**

### 设计原则

- **📦 模块化** — 每个 jar 独立可装，按需引入，无强制依赖
- **🏗️ 企业级** — 完整测试、CI / CD、生产验证、版本化发布
- **🔌 可插拔** — 持久化、缓存、消息均通过 SPI 扩展
- **📐 规范一致** — 与 `easy-4-rust` 接口级对齐，跨语言团队对照阅读
- **🧰 约定优于配置** — 零配置即可上手，进阶场景提供完整配置点

---

## 工具集矩阵

### 文档处理（Document）

| 仓库 | 说明 |
|------|------|
| 待发布 | `easyexcel` 流式 Excel 框架（Spring Boot Starter） |
| 待发布 | `easypdf` PDF 操作库（基于 iText / PDFBox） |
| 待发布 | `easyofd` OFD（开放版式文档）操作库 |
| 待发布 | `easydoc` DOCX 模板生成（基于 docx4j） |

### 安全与权限（Security）

| 仓库 | 说明 |
|------|------|
| 待发布 | `sa-token` 认证鉴权框架（Spring Boot Starter） |
| 待发布 | `sa-token-*` 系列（Redis / JWT / SSO / OAuth2） |

### 通用工具（Toolkit）

| 仓库 | 说明 |
|------|------|
| 待发布 | `hutool` 工具箱增强 / 扩展模块 |
| 待发布 | `easyexcel-enhance` 多数据源 / 加密 / 注解增强 |

---

## 架构概览

```
┌─────────────────────────────────────────────────────────────┐
│                 easy-4-java 工具集矩阵                       │
├─────────────────────────────────────────────────────────────┤
│  文档处理   │ easyexcel · easypdf · easyofd · easydoc       │
├─────────────────────────────────────────────────────────────┤
│  安全鉴权   │ sa-token (core / redis / jwt / sso / oauth2)  │
├─────────────────────────────────────────────────────────────┤
│  通用工具   │ hutool · easyexcel-enhance                     │
├─────────────────────────────────────────────────────────────┤
│   ↓ 基础设施层（依赖）                                      │
│  Spring Boot · ddd-4-java · MyBatis-Plus · ...              │
└─────────────────────────────────────────────────────────────┘
```

---

## 快速开始

> ⏳ 项目处于筹备阶段，欢迎在 [Discussions](https://github.com/orgs/easy-4-java/discussions) 提交需求与共建提案。

### Maven 依赖（规划中）

```xml
<dependency>
    <groupId>org.easy-4-java</groupId>
    <artifactId>easyexcel-spring-boot-starter</artifactId>
    <version>0.1.0-SNAPSHOT</version>
</dependency>

<dependency>
    <groupId>org.easy-4-java</groupId>
    <artifactId>sa-token-spring-boot-starter</artifactId>
    <version>0.1.0-SNAPSHOT</version>
</dependency>

<dependency>
    <groupId>org.easy-4-java</groupId>
    <artifactId>hutool-enhance</artifactId>
    <version>0.1.0-SNAPSHOT</version>
</dependency>
```

### 示例：流式导出 Excel

```java
@Excel("用户列表")
public class UserVO {
    @ExcelProperty("ID")
    private Long id;

    @ExcelProperty("姓名")
    private String name;
}

@GetMapping("/export")
public void exportUsers(HttpServletResponse response) throws Exception {
    List<UserVO> users = userService.listAll();
    EasyExcel.write(response.getOutputStream(), UserVO.class)
        .sheet("用户")
        .doWrite(users);
}
```

### 示例：Sa-Token 鉴权

```java
@RestController
@RequestMapping("/user")
public class UserController {

    // 登录
    @PostMapping("/login")
    public String login(@RequestParam String username,
                        @RequestParam String password) {
        StpUtil.login(1001);
        return StpUtil.getTokenValue();
    }

    // 需要登录
    @SaCheckLogin
    @GetMapping("/info")
    public Object info() {
        return StpUtil.getLoginIdDefaultNull();
    }
}
```

---

## 与 Rust 版本对齐

| 能力 | Java | Rust | 状态 |
|------|------|------|------|
| 流式 Excel | easyexcel | easyexcel-rs | ✅ |
| PDF 操作 | easypdf | easypdf-rs | ✅ |
| OFD 版式 | easyofd | easyofd-rs | ✅ |
| DOCX 模板 | easydoc | easydoc-rs | ✅ |
| 认证鉴权 | sa-token | sa-token-rs | ✅ |
| 工具箱 | hutool | hitool-rs | ✅ |

> **输出兼容**：所有文档类库与 Rust 版本**字节级兼容**，生产环境可直接替换。

---

## 相关生态

| 组织 | 说明 |
|------|------|
| 🧰 [easy-4-rust](https://github.com/easy-4-rust) | Rust 工具集（一一对应） |
| 🏛️ [ddd-4-java](https://github.com/ddd-4-java) | DDD 基础构件 |
| 💾 [rbatis-plus](https://github.com/rbatis-plus) | ORM 生态 |
| 🧠 [partme-ai](https://github.com/partme-ai) | 顶层 AI 智能体生态 |

---

## 贡献指南

欢迎贡献新的工具 jar / starter！

1. **Fork** 目标仓库
2. 创建特性分支
3. 遵循既有命名与 API 风格
4. 补充单元测试、文档与 CHANGELOG
5. 提交 **Pull Request**

> 新工具提案请先在 [Discussions](https://github.com/orgs/easy-4-java/discussions) 发起 RFC。

---

## 联系我们

- Email: [partmeai@gmail.com](mailto:partmeai@gmail.com)
- GitHub: [github.com/easy-4-java](https://github.com/easy-4-java)

---

<div align="center">

**让 Java 高频场景不再重复造轮子**

Made with ❤️ by PartMe AI Team

</div>