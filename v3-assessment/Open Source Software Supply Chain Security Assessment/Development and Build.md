# 开发与构建

定义：评估开发过程的安全性和可信度，反映项目的开发成熟度和构建质量。

# 评估模型

**代码审查质量**

| 度量指标   | 地址                                                         | 阈值 | 权重 |
| ---------- | ------------------------------------------------------------ | ---- | ---- |
| 依赖可获得 | [/api/v3/code_review_quality/dependency_reachable](https://oss-compass.org/dataHub#api_v3_code_review_quality_dependency_reachable) | 10    | 0.25 |
| 片段引用   | [/api/v3/code_review_quality/compliance_snippet_reference](https://oss-compass.org/dataHub#api_v3_code_review_quality_compliance_snippet_reference) | 10    | 0.25 |
| 专利风险   | [/api/v3/code_review_quality/patent_risk_oin](https://oss-compass.org/dataHub#api_v3_code_review_quality_patent_risk_oin) | 10    | 0.25 |
| 测试覆盖度 | [/api/v3/code_review_quality/ecology_test_coverage](https://oss-compass.org/dataHub#api_v3_code_review_quality_ecology_test_coverage) | 10    | 0.25 |

**开发文档质量**

| 度量指标       | 地址                                                         | 阈值 | 权重 |
| -------------- | ------------------------------------------------------------ | ---- | ---- |
| README         | [/api/v3/development_document_quality/ecology_readme](https://oss-compass.org/dataHub#api_v3_development_document_quality_ecology_readme) | 10    | 0.25 |
| 构建文档       | [/api/v3/development_document_quality/ecology_build_doc](https://oss-compass.org/dataHub#api_v3_development_document_quality_ecology_build_doc) | 10    | 0.25 |
| 接口文档       | [/api/v3/development_document_quality/ecology_interface_doc](https://oss-compass.org/dataHub#api_v3_development_document_quality_ecology_interface_doc) | 10    | 0.25 |
| Committers文件 | [/api/v3/development_document_quality/ecology_maintainer_doc](https://oss-compass.org/dataHub#api_v3_development_document_quality_ecology_maintainer_doc) | 10    | 0.25 |

**可信构建**

| 度量指标         | 地址                                                         | 阈值 | 权重 |
| ---------------- | ------------------------------------------------------------ | ---- | ---- |
| 可构建           | [/api/v3/trusted_build/trusted_build_success](https://oss-compass.org/dataHub#api_v3_trusted_build_trusted_build_success) | 100    | 0.25 |
| CI集成           | [/api/v3/trusted_build/ci_integration](https://oss-compass.org/dataHub#api_v3_trusted_build_ci_integration) | 1    | 0.25 |
| 构建元数据可获取 | [/api/v3/trusted_build/build_metadata_available](https://oss-compass.org/dataHub#api_v3_trusted_build_build_metadata_available) | 1    | 0.25 |
| 一致性构建       | [/api/v3/trusted_build/reproducible_build](https://oss-compass.org/dataHub#api_v3_trusted_build_reproducible_build) | 1    | 0.25 |

# 评估模型中的指标

## 代码审查质量

代码审查质量模型关注代码审查过程中的安全性和合规性，确保代码质量和知识产权安全。

### 依赖可获得

- 定义：项目的依赖是否可以正常获取。
- 权重：25%
- 阈值：10（可获得）

依赖可获得是保证项目可构建性的基础。该指标通过依赖可达性检查器检测项目所有依赖是否可正常访问，输出可获得的依赖比例及不可达依赖列表。如果依赖无法获取，项目将无法正常构建和使用。该指标反映了项目的依赖管理水平和可持续性。

### 片段引用

- 定义：项目是否正确引用了第三方代码片段。
- 权重：25%
- 阈值：10（符合）

片段引用合规性是知识产权保护的重要方面。该指标通过 OAT 扫描器检测项目代码中第三方片段的引用合规情况。正确引用第三方代码片段能够避免知识产权纠纷，保护项目和使用者的权益。该指标反映了项目的知识产权管理水平。

### 专利风险

- 定义：项目是否存在专利风险（基于 OIN 专利库）。
- 权重：25%
- 阈值：10（无风险）

专利风险是开源项目面临的重要法律风险。该指标基于 OIN 专利库对项目依赖进行专利风险核查，识别是否存在潜在的专利侵权风险。通过OIN专利库检查能够帮助项目规避法律纠纷。该指标反映了项目的法律风险管理水平。

### 测试覆盖度

- 定义：项目的测试覆盖率。
- 权重：25%
- 阈值：10（符合标准）

测试覆盖度是衡量代码质量的重要指标。高测试覆盖率能够保证代码的稳定性和可靠性，减少缺陷和安全风险。该指标反映了项目的质量保证水平。

## 开发文档质量

开发文档质量模型关注项目文档的完整性和规范性，确保项目易于理解和使用。

### README

- 定义：项目是否包含 README 文档。
- 权重：25%
- 阈值：10（包含）

README是项目的门面，是用户了解项目的第一入口。该指标通过 README 检查器检测项目根目录是否存在 README 文件并评估其内容完整度。完善的README能够帮助用户快速了解项目的功能、安装和使用方法。该指标反映了项目的文档完善程度。

### 构建文档

- 定义：项目是否包含构建文档。
- 权重：25%
- 阈值：10（包含）

构建文档是指导用户构建项目的重要文档。该指标通过构建文档检查器检测项目是否存在构建说明文档。完善的构建文档能够帮助用户顺利构建项目，降低使用门槛。该指标反映了项目的用户友好度。

### 接口文档

- 定义：项目是否包含接口文档。
- 权重：25%
- 阈值：10（包含）

接口文档是指导用户使用项目API的重要文档。该指标通过接口文档检查器检测项目是否存在 API 接口说明文档。完善的接口文档能够帮助用户正确使用项目功能，提升开发效率。该指标反映了项目的开发者友好度。

### Committers文件

- 定义：项目是否包含 Committers 或 Maintainers 文件。
- 权重：25%
- 阈值：10（包含）

Committers文件记录了项目的核心贡献者和维护者信息。该指标通过维护者文档检查器检测项目是否存在 Committers 或 Maintainers 文件。完善的Committers文件能够帮助用户了解项目的治理结构和贡献者。该指标反映了项目的治理透明度。

## 可信构建

可信构建模型关注构建过程的安全性和可重复性，确保构建结果的可信度。

### 可构建

- 定义：项目是否可以成功构建。
- 权重：25%
- 阈值：100（可构建）

可构建性是项目可用性的基础。该指标通过构建检查器执行项目构建并统计构建成功率。如果项目无法构建，将无法被用户使用。该指标反映了项目的构建质量和可用性。

### CI集成

- 定义：项目是否集成了持续集成（CI）系统。
- 权重：25%
- 阈值：1（集成）

CI集成是现代软件开发的标准实践。该指标通过 CI 检查器检测项目是否配置了 CI 工作流或 CI 配置文件。通过CI系统能够自动化构建和测试过程，保证代码质量。该指标反映了项目的开发流程成熟度。

### 构建元数据可获取

- 定义：项目的构建元数据是否可以获取。
- 权重：25%
- 阈值：1（可获取）

构建元数据包括构建时间、构建环境、依赖版本等信息。该指标通过构建元数据检查器检测项目是否输出并可获取构建元数据。可获取的构建元数据能够帮助用户了解构建过程，提升构建的可追溯性。该指标反映了项目的构建透明度。

### 一致性构建

- 定义：项目是否支持一致性构建（Reproducible Build）。
- 权重：25%
- 阈值：1（支持）

一致性构建是指相同的源代码在不同环境下能够产生相同的构建结果。该指标通过可重现构建检查器对比多次构建产物的校验和是否一致。支持一致性构建能够保证构建结果的可信度，防止构建过程被篡改。该指标反映了项目的安全成熟度。

# 评估模型算法

## 权重

各指标权重采用均分方式分配。

### 代码审查质量

4个指标采用均分方式分配，每个指标权重为 25%。

### 开发文档质量

4个指标采用均分方式分配，每个指标权重为 25%。

### 可信构建

4个指标采用均分方式分配，每个指标权重为 25%。

## 阈值

供应链安全评估的阈值基于 openchecker 检查工具的评分规则确定：合规、文档与审查类指标采用 0–10 分制，满分阈值为 10；二值类指标阈值为 1。
