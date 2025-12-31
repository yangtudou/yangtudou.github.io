---
title: Github Action Clean
slug: github-action-clean
date: 2025-12-31T22:01:37+08:00
lastmod: 2025-12-31T22:01:37+08:00
description: 绝对是强迫症患者的福音。
summary: 让 GitHub Action 恢复出厂般干净。
dropCap: false
indent: false
indentFirstParagraph: true
toc: false
tags:
  - github
  - github action
---


>  每次看到自己的 GitHub Action 后台一堆记录，就莫名烦躁。


## 清理 Workeflows Runs 运行记录
有现成的 github action 流程: [Mattraks/delete-workflow-runs](https://github.com/marketplace/actions/delete-workflow-runs)

### 基础用法
```yaml
name: Delete old workflow runs
on:
  schedule:
    - cron: "0 0 1 * *" # Monthly at 00:00 on the 1st
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