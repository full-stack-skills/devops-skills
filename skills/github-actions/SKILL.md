---
name: github-actions
description: Provides comprehensive guidance for GitHub Actions including workflow creation, actions, secrets, and automation. Use when the user asks about GitHub Actions, needs to create GitHub workflows, automate GitHub processes, or configure CI/CD with GitHub Actions.
license: Apache-2.0
---

## When to use this skill

Use this skill whenever the user wants to:
- 编写或调试 GitHub Actions 工作流（`.github/workflows/*.yml`）
- 配置 trigger、jobs、steps、secrets、矩阵与复用
- 集成 checkout、build、test、deploy、通知

## How to use this skill

1. **工作流**：YAML 中定义 `on`、`jobs`、`steps`；用 `actions/checkout`、官方/第三方 action；secrets 在 Settings 中配置。
2. **复用**：composite actions、reusable workflows；矩阵策略跑多版本/多平台。
3. **环境**：runner 环境（Ubuntu/Windows/macOS）；容器 job 时注意网络与挂载。

## Best Practices

- 用 `secrets` 存令牌与密钥；不在 log 中 echo 敏感信息。
- 关键步骤加 `id` 与 `outputs` 便于后续步骤使用。
- 缓存依赖（actions/cache）；必要时用 concurrency 取消旧运行。

## Keywords

github actions, workflow, yaml, CI/CD, 工作流, 自动化

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
