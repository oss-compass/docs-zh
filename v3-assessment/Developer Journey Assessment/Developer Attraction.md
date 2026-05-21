# 开发者吸引

定义：评估社区吸引新开发者加入的能力，反映社区的吸引力和新人友好程度。

# 评估模型

**开发者吸引**

| 度量指标                 | 地址                                                         | 阈值   | 权重 |
| ------------------------ | ------------------------------------------------------------ | ------ | ---- |
| 新增组织数               | [/api/v3/developer_attraction/new_org_count](https://oss-compass.org/dataHub#api_v3_developer_attraction_new_org_count) | 10 个  | 0.20 |
| 新增组织代码开发者数量   | [/api/v3/developer_attraction/new_org_code_contributors](https://oss-compass.org/dataHub#api_v3_developer_attraction_new_org_code_contributors) | 50 个  | 0.20 |
| 新增组织非代码开发者数量 | [/api/v3/developer_attraction/new_org_non_code_contributors](https://oss-compass.org/dataHub#api_v3_developer_attraction_new_org_non_code_contributors) | 50 个  | 0.20 |
| 新增个人代码开发者数量   | [/api/v3/developer_attraction/new_individual_code_contributors](https://oss-compass.org/dataHub#api_v3_developer_attraction_new_individual_code_contributors) | 100 个 | 0.20 |
| 新增个人非代码开发者数量 | [/api/v3/developer_attraction/new_individual_non_code_contributors](https://oss-compass.org/dataHub#api_v3_developer_attraction_new_individual_non_code_contributors) | 100 个 | 0.20 |

# 评估模型中的指标

## 新增组织数

- 定义：统计周期内新加入社区参与贡献的组织数量。
- 权重：20%
- 阈值：10个

组织参与是开源社区成熟度的重要标志。新增组织数反映了社区对企业、研究机构等组织的吸引力。组织的加入不仅带来更多的资源投入，还能提升项目的可持续发展能力。该指标帮助我们了解社区在组织层面的扩张速度。

## 新增组织代码开发者数量

- 定义：统计周期内新加入的组织代码贡献者数量。
- 权重：20%
- 阈值：50个

组织代码开发者是推动项目技术发展的核心力量。新增组织代码开发者数量反映了组织对项目的投入程度和参与意愿。这些开发者通常具有专业的技术背景和资源支持，他们的加入能够显著提升项目的技术实力和代码质量。

## 新增组织非代码开发者数量

- 定义：统计周期内新加入的组织非代码贡献者数量。
- 权重：20%
- 阈值：50个

非代码贡献包括文档编写、社区运营、测试、设计等多种形式。新增组织非代码开发者数量反映了组织对项目的全方位支持。非代码贡献者虽然不直接参与代码开发，但对项目的文档完善、用户体验提升、社区建设等方面起着重要作用。

## 新增个人代码开发者数量

- 定义：统计周期内新加入的个人代码贡献者数量。
- 权重：20%
- 阈值：100个

个人代码开发者是开源社区的基础力量。新增个人代码开发者数量反映了社区对独立开发者的吸引力。这些开发者可能来自不同背景，他们的多样化视角和贡献能够丰富项目的技术生态。保持个人开发者的持续流入是社区活力的重要保障。

## 新增个人非代码开发者数量

- 定义：统计周期内新加入的个人非代码贡献者数量。
- 权重：20%
- 阈值：100个

个人非代码贡献者是社区多元化的重要组成部分。新增个人非代码开发者数量反映了社区对不同类型贡献者的包容性。这些贡献者可能参与翻译、文档改进、社区活动组织等工作，他们的参与降低了贡献门槛，扩大了社区的参与面。

# 评估模型算法

## 权重

各指标权重采用均分方式分配，每个指标权重为 20%。

## 阈值

我们选择的阈值是基于不同类型开源项目的大数据观测。
