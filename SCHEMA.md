# Wiki Schema

## Domain
个人综合知识文库，重点收录 LLM / AI、技术工具、工作方法、学习成长与生活兴趣相关的文章和知识。

## Conventions
- 文件名：使用中文短标题，避免重复；原始来源文件使用描述性文件名。
- 每个知识页必须包含 YAML frontmatter：`title`、`created`、`updated`、`type`、`tags`、`sources`。
- 原始文章放入 `raw/articles/`，原始内容只读，不直接修改。
- 通过 `[[双向链接]]` 连接知识页、主题页和来源页。
- 新建或更新知识页时，必须同步更新 `index.md` 和 `log.md`。
- 每个知识页至少包含 2 个出链；无法建立关联时先放入 `00-收件箱.md`。
- 更新已有页面时必须更新 `updated` 日期。
- 单一来源或快速变化的内容使用 `confidence: medium` 或 `low`；多来源充分支持才使用 `high`。
- 文章原文 frontmatter 必须包含 `source_url`、`ingested`、`sha256`。

## Page Types
- `entity`：人物、组织、产品、模型
- `concept`：概念、技术、方法
- `comparison`：对比分析
- `query`：值得长期保留的问答或综合研究
- `summary`：文章或多来源摘要

## Tag Taxonomy
- `ai`、`llm`、`machine-learning`
- `model`、`architecture`、`training`、`inference`
- `tool`、`programming`、`automation`
- `work`、`method`、`learning`
- `health`、`life`、`resource`
- `comparison`、`summary`、`research`

## Page Thresholds
- 一个实体或概念在 2 个以上来源出现，或是单篇文章的核心主题时，创建独立知识页。
- 仅为顺带提及的内容不创建独立页面，写入相关页面或收件箱。
- 页面超过约 200 行时拆分为多个主题页。

## Ingest Workflow
1. 保存来源原文到 `raw/articles/`，计算正文 SHA-256。
2. 读取 `SCHEMA.md`、`index.md` 和 `log.md` 最近记录，检查重复内容。
3. 检查已有知识页，决定新建还是更新。
4. 提炼结论、关键事实、证据、争议和待验证问题。
5. 建立至少 2 个相关 Wiki 链接，并标注来源。
6. 更新 `index.md` 的条目、日期和页数。
7. 向 `log.md` 追加操作记录，列出所有新增和更新的文件。
8. 汇报实际变更和未解决的问题。

## Update Policy
新来源与旧内容冲突时，不静默覆盖：保留双方观点、标注来源和日期，并在 frontmatter 中使用 `contested: true` 或 `contradictions:`。
