---
title: Hello Test
description: Hello world~~~~~~~~~~~~~~
published: true
date: 2026-01-21T07:09:31.571Z
tags: page
editor: markdown
dateCreated: 2026-01-12T02:33:42.828Z
---

# Header
Hello world~~

测试 公开 git库~~~

``` sequence
Browser->>Wiki.js: 1. HTTP/HTTPS 请求 (如 /home)
Wiki.js->>PostgreSQL: 2. 查询页面元数据
PostgreSQL-->>Wiki.js: 3. 返回元数据
Wiki.js->>Git存储层: 4. 读取 Markdown 文件 (home.md)
Git存储层-->>Wiki.js: 5. 返回 .md 内容
Wiki.js->>Wiki.js: 6. 渲染 Markdown → HTML
Wiki.js-->>Browser: 7. 
```
