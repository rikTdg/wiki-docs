---
title: Hello Test
description: Hello world~~~~~~~~~~~~~~
published: true
date: 2026-01-21T07:20:40.702Z
tags: page
editor: markdown
dateCreated: 2026-01-12T02:33:42.828Z
---

# Header
Hello world~~

测试 公开 git库~~~



```mermaid
sequenceDiagram
    participant Browser
    participant WikiJS as Wiki.js
    participant PostgreSQL
    participant GitStorage as Git存储层

    Browser->>WikiJS: 1. HTTP/HTTPS 请求 (如 /home)
    WikiJS->>PostgreSQL: 2. 查询页面元数据
    PostgreSQL-->>WikiJS: 3. 返回元数据
    WikiJS->>GitStorage: 4. 读取 Markdown 文件 (home.md)
    GitStorage-->>WikiJS: 5. 返回 .md 内容
    WikiJS->>WikiJS: 6. 渲染 Markdown → HTML
    WikiJS-->>Browser: 7. 返回 HTML 响应
