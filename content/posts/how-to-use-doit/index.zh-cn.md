---
title: 如何使用 Hugo Theme DoIt
subtitle: 
date: 2026-01-02T10:31:12+08:00
lastmod: 2026-01-02T10:31:12+08:00
draft: false
description: DoIt 是一个很棒的 hugo 主题，功能很全。

authors:
  - yangtudou
tags:
  - hugo
  - DoIt
categories:
  - 如何使用 DoIt
series: []
hiddenFromHomePage: false
hiddenFromSearch: false
featuredImage: ""
featuredImagePreview: "how-to-use-doit.webp"
toc:
  enable: true
  auto: false
math:
  enable: false
lightgallery: false
license: ""
---


<!--more-->

## 引言
这个主题真不错，开箱即用。[官方说明书](https://hugodoit.pages.dev/zh-cn/theme-documentation-basics/)写的很好，
但涉及到一些细节的使用并没有详细说明，我这里是在**官方基础上**作出的补充，
具体操作还是关注官方介绍和使用说明。

## 扩展用法
{{< admonition warning >}}
以下扩展也许只适用于 DoIt 主题内使用，不具有通用性。
{{< /admonition >}}

### [标签用法]^({{</* admonition */>}})
用这两组标签 `{{</* admonition */>}}` & `{{</* /admonition */>}}` 包裹住内容, 默认在不添加任何参数时，
用的是 `note` 标签,`admonition` 不可以省略。

#### 第一个参数
| 参数名称 | 默认图标 | 默认名称 |
| :-----: | :----: | :-----: |
| [note]^(default) | 笔 | 注意 |
| tip | 灯泡 | 技巧 |
| abstract |  | |
| info |  | |
| success |  | |
| question |  | |
| warning |  | |
| failure |  | |
| danger |  | |
| bug |  | |
| quote |  | |
| example |  | |

#### 第二个参数
可以不添加，作用是更改默认 title

#### 示例用法
可以根据样式，直接复制代码来使用。

<!-- note 默认标签 -->
```markdown
{{</* admonition note */>}}

{{</* /admonition */>}}
```

{{< admonition note >}}
这是一个默认标签，note！
{{< /admonition >}}

<!-- warning 标签 -->
```markdown
{{</* admonition warning */>}}

{{</* /admonition */>}}
```

{{< admonition warning >}}
这是 warning 标签。
{{< /admonition >}}

<!-- tip 标签 -->
```markdown
{{</* admonition tip */>}}

{{</* /admonition */>}}
```

{{< admonition tip >}}
这是 tip 标签。
{{< /admonition >}}

<!-- abstract 标签 -->
```markdown
{{</* admonition abstract */>}}

{{</* /admonition */>}}
```

{{< admonition abstract >}}
这是 abstract 标签。
{{< /admonition >}}

<!-- info 标签 -->
```markdown
{{</* admonition info */>}}

{{</* /admonition */>}}
```

{{< admonition info >}}
这是 info 标签。
{{< /admonition >}}

<!-- success 标签 -->
```markdown
{{</* admonition success */>}}

{{</* /admonition */>}}
```

{{< admonition success >}}
这是 success 标签。
{{< /admonition >}}

<!-- question 标签 -->
```markdown
{{</* admonition question */>}}

{{</* /admonition */>}}
```

{{< admonition question >}}
这是 question 标签。
{{< /admonition >}}

<!-- failure 标签 -->
```markdown
{{</* admonition failure */>}}

{{</* /admonition */>}}
```

{{< admonition failure >}}
这是 failure 标签。
{{< /admonition >}}

<!-- danger 标签 -->
```markdown
{{</* admonition danger */>}}

{{</* /admonition */>}}
```

{{< admonition danger >}}
这是 danger 标签。
{{< /admonition >}}

<!-- bug 标签 -->
```markdown
{{</* admonition bug */>}}

{{</* /admonition */>}}
```

{{< admonition bug >}}
这是 bug 标签。
{{< /admonition >}}

<!-- quote 标签 -->
```markdown
{{</* admonition quote */>}}

{{</* /admonition */>}}
```

{{< admonition quote >}}
这是 quote 标签。
{{< /admonition >}}

<!-- example 标签 -->
```markdown
{{</* admonition example */>}}

{{</* /admonition */>}}
```

{{< admonition example >}}
这是 example 标签。
{{< /admonition >}}

### 样式扩展

```markdown
{{</* style "color: green;text-align: center;" */>}}
这是一段绿色的居中文字。
{{</* /style */>}}
```

{{< style "color: green;text-align: center;" >}}
这是一段绿色的居中文字。
{{< /style >}}