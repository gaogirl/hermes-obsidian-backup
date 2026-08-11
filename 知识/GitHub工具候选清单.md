---
title: GitHub工具候选清单
created: 2026-08-09
updated: 2026-08-09
type: query
tags: [ai, llm, tool, programming, automation, resource]
sources: [raw/articles/github-ai-tools-2026-08-09.md]
confidence: medium
---

# GitHub工具候选清单

以下候选已通过公开 GitHub 元数据初筛，但尚未克隆或安装。纳入依据是与代理开发、浏览器自动化或 CLI 工作流相关，且许可证在 API 元数据中显示为 MIT 或 Apache-2.0。

| 项目 | 许可证 | 候选用途 | 决策前需核验 |
|---|---|---|---|
| `langchain-ai/langgraph` | MIT | 长运行、有状态代理工作流与图式编排参考 | Python 依赖、执行模型、与当前 Hermes 的重复度。 |
| `microsoft/playwright` | Apache-2.0 | 浏览器测试与自动化参考 | 浏览器下载体积、网页权限、自动化边界。 |
| `google-gemini/gemini-cli` | Apache-2.0 | 终端 AI 代理的设计与工具集成参考 | Provider 账户、遥测、命令执行权限。 |

## 引入规则

1. 先读取 README、LICENSE、SECURITY 与依赖清单。
2. 只做浅克隆；不执行 `install`、`setup`、`bootstrap` 或仓库内脚本。
3. 明确记录来源、提交、许可证、实际用途、风险和是否验证过。
4. 能由已有 [[AI代理能力资源库]] 工具完成的功能，不为“收藏”而新增依赖。

## 关联

[[AI代理能力资源库]] · [[MCP Python SDK]] · [[Hermes Agent]]
