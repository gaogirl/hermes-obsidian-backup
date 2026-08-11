# Wiki Log

> Chronological record of wiki actions. Append-only.
> Format: `## [YYYY-MM-DD] action | subject`

## [2026-08-08] create | LLM Wiki initialized
- Domain: 个人综合知识文库，重点收录 LLM / AI 与可复用知识。
- Added `SCHEMA.md`, `index.md`, `log.md`.
- Existing Obsidian navigation was preserved.

## [2026-08-09] ingest | Google AI 官方资讯页首轮抓取
- 来源：https://blog.google/technology/ai/
- 新增：`raw/articles/google-ai-official-2026-08-09.md`、`知识/AI资讯-2026-08-09-首轮入库.md`
- 更新：`index.md`
- 说明：仅写入官方列表页可核验的标题/摘要级信息；完整文章细节列入待验证问题。

## [2026-08-09] query | AI资讯当日精选
- 新增：`知识/AI资讯-2026-08-09-精选.md`
- 更新：`index.md`
- 重点：agentic Gemini、Gemini API Managed Agents、hooks；具体 API 事实待原文核验。

## [2026-08-09] lint | 首轮全库维护
- 检查：Markdown 文件、机器索引、原文 SHA-256、精选页 frontmatter 与 wikilinks。
- 已确认：原文哈希与声明一致；本轮新增知识页均包含至少两个关联链接。
- 待人工处理：既有中文导航页部分没有 LLM Wiki frontmatter；原有 `欢迎.md` 的默认 `[[创建链接]]` 保持不变，避免改动用户原始文件。

## [2026-08-09] ingest | 每日 AI 资讯入库运行摘要
- 检索来源：Google AI 官方栏目、OpenAI News、Anthropic Newsroom、Hugging Face Papers。
- 新增：`queries/AI资讯-2026-08-09-入库.md`。
- 更新：`index.md`、`log.md`。
- 跳过：Google AI 官方栏目已有同 URL/同正文哈希原文，未重复入库；本轮未创建新的实体或概念页。
- 失败/未解决：Hugging Face Papers TLS 吊销检查失败；OpenAI 与 Anthropic 未能核验过去 24 小时内的新增发布时间；Google 条目仍需逐篇取得原文核验。

## [2026-08-09] ingest | GitHub AI 工具与代理能力资源首批收录
- 元数据初筛：NousResearch/hermes-agent、langchain-ai/langgraph、modelcontextprotocol/python-sdk、microsoft/markitdown、microsoft/playwright、google-gemini/gemini-cli、huggingface/skills。
- 浅克隆：`sources/github/mcp-python-sdk`、`sources/github/huggingface-skills`、`sources/github/markitdown`。
- 新增原始目录：`raw/articles/github-ai-tools-2026-08-09.md`。
- 新增知识页：`知识/AI代理能力资源库.md`、`知识/MCP Python SDK.md`、`知识/Hugging Face Skills.md`、`知识/MarkItDown.md`、`知识/Hermes Agent.md`、`知识/GitHub工具候选清单.md`。
- 更新：`index.md`。
- 安全状态：仅读取 README/LICENSE 和 Git 提交信息；未安装依赖，未执行仓库脚本或插件。

## [2026-08-09] ingest | 每日 AI 资讯复核
- 更新：`queries/AI资讯-2026-08-09-入库.md`、`log.md`。
- 本轮检查：Google AI 官方栏目、OpenAI News、Anthropic Newsroom、Hugging Face Papers、arXiv API（`cs.AI` / `cs.CL`）。
- 跳过：Google 栏目已有当日原始页，且未取得可归属到过去 24 小时的新增官方文章；arXiv 最近返回论文提交于 2026-08-06，不在窗口内。
- 失败/未解决：OpenAI 触发 Cloudflare JavaScript/cookie 验证；Hugging Face HTTPS 连接超时；Anthropic 未检出可明确归属到窗口的新增日期。

## [2026-08-09] query | AI资讯当日精选（07:00 入库摘要）
- 新增：`queries/AI资讯-2026-08-09-精选.md`。
- 更新：`index.md`、`log.md`。
- 排序：agentic Gemini、Gemini API Managed Agents、Managed Agents 扩展、Gemini Spark/Chrome 集成、Gemini for macOS。
- 证据边界：唯一来源为 Google 官方栏目标题级原文；未将标题视为已确认的功能、版本或 API 事实，未新建独立概念页。

## [2026-08-10] ingest | 每日 AI 资讯入库
- 检索来源：Google AI 官方栏目、Anthropic News、OpenAI News、Hugging Face Papers、arXiv API（`cs.AI`）。
- 新增：`queries/AI资讯-2026-08-10-入库.md`。
- 更新：`index.md`、`log.md`。
- 结果：未发现可同时满足过去 24 小时、实质性、可靠公开来源且可核验的 3–8 条资讯；未新增 `raw/articles/` 或知识页。
- 失败/未解决：OpenAI 返回 HTTP 403 访问验证页；Hugging Face HTTPS 连接超时；Google 栏目未显示窗口内日期；Anthropic 最新可识别日期为 2026-08-04；arXiv 最近 `cs.AI` 提交为 2026-08-07。

## [2026-08-10] query | AI资讯当日精选（07:00 入库摘要）
- 新增：`queries/AI资讯-2026-08-10-精选.md`。
- 更新：`index.md`、`log.md`。
- 结论：无 3–5 条可同时满足时效、实质性、可靠公开来源与可核验性的候选资讯，未以旧闻或标题级线索凑足条目。
- 关联复核：`知识/AI资讯-2026-08-09-首轮入库.md`、`知识/AI代理能力资源库.md`、`知识/GitHub工具候选清单.md`；未发现足以创建或更新独立知识页的事实。

## [2026-08-10] lint | 每日全库维护
- 检查：`知识/` 与 `queries/` 下 15 个受管知识页、既有导航页、`raw/` 正文 SHA-256、索引与 wikilinks。
- 新增：`queries/AI资讯-2026-08-10-维护报告.md`。
- 更新：`知识/双向链接.md`、`index.md`、`log.md`。
- 已修复：为 `知识/双向链接.md` 补齐受管 frontmatter、受控标签和第三个关联链接；将其教学用未闭合/虚构 wikilink 改为字面示例；通过维护报告为两个此前无知识页入链的查询页建立关联；索引页数更新为 15。
- 已确认：全部受管页已入索引；无超过 200 行页面、无 `contested: true`/`contradictions:`、无无效受管标签；两份 raw 来源正文哈希均匹配声明。
- 待人工处理：两个同标题的 `AI资讯-2026-08-09-精选` 页面仍需确认权威版本；`欢迎.md` 的默认 `[[创建链接]]` 保持不动。

## [2026-08-11] ingest | 每日 AI 资讯入库
- 检索来源：Google AI RSS、Anthropic News、OpenAI News、Hugging Face Papers、arXiv API（`cs.AI` / `cs.CL`）。
- 新增：`queries/AI资讯-2026-08-11-入库.md`。
- 更新：`index.md`、`log.md`。
- 结果：未发现可同时满足过去 24 小时、实质性、可靠公开来源且可核验的 3–8 条资讯；未新增 `raw/articles/` 或知识页。
- 跳过：Google AI 最新条目（2026-08-10 14:30 UTC）及 arXiv API 最新记录（2026-08-10 17:59 UTC）均已超出本地运行时刻的 24 小时窗口。
- 失败/未解决：OpenAI 返回 HTTP 403 Cloudflare 验证页；Hugging Face HTTPS 连接超时；Anthropic 页面未提供可机器核验的窗口内发布时间。

## [2026-08-11] query | AI资讯当日精选（07:00 入库摘要）
- 新增：`queries/AI资讯-2026-08-11-精选.md`。
- 更新：`index.md`、`log.md`。
- 结论：无 3–5 条可同时满足严格 24 小时时效、实质性、可靠公开来源与可直接核验性的候选资讯；未以窗口外的 Google AI RSS / arXiv 条目或不可核验页面凑数。
- 关联复核：`知识/AI资讯-2026-08-09-首轮入库.md`、`知识/AI代理能力资源库.md`、`知识/GitHub工具候选清单.md`；未发现满足阈值的重要新实体或概念。

## [2026-08-11] lint | 每日全库维护
- 检查：`知识/` 与 `queries/` 下 17 个既有受管知识页、导航页、索引、wikilinks 与 `raw/` 正文 SHA-256；未修改 `raw/`。
- 新增：`queries/AI资讯-2026-08-11-维护报告.md`。
- 更新：`queries/AI资讯-2026-08-10-维护报告.md`、`queries/AI资讯-2026-08-11-精选.md`、`index.md`、`log.md`。
- 已修复：为 2026-08-10 维护报告与 2026-08-11 精选建立受管知识页入链；维护报告已入索引；索引页数更新为 18。
- 已确认：18 个受管知识页均已入索引；无路径式/真实断链（历史报告内教学示例除外）、无 frontmatter 缺失、无无效标签、无超 200 行页面、无 `contested: true` / `contradictions:`；5 页低置信度记录保留其证据限制。
- 待人工处理：两份 raw 来源 SHA-256 与声明不一致；两个同标题 `AI资讯-2026-08-09-精选` 页面需确定权威版本；历史报告的教学示例是否改为普通文字需人工决定。
