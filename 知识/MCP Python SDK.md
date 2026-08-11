---
title: MCP Python SDK
created: 2026-08-09
updated: 2026-08-09
type: entity
tags: [ai, llm, tool, programming, automation, resource]
sources: [raw/articles/github-ai-tools-2026-08-09.md]
confidence: high
---

# MCP Python SDK

`modelcontextprotocol/python-sdk` 是 Model Context Protocol 的官方 Python SDK。其 README 说明它可以构建 MCP server 与 client，并支持 stdio、Streamable HTTP 与 SSE 传输；当前 README 指向 v2 稳定线和 2026-07-28 MCP 规范。

## 对代理的价值

- 将本地文件、内部工具、数据库或 API 以标准协议暴露给 LLM 应用。
- 通过类型注解和工具函数减少手写 JSON Schema、请求解析和协议处理。
- 在需要扩展 [[Hermes Agent]] 能力时，是比临时拼接 shell 命令更可维护的工具集成方式。

## 本地副本

- GitHub：https://github.com/modelcontextprotocol/python-sdk
- 许可证：MIT
- 路径：`sources/github/mcp-python-sdk`
- 已核验提交：`a4f4ccd`（2026-07-29）
- 状态：仅克隆和阅读；未安装、未运行。

## 使用前检查

MCP 服务可能提供高权限工具。实现或接入前需要界定可访问的目录、网络范围、密钥来源、输入验证和人工批准规则。

## 关联

[[AI代理能力资源库]] · [[Hermes Agent]] · [[领域/技术与工具]]
