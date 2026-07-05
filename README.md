<!-- generated: DO NOT EDIT BY HAND — produced by apps/web/scripts/export-github-repos.ts from lib/agent/skills.ts + the workflow SSOT. Edit the config + re-run. -->

# ScoutingAPI Agent Skills

Portable **SKILL.md** agent skills for accommodation data across Airbnb, Booking.com, Vrbo and Google Hotels — one unified schema, REST + a native MCP server. Drop a skill into any agent runtime that reads `SKILL.md` (Claude, Codex, OpenClaw/ClawHub, Hermes, Smithery) and it learns to call the API for that task.

**[Get a free key — no card →](https://scoutingapi.com/signup)**

## Skills

- **[scoutingapi-search](skills/scoutingapi-search/SKILL.md)** — Search and compare accommodation prices across Airbnb, Booking.com, Vrbo and Google Hotels via the ScoutingAPI REST API. Use when a user wants to find stays, check availability, get a price, compare one property across OTAs, or read reviews. Covers Bearer auth, the async 202→poll job contract, the unified response envelope, and error handling.
- **[scoutingapi-mcp](skills/scoutingapi-mcp/SKILL.md)** — Connect an AI agent to the ScoutingAPI Model Context Protocol (MCP) server for accommodation search, availability, pricing, cross-OTA price comparison and reviews. Use when the agent runtime supports MCP connectors (e.g. Claude) and you want OAuth-based access without managing API keys. Covers the OAuth 2.1 + PKCE connect flow, the seven read-only tools, and when to prefer MCP vs REST.
- **[scoutingapi-cross-ota-price-comparison](skills/scoutingapi-cross-ota-price-comparison/SKILL.md)** — Compare one property across booking platforms and report the cheapest rate, with savings vs. the median. Powered by the ScoutingAPI REST API / MCP server.
- **[scoutingapi-availability-alert](skills/scoutingapi-availability-alert/SKILL.md)** — Watch a listing over a date window and get alerted the moment a wanted date becomes available. Powered by the ScoutingAPI REST API / MCP server.
- **[scoutingapi-price-drop-watcher](skills/scoutingapi-price-drop-watcher/SKILL.md)** — Watch a specific stay and get alerted the moment its total price falls to or below your threshold. Powered by the ScoutingAPI REST API / MCP server.
- **[scoutingapi-rate-parity-monitor](skills/scoutingapi-rate-parity-monitor/SKILL.md)** — Watch how your own listing's rate shows across OTAs on a schedule and flag any platform underselling the market median. Powered by the ScoutingAPI REST API / MCP server.
- **[scoutingapi-str-market-scan](skills/scoutingapi-str-market-scan/SKILL.md)** — Scan a short-term-rental market — discover listings across platforms, price the top N for your dates, and append a normalized row-per-listing dataset to a Google Sheet. Powered by the ScoutingAPI REST API / MCP server.
- **[scoutingapi-new-inventory-lead-gen](skills/scoutingapi-new-inventory-lead-gen/SKILL.md)** — Re-run a saved search on a schedule, diff it against the last run, and sync only the newly-listed properties into a CRM or Sheet as leads. Powered by the ScoutingAPI REST API / MCP server.
- **[scoutingapi-review-intelligence-digest](skills/scoutingapi-review-intelligence-digest/SKILL.md)** — Pull normalized reviews for a property on a schedule and deliver a weekly digest — average rating, recurring themes, and the latest complaints to act on. Powered by the ScoutingAPI REST API / MCP server.
- **[scoutingapi-comp-set-benchmark](skills/scoutingapi-comp-set-benchmark/SKILL.md)** — Benchmark your listing’s rate and availability against a defined comp-set and get a weekly position report. Powered by the ScoutingAPI REST API / MCP server.
- **[scoutingapi-mcp-agent-scouting](skills/scoutingapi-mcp-agent-scouting/SKILL.md)** — Connect ScoutingAPI as a Claude/Cursor MCP connector and scout stays, compare prices and check availability conversationally — no keys pasted. Powered by the ScoutingAPI REST API / MCP server.
- **[scoutingapi-cheapest-link-resolver](skills/scoutingapi-cheapest-link-resolver/SKILL.md)** — Resolve a property + dates to the single cheapest bookable link (with price and OTA) as clean JSON — for a concierge bot, a "book now" button, or an internal tool. Powered by the ScoutingAPI REST API / MCP server.
- **[scoutingapi-event-radar](skills/scoutingapi-event-radar/SKILL.md)** — Watch supply and prices around an event or peak date-window in a city and get alerted when demand tightens. Powered by the ScoutingAPI REST API / MCP server.
- **[scoutingapi-portfolio-feed](skills/scoutingapi-portfolio-feed/SKILL.md)** — A daily digest across a saved set of listings — price, rating and recent reviews per listing in one report. Powered by the ScoutingAPI REST API / MCP server.

## Install

Each skill is a self-contained `SKILL.md` under [`skills/`](skills/). Copy the folder into your agent's skills directory, give the agent a `SCOUTINGAPI_KEY` (a `scout_test_` sandbox key works for evaluation, at zero cost), and ask it to run the task. The skills are also discoverable at [https://scoutingapi.com/.well-known/agent-skills/index.json](https://scoutingapi.com/.well-known/agent-skills/index.json).

## Per-platform skills

Prefer keyword-named skills for one platform? Each platform has its own repo with search, availability/calendar, prices, cross-OTA comparison and reviews skills:

- [airbnb-skills](https://github.com/scoutingapi/airbnb-skills) — Airbnb agent skills
- [booking-com-skills](https://github.com/scoutingapi/booking-com-skills) — Booking.com agent skills
- [vrbo-skills](https://github.com/scoutingapi/vrbo-skills) — Vrbo agent skills
- [google-hotels-skills](https://github.com/scoutingapi/google-hotels-skills) — Google Hotels agent skills

## Credits

Number-free by design — costs live on the [pricing page](https://scoutingapi.com/pricing). Failed/empty calls are free; sandbox calls cost 0.

---

## Related repositories

Part of the ScoutingAPI open resource set — one unified accommodation-data API across Airbnb, Booking.com, Vrbo and Google Hotels, with a REST API, a native MCP server, and importable workflows.

- [airbnb-api](https://github.com/scoutingapi/airbnb-api)
- [booking-com-api](https://github.com/scoutingapi/booking-com-api)
- [vrbo-api](https://github.com/scoutingapi/vrbo-api)
- [google-hotels-api](https://github.com/scoutingapi/google-hotels-api)
- [hotel-api](https://github.com/scoutingapi/hotel-api)
- [travel-api](https://github.com/scoutingapi/travel-api)
- [hotel-mcp](https://github.com/scoutingapi/hotel-mcp)
- [travel-workflows](https://github.com/scoutingapi/travel-workflows)
- [airbnb-skills](https://github.com/scoutingapi/airbnb-skills)
- [booking-com-skills](https://github.com/scoutingapi/booking-com-skills)
- [vrbo-skills](https://github.com/scoutingapi/vrbo-skills)
- [google-hotels-skills](https://github.com/scoutingapi/google-hotels-skills)

- Website: <https://scoutingapi.com> · Docs: <https://scoutingapi.com/docs> · Status: <https://status.scoutingapi.com>

---

**Get your free key — no card → <https://scoutingapi.com/signup>** · [Docs](https://scoutingapi.com/docs) · [Pricing](https://scoutingapi.com/pricing) · [Status](https://status.scoutingapi.com)

Built with [ScoutingAPI](https://scoutingapi.com) — trusted, ToS-clean, real-time accommodation data across Airbnb, Booking.com, Vrbo and Google Hotels, normalized to one schema. REST + a native MCP server.
