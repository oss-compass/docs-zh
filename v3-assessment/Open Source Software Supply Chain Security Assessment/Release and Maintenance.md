# 发布与维护

定义：评估发布过程的安全性和维护管理水平，反映项目的发布质量和持续维护能力。

# 评估模型

**发布质量**

| 度量指标       | 地址                                                         | 阈值 | 权重 |
| -------------- | ------------------------------------------------------------ | ---- | ---- |
| SBOM检查       | [/api/v3/release_quality/sbom_in_release](https://oss-compass.org/dataHub#api_v3_release_quality_sbom_in_release) | 10    | 0.25 |
| 二进制制品包含 | [/api/v3/release_quality/security_binary_artifact](https://oss-compass.org/dataHub#api_v3_release_quality_security_binary_artifact) | 1    | 0.25 |
| 软件包签名     | [/api/v3/release_quality/security_package_sign](https://oss-compass.org/dataHub#api_v3_release_quality_security_package_sign) | 10    | 0.25 |
| Release Notes  | [/api/v3/release_quality/lifecycle_release_note](https://oss-compass.org/dataHub#api_v3_release_quality_lifecycle_release_note) | 10    | 0.25 |

**维护管理**

| 度量指标             | 地址                                                         | 阈值  | 权重 |
| -------------------- | ------------------------------------------------------------ | ----- | ---- |
| 生命周期申明         | [/api/v3/maintenance_management/lifecycle_statement](https://oss-compass.org/dataHub#api_v3_maintenance_management_lifecycle_statement) | 10     | 0.50 |
| 安全漏洞平均修复时间 | [/api/v3/maintenance_management/avg_vulnerability_fix_time](https://oss-compass.org/dataHub#api_v3_maintenance_management_avg_vulnerability_fix_time) | 90 天 | 0.50 |

# 评估模型中的指标

## 发布质量

发布质量模型关注发布过程的安全性和规范性，确保发布版本的完整性和可信度。

### SBOM检查

- 定义：发布版本是否包含软件物料清单（SBOM）。
- 权重：25%
- 阈值：10（包含）

SBOM（Software Bill of Materials）是软件物料清单，记录了软件中包含的所有组件和依赖。该指标通过发布检查器检测项目发布版本是否随附 SBOM。包含SBOM能够帮助用户了解软件的组成，识别潜在的安全风险。该指标反映了项目的供应链透明度。

### 二进制制品包含

- 定义：发布版本中是否包含不应存在的二进制制品。
- 权重：25%
- 阈值：1（符合）

二进制制品审查是发布安全的重要环节。该指标通过二进制检查器与 OAT 扫描器检测项目发布版本中是否存在不应提交的二进制文件，并按 0–10 分制评分，二进制制品越少得分越高。避免在源码发布中混入二进制制品能够降低供应链安全风险。该指标反映了项目的发布安全管理水平。

### 软件包签名

- 定义：发布版本是否进行了数字签名。
- 权重：25%
- 阈值：10（已签名）

软件包签名是保证软件完整性和真实性的重要措施。该指标通过发布检查器检测项目发布版本是否对发布制品进行了数字签名。通过数字签名能够验证软件包的来源和完整性，防止软件包被篡改。该指标反映了项目的安全成熟度。

### Release Notes

- 定义：发布版本是否包含发布说明。
- 权重：25%
- 阈值：10（包含）

Release Notes记录了版本的变更内容、新功能、修复的问题等信息。该指标通过发布检查器检测项目发布版本是否随附 Release Notes。完善的Release Notes能够帮助用户了解版本变更，做出升级决策。该指标反映了项目的文档完善程度。

## 维护管理

维护管理模型关注项目的维护状态和响应能力，确保项目得到持续维护。

### 生命周期申明

- 定义：项目是否声明了生命周期状态。
- 权重：100%
- 阈值：10（已声明）

生命周期申明告知用户项目的当前状态（如活跃、维护、归档等）。该指标通过生命周期文档检查器检测项目是否声明了生命周期状态。明确的生命周期申明能够帮助用户了解项目的维护状态，做出使用决策。该指标反映了项目的透明度和用户关怀。

### 安全漏洞平均修复时间

- 定义：项目修复安全漏洞的平均时间（待实现）。
- 权重：0%
- 阈值：30天

安全漏洞平均修复时间是衡量项目安全响应能力的重要指标。该指标通过漏洞扫描器采集已披露安全漏洞从公开到修复的时长，并计算平均值（若漏洞策略检查器有数据则作为补充来源）。较短的修复时间能够减少用户暴露在安全风险中的时间，保护用户安全。该指标反映了项目的安全维护能力。

# 评估模型算法

## 权重

各指标权重采用均分方式分配。

### 发布质量

4个指标采用均分方式分配，每个指标权重为 25%。

### 维护管理

生命周期申明权重为100%。

## 阈值

供应链安全评估的阈值基于 openchecker 检查工具的评分规则确定：合规、文档与审查类指标采用 0–10 分制，满分阈值为 10；二值类指标阈值为 1。