# Broker Research Playbook

Use this file when the user asks for sell-side, broker, bank, strategy, sector, macro, or analyst research.

## Goal

Find the highest-quality accessible version of the research while preserving source legitimacy and access labeling.

## What Counts as a Good Result

Prefer, in order:
1. official public PDF on the institution's own site
2. official landing page with title, desk or analyst, date, and abstract
3. authorized portal or event page that clearly identifies the institution
4. secondary mirror only when nothing better is public

## Broker Research Types

### Public and usually acceptable

- annual outlook books
- sector outlooks
- thematic strategy notes
- macro outlooks
- conference decks
- primer documents
- public insights and thought-leadership PDFs

### Often gated

- company initiation notes
- earnings preview or review notes
- valuation updates
- subscriber-only sector notes
- analyst portal downloads

### High-risk sources

- file-host mirrors with no provenance
- reposts on forums or blogs
- PDFs stripped of publisher context

## Search Pattern

### 1. Identify the institution

Normalize:
- institution English name
- local-language brand name if relevant
- research division name if distinct

### 2. Search official public hubs first

Look for:
- insights pages
- research pages
- thought-leadership sections
- conference or events pages
- annual outlook collections

### 3. Search for document class

Combine institution with:
- `outlook`
- `strategy`
- `sector`
- `macro`
- `primer`
- `conference`
- `pdf`
- `研报`
- `策略`
- `行业`
- `宏观`

### 4. Verify access state

Assign one label:
- `official PDF`
- `official page`
- `licensed/paywalled`
- `secondary mirror`

Do not blur these categories.

## Output Fields

For each source, capture:
- institution
- document title
- analyst, desk, or research team when visible
- publication date
- topic or sector
- access label
- official page URL
- direct PDF URL when available

## Decision Rules

### When only a gated official page exists

- keep the source
- label `licensed/paywalled`
- summarize why it is relevant from visible metadata
- avoid substituting a dubious repost as if it were equivalent

### When only a mirror PDF exists

- keep it only if the topic is otherwise blocked and the user values completeness over purity
- label `secondary mirror`
- state that the original public copy was not found

### When many near-duplicate notes appear

Prefer:
1. institution flagship piece over short note
2. newest version within the user's time window
3. broader sector or thematic note over company-specific maintenance note unless the user asked for company coverage

## China-Specific Heuristics

Use Chinese institution names and document classes aggressively.

Common query terms:
- `研究所`
- `行业深度`
- `策略年度`
- `晨会纪要`
- `专题报告`
- `深度报告`

Default rule:
- prefer official research institute or broker insight pages
- if the market mainly exposes report metadata rather than PDFs, return the metadata and official path first

## Global Bank Heuristics

Use these classes before broad web search:
- investment bank insights hubs
- global research outlook pages
- conference presentation pages
- public policy or market commentary pages

If the institution separates marketing insights from licensed research:
- keep both when relevant
- treat the marketing insight as public support material
- treat the licensed note as `licensed/paywalled`

## Avoid

- implying a repost is authorized
- omitting access restrictions
- using a tertiary summary when an official page exists
- mixing public thought leadership with analyst research without labeling the difference
