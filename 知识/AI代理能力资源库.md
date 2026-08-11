---
title: AI代理能力资源库
created: 2026-08-09
updated: 2026-08-09
type: summary
tags: [ai, llm, tool, programming, automation, resource]
sources: [raw/articles/github-ai-tools-2026-08-09.md]
confidence: high
---

# AI代理能力资源库

本页维护能直接提升 AI 助手工作能力的公开工具与源码入口。入选标准：官方或高可信维护方、清晰开源许可证、与检索/文档摄取/工具互操作/工作流能力直接相关；源码必须先审阅，不能因为已克隆而自动安装或执行。

## 已纳入的核心资源

| 资源 | 可带来的能力 | 当前状态 | 风险与边界 |
|---|---|---|---|
| [[MCP Python SDK]] | 为模型提供标准化工具、资源、提示词连接；可构建 MCP 服务端与客户端 | 已浅克隆并核验 MIT 许可证 | 仅在明确需求后创建/配置 MCP server；要审查暴露的权限和网络访问。 |
| [[Hugging Face Skills]] | 检索模型、数据集、论文、评估、训练与部署工作流 | 已浅克隆并核验 Apache-2.0 | 不自动安装外部 skill；每个 skill 需单独审阅其脚本、凭据需求与副作用。 |
| [[MarkItDown]] | 把 PDF、Office、HTML、图片/音频等转为 Markdown，用于后续知识摄取 | 已浅克隆并核验 MIT | 文档声明转换会以当前进程权限执行 I/O；不受信任输入必须先隔离和检查。 |
| [[Hermes Agent]] | 当前代理框架，提供技能、定时任务、工具调用、记忆和多平台网关 | 当前正在使用 | 不修改核心配置或安装插件前先验证来源、兼容性与权限。 |

## 目录结构与更新策略

- GitHub 源码保存到 `sources/github/`，保持浅克隆，便于查看而不制造大体积历史。
- 每次添加仓库都应记录 URL、许可证、固定提交、用途、是否安装、是否执行过代码与安全注意事项。
- 每次更新先 `git fetch` / 检查 release notes；不要无审查地运行安装脚本、GitHub Actions、插件或网络服务。
- 满足“经常使用且经过验证”的资源，才可提炼为本地 Hermes skill 或可复用脚本。

## 关联

[[首页]] · [[领域/技术与工具]] · [[知识/双向链接]] · [[GitHub工具候选清单]]
