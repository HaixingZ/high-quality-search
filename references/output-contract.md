# Output Contract

Default to Chinese unless the user asks otherwise. Keep original document titles in their source language.

## Standard Response Shape

### 1. 检索摘要

- `主题`:
- `地域/市场`:
- `时间范围`:
- `来源偏好`:
- `说明`:

### 2. 必读原文

Use a compact table when there are 3 or more sources. Otherwise use bullets.

Recommended columns:
- `标题`
- `机构`
- `日期`
- `类型`
- `访问`
- `价值`
- `官方页`
- `PDF`

Access labels:
- `official PDF`
- `official page`
- `licensed/paywalled`
- `secondary mirror`

Type labels:
- `consulting report`
- `white paper`
- `broker research`
- `regulator/exchange`
- `company IR`
- `association/standard`

### 3. 补充来源

Include only if they add adjacent evidence, alternate angles, or supporting data.

### 4. 缺口与受限来源

State clearly when:
- only a landing page exists
- a report is client-only or behind login
- only secondary mirrors were found
- the requested source type appears scarce for the topic

### 5. 下一步检索

Offer 2-5 sharp next moves only when the first pass is incomplete.

## Selection Rules

- Lead with the strongest original PDF, not the most famous brand.
- Prefer 5-10 high-signal items over a long weak list.
- Collapse duplicates aggressively.
- If the user explicitly asked for PDF originals, show `PDF` before `官方页` in bullets.
- If no public PDF exists, say `无公开 PDF，仅官方页面`.

## Bullet Format

Use this when the list is short:

- `标题` | 机构 | 日期 | 类型 | 访问
  `价值`: one sentence
  `官方页`: URL
  `PDF`: URL or `无公开 PDF`

## What To Avoid

- long narrative summaries before the source list
- unlabeled mirrors
- mixing official pages and reposts without distinction
- returning broken or irrelevant PDF links just to fill the list
