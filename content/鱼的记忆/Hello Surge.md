---
date: "2025-12-30T10:15:45+08:00"
title: "Hello Surge, Again!"
description: "Surge 是苹果端最强的代理软件。"
summary: "Surge 是苹果端最强的代理软件。"
dropCap: false
indent: true
tags:
  - surge
  - clash
  - 代理上网
---


> **<div align="center" style="color: gary;">「如无必要，勿增实体。」</div>**

# 契机

尽管买了 Surge 快两年了，但工作环境的原因一直用的都是 Clash 系的代理软件，所以也没仔细研究过怎么用这个软件。
契机是正好快年底了，有机会折腾一下家里的 NAS 系统，研究内网穿透的时候，接触到了 Surge Ponte，
原以为 Surge Ponte 一定要 MacOS，那就又要交一笔费用了。
顺道发现现的 Surge 可以运行在 Apple Tv 上，这不巧了嘛，正好家里有一个在积灰。
重拾 Surge 后，最直观的感受就是..顺手..，其实这两个字从我一个 Clash 系的人来说，着实是很奇怪的，
但事实确实如此。以后会开篇阐述为什么会这样，这里就允许我买个关子吧。


# 配置

现在我用的配置在[深港有猫配置](深港有猫配置)基础上做了修改，当然他的配置很棒，注释写的很详细。
我只是加入了一些私人化的内容，以下为逐段分析我自己用配置，仅作参考。
具体异同，需要大家考虑自己的实际使用情况。

配置文件格式采用 `INI 格式`


## 全局配置 General

### 日志级别

```
loglevel = notify
```



<!-- 链接统一存放 🐈 -->
[深港有猫配置]: https://raw.githubusercontent.com/Rabbit-Spec/Surge/Master/Conf/Spec/Surge-EN.conf