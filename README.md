# Agent Readiness Checklist

A practical, open-source checklist for making websites discoverable and usable by AI agents. Based on the [isitagentready.com](https://isitagentready.com) scanner's default "All Checks" profile.

## What This Covers

This checklist documents every check required to achieve **Level 5 (Agent-Native)** status, with implementation examples and file templates.

## Checklist

### Discoverability (4/4)

- [ ] **robots.txt** — Valid format with User-agent directives
- [ ] **sitemap.xml** — XML sitemap linked from robots.txt
- [ ] **Link Headers** — HTTP `Link` header with `api-catalog`, `service-desc`, `service-doc`, `describedby`
- [ ] **DNS-AID** — SVCB record at `_index._agents.yourdomain.com` with DNSSEC

### Content (1/1)

- [ ] **Markdown Negotiation** — Return `text/markdown` when `Accept: text/markdown` is requested

### Bot Access Control (2/2)

- [ ] **robots.txt AI Rules** — No restrictive AI-specific bot rules (wildcard applies to all)
- [ ] **Content Signals** — `Content-Signal` directive in robots.txt

### API, Auth, MCP & Skill Discovery (8/8)

- [ ] **API Catalog** — `/.well-known/api-catalog` with linkset format
- [ ] **OAuth Discovery** — `/.well-known/oauth-authorization-server` with valid issuer
- [ ] **OAuth Protected Resource** — `/.well-known/oauth-protected-resource`
- [ ] **auth.md** — `/auth.md` with H1 heading and agent_auth metadata
- [ ] **MCP Server Card** — `/.well-known/mcp/server-card.json`
- [ ] **A2A Agent Card** — `/.well-known/agent-card.json`
- [ ] **Agent Skills** — `/.well-known/agent-skills/index.json`
- [ ] **WebMCP** — JavaScript registering tools via `document.modelContext`

### Commerce (Optional)

- [ ] x402, MPP, UCP, ACP, AP2 — Only needed for commerce sites

## File Templates

Each check has a template in the `templates/` directory. Copy and customize for your site.

## Real-World Examples

Two sites achieved 100/100 Level 5 using this checklist:

- [InkPreview](https://inkpreview.co) — AI tattoo simulator (16/16 checks passed)
- [BatchBG](https://batchbg.com) — Bulk background remover (16/16 checks passed)

## Scanner

Test your site: [isitagentready.com](https://isitagentready.com)

## License

MIT — Use freely, contribute back.
