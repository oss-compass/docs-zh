# 社区活力

定义：评估社区的活跃程度和吸引力，反映社区的生命力和发展潜力。

# 评估模型

**社区流行度**

| 度量指标        | 地址                                                                                                    | 阈值 | 权重 |
| --------------- | ------------------------------------------------------------------------------------------------------- | ---- | ---- |
| 项目 Stars 新增 | [/api/v3/community_popularity/stars](https://oss-compass.org/dataHub#api_v3_community_popularity_stars) | 100  | 0.50 |
| 项目 Forks 新增 | [/api/v3/community_popularity/forks](https://oss-compass.org/dataHub#api_v3_community_popularity_forks) | 100  | 0.50 |

**贡献活跃度**

| 度量指标       | 地址                                                                                                                                    | 阈值      | 权重 |
| -------------- | --------------------------------------------------------------------------------------------------------------------------------------- | --------- | ---- |
| 代码提交次数   | [/api/v3/contribution_activity/commit_count](https://oss-compass.org/dataHub#api_v3_contribution_activity_commit_count)                 | 12850 个  | 0.20 |
| 新增代码行数   | [/api/v3/contribution_activity/lines_of_code_change](https://oss-compass.org/dataHub#api_v3_contribution_activity_lines_of_code_change) | 300000 个 | 0.20 |
| PR 评论数量    | [/api/v3/contribution_activity/pr_comment_count](https://oss-compass.org/dataHub#api_v3_contribution_activity_pr_comment_count)         | 10 个     | 0.20 |
| Issue 建立数量 | [/api/v3/contribution_activity/new_issue_count](https://oss-compass.org/dataHub#api_v3_contribution_activity_new_issue_count)           | 10 个     | 0.20 |
| Issue 评论数量 | [/api/v3/contribution_activity/issue_comment_count](https://oss-compass.org/dataHub#api_v3_contribution_activity_issue_comment_count)   | 10 个     | 0.20 |

**开发者基数**

| 度量指标     | 地址                                                                                                                                  | 阈值     | 权重   |
|----------| ------------------------------------------------------------------------------------------------------------------------------------- |--------|------|
| 社区贡献者数量  | [/api/v3/developer_base/contributor_count](https://oss-compass.org/dataHub#api_v3_developer_base_contributor_count)                   | 2000 个 | 0.33 |
| 代码贡献者数量  | [/api/v3/developer_base/code_contributor_count](https://oss-compass.org/dataHub#api_v3_developer_base_code_contributor_count)         | 1000 个 | 0.33 |
| 非代码贡献者数量 | [/api/v3/developer_base/non_code_contributor_count](https://oss-compass.org/dataHub#api_v3_developer_base_non_code_contributor_count) | 500 个  | 0.17 |
| 社区关注者数量  | [/api/v3/developer_base/follower_count](https://oss-compass.org/dataHub#api_v3_developer_base_follower_count)                         | 1000      | 0.17   |

# 评估模型中的指标

## 社区流行度

社区流行度模型关注项目在开发者社区中的知名度和关注度，反映项目的市场影响力。

### 项目 Stars 新增

- 定义：统计周期内项目新增的 Stars 数量。
- 权重：50%
- 阈值：100 个

Stars 数量是衡量项目受欢迎程度的直观指标。新增 Stars 数量反映了项目在开发者社区中的关注度和吸引力。持续增长的 Stars 数量表明项目具有良好的市场影响力和用户基础。

### 项目 Forks 新增

- 定义：统计周期内项目新增的 Forks 数量。
- 权重：50%
- 阈值：100 个

Forks 数量反映了开发者对项目的参与意愿。新增 Forks 数量表明开发者对项目感兴趣，希望基于项目进行二次开发或贡献代码。这是评估项目活跃度和开发者参与度的重要指标。

## 贡献活跃度

贡献活跃度模型关注社区的贡献频率和规模，反映社区的活跃程度。

### 代码提交次数

- 定义：统计周期内代码提交的总次数。
- 权重：20%
- 阈值：12850 个

代码提交次数是衡量项目开发活跃度的核心指标。高频次的代码提交表明项目处于积极开发状态，社区贡献者持续投入。该指标反映了项目的整体工作量和发展速度。

### 新增代码行数

- 定义：统计周期内新增和修改的代码行数总和。
- 权重：20%
- 阈值：300000 行

新增代码行数反映了项目的代码贡献规模。虽然代码行数不能直接衡量代码质量，但它能够反映社区的开发投入程度。持续增长的代码行数表明项目在不断演进和完善。

### PR 评论数量

- 定义：统计周期内 PR 评论的总数量。
- 权重：20%
- 阈值：10 个

PR 评论数量反映了社区的代码审查活跃度。积极的 PR 评论表明社区重视代码质量和协作开发。该指标能够反映社区的协作氛围和技术交流深度。

### Issue 建立数量

- 定义：统计周期内新建 Issue 的总数量。
- 权重：20%
- 阈值：10 个

Issue 建立数量反映了社区的问题反馈活跃度。新建的 Issue 包括 Bug 报告、功能需求、使用咨询等多种类型。该指标能够反映用户对项目的关注程度和参与意愿。

### Issue 评论数量

- 定义：统计周期内 Issue 评论的总数量。
- 权重：20%
- 阈值：10 个

Issue 评论数量反映了社区的问题讨论活跃度。积极的 Issue 评论表明社区具有良好的沟通氛围和问题解决能力。该指标能够反映社区的协作效率和用户支持质量。

## 开发者基数

开发者基数模型关注社区的贡献者规模，反映社区的人才基础。

### 社区贡献者数量

- 定义：统计周期内参与社区贡献的总人数。
- 权重：33%
- 阈值：2000 个

社区贡献者数量是衡量社区规模的核心指标。贡献者包括代码贡献者和非代码贡献者，反映了社区的参与广度。大规模的贡献者基础是社区可持续发展的重要保障。

### 代码贡献者数量

- 定义：统计周期内参与代码贡献的人数。
- 权重：33%
- 阈值：1000 个

代码贡献者数量反映了社区的技术贡献能力。代码贡献者是推动项目技术发展的核心力量。该指标能够反映项目的技术吸引力和开发活跃度。

### 非代码贡献者数量

- 定义：统计周期内，在社区中有任何贡献行为，但未发生代码相关贡献的用户数。
- 权重：17%
- 阈值：500 个

非代码贡献者数量反映了社区的多元化参与程度。该指标统计了社区中未参与代码提交、代码合入等直接代码生产活动，但通过项目维护、Issue管理和社区互动等方式参与项目发展的贡献者。根据贡献行为类型，可划分为以下角色：

- 文档维护者：负责维护项目相关文字信息，包括完善 Issue 和 Pull Request 描述内容、修改标题信息。

- Issue 管理者：负责管理 Issue 生命周期，包括创建Issue、分类标记、状态跟踪、关闭Issue以及关联 PR 。

- PR 协作管理者：负责 PR 协作流程管理，包括任务分配、状态维护、标签管理。

- 社区互动参与者：通过Issue 评论、项目讨论等轻量级社区行为参与项目贡献。

较高的非代码贡献者数量通常意味着社区参与门槛更低，贡献形式更加多样，生态开放性和包容性更强。


### 社区关注者数量

- 定义：统计周期内，在社区中Star和Fork的用户数。
- 权重：17%
- 阈值：1000 个

社区关注者数量是衡量项目社区影响力和外部认可度的指标。在社区中仅通过 Star 或 Fork 行为关注、传播项目，但未参与代码提交、PR、Issue、评论以及其他项目协作行为的用户数量，反映了社区的传播范围和潜在参与规模。

# 评估模型算法

## 权重

各指标权重采用均分方式分配。

### 社区流行度

2 个指标采用均分方式分配，每个指标权重为 50%。

### 贡献活跃度

5 个指标采用均分方式分配，每个指标权重为 20%。

### 开发者基数

3 个指标采用均分方式分配，每个指标权重约为 33.33%。

## 阈值

我们选择的阈值是基于不同类型开源项目的大数据观测。
