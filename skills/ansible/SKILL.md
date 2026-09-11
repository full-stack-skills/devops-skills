---
name: ansible
description: Provides comprehensive guidance for Ansible automation including playbooks, roles, inventory, and module usage. Use when the user asks about Ansible, needs to automate IT tasks, create Ansible playbooks, or manage infrastructure with Ansible.
license: Apache-2.0
---

## When to use this skill

Use this skill whenever the user wants to:
- 编写 playbook、role、inventory；执行 ad-hoc 或 playbook
- 用 module（package、copy、template、service、user 等）管理配置与部署
- 处理变量、条件、循环与错误处理

## How to use this skill

1. **Playbook**：YAML 定义 hosts、tasks、handlers、vars；role 组织可复用任务与模板。
2. **CLI**：`ansible-playbook playbook.yml`、`ansible -m ping all`；inventory 用 INI 或 YAML；凭据用 vault 或 SSH 密钥。
3. **环境**：控制机需 Python；目标机 SSH 可达；可选 Ansible Tower/AWX 做调度与审计。

## Best Practices

- 用 role 与 group_vars/host_vars 分层；避免单一大 playbook。
- 敏感数据用 ansible-vault 加密；幂等 task 用 state 与条件。
- 明确失败处理（ignore_errors、block/rescue）；日志与 tag 便于排查。

## Keywords

ansible, playbook, role, inventory, 自动化, 配置管理

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
