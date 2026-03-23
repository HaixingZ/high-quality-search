---
name: high-quality-source-research
description: Collect high-quality primary research materials and original downloadable documents for business, market, industry, and company topics. Use when Codex needs to find consulting-firm PDFs, white papers, regulator or exchange publications, company investor-relations decks, standards or association reports, and publicly accessible or licensed broker research; prioritize official source pages and direct PDF links, separate originals from secondary summaries, and clearly label paywalls, mirrors, and confidence.
---

# High Quality Source Research

Use this skill to gather high-quality, citation-ready materials with a strong bias toward official source pages and original PDF files.

## Quick Start

1. Clarify only missing boundaries: topic, geography, time window, language, source types, and whether paywalled sources are acceptable.
2. Default to the last 3 years, Chinese plus English search terms, and publicly accessible sources when the user does not specify.
3. Search in source priority order: official publisher page first, original PDF second, authorized index or archive third.
4. Prefer source packets over long prose. Return the direct PDF link when available and the official landing page when it is not.
5. Mark every item as `official PDF`, `official page`, `licensed/paywalled`, or `secondary mirror`.

## Workflow

### 1. Frame the request

- Convert the ask into tight facets: subject, geography, year range, issuer types, document types, and excluded source classes.
- Add bilingual terms when the topic spans Chinese and English source ecosystems.
- For broker research, distinguish between public thought leadership and client-only research. Do not assume unofficial redistribution is acceptable.

### 2. Search by source priority

- Read [references/source-priority.md](references/source-priority.md) before broad searching.
- Read [references/china-global-source-map.md](references/china-global-source-map.md) when the request spans China, the US, Europe, regulators, exchanges, or multilateral institutions.
- Start from likely publishers and constrain by domain whenever possible.
- Use [references/query-patterns.md](references/query-patterns.md) to generate query sets for official domains, PDF filters, and landing-page fallbacks.
- Read [references/broker-research-playbook.md](references/broker-research-playbook.md) when the user asks for broker, bank, strategy, macro, sector, or analyst research.
- Expand to wider web search only after likely official domains are exhausted.

### 3. Verify the document

- Confirm the title, publisher, publication date, and whether the file is the original.
- Prefer the publisher's own PDF URL. If only HTML is official, return the official page and note `no public PDF`.
- For broker research, treat publicly posted notes, outlooks, and strategy pieces as valid. If access requires subscription or client login, keep the source in the list but label it `licensed/paywalled`.
- Avoid presenting unofficial mirrors as originals. If a mirror is the only public copy, label it clearly and state the risk.

### 4. Rank and trim

- Rank by authority, relevance, recency, and originality.
- Remove thin summaries, SEO pages, and reposts when a better original exists.
- Keep duplication low: if multiple sites host the same PDF, keep the original host and at most one backup mirror.

### 5. Deliver a source packet

- Read [references/output-contract.md](references/output-contract.md) before responding.
- Default to a compact table or bullet packet, not an essay.
- Separate `must-read originals`, `useful supporting sources`, and `gaps / blocked sources`.
- When the user asks for `原文` or `pdf`, surface the direct PDF link first.

### 6. Save a search record

- Read [references/search-record-format.md](references/search-record-format.md) before saving.
- After delivering results, write a `.md` archive file to the `research/` subdirectory of the current working directory.
- File name: `主题-YYMMDD.md` (e.g. `新能源汽车市场-260323.md`).
- The record must include: source list with `[title](URL)` links, per-source content summary with document structure/TOC and retrieval hints, standout data points, coverage assessment, gaps, and the queries used.
- Tell the user where the file was saved after writing it.

## Guardrails

- Prefer official publisher domains, regulators, exchanges, company IR sites, standards bodies, top consulting firms, and authorized research portals.
- Prefer primary documents over commentary about documents.
- State when a document is paywalled, client-only, or requires login.
- Do not imply that unofficial reposts are licensed.
- Do not fabricate PDF availability. If no public PDF exists, say so explicitly.
- Preserve original titles and add a Chinese gloss only when it improves scanability.
- When the request is broad, stop after a high-signal first pass rather than dumping dozens of weak links.

## References

- Read [references/source-priority.md](references/source-priority.md) to decide which issuers, publishers, and channels deserve first-pass attention.
- Read [references/china-global-source-map.md](references/china-global-source-map.md) when you need a fast shortlist of likely official domains across China, the US, Europe, multilateral institutions, associations, and company IR channels.
- Read [references/query-patterns.md](references/query-patterns.md) when building search operators, bilingual variants, and fallback queries.
- Read [references/broker-research-playbook.md](references/broker-research-playbook.md) when collecting sell-side or bank research and deciding how to label public, gated, or mirrored copies.
- Read [references/output-contract.md](references/output-contract.md) before delivering results so the response stays compact and decision-ready.
- Read [references/search-record-format.md](references/search-record-format.md) before saving the post-search archive file.
