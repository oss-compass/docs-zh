---
title: 组织活跃度
slug: /metrics-models/niche-creation/developer-retention
tags:
  - 评估模型
  - 创新力
  - 组织活跃度
description: 评估一个社区中组织的活跃程度。
---

# 组织活跃度

该模型用于评估社区中组织的活跃程度。

# 评估模型中的指标

## 组织数量

* 定义：过去 90 天内活跃的代码提交者所属组织的数目
* 权重：32.258%
* 阈值：30

## 贡献者数量

* 定义：过去 90 天内有组织附属关系的活跃的代码贡献者人数
* 权重：25.806%
* 阈值：300

## 代码提交频率

* 定义：过去 90 天内平均每周有组织归属的代码提交次数。
* 权重：25.81%
* 阈值：800

## 持续贡献

* 定义：在过去 90 天所有组织向社区有代码贡献的累计时间（周）。
* 权重：16.13%
* 阈值：200

# 评估模型算法

## 权重

我们使用 [AHP](https://en.wikipedia.org/wiki/Analytic_hierarchy_process) 来计算每个指标的权重。

### AHP 输入数据

| 指标名称  | 组织数量 | 贡献者数量 | 代码提交频率 | 持续贡献  |
| --- | --- | --- | --- | --- |
| 组织数量  | 1.000 | 1.250 | 1.250 | 2.000 |
| 贡献者数量 | 0.800 | 1.000 | 1.000 | 1.600 |
| 代码提交频率 | 0.800 | 1.000 | 1.000 | 1.600 |
| 持续贡献  | 0.500 | 0.625 | 0.625 | 1.000 |

### AHP 分析结果

| 指标名称  | 特征向量 | 权重      |
| --- | --- | --- |
| 组织数量  | 1.290 | 32.258% |
| 贡献者数量 | 1.032 | 25.806% |
| 代码提交频率 | 1.032 | 25.806% |
| 持续贡献  | 0.645 | 16.129% |

### 一致性检验结果

| 最大特征根 | CI 值 | RI 值 | CR 值 | 一致性检验结果 |
| --- | --- | --- | --- | --- |
| 4.000 | 0.000 | 0.890 | 0.000 | PASS    |

## 阈值

我们选择的阈值是基于不同类型开源项目的大数据观测。

# 参考文献

* [CHAOSS Metric Model: Organizations Activity](https://github.com/chaoss/wg-metrics-models/tree/main/metrics-model-libs/organization-activity)

# 贡献者

## 前端

* Shengxiang Zhang
* Feng Zhong
* Chaoqun Huang
* Huatian Qin
* Xingyou Lai

## 后端

* Yehui Wang
* Shengbao Li
* Huatian Qin

## 评估模型

* Yehui Wang
* Shengbao Li
