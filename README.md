<!-- generated: DO NOT EDIT BY HAND — produced by apps/web/scripts/export-github-repos.ts from lib/agent/skills.ts + the workflow SSOT. Edit the config + re-run. -->

# StayingAPI Agent Skills

Portable **SKILL.md** agent skills for accommodation data across Airbnb, Booking.com, Vrbo and Google Hotels — one unified schema, REST + a native MCP server. Drop a skill into any agent runtime that reads `SKILL.md` (Claude, Codex, OpenClaw/ClawHub, Hermes, Smithery) and it learns to call the API for that task.

**[Get a free key — no card →](https://stayingapi.com/signup)**

## Skills

- **[stayingapi-search](skills/stayingapi-search/SKILL.md)** — Search and compare accommodation prices across Airbnb, Booking.com, Vrbo and Google Hotels via the StayingAPI REST API. Use when a user wants to find stays, check availability, get a price, compare one property across OTAs, or read reviews. Covers Bearer auth, the async 202→poll job contract, the unified response envelope, and error handling.
- **[stayingapi-mcp](skills/stayingapi-mcp/SKILL.md)** — Connect an AI agent to the StayingAPI Model Context Protocol (MCP) server for accommodation search, availability, pricing, cross-OTA price comparison and reviews. Use when the agent runtime supports MCP connectors (e.g. Claude) and you want OAuth-based access without managing API keys. Covers the OAuth 2.1 + PKCE connect flow, the seven read-only tools, and when to prefer MCP vs REST.
- **[stayingapi-cross-ota-price-comparison](skills/stayingapi-cross-ota-price-comparison/SKILL.md)** — Compare one property across booking platforms and report the cheapest rate, with savings vs. the median. Powered by the StayingAPI REST API / MCP server.
- **[stayingapi-availability-alert](skills/stayingapi-availability-alert/SKILL.md)** — Watch a listing over a date window and get alerted the moment a wanted date becomes available. Powered by the StayingAPI REST API / MCP server.
- **[stayingapi-price-drop-watcher](skills/stayingapi-price-drop-watcher/SKILL.md)** — Watch a specific stay and get alerted the moment its total price falls to or below your threshold. Powered by the StayingAPI REST API / MCP server.
- **[stayingapi-rate-parity-monitor](skills/stayingapi-rate-parity-monitor/SKILL.md)** — Watch how your own listing's rate shows across OTAs on a schedule and flag any platform underselling the market median. Powered by the StayingAPI REST API / MCP server.
- **[stayingapi-str-market-scan](skills/stayingapi-str-market-scan/SKILL.md)** — Scan a short-term-rental market — discover listings across platforms, price the top N for your dates, and append a normalized row-per-listing dataset to a Google Sheet. Powered by the StayingAPI REST API / MCP server.
- **[stayingapi-new-inventory-lead-gen](skills/stayingapi-new-inventory-lead-gen/SKILL.md)** — Re-run a saved search on a schedule, diff it against the last run, and sync only the newly-listed properties into a CRM or Sheet as leads. Powered by the StayingAPI REST API / MCP server.
- **[stayingapi-review-intelligence-digest](skills/stayingapi-review-intelligence-digest/SKILL.md)** — Pull normalized reviews for a property on a schedule and deliver a weekly digest — average rating, recurring themes, and the latest complaints to act on. Powered by the StayingAPI REST API / MCP server.
- **[stayingapi-comp-set-benchmark](skills/stayingapi-comp-set-benchmark/SKILL.md)** — Benchmark your listing’s rate and availability against a defined comp-set and get a weekly position report. Powered by the StayingAPI REST API / MCP server.
- **[stayingapi-mcp-agent-scouting](skills/stayingapi-mcp-agent-scouting/SKILL.md)** — Connect StayingAPI as a Claude/Cursor MCP connector and scout stays, compare prices and check availability conversationally — no keys pasted. Powered by the StayingAPI REST API / MCP server.
- **[stayingapi-cheapest-link-resolver](skills/stayingapi-cheapest-link-resolver/SKILL.md)** — Resolve a property + dates to the single cheapest bookable link (with price and OTA) as clean JSON — for a concierge bot, a "book now" button, or an internal tool. Powered by the StayingAPI REST API / MCP server.
- **[stayingapi-event-radar](skills/stayingapi-event-radar/SKILL.md)** — Watch supply and prices around an event or peak date-window in a city and get alerted when demand tightens. Powered by the StayingAPI REST API / MCP server.
- **[stayingapi-portfolio-feed](skills/stayingapi-portfolio-feed/SKILL.md)** — A daily digest across a saved set of listings — price, rating and recent reviews per listing in one report. Powered by the StayingAPI REST API / MCP server.

## Install

Each skill is a self-contained `SKILL.md` under [`skills/`](skills/). Copy the folder into your agent's skills directory, give the agent a `STAYINGAPI_KEY` (a `stay_test_` sandbox key works for evaluation, at zero cost), and ask it to run the task. The skills are also discoverable at [https://stayingapi.com/.well-known/agent-skills/index.json](https://stayingapi.com/.well-known/agent-skills/index.json).

## Per-platform skills

Prefer keyword-named skills for one platform? Each platform has its own repo with search, availability/calendar, prices, cross-OTA comparison and reviews skills:

- [airbnb-skills](https://github.com/stayingapi/airbnb-skills) — Airbnb agent skills
- [booking-com-skills](https://github.com/stayingapi/booking-com-skills) — Booking.com agent skills
- [vrbo-skills](https://github.com/stayingapi/vrbo-skills) — Vrbo agent skills
- [google-hotels-skills](https://github.com/stayingapi/google-hotels-skills) — Google Hotels agent skills

## Credits

Number-free by design — costs live on the [pricing page](https://stayingapi.com/pricing). Failed/empty calls are free; sandbox calls cost 0.

---

## Related repositories

Part of the StayingAPI open resource set — one unified accommodation-data API across Airbnb, Booking.com, Vrbo and Google Hotels, with a REST API, a native MCP server, and importable workflows.

- [airbnb-api](https://github.com/stayingapi/airbnb-api)
- [booking-com-api](https://github.com/stayingapi/booking-com-api)
- [vrbo-api](https://github.com/stayingapi/vrbo-api)
- [google-hotels-api](https://github.com/stayingapi/google-hotels-api)
- [hotel-api](https://github.com/stayingapi/hotel-api)
- [travel-api](https://github.com/stayingapi/travel-api)
- [hotel-mcp](https://github.com/stayingapi/hotel-mcp)
- [travel-workflows](https://github.com/stayingapi/travel-workflows)
- [airbnb-skills](https://github.com/stayingapi/airbnb-skills)
- [booking-com-skills](https://github.com/stayingapi/booking-com-skills)
- [vrbo-skills](https://github.com/stayingapi/vrbo-skills)
- [google-hotels-skills](https://github.com/stayingapi/google-hotels-skills)

- Website: <https://stayingapi.com> · Docs: <https://stayingapi.com/docs> · Status: <https://status.stayingapi.com>

---

**Get your free key — no card → <https://stayingapi.com/signup>** · [Docs](https://stayingapi.com/docs) · [Pricing](https://stayingapi.com/pricing) · [Status](https://status.stayingapi.com)

Built with [StayingAPI](https://stayingapi.com) — trusted, ToS-clean, real-time accommodation data across Airbnb, Booking.com, Vrbo and Google Hotels, normalized to one schema. REST + a native MCP server.
