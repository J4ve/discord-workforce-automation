# Graph Report - discord-workforce-automation  (2026-10-23)

## Corpus Check
- Large corpus: 500 files · ~680,437 words. Semantic extraction will be expensive (many Claude tokens). Consider running on a subfolder.

## Summary
- 8 nodes · 14 edges · 3 communities (2 shown, 1 thin omitted)
- Extraction: 100% EXTRACTED · 0% INFERRED · 0% AMBIGUOUS
- Token cost: 0 input · 0 output

## Community Hubs (Navigation)
- Enterprise Workforce Automation Bot
- Outbound aiohttp sync with
- Enterprise Workforce Automation &

## God Nodes (most connected - your core abstractions)
1. `Enterprise Workforce Automation Bot - Case Study README` - 7 edges
2. `Enterprise Workforce Automation & Community Gateway Bot (discord.py)` - 5 edges
3. `Outbound aiohttp sync with Next.js HR platform` - 4 edges
4. `Operational metrics & gamification engine (leaderboards, milestone badges)` - 3 edges
5. `Automated shift & schedule reminder workers` - 3 edges
6. `Modular Cog-based slash commands (discord.py app_commands)` - 2 edges
7. `Embedded SQLite persistence (hand-tuned schema, no ORM)` - 2 edges
8. `Pure outbound gateway architecture (zero inbound HTTP ports)` - 2 edges

## Surprising Connections (you probably didn't know these)
- `Enterprise Workforce Automation Bot - Case Study README` --references--> `Modular Cog-based slash commands (discord.py app_commands)`  [EXTRACTED]
  README.md → README.md  _Bridges community 0 → community 2_
- `Enterprise Workforce Automation Bot - Case Study README` --references--> `Outbound aiohttp sync with Next.js HR platform`  [EXTRACTED]
  README.md → README.md  _Bridges community 0 → community 1_
- `Enterprise Workforce Automation & Community Gateway Bot (discord.py)` --references--> `Outbound aiohttp sync with Next.js HR platform`  [EXTRACTED]
  README.md → README.md  _Bridges community 2 → community 1_

## Communities (3 total, 1 thin omitted)

### Community 0 - "Enterprise Workforce Automation Bot"
Cohesion: 1.00
Nodes (3): Enterprise Workforce Automation Bot - Case Study README, Operational metrics & gamification engine (leaderboards, milestone badges), Embedded SQLite persistence (hand-tuned schema, no ORM)

### Community 1 - "Outbound aiohttp sync with"
Cohesion: 0.67
Nodes (3): Outbound aiohttp sync with Next.js HR platform, Pure outbound gateway architecture (zero inbound HTTP ports), Automated shift & schedule reminder workers

## Knowledge Gaps
- **1 thin communities (<3 nodes) omitted from report** — run `graphify query` to explore isolated nodes.

## Suggested Questions
_Questions this graph is uniquely positioned to answer:_

- **Why does `Enterprise Workforce Automation Bot - Case Study README` connect `Enterprise Workforce Automation Bot` to `Outbound aiohttp sync with`, `Enterprise Workforce Automation &`?**
  _High betweenness centrality (0.476) - this node is a cross-community bridge._
- **Why does `Enterprise Workforce Automation & Community Gateway Bot (discord.py)` connect `Enterprise Workforce Automation &` to `Enterprise Workforce Automation Bot`, `Outbound aiohttp sync with`?**
  _High betweenness centrality (0.119) - this node is a cross-community bridge._
- **Why does `Outbound aiohttp sync with Next.js HR platform` connect `Outbound aiohttp sync with` to `Enterprise Workforce Automation Bot`, `Enterprise Workforce Automation &`?**
  _High betweenness centrality (0.048) - this node is a cross-community bridge._