# 社区活力

定义：评估社区的活跃程度和吸引力，反映社区的生命力和发展潜力。

# 评估模型

**社区流行度**

| 度量指标      | 地址                                                         | 阈值 | 权重 |
| ------------- | ------------------------------------------------------------ | ---- | ---- |
| 项目Stars新增 | [/api/v3/community_popularity/stars](https://oss-compass.org/dataHub#api_v3_community_popularity_stars) | 100  | 0.50 |
| 项目Forks新增 | [/api/v3/community_popularity/forks](https://oss-compass.org/dataHub#api_v3_community_popularity_forks) | 100  | 0.50 |

**贡献活跃度**

| 度量指标       | 地址                                                         | 阈值      | 权重 |
| -------------- | ------------------------------------------------------------ | --------- | ---- |
| 代码提交次数   | [/api/v3/contribution_activity/commit_count](https://oss-compass.org/dataHub#api_v3_contribution_activity_commit_count) | 12850 个  | 0.20 |
| 新增代码行数   | [/api/v3/contribution_activity/lines_of_code_change](https://oss-compass.org/dataHub#api_v3_contribution_activity_lines_of_code_change) | 300000 个 | 0.20 |
| PR 评论数量    | [/api/v3/contribution_activity/pr_comment_count](https://oss-compass.org/dataHub#api_v3_contribution_activity_pr_comment_count) | 10 个     | 0.20 |
| Issue 建立数量 | [/api/v3/contribution_activity/new_issue_count](https://oss-compass.org/dataHub#api_v3_contribution_activity_new_issue_count) | 10 个     | 0.20 |
| Issue 评论数量 | [/api/v3/contribution_activity/issue_comment_count](https://oss-compass.org/dataHub#api_v3_contribution_activity_issue_comment_count) | 10 个     | 0.20 |

**开发者基数**

| 度量指标         | 地址                                                         | 阈值    | 权重 |
| ---------------- | ------------------------------------------------------------ | ------- | ---- |
| 社区贡献者数量   | [/api/v3/developer_base/contributor_count](https://oss-compass.org/dataHub#api_v3_developer_base_contributor_count) | 2000 个 | 0.33 |
| 代码贡献者数量   | [/api/v3/developer_base/code_contributor_count](https://oss-compass.org/dataHub#api_v3_developer_base_code_contributor_count) | 1000 个 | 0.33 |
| 非代码贡献者数量 | [/api/v3/developer_base/non_code_contributor_count](https://oss-compass.org/dataHub#api_v3_developer_base_non_code_contributor_count) | 1000 个 | 0.34 |

# 评估模型中的指标

## 社区流行度

社区流行度模型关注项目在开发者社区中的知名度和关注度，反映项目的市场影响力。

### 项目Stars新增

- 定义：统计周期内项目新增的Stars数量。
- 权重：50%
- 阈值：100个

Stars数量是衡量项目受欢迎程度的直观指标。新增Stars数量反映了项目在开发者社区中的关注度和吸引力。持续增长的Stars数量表明项目具有良好的市场影响力和用户基础。

### 项目Forks新增

- 定义：统计周期内项目新增的Forks数量。
- 权重：50%
- 阈值：100个

Forks数量反映了开发者对项目的参与意愿。新增Forks数量表明开发者对项目感兴趣，希望基于项目进行二次开发或贡献代码。这是评估项目活跃度和开发者参与度的重要指标。

## 贡献活跃度

贡献活跃度模型关注社区的贡献频率和规模，反映社区的活跃程度。

### 代码提交次数

- 定义：统计周期内代码提交的总次数。
- 权重：20%
- 阈值：12850个

代码提交次数是衡量项目开发活跃度的核心指标。高频次的代码提交表明项目处于积极开发状态，社区贡献者持续投入。该指标反映了项目的整体工作量和发展速度。

### 新增代码行数

- 定义：统计周期内新增和修改的代码行数总和。
- 权重：20%
- 阈值：300000行

新增代码行数反映了项目的代码贡献规模。虽然代码行数不能直接衡量代码质量，但它能够反映社区的开发投入程度。持续增长的代码行数表明项目在不断演进和完善。

### PR 评论数量

- 定义：统计周期内PR评论的总数量。
- 权重：20%
- 阈值：10个

PR评论数量反映了社区的代码审查活跃度。积极的PR评论表明社区重视代码质量和协作开发。该指标能够反映社区的协作氛围和技术交流深度。

### Issue 建立数量

- 定义：统计周期内新建Issue的总数量。
- 权重：20%
- 阈值：10个

Issue建立数量反映了社区的问题反馈活跃度。新建的Issue包括Bug报告、功能需求、使用咨询等多种类型。该指标能够反映用户对项目的关注程度和参与意愿。

### Issue 评论数量

- 定义：统计周期内Issue评论的总数量。
- 权重：20%
- 阈值：10个

Issue评论数量反映了社区的问题讨论活跃度。积极的Issue评论表明社区具有良好的沟通氛围和问题解决能力。该指标能够反映社区的协作效率和用户支持质量。

## 开发者基数

开发者基数模型关注社区的贡献者规模，反映社区的人才基础。

### 社区贡献者数量

- 定义：统计周期内参与社区贡献的总人数。
- 权重：33%
- 阈值：2000个

社区贡献者数量是衡量社区规模的核心指标。贡献者包括代码贡献者和非代码贡献者，反映了社区的参与广度。大规模的贡献者基础是社区可持续发展的重要保障。

### 代码贡献者数量

- 定义：统计周期内参与代码贡献的人数。
- 权重：33%
- 阈值：1000个

代码贡献者数量反映了社区的技术贡献能力。代码贡献者是推动项目技术发展的核心力量。该指标能够反映项目的技术吸引力和开发活跃度。

### 非代码贡献者数量

- 定义：统计周期内参与非代码贡献的人数。
- 权重：34%
- 阈值：1000个

非代码贡献者数量反映了社区的多元化参与程度。非代码贡献包括文档编写、翻译、测试、设计、社区运营等多种形式。该指标能够反映社区的包容性和参与门槛。

# 评估模型算法

## 权重

各指标权重采用均分方式分配。

### 社区流行度

2个指标采用均分方式分配，每个指标权重为 50%。

### 贡献活跃度

5个指标采用均分方式分配，每个指标权重为 20%。

### 开发者基数

3个指标采用均分方式分配，每个指标权重约为 33.33%。

## 阈值

我们选择的阈值是基于不同类型开源项目的大数据观测。
