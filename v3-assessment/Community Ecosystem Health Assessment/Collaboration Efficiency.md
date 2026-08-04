# 协作效率

定义：评估社区的协作质量和响应效率，反映社区的协作成熟度和服务水平。

# 评估模型

**响应及时性**

| 度量指标           | 地址                                                         | 阈值   | 权重 |
| ------------------ | ------------------------------------------------------------ | ------ | ---- |
| Issue 未响应占比   | [/api/v3/response_timeliness/issue_unresponsive_rate](https://oss-compass.org/dataHub#api_v3_response_timeliness_issue_unresponsive_rate) | 1 占比 | 0.17 |
| Issue 首次响应时间 | [/api/v3/response_timeliness/issue_first_reponse](https://oss-compass.org/dataHub#api_v3_response_timeliness_issue_first_reponse) | 15 天  | 0.17 |
| Issue 处理时长     | [/api/v3/response_timeliness/issue_open_time](https://oss-compass.org/dataHub#api_v3_response_timeliness_issue_open_time) | 60 天  | 0.17 |
| PR 未响应占比      | [/api/v3/response_timeliness/pr_unresponsive_rate](https://oss-compass.org/dataHub#api_v3_response_timeliness_pr_unresponsive_rate) | 1 占比 | 0.17 |
| PR 首次响应时间    | [/api/v3/response_timeliness/pr_time_to_first_response](https://oss-compass.org/dataHub#api_v3_response_timeliness_pr_time_to_first_response) | 15 天  | 0.17 |
| PR 处理时长        | [/api/v3/response_timeliness/pr_open_time](https://oss-compass.org/dataHub#api_v3_response_timeliness_pr_open_time) | 30 天  | 0.17 |

**协作开发质量**

| 度量指标         | 地址                                                         | 阈值   | 权重 |
|--------------| ------------------------------------------------------------ | ------ | ---- |
| PR 提交代码率     | [/api/v3/collaboration_quality/pr_merge_rate](https://oss-compass.org/dataHub#api_v3_collaboration_quality_pr_merge_rate) | 1      | 0.17 |
| PR/Issue 关联率 | [/api/v3/collaboration_quality/pr_issue_link_rate](https://oss-compass.org/dataHub#api_v3_collaboration_quality_pr_issue_link_rate) | 1 占比 | 0.17 |
| PR 评审参与率     | [/api/v3/collaboration_quality/pr_review_participation_rate](https://oss-compass.org/dataHub#api_v3_collaboration_quality_pr_review_participation_rate) | 1 占比 | 0.17 |
| Merge协作比率    | [/api/v3/collaboration_quality/pr_non_author_merge_rate](https://oss-compass.org/dataHub#api_v3_collaboration_quality_pr_non_author_merge_rate) | 1 占比 | 0.17 |
| PR 平均交互数     | [/api/v3/collaboration_quality/pr_average_interactions](https://oss-compass.org/dataHub#api_v3_collaboration_quality_pr_average_interactions) | 1 个   | 0.17 |
| 分级代码审查时长     | [/api/v3/collaboration_quality/pr_review_time_by_size](https://oss-compass.org/dataHub#api_v3_collaboration_quality_pr_review_time_by_size) | 10 天  | 0.17 |

# 评估模型中的指标

## 响应及时性

响应及时性模型关注社区对Issue和PR的响应速度，反映社区的服务水平和沟通效率。

### Issue 未响应占比

- 定义：统计周期内新建但未得到任何响应的 Issue占Issue总数的比例。
- 权重：17%
- 阈值：1占比（100%）

Issue未响应占比反映了社区对用户问题的关注程度。该指标统计周期内新建且截至周期结束仍未收到任何评论、且处于开启状态的 Issue 占比。未响应的Issue会让用户感到被忽视，影响用户体验和社区声誉。降低未响应占比是提升社区服务质量的重要目标。

### Issue 首次响应时间

- 定义：统计周期内新建Issue首次得到响应的平均时间。
- 权重：17%
- 阈值：15天

Issue首次响应时间是衡量社区响应速度的关键指标。该指标统计周期内新建Issue从创建到首次获得非机器人评论的时间。快速的首次响应能够给用户带来良好的体验，增强用户对社区的信任。该指标反映了社区的沟通效率和服务意识。

### Issue 处理时长

- 定义：统计周期内Issue从创建到关闭的平均时间。
- 权重：17%
- 阈值：60天

Issue处理时长反映了社区解决问题的效率。该指标统计周期内新建 Issue 的处理时长，已关闭的 Issue 取关闭时间与创建时间之差，未关闭的 Issue 取统计时刻与创建时间之差。较短的处理时长表明社区能够快速解决用户问题，提升用户满意度。

### PR 未响应占比

- 定义：统计周期内新建但未得到任何响应的 PR 占新建 PR 总数的比例。
- 权重：17%
- 阈值：1占比（100%）

PR未响应占比反映了社区对代码贡献的关注程度。该指标统计周期内新建且截至周期结束既未合并也未获得任何非机器人评论的 PR 占比。未响应的PR会让贡献者感到沮丧，影响贡献者的积极性和留存率。降低PR未响应占比是维护良好贡献者关系的重要措施。

### PR 首次响应时间

- 定义：统计周期内新建 PR 首次得到响应的平均时间。
- 权重：17%
- 阈值：15天

PR首次响应时间是衡量社区对代码贡献响应速度的关键指标。该指标统计周期内新建 PR 从创建到首次非机器人评论的时间（取平均值，单位为天）。快速的首次响应能够给贡献者带来良好的体验，增强贡献者对社区的信任。该指标反映了社区的协作效率和贡献者支持质量。

### PR 处理时长

- 定义：统计周期内 PR 从创建到合并或关闭的平均处理时长。
- 权重：17%
- 阈值：30天

PR处理时长反映了社区处理代码贡献的效率。该指标统计周期内新建 PR 的处理时长，已合并或关闭的 PR 取结束时间与创建时间之差，未结束的 PR 取本周期开始时间与创建时间之差（取平均值，单位为天）。较短的处理时长能够减少贡献者的等待时间，降低合并冲突的风险。该指标是评估社区协作效率的重要指标。

## 协作开发质量

协作开发质量模型关注社区的代码审查和协作流程质量，反映社区的开发成熟度。

### PR 提交代码率

- 定义：统计周期内成功合并的 PR 产生的commit数占总commit比例。
- 权重：17%
- 阈值：1（100%）

PR提交代码率反映了社区通过 PR 流程提交代码的规范程度。该指标统计周期内成功合并的 PR 所产生的 commit 数占项目总 commit 数的比例。较高的比例表明项目代码主要通过 PR 流程合入，代码变更经过审查，有利于保障代码质量。该指标能够反映社区的协作规范性和代码审查覆盖度。

### PR/Issue 关联率

- 定义：统计周期内关联了 Issue 的 PR 占 PR 总数的比例。
- 权重：17%
- 阈值：1占比（100%）

PR/Issue关联率反映了社区的协作规范性。该指标统计周期内 PR 中关联了 Issue 的 PR 占比。关联Issue能够帮助理解代码变更的背景和目的，提升代码审查效率。该指标反映了社区的协作成熟度和流程规范性。

### PR 评审参与率

- 定义：统计周期内经过评审的 PR 占 PR 总数的比例。
- 权重：17%
- 阈值：1占比（100%）

PR评审参与率反映了社区的代码审查文化。该指标统计周期内新建 PR 中存在非作者评审记录（评审评论或指派接受）的 PR 占比。经过评审的PR能够保证代码质量，减少缺陷和安全风险。该指标反映了社区对代码质量的重视程度。

### Merge协作比率

- 定义：统计周期内由非 PR 作者合并的 PR 占已合并 PR 总数的比例。
- 权重：17%
- 阈值：1占比（100%）

Merge协作比率反映了社区的协作安全性。该指标统计周期内合并人与作者不为同一人的 PR 占已合并 PR 总数的比例。由非作者合并PR能够避免权限滥用，保证代码审查的有效性。该指标反映了社区的治理成熟度和安全意识。

### PR 平均交互数

- 定义：统计周期内每个 PR 的平均评论交互次数。
- 权重：17%
- 阈值：1个

PR平均交互数反映了社区的协作深度。该指标统计周期内新建 PR 的评论总数与新建 PR 数量的比值（排除机器人评论）。较多的交互表明社区对代码变更进行了充分的讨论和审查，有助于提升代码质量。该指标能够反映社区的协作氛围和技术交流深度。

### 分级代码审查时长

- 定义：统计周期内按代码变更规模分级的 PR 平均审查时长。
- 权重：17%
- 阈值：10天

分级代码审查时长反映了社区的审查效率。该指标按 PR 代码变更行数统计各等级 PR 的平均首次审查响应时长。根据PR规模进行分级审查能够优化审查资源分配，提升审查效率。该指标反映了社区的审查流程成熟度。

# 评估模型算法

## 权重

各指标权重采用均分方式分配。

### 响应及时性

6个指标采用均分方式分配，每个指标权重约为 16.67%。

### 协作开发质量

6个指标采用均分方式分配，每个指标权重约为 16.67%。

## 阈值

我们选择的阈值是基于不同类型开源项目的大数据观测。
