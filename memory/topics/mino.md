# mino.md

## Project
- Workspace is the assistant's home environment for MyAgents-related work and personal agent continuity.
- Work in this topic now has two major tracks: evidence-heavy nutrition/business research deliverables and a local-first nutrition web demo built from recovered static assets. (2026-03-31)

## Recent Work
- Reframed provider research away from C-end nutrition/weight-loss apps toward B2B enterprise nutrition services, especially团餐/企业食堂/营养配餐 providers.
- Produced three deliverables in `workspace/`:
  - `B2B企业营养服务商汇总.xlsx`
  - `B2B营养服务TOP5对比海报.html`
  - `小红书文案-B2B企业营养服务TOP5对比.docx`
- Supporting scripts were also created in `workspace/` for generating the spreadsheet and Word document.
- A later长沙网球场选址 request established a stricter evidence bar: the user only wants真实公告/招租/公示数据 with source links, not templates or inferred opportunity maps.
- Recovered a Google/Gemini-related local bundle and turned it into a local static nutrition demo with a shell page, iframe bridge, Gemini local fallback, and public-deployable `dist/` package. (2026-03-31)
- Ingested `中国食物成分表.xls` into `dist/food-composition.json`, registered uploaded PDF guides in `dist/knowledge-base.json`, and added visible knowledge sections plus food search to `dist/index.html`. (2026-03-31)
- Verified the local visual demo is reachable at `http://127.0.0.1:8787`. Public launch was intentionally paused pending user confirmation. (2026-03-31)
- Deployed a separate nutrition analyzer (MACROS) to GitHub Pages at `https://worldtena646-blip.github.io/vicky/` — a Vue.js-based nutritional content analyzer with food database and macro tracking. (2026-04-01)
- Installed and learned 10 MCP servers (Playwright, GitHub, Puppeteer, Memory, File System, Sequential Thinking, Fetch, SQLite, Brave Search, Douyin) and multiple Skills including seedance-prompt-skill, skill-creator, internal-comms. Created comprehensive learning notes in `workspace/`. (2026-04-01)

## What Worked
- Using public company pages, industry rankings, annual reports, and business press was good enough to assemble a practical first-pass provider list quickly.
- International + China hybrid framing made the comparison more useful than a China-only list.
- Being blunt about evidence gaps is better than filling space with plausible but unverified venue recommendations.
- For the recovered web bundle, a wrapper-shell approach worked: keep the child app mostly intact, patch the parent bridge, localize CDN assets, and stub only the online-only pieces. (2026-03-31)
- Even when PDF extraction tooling was missing, structuring the available `.xls` data and surfacing it visibly in the UI still moved the project forward. (2026-03-31)

## What Didn't
- Initial provider selection was too C-end oriented and got rejected. The user wanted enterprise nutrition service vendors with real-world company data, not consumer apps.
- Some Chinese company metrics are only partially public; a few figures had to remain rough/estimated pending stricter scraping or primary-source verification.
- Browser scraping setup was blocked by local Playwright browser-install issues, so the work relied on public-source collection rather than a fully automated crawl.
- A generic "template first" response for the tennis-site request was rejected because the user wanted only real, linked data.
- The uploaded PDFs could not be deeply extracted locally because `pdftoppm`/poppler tooling was unavailable, so they were only registered as sources for now. (2026-03-31)

## Decisions
- Treat this topic as B2B团餐/企业食堂营养服务, not general nutrition products. (2026-03-30)
- Prefer real-world, company-level data and high-star scraping/tooling references over generic market summaries. (2026-03-30)
- For location/opportunity scouting tasks, only present candidates that are backed by concrete public notices or source links when the user asks for真实数据. (2026-03-31)
- For the nutrition web demo, ship local-first: show a working visual local project before any public deployment, and only publish after user confirmation. (2026-03-31)

## Next Time
- If the nutrition/business research track continues, tighten the dataset by verifying each provider with primary pages and, where possible, automate collection using a stable scraping stack.
- Revisit estimated Chinese provider figures before presenting them as definitive.
- For public-opportunity searches like场地/招租/公示, narrow geography and source scope early and output only link-backed items.
- For the nutrition web demo, continue enriching Chinese nutrition knowledge, try a stronger PDF extraction path, and only then complete GitHub Pages/public deployment after the user signs off on the local version. (2026-03-31)
- The MACROS nutrition analyzer is now live on GitHub Pages; future iterations could add more foods or features if requested. (2026-04-01)
- MCP/Skill installation workflow: use `myagents` CLI for MCP servers, copy Skill folders to `.claude/skills/` for Skills. Both require validation that the tool actually loads in the next session. (2026-04-01)
