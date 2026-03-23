# Search Record Format

After delivering results to the user, save a search record as a `.md` file in the `research/` subdirectory of the current working directory (create it if it does not exist).

## File Naming

```
主题-YYMMDD.md
```

- `主题`: concise topic label in Chinese, no spaces (use hyphens if needed), e.g. `新能源汽车市场`, `AI芯片供应链`
- `YYMMDD`: date of the search, e.g. `260323`
- Example: `新能源汽车市场-260323.md`

If the same topic has been searched before, create a new independent file and link the prior file in the `related` field — do not overwrite.

## File Structure

```markdown
---
topic: 主题
date: YYYY-MM-DD
queries:
  - "检索词1（中文）"
  - "English query 2 filetype:pdf"
scope: 地域 | 时间范围 | 来源偏好
related:
  - 主题-260310.md   # 同主题上次搜索，留空则删除此字段
---

## 来源列表

| 标题 | 机构 | 日期 | 类型 | 访问 | 链接 |
|------|------|------|------|------|------|
| 标题文字 | 机构名 | 2024-Q3 | consulting report | official PDF | [官方页](URL) · [PDF](URL) |

Access labels: `official PDF` / `official page` / `licensed/paywalled` / `secondary mirror`
Type labels: `consulting report` / `white paper` / `broker research` / `regulator/exchange` / `company IR` / `association/standard`

## 主要内容摘要

For each source in the list above, write a block:

### [标题](URL)

- **目录/结构**: 列出报告的主要章节或部分，e.g. "第1章 市场规模 · 第2章 竞争格局 · 第3章 政策环境 · 附录 数据表"
- **核心内容**: 一句话说明这份资料解决了什么问题
- **检索提示**: 后续写报告时，哪个主题应查此文件的哪个章节，e.g. "市场规模数据→第2章；政策梳理→第4章"

## 亮点数据

List specific figures, statistics, or findings worth quoting directly. Use bullet format:

- **数据点**: 具体数字或结论 | 来源: [机构名](URL) | 页码/章节（如知道）

## 资料覆盖评估

- **偏向类型**: 本次搜索以哪类资料为主（e.g. 咨询报告为主，缺乏监管/官方数据）
- **明显缺口**: 哪个角度或数据点没有找到权威来源

## 缺口与受限来源

List sources that exist but could not be fully accessed:

- [来源名称](landing page URL) | 原因: client-only / paywalled / no public PDF | 备注
```

## Saving Rules

- Always create the `research/` directory if it does not exist before writing.
- Do not alter or summarize sources beyond what was returned in the search — the record is a faithful archive, not an editorial rewrite.
- Omit any section that has no content (e.g. if no gaps exist, omit "缺口与受限来源").
- Keep the file self-contained: a reader who has not seen the conversation should be able to understand what was searched and what was found.
