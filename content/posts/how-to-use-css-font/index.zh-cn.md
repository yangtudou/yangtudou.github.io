---
title: "css 字体 详解"
subtitle:
date: 2026-01-05T00:00:00+08:00
lastmod: 2026-01-05T00:00:00+08:00
draft: false
description: "字体对于一个页面很重要。"

authors:
  - "洋san芋"

tags:
  - css
  - font

categories: []

series: []

hiddenFromHomePage: false
hiddenFromSearch: false
featuredImage: ""
featuredImagePreview: "how-to-use-css-font.webp"
toc:
  enable: true
  auto: false
math:
  enable: false
lightgallery: true
license: ""
---

<!--more-->


## 起因

起因是这样的，DoIt 主题有 stlye 的简码，想着做一个字体预览吧，结果遇到一堆事。

- 中文字体包普遍很大，web 传输是不合理的。
- 自定义字体引入，就需要一个文件服务器，还得需要支持跨域，特别是 `@import` 引入。
- 截取所需部分中文字符单独做成一个 woff2 得字体包来传输。python 的 subset
