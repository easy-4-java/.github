# Easy-4-Java

> **🧰 Java 易用工具集** —— 由 [@Loong Wan](https://github.com/loong10k) Fork、开发与维护
>
> Spring Boot Starter · 第三方服务 SDK · 框架扩展 · Prometheus 指标集成

<p align="center">
  <img alt="Easy4Java Logo" src="./assets/logo-512.png" width="220">
</p>

<p align="center">
  <a href="https://github.com/easy-4-java"><img alt="Repos" src="https://img.shields.io/badge/Repos-274-blue?style=flat-square&logo=openjdk"></a>
  <a href="https://github.com/easy-4-rust"><img alt="Rust Counterpart" src="https://img.shields.io/badge/Counterpart-easy--4--rust-orange?style=flat-square&logo=rust"></a>
  <a href="https://github.com/partme-ai"><img alt="Ecosystem" src="https://img.shields.io/badge/Ecosystem-partme--ai-6366f1?style=flat-square"></a>
  <a href="https://github.com/easy-4-java/.github/blob/main/LICENSE"><img alt="License" src="https://img.shields.io/badge/License-Apache_2.0-green?style=flat-square"></a>
</p>

---

## 关于本组织

**Easy-4-Java** 是 [partme-ai](https://github.com/partme-ai) 开源生态下的 **Java 工具集组织**，托管由 [@Loong Wan](https://github.com/loong10k) Fork、开发与维护的 Java 组件（原 `io.github.hiwepy` 系列项目迁移而来）。围绕 Spring Boot 应用开发的高频场景，提供**开箱即用的 Starter、第三方服务 SDK 与框架扩展**，目前共 **274 个公开仓库**。

> 📌 **重要说明**：本组织**不托管**以下常见开源项目的镜像或 fork：
> - [`easyexcel`](https://github.com/alibaba/easyexcel) —— Alibaba 开源项目，独立维护
> - [`sa-token`](https://github.com/dromara/Sa-Token) —— dromara 开源项目，独立维护
> - [`hutool`](https://github.com/dromara/hutool) —— dromara 开源项目，独立维护
>
> 这些项目都有完整的官方仓库，**请直接使用官方版本**。
>
> 组织内的 `easyexcel` 仓库为 [alibaba/easyexcel](https://github.com/alibaba/easyexcel) 的 **fork**（仅作上游跟踪），使用请以官方为准。

---

## 🧰 工具集矩阵

### Spring Boot Starter（155 个）

面向中间件与三方服务的自动装配，`pom` 引入即用：

| 方向 | 代表仓库 |
|------|----------|
| 高性能并发 | [`disruptor-spring-boot-starter`](https://github.com/easy-4-java/disruptor-spring-boot-starter) |
| 实时通信 | [`socketio-spring-boot-starter`](https://github.com/easy-4-java/socketio-spring-boot-starter) |
| IP 归属地 | [`ip2region-spring-boot-starter`](https://github.com/easy-4-java/ip2region-spring-boot-starter) |
| 任务调度 | [`xxljob-spring-boot-starter`](https://github.com/easy-4-java/xxljob-spring-boot-starter) |
| 对象存储 | [`minio-spring-boot-starter`](https://github.com/easy-4-java/minio-spring-boot-starter) |
| 安全认证 | [`security-*`](https://github.com/orgs/easy-4-java/repositories?q=security-spring-boot-starter)、[`shiro-*`](https://github.com/orgs/easy-4-java/repositories?q=shiro-spring-boot-starter) 系列 |
| 云厂商接入 | [`aliyun-oss`](https://github.com/easy-4-java/aliyun-oss-spring-boot-starter)、[`tencentapi`](https://github.com/easy-4-java/tencentapi-spring-boot-starter)、[`faceplusplus`](https://github.com/easy-4-java/faceplusplus-spring-boot-starter) 等 |

### 框架扩展（25 个）

对成熟框架的能力增强，**不依赖 Spring Boot**，JDK 8 兼容：

| 框架 | 代表仓库 |
|------|----------|
| OkHttp | [`okhttp3-extension`](https://github.com/easy-4-java/okhttp3-extension) |
| HttpClient | [`httpclient-extension`](https://github.com/easy-4-java/httpclient-extension)、[`httpclient3-extension`](https://github.com/easy-4-java/httpclient3-extension) |
| Pac4j | [`pac4j-oauth-extension`](https://github.com/easy-4-java/pac4j-oauth-extension)、[`pac4j-otp-extension`](https://github.com/easy-4-java/pac4j-otp-extension) |
| Shiro | [`shiro-jwt-extension`](https://github.com/easy-4-java/shiro-jwt-extension)、[`shiro-saml-extension`](https://github.com/easy-4-java/shiro-saml-extension) |
| 插件体系 | [`pf4j-extension`](https://github.com/easy-4-java/pf4j-extension)、[`pf4j3-extension`](https://github.com/easy-4-java/pf4j3-extension) |
| 其他 | [`validation-api-extension`](https://github.com/easy-4-java/validation-api-extension)、[`zxing-extension`](https://github.com/easy-4-java/zxing-extension)、[`spring-data-redis-extension`](https://github.com/easy-4-java/spring-data-redis-extension) |

### 第三方服务 SDK（17 个）

| 服务 | 代表仓库 |
|------|----------|
| 数据同步 | [`canal-client-plus-sdk`](https://github.com/easy-4-java/canal-client-plus-sdk) |
| 音视频 | [`agora-java-sdk`](https://github.com/easy-4-java/agora-java-sdk) |
| 协同办公 | [`dingtalk-sdk-extension`](https://github.com/easy-4-java/dingtalk-sdk-extension) |
| AI 编程工具 | [`openclaw-java-sdk`](https://github.com/easy-4-java/openclaw-java-sdk)、[`opencode-java-sdk`](https://github.com/easy-4-java/opencode-java-sdk)、[`codex-java-sdk`](https://github.com/easy-4-java/codex-java-sdk) |
| 人脸识别 | [`faceplusplus-java-sdk`](https://github.com/easy-4-java/faceplusplus-java-sdk)、[`arcface`](https://github.com/easy-4-java/arcface-spring-boot-starter) |
| 其他 | [`ishumei-java-sdk`](https://github.com/easy-4-java/ishumei-java-sdk)、[`fetion4j-sdk`](https://github.com/easy-4-java/fetion4j-sdk)、[`hermes-java-sdk`](https://github.com/easy-4-java/hermes-java-sdk) |

### 指标集成（6 个）

组件运行指标 → Prometheus 格式：

[`druid-metrics-prometheus`](https://github.com/easy-4-java/druid-metrics-prometheus) · [`okhttp3-metrics-prometheus`](https://github.com/easy-4-java/okhttp3-metrics-prometheus) · [`sentinel-metrics-prometheus`](https://github.com/easy-4-java/sentinel-metrics-prometheus) · [`redis-metrics-prometheus`](https://github.com/easy-4-java/redis-metrics-prometheus) · [`undertow-metrics-prometheus`](https://github.com/easy-4-java/undertow-metrics-prometheus) · [`mybatis-metrics-prometheus`](https://github.com/easy-4-java/mybatis-metrics-prometheus)

### 文档与工具库

| 仓库 | 说明 |
|------|------|
| [`easydoc`](https://github.com/easy-4-java/easydoc) | Word 文档生成（Docx4j + 多模板引擎） |
| [`easypdf`](https://github.com/easy-4-java/easypdf) | Word/PDF 文档生成（XHTML 模板 + Docx4j/iText） |
| [`hitool`](https://github.com/easy-4-java/hitool) | 基础开发工具集合 |
| [`mybatis-enhance`](https://github.com/easy-4-java/mybatis-enhance) / [`mybatis-plus-enhance`](https://github.com/easy-4-java/mybatis-plus-enhance) | MyBatis 能力增强 |
| [`spring-bytebuddy`](https://github.com/easy-4-java/spring-bytebuddy) / [`spring-javassist`](https://github.com/easy-4-java/spring-javassist) | 字节码生成 Spring MVC Controller |

---

## 🌟 代表性项目

| 项目 | 说明 | ⭐ |
|------|------|:---:|
| [`disruptor-spring-boot-starter`](https://github.com/easy-4-java/disruptor-spring-boot-starter) | Disruptor 高性能队列 Starter | 128 |
| [`spring-boot-starter-samples`](https://github.com/easy-4-java/spring-boot-starter-samples) | Starter 使用示例合集 | 76 |
| [`socketio-spring-boot-starter`](https://github.com/easy-4-java/socketio-spring-boot-starter) | Netty-socketio Starter | 73 |
| [`easydoc`](https://github.com/easy-4-java/easydoc) | Word 文档生成（Docx4j + 多模板引擎） | 61 |
| [`ip2region-spring-boot-starter`](https://github.com/easy-4-java/ip2region-spring-boot-starter) | IP 归属地查询 Starter | 53 |
| [`mybatis-plus-enhance`](https://github.com/easy-4-java/mybatis-plus-enhance) | MyBatis-Plus 能力增强 | 15 |

> 星标数为 2026-08-06 GitHub 数据，完整列表见 [组织仓库页](https://github.com/orgs/easy-4-java/repositories)。

---

## 🚀 发布与使用

- **groupId**：`io.github.easy4j`（自 `io.github.hiwepy` 迁移）
- **分支基线**：`feature/1.0.x`（JDK 8）· `feature/2.0.x`（JDK 17）· `feature/3.0.x`（JDK 21）
- **发布渠道**：阿里云 Maven 制品仓库（packages.aliyun.com）
- **Maven Central**：尚未发布，请勿使用虚构的 Central 坐标

各仓库的版本号、依赖方式与使用示例，**以对应仓库的 README 与 release 为准**：

```xml
<dependency>
    <groupId>io.github.easy4j</groupId>
    <artifactId>disruptor-spring-boot-starter</artifactId>
    <version>请以仓库 release 为准</version>
</dependency>
```

---

## 🦀 Rust 版本

如果你对 Rust 感兴趣，可以看 [easy-4-rust](https://github.com/easy-4-rust) —— **本组织的 Rust 姊妹组织**，已发布多个文档处理与通用工具 crate（`easyexcel-rs`、`easypdf-rs`、`easyofd-rs`、`hitool-rs` 等）。

---

## 相关生态

| 组织 | 说明 |
|------|------|
| 🦀 [easy-4-rust](https://github.com/easy-4-rust) | Rust 工具集（文档处理 · 通用工具） |
| 🏛️ [ddd-4-java](https://github.com/ddd-4-java) | DDD 基础构件 |
| 🏛️ [ddd-4-rust](https://github.com/ddd-4-rust) | DDD 基础构件 Rust 版 |
| 💾 [rbatis-plus](https://github.com/rbatis-plus) | RBatis ORM 增强生态 |
| 🧠 [partme-ai](https://github.com/partme-ai) | 顶层 AI 智能体生态品牌 |

---

## 📄 License

本组织下所有项目采用 [Apache 2.0](LICENSE) 开源许可证。

---

<div align="center">

**Made with ❤️ by [PartMe AI Team](https://github.com/partme-ai)**

</div>
