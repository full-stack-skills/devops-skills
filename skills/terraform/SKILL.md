---
name: terraform
description: Provides comprehensive guidance for Terraform including infrastructure as code, providers, modules, and state management. Use when the user asks about Terraform, needs to create infrastructure as code, manage cloud resources with Terraform, or implement IaC best practices.
license: Apache-2.0
---

## When to use this skill

Use this skill whenever the user wants to:
- 编写或调试 Terraform 配置文件（`.tf`）
- 管理云基础设施（AWS、Azure、GCP、阿里云等）
- 配置 Terraform providers、resources、data sources
- 管理 Terraform state、modules、workspaces

## How to use this skill

1. **配置文件**：HCL 语法定义 provider、resource、variable、output、module。
2. **工作流**：`terraform init` → `terraform plan` → `terraform apply` → `terraform destroy`。
3. **State 管理**：本地或远程（ S3 + DynamoDB、Azure Blob、阿里云 OSS 等）。
4. **Modules**：复用基础设施模板，版本化管理。

## Best Practices

- 使用 remote state 替代本地 state，避免状态文件冲突。
-敏感信息用 variable 或 environment variable，不在 .tf 文件中硬编码。
- 使用 `terraform fmt` 格式化代码，`terraform validate` 检查语法。
- 生产环境使用 workspace 或 environment 隔离。

## Keywords

terraform, iac, infrastructure as code, hcl, aws, azure, gcp, aliyun, 基础设施即代码, 云资源管理

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
