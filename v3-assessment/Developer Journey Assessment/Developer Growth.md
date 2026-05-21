# 开发者成长

定义：评估社区培养开发者从新手成长为核心贡献者的能力，反映社区的人才培养机制和成长路径。

# 评估模型

**开发者参与度分层**

| 度量指标                            | 地址                                                         | 阈值   | 权重 |
| ----------------------------------- | ------------------------------------------------------------ | ------ | ---- |
| 组织代码核心开发者（含管理者）数量  | [/api/v3/participation_tier/org_code_core_contributors](https://oss-compass.org/dataHub#api_v3_participation_tier_org_code_core_contributors) | 50 个  | 0.08 |
| 组织Issue核心开发者（含管理者）数量 | [/api/v3/participation_tier/org_issue_core_contributors](https://oss-compass.org/dataHub#api_v3_participation_tier_org_issue_core_contributors) | 50 个  | 0.08 |
| 组织代码常客开发者数量              | [/api/v3/participation_tier/org_code_regular_contributors](https://oss-compass.org/dataHub#api_v3_participation_tier_org_code_regular_contributors) | 100 个 | 0.08 |
| 组织Issue常客开发者数量             | [/api/v3/participation_tier/org_issue_regular_contributors](https://oss-compass.org/dataHub#api_v3_participation_tier_org_issue_regular_contributors) | 100 个 | 0.08 |
| 组织代码访客开发者数量              | [/api/v3/participation_tier/org_code_visitor_contributors](https://oss-compass.org/dataHub#api_v3_participation_tier_org_code_visitor_contributors) | 200 个 | 0.08 |
| 组织Issue访客开发者数量             | [/api/v3/participation_tier/org_issue_visitor_contributors](https://oss-compass.org/dataHub#api_v3_participation_tier_org_issue_visitor_contributors) | 200 个 | 0.08 |
| 个人代码核心开发者（含管理者）数量  | [/api/v3/participation_tier/individual_code_core_contributors](https://oss-compass.org/dataHub#api_v3_participation_tier_individual_code_core_contributors) | 100 个 | 0.08 |
| 个人Issue核心开发者（含管理者）数量 | [/api/v3/participation_tier/individual_issue_core_contributors](https://oss-compass.org/dataHub#api_v3_participation_tier_individual_issue_core_contributors) | 100 个 | 0.08 |
| 个人代码常客开发者数量              | [/api/v3/participation_tier/individual_code_regular_contributors](https://oss-compass.org/dataHub#api_v3_participation_tier_individual_code_regular_contributors) | 200 个 | 0.08 |
| 个人Issue常客开发者数量             | [/api/v3/participation_tier/individual_issue_regular_contributors](https://oss-compass.org/dataHub#api_v3_participation_tier_individual_issue_regular_contributors) | 200 个 | 0.08 |
| 个人代码访客开发者数量              | [/api/v3/participation_tier/individual_code_visitor_contributors](https://oss-compass.org/dataHub#api_v3_participation_tier_individual_code_visitor_contributors) | 300 个 | 0.09 |
| 个人Issue访客开发者数量             | [/api/v3/participation_tier/individual_issue_visitor_contributors](https://oss-compass.org/dataHub#api_v3_participation_tier_individual_issue_visitor_contributors) | 300 个 | 0.09 |



**开发者晋升**

| 度量指标                    | 地址                                                         | 阈值  | 权重 |
| --------------------------- | ------------------------------------------------------------ | ----- | ---- |
| 组织代码核心晋升数量        | [/api/v3/developer_promotion/org_code_core_promotion_count](https://oss-compass.org/dataHub#api_v3_developer_promotion_org_code_core_promotion_count) | 10 个 | 0.25 |
| 组织Issue核心晋升数量       | [/api/v3/developer_promotion/org_issue_core_promotion_count](https://oss-compass.org/dataHub#api_v3_developer_promotion_org_issue_core_promotion_count) | 10 个 | 0.25 |
| 个人代码核心晋升数量        | [/api/v3/developer_promotion/individual_code_core_promotion_count](https://oss-compass.org/dataHub#api_v3_developer_promotion_individual_code_core_promotion_count) | 10 个 | 0.25 |
| 个人Issue核心开发者晋升数量 | [/api/v3/developer_promotion/individual_issue_core_promotion_count](https://oss-compass.org/dataHub#api_v3_developer_promotion_individual_issue_core_promotion_count) | 10 个 | 0.25 |

# 评估模型中的指标

## 开发者参与度分层

开发者参与度分层模型将社区贡献者分为三个层次：核心贡献者、常客贡献者和访客贡献者。这种分层有助于了解社区的人才结构，识别关键贡献者，并制定针对性的培养策略。

### 组织代码核心开发者（含管理者）数量

- 定义：统计周期内组织代码核心贡献者（含管理者）的数量。
- 权重：8%
- 阈值：50个

组织代码核心开发者是项目技术方向的主要决策者和实施者。他们通常具有深厚的项目理解和技术能力，负责核心功能的开发和代码审查。该指标反映了组织在项目技术层面的深度参与程度。

### 组织Issue核心开发者（含管理者）数量

- 定义：统计周期内组织Issue核心贡献者（含管理者）的数量。
- 权重：8%
- 阈值：50个

组织Issue核心开发者在问题跟踪、需求管理和社区沟通方面发挥重要作用。他们不仅处理技术问题，还参与社区讨论和决策。该指标反映了组织在社区管理和沟通方面的投入。

### 组织代码常客开发者数量

- 定义：统计周期内组织代码常客贡献者的数量。
- 权重：8%
- 阈值：100个

组织代码常客开发者是项目的稳定贡献者，他们定期参与代码贡献，但参与深度不如核心开发者。他们是核心开发者的后备力量，是社区持续发展的重要支撑。

### 组织Issue常客开发者数量

- 定义：统计周期内组织Issue常客贡献者的数量。
- 权重：8%
- 阈值：100个

组织Issue常客开发者定期参与Issue讨论和处理，为社区提供持续的问题反馈和解决方案。他们的参与保证了社区问题的及时响应和处理。

### 组织代码访客开发者数量

- 定义：统计周期内组织代码访客贡献者的数量。
- 权重：8%
- 阈值：200个

组织代码访客开发者是偶尔参与代码贡献的开发者。他们可能是初次贡献者或临时参与者。该指标反映了社区对新贡献者的吸引力和包容性。

### 组织Issue访客开发者数量

- 定义：统计周期内组织Issue访客贡献者的数量。
- 权重：8%
- 阈值：200个

组织Issue访客开发者偶尔参与Issue讨论和反馈。他们的参与虽然不频繁，但为社区带来了多样化的视角和反馈。

### 个人代码核心开发者（含管理者）数量

- 定义：统计周期内个人代码核心贡献者（含管理者）的数量。
- 权重：8%
- 阈值：100个

个人代码核心开发者是独立贡献者中的骨干力量。他们不依赖组织支持，凭借个人热情和专业能力为项目做出持续贡献。该指标反映了社区对个人贡献者的吸引力和培养能力。

### 个人Issue核心开发者（含管理者）数量

- 定义：统计周期内个人Issue核心贡献者（含管理者）的数量。
- 权重：8%
- 阈值：100个

个人Issue核心开发者在社区沟通和问题管理方面发挥重要作用。他们的持续参与保证了社区问题的及时响应和有效解决。

### 个人代码常客开发者数量

- 定义：统计周期内个人代码常客贡献者的数量。
- 权重：8%
- 阈值：200个

个人代码常客开发者是项目的稳定贡献者。他们定期参与代码贡献，是社区持续发展的重要力量，也是核心开发者的潜在候选人。

### 个人Issue常客开发者数量

- 定义：统计周期内个人Issue常客贡献者的数量。
- 权重：8%
- 阈值：200个

个人Issue常客开发者定期参与Issue讨论和处理，为社区提供持续的问题反馈和解决方案。

### 个人代码访客开发者数量

- 定义：统计周期内个人代码访客贡献者的数量。
- 权重：9%
- 阈值：300个

个人代码访客开发者是偶尔参与代码贡献的开发者。他们可能是初次贡献者或临时参与者。该指标反映了社区对新贡献者的吸引力和包容性。

### 个人Issue访客开发者数量

- 定义：统计周期内个人Issue访客贡献者的数量。
- 权重：9%
- 阈值：300个

个人Issue访客开发者偶尔参与Issue讨论和反馈。他们的参与为社区带来了多样化的视角和反馈。

## 开发者晋升

开发者晋升模型关注开发者从低层次向高层次晋升的情况，反映社区的人才培养效果。

### 组织代码核心晋升数量

- 定义：统计周期内组织代码开发者晋升为核心贡献者的数量。
- 权重：25%
- 阈值：10个

组织代码核心晋升数量反映了组织对开发者的培养能力。成功的晋升机制能够激励开发者持续贡献，提升项目的技术实力。

### 组织Issue核心晋升数量

- 定义：统计周期内组织Issue开发者晋升为核心贡献者的数量。
- 权重：25%
- 阈值：10个

组织Issue核心晋升数量反映了组织在社区管理和沟通人才培养方面的成效。这些晋升的开发者在社区治理中发挥重要作用。

### 个人代码核心晋升数量

- 定义：统计周期内个人代码开发者晋升为核心贡献者的数量。
- 权重：25%
- 阈值：10个

个人代码核心晋升数量反映了社区对个人贡献者的培养能力。成功的晋升机制能够激励个人开发者持续贡献，增强社区的活力。

### 个人Issue核心开发者晋升数量

- 定义：统计周期内个人Issue开发者晋升为核心贡献者的数量。
- 权重：25%
- 阈值：10个

个人Issue核心开发者晋升数量反映了社区在社区管理和沟通人才培养方面的成效。

# 评估模型算法

## 权重

各指标权重采用均分方式分配。

### 开发者参与度分层

12个指标采用均分方式分配，每个指标权重约为 8.33%。

### 开发者晋升

4个指标采用均分方式分配，每个指标权重为 25%。

## 阈值

我们选择的阈值是基于不同类型开源项目的大数据观测。
