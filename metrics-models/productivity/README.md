---
title: 生产力
slug: /dimensions-define/productivity
tags:
 - 评估模型
 - 生产力
description: 一个开源生态将投入转化为产出的能力。
---

# 生产力

定义：一个开源生态将投入转化为产出的能力。

# 评估模型

## [开发协作管理](./collaboration-development-index.md)

| 指标名称 | 定 义 | 阈值 | 权重 |
| --- | --- | --- | --- |
| [代码参与者数量](./collaboration-development-index.md#代码参与者数量) | 确定在过去 90 天内有多少活跃的代码提交者、代码审核者和 PR 提交者。 | 1000 | 19.987% |
| [代码提交频率](./collaboration-development-index.md#代码提交频率) | 过去 90 天内平均每周代码提交次数。 | 1000 | 16.363% |
| [是否维护](./collaboration-development-index.md#是否维护) | 在过去 90 天内至少提交了一次代码的周百分比 (单仓场景)。在过去 30 天内至少有一次代码提交记录的的代码仓百分比 (多仓场景)。 | 100% | 13.853% |
| [代码提交关联 PR 的比率](./collaboration-development-index.md#commit-pr-linked-ratio) | 在过去 90 天内提交的代码链接 PR 的百分比。 | 100% | 12.612% |
| [PR 关联 Issue 的比率](./collaboration-development-index.md#代码提交关联-pr-的比率) | 确定过去 90 天内新建 PR 关联 Issue 的百分比。 | 100% | 11.319% |
| [代码审查比率](./collaboration-development-index.md#代码审查比率) | 确定在过去 90 天内提交代码中，至少包含一名审核者 (不是 PR 创建者) 的百分比。 | 100% | 10.113% |
| [代码合并比率](./collaboration-development-index.md#代码合并比率) | 过去 90 天提交代码中，PR 合并者和 PR 作者不属于同一人的百分比。 | 100% | 10.113% |
| [代码行数](./collaboration-development-index.md#代码行数) | 确定在过去 90 天内平均每周提交的代码行数 (增加行数加上删除行数)。 | 300000 | 5.640% |

## [社区服务与支撑](./community-service-and-support.md#community-service-and-support)

| 指标名称 | 定 义 | 阈值 | 权重 |
| --- | --- | --- | --- |
| [更新 Issue 数量](./community-service-and-support.md#更新-issue-数量) | 过去 90 天 Issue 更新的数量。 | 2000 | 19.721% |
| [关闭 PR 数量](./community-service-and-support.md#关闭-pr-数量) | 过去 90 天内合并和拒绝的 PR 数量。 | 4500 | 19.721% |
| [Issue 首次响应时间](./community-service-and-support.md#issue-首次响应时间) | 过去 90 天新建 Issue 首次响应时间的均值和中位数（天）。这不包括机器人响应、创建者自己的评论或 Issue 的分配动作（action）。如果 Issue 一直未被响应，该 Issue 不被算入统计。 | 15 | 14.372% |
| [Bug 类 Issue 处理时间](./community-service-and-support.md#bug-类-issue-处理时间) | 过去 90 天新建的 Bug 类 Issue 处理时间的均值和中位数（天），包含已经关闭的 Issue 以及未解决的 Issue。 | 60 | 12.876% |
| [PR 处理时间](./community-service-and-support.md#pr-处理时间) | 过去 90 天新建 PR 的处理时间的均值和中位数（天），包含已经关闭的 PR 以及未解决的 PR | 30 | 12.876% |
| [Issue 评论频率](./community-service-and-support.md#issue-评论频率) | 过去 90 天内新建 Issue 的评论平均数（不包含机器人和 Issue 作者本人评论）。 | 5 | 10.217% |
| [代码审查评论频率](./community-service-and-support.md#代码审查评论频率) | 过去 90 天内新建 PR 的评论平均数量（不包含机器人和 PR 作者本人评论）。 | 8 | 10.217% |

## [代码安全保障](./code/code-security-guarantee.md#code-security-guarantee)

即将推出！

## [代码合规保障](./code/code-compliance-guarantee.md#code-compliance-guarantee)

即将推出！

## [文档](./content.md#content)

即将推出！