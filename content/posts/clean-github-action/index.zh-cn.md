---
title: Clean Github Action
subtitle: 还你 Github Action 出厂般的干净
date: 2025-12-31T22:01:37+08:00
lastmod: 2026-01-01T00:00:00+08:00
description:
featuredImagePreview: "clean-github-action.jpg"
authors:
  - yangtudou
categories:
  - github action
tags:
  - github
  - github action

series: github
series_weight: 0
seriesNavigation: true
---


每次看到自己的 GitHub Action 后台一堆记录，就莫名烦躁。
这个自动删除运行记录的 Action,绝对是强迫症患者的福音。
<!--more-->


## 清理 Workeflows Runs 运行记录
[现成的 action]^([Mattraks/delete-workflow-runs](https://github.com/marketplace/actions/delete-workflow-runs))

### 基础用法
```yaml
name: Delete old workflow runs
on:
  schedule:
    - cron: "0 0 1 * *"
jobs:
  delete-runs:
    runs-on: ubuntu-latest
    permissions:
      actions: write
      contents: read
    steps:
      - name: Delete workflow runs
        uses: Mattraks/delete-workflow-runs@v2
        with:
          token: ${{ github.token }}
          repository: ${{ github.repository }}
          retain_days: 30
          keep_minimum_runs: 6
```

## 清理 Github Pages 部署记录
现成的 action 工作流: [strumwolf/delete-deployment-environment](https://github.com/marketplace/actions/delete-deployment-environment)

### 基础用法
```yaml
cleanup:
  runs-on: ubuntu-latest
  permissions: write-all
  steps:
    - name: Delete deployment
      uses: strumwolf/delete-deployment-environment@v2.3.0
      with:
        token: ${{ secrets.GITHUB_TOKEN }}
        environment: github-pages
        onlyRemoveDeployments: true
```