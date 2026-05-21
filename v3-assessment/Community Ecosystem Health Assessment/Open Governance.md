# 开放治理

定义：评估社区的治理开放性和包容性，反映社区的治理成熟度和多元化程度。

# 评估模型

**组织开放治理**

| 度量指标           | 地址                                                         | 阈值   | 权重 |
| ------------------ | ------------------------------------------------------------ | ------ | ---- |
| 参与治理的组织个数 | [/api/v3/organizational_governance/governance_orgs_by_period](https://oss-compass.org/dataHub#api_v3_organizational_governance_governance_orgs_by_period) | 5 个   | 0.33 |
| 组织管理者数量     | [/api/v3/organizational_governance/org_managers_by_period](https://oss-compass.org/dataHub#api_v3_organizational_governance_org_managers_by_period) | 20 个  | 0.33 |
| 组织管理者数量占比 | [/api/v3/organizational_governance/org_managers_ratio_by_period](https://oss-compass.org/dataHub#api_v3_organizational_governance_org_managers_ratio_by_period) | 1 占比 | 0.33 |

**个人开放治理**

| 度量指标           | 地址                                                         | 阈值   | 权重 |
| ------------------ | ------------------------------------------------------------ | ------ | ---- |
| 个人管理者数量     | [/api/v3/personal_governance/individual_managers_by_period](https://oss-compass.org/dataHub#api_v3_personal_governance_individual_managers_by_period) | 10 个  | 0.5  |
| 个人管理者数量占比 | [/api/v3/personal_governance/individual_managers_ratio_by_period](https://oss-compass.org/dataHub#api_v3_personal_governance_individual_managers_ratio_by_period) | 1 占比 | 0.5  |

# 评估模型中的指标

## 组织开放治理

组织开放治理模型关注组织在社区治理中的参与程度，反映社区的组织多元化和治理开放性。

### 参与治理的组织个数

- 定义：统计周期内参与社区治理的组织数量。
- 权重：33%
- 阈值：5个

参与治理的组织个数反映了社区的组织多元化程度。多个组织参与治理能够避免单一组织垄断决策，保证社区的中立性和可持续发展。该指标是评估社区开放治理的重要标志。

### 组织管理者数量

- 定义：统计周期内来自组织的管理者数量。
- 权重：33%
- 阈值：20个

组织管理者数量反映了组织在社区治理中的投入程度。组织管理者通常具有丰富的项目经验和资源支持，他们的参与能够提升社区治理的专业性和效率。该指标能够反映组织对社区治理的重视程度。

### 组织管理者数量占比

- 定义：统计周期内组织管理者占总管理者数量的比例。
- 权重：33%
- 阈值：1占比（100%）

组织管理者数量占比反映了组织在社区治理中的影响力。适度的组织管理者占比能够保证社区的专业性和资源支持，但过高的占比可能导致社区治理过于依赖组织，影响社区的独立性和中立性。

## 个人开放治理

个人开放治理模型关注个人在社区治理中的参与程度，反映社区的个人参与度和治理包容性。

### 个人管理者数量

- 定义：统计周期内个人管理者的数量。
- 权重：50%
- 阈值：10个

个人管理者数量反映了社区对个人贡献者的认可和培养。个人管理者通常凭借个人能力和贡献获得治理权限，他们的参与能够保证社区的多元化和活力。该指标能够反映社区的个人参与度和治理包容性。

### 个人管理者数量占比

- 定义：统计周期内个人管理者占总管理者数量的比例。
- 权重：50%
- 阈值：1占比（100%）

个人管理者数量占比反映了个人在社区治理中的影响力。适度的个人管理者占比能够保证社区的独立性和中立性，避免组织过度控制。该指标能够反映社区的治理开放性和个人参与度。

# 评估模型算法

## 权重

各指标权重采用均分方式分配。

### 组织开放治理

3个指标采用均分方式分配，每个指标权重约为 33.33%。

### 个人开放治理

2个指标采用均分方式分配，每个指标权重为 50%。

## 阈值

我们选择的阈值是基于不同类型开源项目的大数据观测。
