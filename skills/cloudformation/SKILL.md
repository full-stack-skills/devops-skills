---
name: cloudformation
description: Provides comprehensive guidance for AWS CloudFormation including templates, stacks, parameters, and infrastructure automation. Use when the user asks about CloudFormation, needs to create AWS infrastructure as code, manage CloudFormation stacks, or implement AWS IaC best practices.
license: Apache-2.0
---

## When to use this skill

Use this skill whenever the user wants to:
- 编写或调试 CloudFormation 模板（YAML/JSON）
- 创建和管理 AWS 资源（EC2、S3、RDS、Lambda 等）
- 配置 CloudFormation stacks、nested stacks、stack sets
- 使用 CloudFormation 最佳实践实现基础设施自动化

## How to use this skill

1. **模板结构**：AWSTemplateFormatVersion、Description、Parameters、Resources、Outputs。
2. **工作流**：创建堆栈 → 更新堆栈 → 删除堆栈；使用变更集预览变更。
3. **嵌套堆栈**：将重复使用的资源封装为 nested stack，提高复用性。
4. **Cross-stack references**：通过 Export/Import-Value 在堆栈间共享资源。

## Best Practices

- 使用 YAML 格式替代 JSON，便于版本控制和 Code Review。
- 敏感信息用 Parameter + NoEcho 或 Secrets Manager，不在模板中硬编码。
- 使用 Mappings 和 Conditions 实现环境差异化配置。
- 堆栈名称加环境前缀（dev-、prod-），避免冲突。

## Keywords

cloudformation, aws, infrastructure as code, cloudformation template, 亚马逊云科技, aws iac, 基础设施自动化

## 能力边界

### ✅ 适用场景
- 当你需要使用此技能对应的技术栈时
- 当项目需要遵循最佳实践时
- 当需要快速上手或深入理解核心概念时

### ⚠️ 需要注意
- 复杂业务逻辑需要结合具体场景调整
- 性能优化需要根据实际数据量评估

### ❌ 不适用场景
- 不相关的技术栈或框架
- 需要完全自定义的特殊场景

## 常见陷阱 (Gotchas)

1. **版本兼容性**：注意框架版本与依赖库的兼容性，不同版本 API 可能有差异
2. **配置文件格式**：配置文件格式错误是最常见的问题，建议使用编辑器的语法检查
3. **环境变量**：确保所有必要的环境变量已正确设置，敏感信息不要硬编码
4. **依赖冲突**：多版本共存时注意依赖冲突，使用 lock 文件锁定版本
5. **性能陷阱**：大数据量场景下注意性能优化，避免 N+1 查询等常见问题

## 使用流程

### Step 1: 环境准备
确保开发环境已安装必要的依赖和工具。

### Step 2: 配置初始化
根据项目需求进行基础配置。

### Step 3: 核心功能使用
按照示例代码实现核心功能。

### Step 4: 测试验证
运行测试确保功能正常。

### Step 5: 部署上线
完成开发后进行部署和监控。
