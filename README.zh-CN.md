<div align="center">

# devops-skills

**DevOps and CI/CD skills — GitLab CI, GitHub Actions, K8s, Terraform, Ansible**

[![GitHub](https://img.shields.io/badge/github-full--stack--skills%2Fdevops-skills-green.svg)](https://github.com/full-stack-skills/devops-skills)
[![License](https://img.shields.io/badge/license-Apache%202.0-blue.svg)](LICENSE)
[![Agent Skills](https://img.shields.io/badge/Agent%20Skills-兼容-purple.svg)](https://agentskills.io)

[English](./README.md) | 简体中文

[简介](#-简介) ·
[安装](#-安装) ·
[技能列表](#-技能列表) ·
[支持的智能体](#-支持的智能体) ·
[生态](#-生态)

</div>

---

## 📖 简介

**DevOps 技能** 是一组 AI 编码智能体技能，属于 [Full Stack Skills](https://github.com/partme-ai/full-stack-skills) 生态，由 [PartMe.AI](https://github.com/partme-ai) 维护。

本包包含 **9 个技能**。每个技能是一个可按需加载的独立 Agent Skill。

## 📦 安装

```bash
npx skills add full-stack-skills/devops-skills
```

或按需安装特定技能：

```bash
npx skills add full-stack-skills/devops-skills --skill <skill-name>
```

## 🎯 技能列表 (9)

| 技能 | 描述 |
|------|------|
| `ansible` | Provides comprehensive guidance for Ansible automation including playbooks, roles, inventory, and module usage. Use w... |
| `cloudformation` | Provides comprehensive guidance for AWS CloudFormation including templates, stacks, parameters, and infrastructure au... |
| `github-actions` | Provides comprehensive guidance for GitHub Actions including workflow creation, actions, secrets, and automation. Use... |
| `gitlab-ci` | Provides comprehensive guidance for GitLab CI/CD including pipeline configuration, runners, artifacts, and automation... |
| `kubernetes` | Provides comprehensive guidance for Kubernetes including pods, services, deployments, ingress, and cluster management... |
| `linuxmirrors-awesome` | 介绍 LinuxMirrors 的能力、边界、兼容性、源码结构以及最新权威资料核验方法。 |
| `linuxmirrors-os` | 指导 GNU/Linux 系统软件源安全更换，覆盖预检、自动化、验证、排障与回滚。 |
| `linuxmirrors-docker` | 指导 Docker Engine 安装、Docker CE 换源、Registry Mirror 配置、验证与回滚。 |
| `terraform` | Provides comprehensive guidance for Terraform including infrastructure as code, providers, modules, and state managem... |

## 🤖 支持的智能体

适用于 [Claude Code](https://code.claude.com)、[Codex](https://developers.openai.com/codex)、[Cursor](https://cursor.com)、[OpenCode](https://opencode.ai)、[Gemini CLI](https://geminicli.com)、[GitHub Copilot](https://github.com/features/copilot)、[Windsurf](https://codeium.com/windsurf) 及 [70+ 其他平台](https://agentskills.io/clients)。

### Claude Code 安装

**方式一：npx skills CLI（推荐）**

```bash
npx skills add full-stack-skills/devops-skills
```

**方式二：手动安装**

```bash
git clone https://github.com/full-stack-skills/devops-skills.git
cp -r devops-skills/skills/* .claude/skills/
```

更多详情请参阅 [Claude Code 技能指南](https://code.claude.com/docs/en/skills) 和 [Agent Skills 规范](https://agentskills.io/)。

## 🌐 生态

| 资源 | 链接 |
|------|------|
| **Full Stack Skills** | [github.com/partme-ai/full-stack-skills](https://github.com/partme-ai/full-stack-skills) |
| **全部技能组** | [github.com/full-stack-skills](https://github.com/full-stack-skills) |
| **Agent Skills 规范** | [agentskills.io](https://agentskills.io) |
| **Skills CLI** | [github.com/vercel-labs/skills](https://github.com/vercel-labs/skills) |

## 📄 许可证

Apache 2.0 — 详见 [LICENSE](LICENSE)。
