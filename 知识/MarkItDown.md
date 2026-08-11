---
title: MarkItDown
created: 2026-08-09
updated: 2026-08-09
type: entity
tags: [ai, tool, programming, automation, resource]
sources: [raw/articles/github-ai-tools-2026-08-09.md]
confidence: high
---

# MarkItDown

`microsoft/markitdown` 是 Microsoft 维护的 Python 文档转换工具，目标是把 PDF、PowerPoint、Word、Excel、图片、音频、HTML、CSV/JSON/XML、ZIP、YouTube 与 EPUB 等内容转为适合 LLM 分析的 Markdown，同时尽量保留标题、列表、表格和链接结构。

## 对代理的价值

- 为知识库摄取提供统一的文档转 Markdown 路径，减少不同文件格式的处理差异。
- 可与 [[AI代理能力资源库]] 的原始资料层配合：原件保留在 `raw/`，转换结果作为可检索内容。
- 对表格、Office 文档和网页资料尤其有用，可补足一般纯文本提取的结构缺失。

## 本地副本

- GitHub：https://github.com/microsoft/markitdown
- 许可证：MIT
- 路径：`sources/github/markitdown`
- 已核验提交：`fd239d5`（2026-07-29）
- 状态：仅克隆和阅读；未安装依赖、未运行。

## 安全边界

官方 README 指出该工具以当前进程权限访问 I/O 资源。处理不受信任文件、URL、压缩包、Office 宏相关内容或插件时，应先隔离输入、只调用最窄的转换接口，并避免启用未经审查的插件。

## 关联

[[AI代理能力资源库]] · [[领域/技术与工具]] · [[知识/双向链接]]
