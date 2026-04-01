# MEMORY.md - Long-Term Memory

*Your curated memories. The distilled essence, not raw logs.*

## About This File & Memory System

- **Be mindful in shared contexts** — this file contains personal context about your human. In group chats or shared sessions, don't leak private preferences, decisions, or project details

### Three-Layer Memory

Your memory has three layers, each with different responsibilities and access patterns:

**Core memory (this file, 04-MEMORY.md)** — Auto-loaded every session
- What goes here: cross-project lessons, key decisions, user preferences, technical knowledge, one-line project summaries + pointers
- What doesn't: detailed project experience (that's what topic files are for)
- **Add a timestamp `(YYYY-MM-DD)` to each entry** — helps trace back, judge recency, clean up

**Topic memory (`memory/topics/<name>.md`)** — Read before working on a project
- What goes here: full accumulated experience for one project/topic — status, key facts, what you did, what worked, what didn't, decisions and rationale, next steps
- More detailed than core memory (which only has pointers), more synthesized than daily logs (which are raw chronological notes)
- Update during memory maintenance or when a project enters a new phase

**Daily journal (`memory/YYYY-MM-DD.md`)** — Read today + yesterday at session start
- What goes here: what happened that day, raw chronological record
- This is the source of all memory, but searching it for specific project info is inefficient (multiple projects mixed in one day)

### Information Flow

```
Daily logs (raw material) → topic files (synthesized per-project) → 04-MEMORY (cross-project essence)
```

- During work: just write the daily log
- During maintenance: sync from logs to topics, distill new cross-project lessons to this file
- **Information lives in one place only** — don't duplicate between topic files and 04-MEMORY

### When to Read What

- Just woke up → this file is already loaded + read today/yesterday's logs
- About to work on a project → read its `memory/topics/<name>.md`
- Memory maintenance → read all recent logs + all active topic files

---

## Lessons Learned

Organize by topic as your lessons grow. A flat list becomes unreadable fast.

### Working Style

- When a research task has a strong business-context constraint, validate the target category early instead of optimizing the wrong dataset. (2026-03-31)
- When the user asks for 真实数据, raise the evidence bar immediately: only output claims backed by concrete public sources or direct links, and say "not enough evidence yet" when the search comes up short. (2026-03-31)

### Communication

- 老刘 prefers direct, action-first Chinese communication and will quickly reject outputs that are off-target, so alignment should be shown through the work itself, not long explanation. (2026-03-31)
- If the deliverable is for practical use, file format matters: Markdown can be rejected even when the content is okay; provide WPS/Word-friendly output when asked. (2026-03-31)
- For evidence-seeking tasks, templates and generic frameworks are noise unless the user explicitly asks for them. (2026-03-31)

### Technical

- For company/vendor research, public rankings + company sites can bootstrap a useful list fast, but some private-company metrics remain fuzzy until validated by primary sources or stronger scraping. (2026-03-31)
- Local browser automation can fail on environment setup; keep a fallback path so progress does not depend on one scraping stack. (2026-03-31)
- Government/public bidding and leasing sites can be brittle to fetch and search, so narrowing geography plus source scope early is often necessary to get verifiable hits. (2026-03-31)
- For recovered static web bundles, the fastest path is often wrapper-shell restoration: localize remote assets, patch only the missing bridge/dependency points, and leave the embedded app mostly intact. (2026-03-31)
- When a knowledge-heavy demo is blocked on perfect extraction, ship a visible structured layer first from the data you can trust now, then deepen ingestion later. (2026-03-31)

## Important Decisions

- Treat the nutrition-provider research as B2B enterprise nutrition services (团餐/企业食堂/营养配餐), not consumer nutrition apps. (2026-03-31)

## User Preferences

- Call the user 老刘. (2026-03-31)
- They prefer real, scrapeable, verifiable data over generic summaries, especially for vendor research. (2026-03-31)
- When they say they want 真实数据, do not substitute templates, candidate maps, or plausible inference. (2026-03-31)

## Technical Knowledge

- High-star scraping tools relevant to future work here include Playwright, Scrapy, Selenium, and newer AI-assisted scraping projects; use them as references, but validate environment readiness before committing to an automation path. (2026-03-31)
- MyAgents uses the same Skill system as Claude Code; Skills go in `.claude/skills/` and auto-load. MCP servers are configured via `myagents` CLI and take effect on next session. (2026-04-01)
- Popular Skills follow a three-level loading pattern: metadata (name+description) always in context, SKILL.md body when triggered, bundled resources (scripts/references) on demand. (2026-04-01)

## Ongoing Context

- `memory/topics/mino.md` tracks the current workspace context. Recent work spans: B2B enterprise nutrition service research deliverables in `workspace/`, a local-first nutrition web demo in `dist/`, a deployed Vue.js nutrition analyzer (MACROS) live at `https://worldtena646-blip.github.io/vicky/`, and installation of 10 MCP servers + multiple Skills (seedance, skill-creator, internal-comms, etc.). (2026-04-01)

---

*Update this file as you learn. It's how you persist.*
