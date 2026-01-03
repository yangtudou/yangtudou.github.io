---
title: 如何使用 Hugo Theme DoIt
subtitle:
date: 2026-01-02T10:31:12+08:00
lastmod: 2026-01-03T06:00:00+08:00
draft: false
description: ToIt 是一个很棒的 hugo 主题。

authors:
  - “洋san芋”

tags:
  - “hugo”
  - “DoIt”

---


<!--more-->

## 引言
这个主题真不错，开箱即用。[官方说明书](https://hugodoit.pages.dev/zh-cn/theme-documentation-basics/)写的很好，但涉及到一些细节的使用并没有详细说明，我这里是在**官方基础上**作出的补充，具体操作还是关注官方介绍和使用说明。

## 扩展用法
{{< admonition warning “注意”>}}
以下扩展也许只适用于 ToIt 主题，不具有通用性。
{{< /admonition >}}

### 标签用法
用这两组标签 `{{< admonition >}}` & `{{< /admonition >}}`
包裹住内容, 默认在不添加参数时，用的是 `note`
1. `admonition` 不可以省略
2. `note` 默认值

| 参数名称 | 默认图标 | 默认名称 |
| :-: | :-----------: | :-: |
| note | 笔 | 注意 |
| tip | 灯泡 | 技巧 |

3. `title` 可以不填写，自定义标签标题。

#### 示例用法
```markdown
{{< admonition note “第三个变量”>}}
这个标签是注意，图标是一支笔。
这里第三个变量可以自定义标签 title
{{< /admonition >}}
```

### 样式扩展
```markdown
{{< style "text-align: right;" >}}

{{< /style >}}
```