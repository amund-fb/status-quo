# Friendly Beast — Status Quo

## What this project is
A weekly AI intelligence newsletter for Friendly Beast, generated as a static HTML file. Claude searches the web, compiles the news, and writes a self-contained `.html` file that opens directly in any browser. No server, no API key, no dependencies.

## How to generate a newsletter

Two modes:
- **"run"** — one-shot, no review. Searches and builds the full newsletter in one pass.
- **"jog"** — two-step with review. Shows research first, waits for approval, then builds.

### Research (8 searches across 3 tiers)
- **Tier A** (3) — Anthropic/Claude/MCP, OpenAI/GPT, Google/Gemini/Meta/Llama/Mistral/Qwen
- **Tier B** (2) — Stack tools (Notion/BigQuery/Workspace/Cowork/pricing/open-source), AI consulting/agents/boutiques
- **Tier C** (3) — Consumer brands/CPG/PE/portfolio companies, PE/value creation/operational efficiency, X/Twitter signals (1,000+ likes)

### Compile into structured sections
- **Models & benchmarks** (◆ green) — model releases, benchmark scores, capability shifts
- **Stack & MCP ecosystem** (◇ yellow) — tools, MCP servers, API changes, developer tooling
- **AI-native consultancy plays** (△ white) — strategy, service models, AI analyst teams. Use 3 Systems framework (demand/distribution/supply) for relevance.
- **Industry & pricing shifts** (○ green) — competitive moves, pricing, market structure
- **Signals from X** (◎ blue) — high-engagement tweets (1,000+ likes) grouped by section
- **Things to try this week** (▸ green) — 5 actionable experiments with effort estimates
- **Watch next week** — 5 items with specific dates/triggers
- **Analyst note** — paragraph connecting the biggest trend to the 50M NOK/year mission

### Write the HTML file
Use `template.html` as the exact format reference. Key structure:
- `body` has `padding-left: 200px` for sidebar space
- `.main-content` wrapper with `max-width: 720px; margin: 0 auto` for centering
- Sidebar nav (`<nav class="sidebar-nav">`) is outside `.main-content`
- All sections need `id` attributes for sidebar links (top, summary, models, stack, consultancy, industry, signals, try, watchlist, analyst)
- Summary includes `<ul>` with 3–5 bullet points above the summary paragraph

Save as `REPORT_Friendly-Beast_YYYY-MM-DD_Status-Quo.html`.

### Relevance filtering
Every item must pass at least one filter:
- **Stack:** Affects Claude, MCP, Notion, BigQuery, Google Workspace, Slack, Claude Code, Cowork
- **Capability:** Changes what we can build or deliver for clients
- **Client (3 Systems):** Affects demand, distribution, or supply systems for consumer brands, PE firms, holding companies
- **Competitive:** Affects how AI-native boutiques compete vs. traditional consulting
- **Timing:** Requires action this week or next

## About Friendly Beast
AI-native operating partner to owners and investors in consumer goods brands. Oslo, Norway. PE firms, holding companies, family offices, founders.

### The stack
- **Claude** — orchestration layer via MCP (Projects, Skills, Cowork, Code)
- **Notion** — structured knowledge, client workspaces, IP library
- **Google Workspace** — email, calendar, Drive
- **BigQuery** — quantitative data, client metrics, financial pipelines
- **Slack** — async comms via MCP
- **Microsoft Office** — PowerPoint decks, Excel models, Word docs

### Business model
Monthly flat fee, single invoice, equity/fee hybrid options. Journey / Intervention / Rental. Target: 50M NOK/year boutique with <5 people and 50% operating EBITDA.

## Writing guidelines
- 2–3 cards per section with specific numbers, model names, benchmark scores, and pricing
- Every relevance note must name a specific tool, workflow, or client type — never generic
- Write like FT/Bloomberg — lead with the news, numbers first, no marketing language
- Analyst note connects to the 50M NOK/year mission
- Things to try reference actual tools: Claude Code, MCP, BigQuery, Notion, Cowork
- X/Twitter signals: 1,000+ likes minimum, extract the insight
- Source URLs required for every claim

## Template
`template.html` contains the exact HTML/CSS structure. Match it precisely — same fonts, colors, spacing, class names, `.main-content` wrapper, sidebar nav. Only change the content.

## Brand
- Green: #3AE49D
- Yellow: #FFF766
- Black: #000000
- Fonts: DM Sans (headings, labels), Newsreader (body text)
