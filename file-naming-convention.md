# File Organizer — Friendly Beast Naming Convention

All files produced by this project must follow the Friendly Beast naming convention.

## The Format

```
TYPE_CLIENT_DATE_SUBJECT.ext
```

Four fields separated by **underscores**. Hyphens within fields. Title-Case-Hyphenated for multi-word values.

### Field Definitions

1. **TYPE** — Uppercase. Describes what the document *is*. Must come from the standardized type index below.
2. **CLIENT** — Title-Case-Hyphenated. The client or company the file belongs to.
3. **DATE** — Optional. Use `YYYY`, `YYYY-MM`, or `YYYY-MM-DD`. Omit if unknown.
4. **SUBJECT** — Title-Case-Hyphenated. Descriptive enough to identify the document without opening it.

### Newsletter output example

```
REPORT_Friendly-Beast_2026-04-14_Status-Quo.html
```

## Standardized TYPE Index

| TYPE | Use For | NOT For |
|------|---------|---------|
| **ASSET** | Images, logos, photos, design files (.jpg, .png, .ai, .eps, .webp) | — |
| **BRAND** | Brand guidelines, visual identity docs, brand platforms, brand books | Brand strategy (use STRAT) |
| **CONTRACT** | Agreements, NDAs, LOIs, term sheets, scope of services, MOUs | — |
| **DATA** | Raw data, CSVs, inventory lists, buy sheets, order forms, pricing files | Financial models (use FIN) |
| **FIN** | Budgets, P&Ls, financial reports, forecasts, business plans, valuations, cashflow models | Sales reports (use REPORT) |
| **FONT** | Font files (.otf, .ttf, .woff) and font license files | — |
| **HR** | Job descriptions, offer letters, org charts, handbooks, employment contracts | — |
| **LEGAL** | Trademarks, EULAs, copyright certificates, legal filings | Commercial contracts (use CONTRACT) |
| **MEETING** | Board meeting decks, workshop slides, meeting agendas, all-hands presentations | Monthly business reports (use REPORT) |
| **PITCH** | Investor decks, pitch decks, teaser decks, fundraising materials, partnership proposals | Internal company presentations (use PRES) |
| **PRES** | Company overviews, product presentations, sales tools, lookbooks, concept pitches, catalogues | Investor-facing materials (use PITCH) |
| **REPORT** | Sales reports, monthly reports, board reports, performance reviews, weekly business reports | Financial models (use FIN) |
| **RESEARCH** | Market research, case studies, competitor analysis, management diagnostics, investment memos | — |
| **STRAT** | Strategic plans, GTM plans, growth plans, roadmaps, turnaround plans, campaign plans | Financial forecasts (use FIN) |
| **TEMPLATE** | Slide templates, document templates, reusable frameworks | — |

## The 8 Rules

1. **One TYPE per file** — every file gets exactly one TYPE from the index above.
2. **Client name appears once** — never repeat the client name in the SUBJECT field.
3. **Expand all abbreviations** — no abbreviations in filenames. `FW25` → `Fall-Winter-2025`, `GTM` → `Go-To-Market`.
4. **Subjects must be descriptive** — "Deck" or "Notes" alone is too vague. Add context.
5. **Underscores between fields, hyphens within** — `FIN_Brain-Dead_2025_Quarterly-Budget-Review.xlsx`.
6. **Dates go in the middle** — between CLIENT and SUBJECT. Use most specific format available.
7. **Version numbers stay in SUBJECT** — keep `-V02`, `-V03` at end of SUBJECT.
8. **Infer client from folder** — if the client isn't in the filename, use the parent folder name.

## Workflow for organizing files

1. **Scan** — list all files with current names.
2. **Audit** — check each file against the 8 rules, flag violations.
3. **Read ambiguous files** — if TYPE or SUBJECT can't be determined from the filename, read contents.
4. **Propose** — present a table of renames (current → new → reason). Group by folder.
5. **Get approval** — never bulk-rename without user confirmation.
6. **Rename** — execute, logging every change.
7. **Report** — summary of files renamed, skipped, and errors.
