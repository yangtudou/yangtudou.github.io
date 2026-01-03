---
title: Hello Surge, Again!
subtitle: 「 如无必要，勿增实体。」
date: 2025-12-30T10:15:45+08:00
lastmod: 2026-01-02T00:01:26+08:00
draft: false
featuredImagePreview: "surge.png"

authors:
  - yangtudou
description:
tags:
  - surge
series:
  - "www-proxy"
series_weight: 1
seriesNavigation: true
---

时隔将近三年，我又重新用回 Surge。
发现 Surge 的很多优点，以后会和 Clash 系配合着使用。
<!--more-->

## 契机
尽管买了 [Surge][Surge] 快两年了，但工作环境的原因一直用的都是 Clash 系的代理软件，所以也没仔细研究过怎么用这个软件。
契机是正好快年底了，有机会折腾一下家里的 NAS 系统，研究内网穿透的时候，接触到了 [Surge Ponte][Surge Ponte]，
原以为 Surge Ponte  一定要 MacOS，那就又要交一笔费用了。
读文档时发现 Surge Ponte 可以部署在 Apple Tv 上，这不巧了嘛，正好家里有一个在积灰。
重拾 Surge 后，最直观的感受就是**好用**，其实这两个字从我一个 Clash 系的人来说，着实是很奇怪的，
因为这样代表我要同时维护两套配置，但事实确实如此。以后会开篇阐述为什么会这样，这里就允许我买个关子吧。


## 配置
现在我用的配置在[**深港有猫配置**][深港有猫配置]基础上做了修改，当然他的配置很棒，注释写的很详细。
我只是加入了一些私人化的内容，以下为逐段分析我自己用配置，仅作参考。
具体异同，需要大家考虑自己的实际使用情况。

配置文件格式采用 `INI 格式`

{{< admonition type=tip title="注意" open=false >}}
当前配置仅在 ios Surge5 上使用过。
{{< /admonition >}}

### [General]^(全局配置)
#### loglevel
日志级别: warning, notify, info, verbose (默认值: notify)
```conf
loglevel = notify
```

#### skip-proxy
跳过某个域名或者 IP 段，这些目标主机将不会由 Surge Proxy 处理。
```
skip-proxy = 127.0.0.1, 192.168.0.0/16, 10.0.0.0/8, 172.16.0.0/12, 100.64.0.0/10, localhost, *.local
```

#### dns-server
DNS 服务器, 这里之前收到过 Clash DNS 泄露影响, 在配置的时候着重研究了。具体请阅读[Sukka][Sukka]博客内容，受益良多。
```
dns-server = system
```

#### exclude-simple-hostnames
排除简单的主机名
```
exclude-simple-hostnames = true
```

#### udp-policy-not-supported-behaviour
UDP 退回行为
```
udp-policy-not-supported-behaviour = REJECT
```

#### allow-wifi-access
允许 Wi-Fi 访问
```
allow-wifi-access = false
```

### [Proxy Group]^(策略分组)
### [Rule]^(分流规则)



<!-- 链接统一存放 🐈 -->
[Surge]: https://www.nssurge.com/
[Surge Ponte]: https://kb.nssurge.com/surge-knowledge-base/zh/guidelines/ponte
[深港有猫配置]: https://raw.githubusercontent.com/Rabbit-Spec/Surge/Master/Conf/Spec/Surge-EN.cond