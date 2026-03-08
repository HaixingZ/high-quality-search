# Query Patterns

Use a narrow-to-broad search loop. Start with the likely issuer. Expand only after official paths fail.

## Core Operators

- `site:domain.tld`
- `filetype:pdf`
- quoted phrases for exact titles or topic terms
- year filters such as `2024`, `2025`, or a specific month
- bilingual variants of the topic, issuer, and document type

## Search Loop

### 1. Official-domain PDF lookup

Use when the likely publisher is known.

Examples:
- `"semiconductor" filetype:pdf site:mckinsey.com`
- `"电动车" filetype:pdf site:bcg.com`
- `"AI infrastructure" "white paper" filetype:pdf site:company-domain`

### 2. Official landing-page lookup

Use when the PDF is not indexed directly.

Examples:
- `"semiconductor report" site:mckinsey.com`
- `"生成式 AI" "白皮书" site:issuer-domain`
- `"2025 outlook" site:institution-domain`

### 3. Title-led lookup

Use when you already have a probable document title from discovery.

Examples:
- `"The State of AI in 2025" pdf`
- `"中国汽车行业白皮书" pdf`
- `"global chemicals outlook 2025" pdf`

### 4. Broker research lookup

Use official institution names plus document intent.

Public research patterns:
- `"institution name" sector outlook pdf`
- `"institution name" thematic report pdf`
- `"institution name" strategy outlook pdf`
- `"券商名" 行业 研报 pdf`
- `"券商名" 策略展望 pdf`

Access-aware fallback patterns:
- `"institution name" research portal sector`
- `"institution name" insights market outlook`
- `"券商名" 研究所 行业 观点`

If official pages exist but the PDF is gated:
- return the official page
- mark `licensed/paywalled`
- do not replace it with an unverified mirror unless the user explicitly accepts mirrors

### 5. White paper lookup

Use issuer plus document class.

Examples:
- `"topic" "white paper" pdf "issuer"`
- `"topic" 白皮书 pdf 机构名`
- `"topic" report pdf association`

### 6. Regulator and exchange lookup

Use topic plus document class and jurisdiction.

Examples:
- `"short selling" report pdf regulator`
- `"数据要素" 指南 pdf 监管`
- `"listing rules" consultation paper pdf exchange`

## Bilingual Expansion

When the topic has both Chinese and English ecosystems:

1. Search English topic + English document types.
2. Search Chinese topic + Chinese document types.
3. Search mixed forms when institution names are English but the market is Chinese.

Document-type expansions:
- `report`
- `white paper`
- `outlook`
- `primer`
- `deck`
- `annual report`
- `investor presentation`
- `报告`
- `白皮书`
- `洞察`
- `展望`
- `研报`
- `路演材料`
- `投资者演示`

## Failure Recovery

If direct PDF search fails:
1. search the official landing page
2. search the likely title without `site:`
3. search the topic plus issuer plus year
4. search the topic plus document class on adjacent official domains
5. only then inspect high-quality secondary references for the original title and publisher

## Output Discipline

For each kept source, capture:
- title
- publisher
- date
- source type
- access label
- official page URL
- direct PDF URL when available
- one-line reason it matters
