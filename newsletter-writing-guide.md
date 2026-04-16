# Status Quo — Writing Guide

## What this is

A weekly AI intelligence newsletter for Friendly Beast, generated as a self-contained static HTML file. No server, no API key, no JavaScript. Pure hardcoded HTML that opens in any browser.

## Output format

A single `.html` file named `REPORT_Friendly-Beast_YYYY-MM-DD_Status-Quo.html`. Use `template.html` as the exact CSS and structural reference — match all class names, colors, spacing, and layout precisely. Only change the content.

## Sections

The newsletter has four main content sections, each with 2–4 cards:

### 1. Models & Benchmarks (◆ green)
Model releases, benchmark scores, capability shifts. Include specific numbers: parameter counts, benchmark percentages, pricing per million tokens, release dates.

### 2. Stack & MCP Ecosystem (◇ yellow)
Tools, MCP servers, API changes, developer tooling, Claude Code/Cowork updates. Focus on what's new in Friendly Beast's actual stack.

### 3. AI-Native Consultancy Plays (△ white)
Strategy, service models, AI analyst teams, consulting industry shifts. Connect every item to how a <5 person AI-native firm operates. Frame relevance through the 3 Systems of Markets (see `3-systems-framework.md`): does the news affect client demand systems, distribution systems, or supply systems? Name the system and the bottleneck it addresses.

### 4. Industry & Pricing Shifts (○ green)
Competitive moves, pricing changes, open-source releases, licensing, market structure.

### Additional sections (in order after the four main sections):

**Signals from X (◎ blue)**
5 cards showing high-engagement X/Twitter posts (1,000+ likes minimum). Group by the section they relate to. Each card links to the actual tweet and shows: @handle, engagement count, and the core insight extracted from the post — not just "someone tweeted about X."

**Things to Try This Week (▸ green)**
5 actionable experiments with effort labels: `30 min`, `1 hour`, `half day`, `this sprint`. Each has an action line and a why line. Must reference actual tools: Claude Code, MCP, BigQuery, Notion, Cowork, ant CLI. Prioritize quick wins but include one ambitious item.

**Watch Next Week**
5 items with specific dates or triggers. These are forward-looking: upcoming releases, deadlines, decisions to make.

**Summary bullets**
The summary section opens with 3–5 bullet points — one-line takeaways that let the reader scan the week in seconds. Each bullet starts with the key fact or number. These appear as a `<ul>` above the summary paragraph in the template.

**Analyst Note**
One paragraph (3–5 sentences) connecting the week's biggest theme to Friendly Beast's 50M NOK/year mission. Written in italic. Opinionated, not neutral.

## Card structure

Every card in the four main sections must have:
1. **Title** — specific headline with numbers or names, not vague
2. **Body** — 2–3 sentences with specific data (benchmark scores, pricing, dates, parameter counts)
3. **Relevance note** — 1–2 sentences tied to Friendly Beast's stack, clients, or mission. Uses the section's relevance color class (`relevance-green`, `relevance-yellow`, or `relevance-white`)
4. **Sources** — 1–3 linked source URLs. Never fabricate URLs — only use URLs found via web search

## Editorial style — write like FT, not like a blog

This newsletter should read like a professional business intelligence briefing. Model it on the Financial Times, Bloomberg, and Forbes — not on Medium posts, corporate blogs, or marketing copy.

### Rules

1. **Lead with the news.** First sentence = what happened, who did it, and the single most important number. Never open with context, background, or "In a move that..."
2. **Numbers in the first sentence.** Benchmark scores, pricing, parameter counts, dates — the hard data goes up top, not buried in paragraph two.
3. **Active voice, short sentences.** "Anthropic launched X" not "X was launched by Anthropic." Cut every sentence that doesn't add information.
4. **Attribution.** "the company said," "according to," "benchmarks show" — state your source, don't narrate omnisciently.
5. **Answer "so what?" immediately.** After stating the fact, the next sentence explains why it matters. Never leave the reader guessing.
6. **Comparisons that give scale.** "58.4% — edging past GPT-5.4 at 57.7%" is useful. "Strong performance" is not.
7. **No marketing language.** Ban: "groundbreaking," "game-changing," "revolutionary," "exciting," "incredibly," "unleashing." These are press release words.
8. **No filler phrases.** Ban: "it's worth noting that," "interestingly," "in today's rapidly evolving landscape," "it remains to be seen," "needless to say," "as we all know."
9. **No exclamation marks.** Ever.
10. **Understated confidence.** State the facts, draw a sharp conclusion, move on. The tone is a senior analyst briefing a partner — not a blogger trying to impress.

### Anti-patterns — never write like this

Bad: "In an exciting development that could reshape the AI landscape, OpenAI has announced a groundbreaking new model that pushes the boundaries of what's possible."

Good: "OpenAI released GPT-5.5 on April 28 with a 4M-token context window and 91% on SWE-bench Verified, a 6-point jump over GPT-5.4. Pricing holds flat at $2.50/$12 per million tokens — the third consecutive release where OpenAI has absorbed capability gains instead of raising prices."

Bad: "This is really important for Friendly Beast because it means we can potentially leverage this technology to improve our workflows."

Good: "Test GPT-5.5 on the BigQuery→docx pipeline this week. The 4M context window means we can feed an entire quarter of client data in a single pass — something that currently requires chunking across three Opus calls."

## Tone

In addition to the editorial rules above:

- Direct and opinionated — this is an internal briefing, not a press release
- Specific over vague — "scored 58.4% on SWE-Bench Pro" not "performed well on benchmarks"
- Forward-looking — what should Friendly Beast do about this?
- Confident but honest — flag uncertainty, don't overstate claims

## Research process

Run exactly 8 web searches across three tiers:

**Tier A — Frontier models & providers (3 searches):**
Anthropic/Claude/MCP, OpenAI/GPT, Google/Gemini/Meta/Llama/Mistral/Qwen.

**Tier B — Friendly Beast stack (2 searches):**
AI pricing/open-source/Notion/BigQuery/Workspace/Cowork, AI consulting/agents/boutiques/fractional.

**Tier C — Client context & signals (3 searches):**
Consumer brands/CPG/retail/demand forecasting/portfolio companies, PE/value creation/operational efficiency, X/Twitter (1,000+ likes).

8 searches is the hard limit — claude.ai caps tool calls per response. Tier B and C are what makes this newsletter ours, not a generic AI roundup. Never skip them.

## Relevance filtering

Every item must pass at least one filter before inclusion:

- **Stack filter:** Affects a tool we use (Claude, MCP, Notion, BigQuery, Google Workspace, Slack, Claude Code, Cowork)
- **Capability filter:** Changes what we can build or deliver for clients
- **Client filter (3 Systems):** Affects demand, distribution, or supply systems for consumer brands, PE firms, holding companies, or portfolio ops
- **Competitive filter:** Affects how AI-native boutiques compete vs. traditional consulting
- **Timing filter:** Requires action this week or next

Drop interesting-but-generic AI news. If an item only passes weakly, it goes in the watchlist, not a main card.

## Source trust tiers

**Tier 1 — Primary sources (always trust, always prefer):**
Official blogs and docs: anthropic.com, openai.com, blog.google, ai.meta.com, mistral.ai, docs.anthropic.com, platform.claude.com, ai.google.dev, modelcontextprotocol.io, linuxfoundation.org

**Tier 2 — Established press & industry research (trust, good for context):**
Tech press: The Verge, TechCrunch, Ars Technica, Bloomberg, Reuters, Financial Times, InfoQ, The New Stack, Wired, 9to5Google, VentureBeat, Hacker News (top stories)
Consulting & strategy: McKinsey, BCG, Bain, Deloitte, Gartner, Forrester, Harvard Business Review, CB Insights, a16z, Sequoia, AlphaSense, Consultancy.org

**Tier 3 — Specialist AI coverage (trust with attribution):**
BenchLM.ai, HuggingFace blog, arXiv papers, Weights & Biases blog, Simon Willison's blog, The Information

**Tier 4 — Use with caution (verify claims against Tier 1–3):**
Medium posts, Substack newsletters, LinkedIn articles, personal blogs, SEO content farms

**Never use:**
AI-generated news aggregators with no editorial oversight, sites that rewrite press releases without attribution, anything without a byline or clear source

When a claim only appears in Tier 4 sources, flag it with "according to" attribution or move it to watchlist instead of a main card.

## Verification

For main section cards:
- Key claims (benchmarks, pricing, dates) must appear in at least one Tier 1 or Tier 2 source
- Tier 3-only claims get "according to" attribution
- Tier 4-only claims go in watchlist, not main cards
- Never include numbers you can't trace to a source URL

## Golden examples — match this quality

These are the standard. Every card, signal, and action item in the newsletter should be written at this level.

### Example news card (Models & Benchmarks)

**Title:** Z.ai's GLM-5.1 takes #1 on SWE-Bench Pro — 744B parameters, MIT license

**Body:** Z.ai released GLM-5.1 on April 7, a 744-billion-parameter mixture-of-experts model with 40B active parameters per token and a 200K context window. It scored 58.4% on SWE-Bench Pro, edging past GPT-5.4 at 57.7% and Claude Opus 4.6 at 57.3%. Released under the MIT license with full weights on HuggingFace.

**Relevance:** The most capable fully open model ever released, and it's MIT-licensed — zero restrictions on commercial use. For cost-sensitive recurring client tasks (inventory forecasting, weekly data pulls), self-hosted GLM-5.1 could eliminate API costs entirely. Worth benchmarking against Sonnet on our demand forecasting pipeline.

**Why this works:**
- Title has the who, the what, and two key numbers
- First sentence: who did it, when, and the core specs
- Second sentence: the benchmark result with direct comparisons to competitors
- Third sentence: availability and licensing — the "so what" for builders
- Relevance connects to a specific Friendly Beast workflow, names a tool, and ends with a concrete next step

### Example X signal card

**@handle:** @alvinfoo
**Engagement:** viral thread
**Insight:** Anthropic just quietly shipped something that could change how every founder builds AI products. It's called Claude Managed Agents, and most people haven't figured out what it actually means yet. Until now, deploying an AI agent meant building your own orchestration from scratch.

**Why this works:**
- Extracts the actual insight from the thread, not just "someone tweeted about Managed Agents"
- The handle and engagement give credibility context
- The insight stands alone — a reader who never opens the link still gets the takeaway

### Example Things to Try item

**Effort:** 30 min
**Action:** Set up ant CLI and version one client's Claude Project config in git
**Why:** The ant CLI supports YAML-based resource versioning. Export an existing client's system prompt, MCP servers, and skills to YAML, commit to a repo, and test redeployment. If this works, every client gets reproducible Claude Project deployments.

**Why this works:**
- Action is a single imperative sentence — do this specific thing
- Effort estimate is honest (30 min for a setup + test, not a full migration)
- Why explains what the tool does, what to test, and what success looks like
- References actual tools in our stack (ant CLI, MCP servers, Claude Projects)
- Ends with the payoff: what changes if this works
