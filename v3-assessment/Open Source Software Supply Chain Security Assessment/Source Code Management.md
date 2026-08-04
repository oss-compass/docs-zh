# 源码管理

定义：评估源代码的安全管理水平，反映项目的法律合规性和安全防护能力。

# 评估模型

**合法合规**

| 度量指标               | 地址                                                         | 阈值 | 权重 |
| ---------------------- | ------------------------------------------------------------ | ---- | ---- |
| 许可头与版权声明       | [/api/v3/legal_compliance/compliance_copyright_statement](https://oss-compass.org/dataHub#api_v3_legal_compliance_compliance_copyright_statement) | 10    | 0.25 |
| 许可证包含（OSI）      | [/api/v3/legal_compliance/compliance_license](https://oss-compass.org/dataHub#api_v3_legal_compliance_compliance_license) | 10    | 0.25 |
| 许可证兼容性           | [/api/v3/legal_compliance/compliance_license_compatibility](https://oss-compass.org/dataHub#api_v3_legal_compliance_compliance_license_compatibility) | 10    | 0.25 |
| 许可证与版权声明防篡改 | [/api/v3/legal_compliance/compliance_copyright_anti_tamper](https://oss-compass.org/dataHub#api_v3_legal_compliance_compliance_copyright_anti_tamper) | 10    | 0.25 |

**安全管理**

| 度量指标       | 地址                                                         | 阈值 | 权重 |
| -------------- | ------------------------------------------------------------ | ---- | ---- |
| 漏洞响应与披露 | [/api/v3/security_management/vulnerability_disclosure](https://oss-compass.org/dataHub#api_v3_security_management_vulnerability_disclosure) | 10    | 0.50 |
| 公开未修复漏洞 | [/api/v3/security_management/security_vulnerability](https://oss-compass.org/dataHub#api_v3_security_management_security_vulnerability) | 10    | 0.50 |

# 评估模型中的指标

## 合法合规

合法合规模型关注项目的法律合规性，确保项目在知识产权和许可证方面符合规范。

### 许可头与版权声明

- 定义：项目是否在源代码文件中包含许可头和版权声明。
- 权重：25%
- 阈值：10（符合）

许可头与版权声明是保护知识产权的重要措施。该指标通过 scancode 扫描器检测源代码文件中的许可头与版权声明合规情况，并结合变更文件检测器核查自基线提交以来新增文件的合规性。在源代码文件中包含许可头能够明确代码的使用权限，保护贡献者的权益。该指标反映了项目对知识产权保护的重视程度。

### 许可证包含（OSI）

- 定义：项目是否包含 OSI（Open Source Initiative）认可的开源许可证。
- 权重：25%
- 阈值：10（符合）

OSI认可的开源许可证是开源项目的标准配置。该指标通过 scancode 扫描器识别项目声明的许可证，并结合 README 开源声明检查器判断是否为 OSI 认可的开源许可证。使用OSI认可的许可证能够保证项目的开源性质，避免法律风险。该指标反映了项目的开源合规性和法律风险。

### 许可证兼容性

- 定义：项目所使用的许可证之间是否兼容。
- 权重：25%
- 阈值：10（兼容）

许可证兼容性是开源项目合规性的重要方面。该指标通过 scancode 扫描器采集项目及其依赖的许可证信息，并检测是否存在不兼容的许可证组合。不兼容的许可证组合可能导致法律纠纷和使用限制。该指标反映了项目的许可证管理水平和法律风险。

### 许可证与版权声明防篡改

- 定义：项目是否采取措施防止许可证和版权声明被篡改。
- 权重：25%
- 阈值：10（符合）

许可证与版权声明防篡改是保护项目知识产权的重要措施。该指标通过 OAT 扫描器检测项目的许可证与版权声明是否存在被篡改或缺失的情况。通过技术手段防止篡改能够保证许可证和版权声明的有效性。该指标反映了项目的安全防护能力。

## 安全管理

安全管理模型关注项目的安全漏洞管理，确保项目能够及时发现和修复安全漏洞。

### 漏洞响应与披露

- 定义：项目是否有完善的漏洞响应和披露机制。
- 权重：50%
- 阈值：10（符合）

漏洞响应与披露机制是开源项目安全管理的重要组成部分。该指标通过安全策略检查器检测项目是否提供 SECURITY.md 安全策略文档及漏洞披露流程。完善的机制能够确保安全漏洞得到及时响应和处理，保护用户安全。该指标反映了项目的安全管理成熟度。

### 公开未修复漏洞

- 定义：项目是否存在公开的未修复安全漏洞。
- 权重：50%
- 阈值：10（无）

公开未修复漏洞是项目安全风险的重要指标。该指标通过漏洞扫描器扫描项目依赖与代码中已披露但未修复的安全漏洞，并按严重程度分级统计。未修复的漏洞可能被恶意利用，威胁用户安全。该指标反映了项目的安全风险和维护质量。

# 评估模型算法

## 权重

各指标权重采用均分方式分配。

### 合法合规

4个指标采用均分方式分配，每个指标权重为 25%。

### 安全管理

2个指标采用均分方式分配，每个指标权重为 50%。

## 阈值

供应链安全评估的阈值基于 openchecker 检查工具的评分规则确定：合规、文档与审查类指标采用 0–10 分制，满分阈值为 10；二值类指标阈值为 1。
