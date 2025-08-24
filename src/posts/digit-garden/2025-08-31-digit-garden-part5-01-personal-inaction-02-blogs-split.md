---
title: 个人博客拆分
date: 2025-08-22
categories: [DigitGarden]
tags: [digit-garden, sh]
published: true
---

# 前言

个人写了快 10 年的博客 [houbb.github.io](https://houbb.github.io)

一直用的是 jekyll，技术已经很老了。

想升级为 vuepress，发现编译直接内存 OOM。

于是想着拆分为更多的子项目。

# 拆分思路

可以按照几个方面：后端工程师、前端工程师、DBA、DevOps 运维、Big-Data AI 前沿技术团队、其他杂项。

我目前博客大概6000篇，一次编译 vuepress 会爆掉。

于是想着如何拆分比较合适。

## vuepress 中的如何整合知识图谱插件

把 6000 篇文章 按照「技术岗位/角色」来归类，这样更贴近读者的实际定位。

然后再考虑如何 拆分成 3 个子博客，避免 VuePress 爆掉。

## 🧩 岗位视角的分类（重新归类）

### 1. 后端工程师

面向 Java / 分布式 / 系统设计 / 中间件等

* Java 系列: Java (655), Spring (100), JVM (36), JMM (10), Kotlin (14), C# (11), Go (9), Python (6)
* 分布式 / 微服务: Distributed (189), Dubbo (60), SOFA (65), Zookeeper (31), RPC (6), Consistency/Lock/Concurrency/Thread (126 合计)
* 中间件 / 基础组件: MQ (89), Netty (88), Redis (61), Cache (64), IM (55), Engine (49), Schedule (40)
* 架构 / 设计: Design (85), DesignPattern (45), System-Design (10), Architecture (6), Pattern (8)
* 性能 / 监控: Trace (50), APM (36), Monitor (48), Log (87), Memory (51), Safe/Security/SSO (30 合计)
* 开发工具链: Maven (9), java-tool (9), Config (22)

👉 大约 2000 篇

---

### 2. 前端工程师

面向 Web / 前端框架 / UI

* Web 基础: Web (348), FrontEnd (71), HTML (13), JS (25), Protocol (23), HTTP (8)
* 框架 & 构建: Vue (134), WebPack (31), NodeJs (10), React (2), NPM (6)
* 前端专题: UI (37), CSS/样式类（归入 Web/FrontEnd），性能调优 Performance (3)

👉 大约 600–700 篇

---

### 3. DBA / 数据工程

数据库 / SQL / ETL / 搜索引擎

* 数据库: Database (366), SQL (155), mybatis (17), ORM (10), Oracle (6), NoSQL (6), Mysql (2)
* 大数据 / ETL: ETL (85), Big-Data (4), BigData (3), Data (38), DataStruct (3), Data-Management (2)
* 搜索 & 存储: Lucene (51), Search (40), Search-Engine (3), File-system (72)

👉 大约 700–800 篇

---

### 4. DevOps / 运维工程师

系统 / CI/CD / 容器 / Linux

* OS / 系统: Linux (95), Windows (39), OS (22), Ubuntu (13), Mac (5)
* 容器 & 运维: Docker (57), Container (3), DevOps (127), Devpos (8), CI (7), CMDB (8)
* 工具: Git (57), Tool (140), vcs (11), IDE (5)
* 监控 / 配置: Config (22), System (18), ITSM (3)

👉 大约 600–700 篇

---

### 5. Big Data / AI / 前沿探索团队

AI、NLP、机器学习、区块链、Web3、Metaverse

* AI & ML: AI (108), NLP (75), ML (20), DeepLearning (29)
* 大数据前沿: AIOps (13), Cloud (23), BI (5)
* Web3 & 区块链: WEB3 (133), BlockChain (10), Bitcoin (6), Metaverse (11)
* 量化 / 金融: Finance (18), Quant (9), Investment (4), Money (3)

👉 大约 500–600 篇

---

### 6. 其他杂项 / 思考随笔

* 学习 & 思考: Note (54), Think (21), Life (16), Reading (6), Work (6), Interview (21), Project (15), Team (16)
* 杂项: blogs (29), Biz (58), Doc (10), Awesome (19), Summary (2)
* 小分类 & 零散主题: Safe, Acquire, Games, LAW, SEO, Marketing, etc.

👉 大约 500 篇

---

## 📦 如何拆分成 3 个子博客？

结合数量（6000 篇总量），我建议这样拆：

### 子站 1：后端工程师 + DBA

* 内容：Java、Spring、分布式、中间件、数据库
* 篇数：\~2800 篇
* 目标用户：后端开发 / 架构师 / DBA

---

### 子站 2：前端工程师 + DevOps 运维

* 内容：Web、前端框架、Linux、Docker、CI/CD、工具链
* 篇数：\~1300–1400 篇
* 目标用户：前端 / 运维 / 全栈

---

### 子站 3：AI & Big Data & 前沿探索 + 杂项

* 内容：AI/ML、Web3、区块链、元宇宙、大数据探索、随笔
* 篇数：\~1600–1700 篇
* 目标用户：AI 团队、研究人员、关注未来技术的读者

---

## ⚙️ 好处

1. 每个子站 ≤ 3000 篇，VuePress 编译压力大幅降低。
2. 按岗位视角分类，读者能自然找到适合自己的内容。
3. 跨站链接 仍可通过 wiki-link 实现，保持“数字花园”体验。
