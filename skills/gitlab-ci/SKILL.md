---
name: gitlab-ci
description: Provides comprehensive guidance for GitLab CI/CD including pipeline configuration, runners, artifacts, and automation. Use when the user asks about GitLab CI, needs to create GitLab pipelines, configure CI/CD workflows, or automate deployments with GitLab.
license: Apache-2.0
---

## When to use this skill

Use this skill whenever the user wants to:
- 编写或调试 GitLab CI 流水线 (`.gitlab-ci.yml`)
- 配置 GitLab Runner、stages、jobs、artifacts
- 设置 GitLab CI/CD 变量、secrets、environments
- 集成测试、构建、部署自动化

## How to use this skill

1. **流水线结构**：YAML 中定义 `stages`、`jobs`；每个 job 属于某个 stage。
2. **Runner 配置**：shared runner、specific runner、tags 选择。
3. **Artifacts 与缓存**：在 jobs 间传递构建产物，使用 cache 加速。
4. **环境与部署**：使用 `environment` 定义部署目标，配置 `only/except` 规则。

## Best Practices

- 用 `stages` 明确构建顺序，job 并行执行。
- 敏感信息用 CI/CD 变量（Settings → CI/CD → Variables），不在 yaml 中硬编码。
- 用 `needs` 实现复杂依赖图，避免不必要的等待。
- 失败 job 加 `artifacts` 保留日志和产物。

## Keywords

gitlab ci, gitlab-ci, pipeline, runner, ci/cd, 流水线, 自动化部署, gitlab runner

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
