---
title: 社区服务与支撑
slug: /metrics-models/productivity/niche-creation
tags:
 - 评估模型
 - 生产力
 - 社区服务与支撑
description: 用于评估开发者在贡献过程中，所能直接感知到社区提供的服务和支撑做得如何。
---

# 社区服务与支撑

用于评估开发者在贡献过程中，所能直接感知到社区提供的服务和支撑做得如何。

# 评估模型中的指标

## 更新 Issue 数量

* 定义：过去 90 天 Issue 更新的数量。
* 权重：19.721%
* 阈值：2000

## 关闭 PR 数量

* 定义：过去 90 天内合并和拒绝的 PR 数量。
* 权重：19.721%
* 阈值：4500

## Issue 首次响应时间

* 定义：过去 90 天新建 Issue 首次响应时间的均值和中位数（天）。这不包括机器人响应、创建者自己的评论或 Issue 的分配动作（action）。如果 Issue 一直未被响应，该 Issue 不被算入统计。
* 权重：14.372%
* 阈值：15 天

## Bug 类 Issue 处理时间

* 定义：过去 90 天新建的 Bug 类 Issue 处理时间的均值和中位数（天），包含已经关闭的 Issue 以及未解决的 Issue。
* 权重：12.88%
* 阈值：60 天
* 注：标记为 Bug 类的 Issue。

## PR 处理时间

* 定义：过去 90 天新建 PR 的处理时间的均值和中位数（天），包含已经关闭的 PR 以及未解决的 PR
* 权重：12.88%
* 阈值：30 天

## Issue 评论频率

* 定义：过去 90 天内新建 Issue 的评论平均数（不包含机器人和 Issue 作者本人评论）。
* 权重：10.217%
* 阈值：5

## 代码审查评论频率

* 定义：过去 90 天内新建 PR 的评论平均数量（不包含机器人和 PR 作者本人评论）。
* 权重：10.217%
* 阈值：8

# 评估模型算法

## 权重

我们使用 [AHP](https://en.wikipedia.org/wiki/Analytic_hierarchy_process) 来计算每个指标的权重。

### AHP 输入数据

| 指标名称 | 更新 Issue 数量 | 关闭 PR 数量 | Issue 首次响应时间 | Bug 类 Issue 处理时间 | PR 处理时间 | Issue 评论频率 | 代码审查评论频率 |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 更新 Issue 数量 | 1.000 | 1.000 | 1.333 | 1.500 | 1.500 | 2.000 | 2.000 |
| 关闭 PR 数量 | 1.000 | 1.000 | 1.333 | 1.500 | 1.500 | 2.000 | 2.000 |
| Issue 首次响应时间 | 0.750 | 0.750 | 1.000 | 1.143 | 1.143 | 1.333 | 1.333 |
| Bug 类 Issue 处理时间 | 0.667 | 0.667 | 0.875 | 1.000 | 1.000 | 1.250 | 1.250 |
| PR 处理时间 | 0.667 | 0.667 | 0.875 | 1.000 | 1.000 | 1.250 | 1.250 |
| Issue 评论频率 | 0.500 | 0.500 | 0.750 | 0.800 | 0.800 | 1.000 | 1.000 |
| 代码审查评论频率 | 0.500 | 0.500 | 0.750 | 0.800 | 0.800 | 1.000 | 1.000 |

### AHP 分析结果

| 指标名称 | 特征向量 | 权重 |
| --- | --- | --- |
| 更新 Issue 数量 | 1.380 | 19.721% |
| 关闭 PR 数量 | 1.380 | 19.721% |
| Issue 首次响应时间 | 1.006 | 14.372% |
| Bug 类 Issue 处理时间 | 0.901 | 12.876% |
| PR 处理时间 | 0.901 | 12.876% |
| Issue 评论频率 | 0.715 | 10.217% |
| 代码审查评论频率 | 0.715 | 10.217% |

### 一致性检验结果

| 最大特征根 | CI 值 | RI 值 | CR 值 | 一致性检验结果 |
| --- | --- | --- | --- | --- |
| 7.002 | 0.000 | 1.360 | 1.360 | PASS |

## 阈值

我们选择的阈值是基于不同类型开源项目的大数据观测。

# 参考文献

* [CHAOSS Metric Model: Community Service and Support](https://github.com/chaoss/wg-metrics-models/tree/main/metrics-model-libs/community-service-and-support)

# 贡献者

## 前端

* Shengxiang Zhang
* Feng Zhong
* Chaoqun Huang
* Huatian Qin
* Xingyou Lai

## 后端

* Yehui Wang
* Chenqi Shan
* Shengbao Li
* Huatian Qin

## 评估模型

* Yehui Wang
* Liang Wang
* Chenqi Shan
* Shengbao Li
* Matt Germonprez
* Sean Goggins
