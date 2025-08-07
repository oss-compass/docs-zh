---
title: Criticality Score
slug: /metrics-models/software_artifact/robustness/criticality_score
tags:
  - 评估模型
  - 软件制品
  - 稳健性
  - Criticality Score
description: 评估开源项目的影响力和重要性的关键性评分模型
---

# Criticality Score



本评估模型参考了[OpenSSF Criticality Score项目](https://github.com/ossf/criticality_score)的实现，用于生成每个开源项目的关键性评分，创建关键项目列表，并利用这些数据主动改善这些关键项目的安全状况。

# 评估模型中的指标

## 创建时间

- 定义：项目创建至今的时间（以月为单位）
- 权重：9.523%
- 阈值：120

较老的项目有更高的机会被广泛使用或被其他项目依赖。

## 更新时间

- 定义：项目最后更新时间至今的时间（以月为单位）
- 权重：-9.523%
- 阈值：120

没有最近提交的未维护项目被依赖的可能性较低。

## 贡献者数量

- 定义：项目贡献者数量（有提交记录的）
- 权重： 19.047%
- 阈值：5000

不同贡献者的参与表明项目的重要性。

## 组织数量

- 定义：贡献者所属的不同组织的数量
- 权重：9.523%
- 阈值：10

表明跨组织依赖关系。

## 提交频率

- 定义：过去一年中平均每周提交次数
- 权重：9.523%
- 阈值：1000

更高的代码变更率略微表明项目的重要性。同时，也更容易受到漏洞影响。

## 最近发布数量

- 定义：过去一年中的发布次数
- 权重：4.761%
- 阈值：26

频繁发布表明用户依赖。权重较低，因为这不总是被使用。

## 关闭问题数量

- 定义：过去90天内关闭的问题数量
- 权重：4.761%
- 阈值：5000

表明高贡献者参与度和对关闭用户问题的关注。权重较低，因为它依赖于项目贡献者。

## 更新问题数量

- 定义：过去90天内更新的问题数量
- 权重：4.761%
- 阈值：5000

表明高贡献者参与度。权重较低，因为它依赖于项目贡献者。

## 评论频率

- 定义：过去90天内每个问题的平均评论数
- 权重：9.523%
- 阈值：15

表明用户活动和依赖关系。

## 依赖者数量

- 定义：提交消息中该项目被其他项目提及的次数
- 权重：19.047%
- 阈值：50

表明仓库使用情况，通常在版本更新中。此参数适用于所有语言。

# 评估模型算法

## 模型权重和阈值

我们使用以下参数来计算开源项目的关键性评分：

| 指标名称 (S<sub>i</sub>)  | 权重 (&alpha;<sub>i</sub>) | 阈值 (T<sub>i</sub>) | 定义 |
|---|---|---|---|
| 创建时间 | 9.523% | 120 | 项目创建至今的时间（以月为单位） |
| 更新时间  | -9.523% | 120 | 项目最后更新时间至今的时间（以月为单位）|
| 贡献者数量 | 19.047% | 5000 | 项目贡献者数量（有提交记录的） |
| 组织数量 | 9.523% | 10 | 贡献者所属的不同组织的数量 |
| 提交频率 | 9.523% | 1000 | 过去一年中平均每周提交次数 |
| 最近发布数量 | 4.761% | 26 | 过去一年中的发布次数 |
| 关闭问题数量 | 4.761% | 5000 | 过去90天内关闭的问题数量 |
| 更新问题数量 | 4.761% | 5000 | 过去90天内更新的问题数量 |
| 评论频率 | 9.523% | 15 | 过去90天内每个问题的平均评论数 
| 依赖者数量 | 19.047% | 50 | 提交消息中该项目被其他项目提及的次数 |

## 评分计算

开源项目的关键性评分定义了项目的影响力和重要性。它是一个介于0（最不关键）和1（最关键）之间的数字。该评分基于[Rob Pike](https://github.com/robpike)提出的[算法](https://github.com/ossf/criticality_score/blob/main/Quantifying_criticality_algorithm.pdf)：

<img src="https://raw.githubusercontent.com/ossf/criticality_score/main/images/formula.png" width="359" height="96" />

其中：
- αi 是每个指标的权重
- Si 是每个指标的实际值
- Ti 是每个指标的最大阈值


# 参考文献

- [OpenSSF Criticality Score](https://github.com/ossf/criticality_score)
- [Quantifying Criticality Algorithm](https://github.com/ossf/criticality_score/blob/main/Quantifying_criticality_algorithm.pdf)
- [Securing Critical Projects WG](https://github.com/ossf/wg-securing-critical-projects)


# 贡献者

## 后端

- Yehui Wang
- Shengbao Li

## 评估模型

- Yehui Wang
- Guoqiang Qi
- Shengbao Li
