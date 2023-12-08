---
title: 贡献者里程
slug: /metrics-models/people/productivity/contributor-milestone-persona
tags:
  - 评估模型
  - 贡献者
  - 生产力
  - 贡献者里程
description: 
---

# 贡献者里程模型

贡献者可能基于上下游生态利益或个人发展等原因与开源项目产生共鸣，并进入社区参与贡献。他们可能长期留在社区，逐渐淡出，甚至再次被唤醒。基于这些情况，我们定义了贡献者在社区中的多种状态，构成了里程画像。这个模型受到状态机的启发，每个状态之间可以相互迁移，而贡献者同时只能处于一种状态。这样做可以确保行为的解耦，更有利于观察贡献者在社区中的行为。

 ![image](https://github.com/oss-compass/docs-zh/assets/53640896/b4313e7c-95c2-4ef2-ad13-ecc009ee5672)

我们根据贡献者在社区的贡献量、贡献频率、贡献类型以及他们的状态，将贡献者里程在考虑时间周期的同时，划分为如上5种状态：无状态、访客、常客、核心以及静默。以年度为例，这里给出五种状态的定义：
- 核心： 指贡献者在本年度完成了所有领域贡献的50%（不包括观察者类贡献，如star、fork、watch）。这些贡献由最少得一组人完成，该组人被称为核心贡献者。所有领域贡献不进行加权处理，只统计次数。
- 常客：排除核心贡献者所贡献的50%之后，接下来的30%贡献（不包括观察者类贡献，如star、fork、watch），由至少一组人完成。这些人及在本年度中至少参与了9个月的贡献，被称为常客贡献者。
- 访客：排除核心、常客贡献后，参与社区剩余贡献的人（包含观察者类贡献，即star、fork、watch），称之为访客。
- 静默：本年度之前活跃的核心、常客或者访客，本年度没有任何贡献的人。
- 无状态：从未在本社区做出贡献的人。


# 评估模型中的指标

## 核心贡献者数量

- 定义：在过去90天内有多少活跃的核心贡献者数量。
- 权重：20%
- 阈值：20

## 核心贡献次数

- 定义：在过去90天内活跃核心贡献者的人均贡献次数。
- 权重：30%
- 阈值：200

## 常客贡献者数量

- 定义：在过去90天内有多少活跃的常客贡献者数量。
- 权重：12%
- 阈值：100

## 常客贡献次数

- 定义：在过去90天内活跃常客贡献者的人均贡献次数。
- 权重：18%
- 阈值：25

  
## 访客贡献者数量

- 定义：在过去90天内有多少活跃的访客贡献者数量。
- 权重：8%
- 阈值：2000

## 访客贡献次数

- 定义：在过去90天内活跃访客贡献者的人均贡献次数。
- 权重：12%
- 阈值：5


# 评估模型算法

## 权重

我们使用 [AHP](https://en.wikipedia.org/wiki/Analytic_hierarchy_process) 来计算每个指标的权重。

### AHP 输入数据

| 指标名称  | 核心贡献者数量 | 核心贡献次数 | 常客贡献者数量 | 常客贡献次数  | 访客贡献者数量 | 访客贡献次数  |
| --- | --- | --- | --- | --- | --- | --- |
| 核心贡献者数量 | 1.000 | 0.667 | 1.667 | 1.111 | 2.500 | 1.667 |
| 核心贡献次数 | 1.500 | 1.000 | 2.500 | 1.667 | 3.750 | 2.500 |
| 常客贡献者数量 | 0.600 | 0.400 | 1.000 | 0.667 | 1.500 | 1.000 |
| 常客贡献次数 | 0.900 | 0.600 | 1.500 | 1.000 | 2.250 | 1.500 |
| 访客贡献者数量 | 0.400 | 0.267 | 0.667 | 0.444 | 1.000 | 0.667 |
| 访客贡献次数 | 0.600 | 0.400 | 1.000 | 0.667 | 1.500 | 1.000 |

### AHP 分析结果

| 指标名称  | 特征向量 | 权重      |
| --- | --- | --- |
| 核心贡献者数量 | 1.200 | 20.000% |
| 核心贡献次数 | 1.800 | 30.000% |
| 常客贡献者数量 | 0.720 | 12.000% |
| 常客贡献次数 | 1.080 | 18.000% |
| 访客贡献者数量 | 0.480 | 8.000% |
| 访客贡献次数 | 0.720 | 12.000% |

### 一致性检验结果

| 最大特征根 | CI 值 | RI 值 | CR 值 | 一致性检验结果 |
| --- | --- | --- | --- | --- |
| 6.000 | 0.000 | 1.260 | 0.000 | PASS    |

## 阈值

我们选择的阈值是基于不同类型开源项目的大数据观测。

# 参考文献

* [开源生态评估与度量的思考（一）——演进与趋势](https://mp.weixin.qq.com/s/7vUUPgrfRpSUasZdQLRAhA) 
* [开源生态评估与度量的思考（二）——评估体系的多维空间](https://mp.weixin.qq.com/s/ZEcphoxPVTux5_0J7JMxqA) 
* [开源生态评估与度量的思考（三）——贡献者的动与静](https://mp.weixin.qq.com/s/MDzUmOPgzBRaPMDnKlhaRw) 

# 贡献者

## 前端

* Shengxiang Zhang
* Feng Zhong
* Xingyou Lai

## 后端

* Yehui Wang
* Shengxiang Zhang
* Shengbao Li
* Huatian Qin

## 评估模型

* Yehui Wang
* Liang Wang
* Shengbao Li