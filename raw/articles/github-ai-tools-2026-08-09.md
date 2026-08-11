---
source_url: https://github.com/NousResearch/hermes-agent
ingested: 2026-08-09
sha256: 203499dc1fffb74ac925da0485d12baf2f77349fe73eff6aaddc35bdea0249c8
---

# GitHub 工具源码目录（首批）

采集日期：2026-08-09

## NousResearch/hermes-agent
- URL: https://github.com/NousResearch/hermes-agent
- 用途：当前 Hermes Agent 本体，记录自身架构、工具、技能、网关和调度能力。
- 许可证：MIT
- 说明：当前环境已经在使用该源码，不重复克隆到知识库。

## modelcontextprotocol/python-sdk
- URL: https://github.com/modelcontextprotocol/python-sdk
- 用途：官方 Python MCP SDK；用于实现 MCP server/client，支持 stdio、Streamable HTTP、SSE。
- 许可证：MIT
- 浅克隆目录：sources/github/mcp-python-sdk
- 已核验提交：a4f4ccd（2026-07-29）

## huggingface/skills
- URL: https://github.com/huggingface/skills
- 用途：Hugging Face 的 Agent Skills 集合，覆盖 Hub、数据集、评估、训练、部署等工作流。
- 许可证：Apache-2.0
- 浅克隆目录：sources/github/huggingface-skills
- 已核验提交：ec01082（2026-08-07）

## microsoft/markitdown
- URL: https://github.com/microsoft/markitdown
- 用途：将 PDF、Office、HTML、图片和音频等转换成适合 LLM 处理的 Markdown。
- 许可证：MIT
- 浅克隆目录：sources/github/markitdown
- 已核验提交：fd239d5（2026-07-29）

安全说明：三个仓库均仅作源码和文档参考；未安装依赖、未执行仓库脚本或第三方插件。MarkItDown 文档明确指出它以当前进程权限进行 I/O，处理不受信任输入时需要使用最窄的转换接口并先做输入审查。
