# Knoetic

Knoetic is an HR technology company that operates **CPOHQ**, a platform for Chief People Officers and
senior people-function executives: a private, invite-only community of 3,000+ CPOs (one member per
company), an AI "Chief of Staff" delivering personalized briefings and market/talent monitoring, and a
suite of workflow-specific AI agents for people analytics, performance insight, and peer benchmarking.

Backed by: Accel, EQT Ventures, Menlo Ventures ($50M+ raised).

## Brand note

`knoetic.com` now 301-redirects to **https://cpohq.com**. Knoetic remains the company name; CPOHQ is
the product and public brand. The customer application is still served from `app.knoetic.com`.

## API surface

**None public.** As of the 2026-07-19 enrichment pass Knoetic publishes no API documentation,
developer portal, OpenAPI/AsyncAPI specification, SDKs, CLI, webhook catalog, MCP server, changelog,
status page, or sandbox. The GitHub organization `github.com/knoetic` exists but has zero public
repositories, and there are no packages on npm or PyPI. `api.knoetic.com` resolves and returns JSON
but is a private application backend with no published contract. The `apis[]` array is intentionally
empty.

## What was captured

| Artifact | Notes |
|---|---|
| `security/knoetic-trust-center.yml` | Vanta-hosted trust center at `trust.knoetic.com`; SOC 2 Type II |
| `security/knoetic-domain-security.yml` | TLS/HSTS/SPF/DMARC across both registrable domains |
| `well-known/knoetic-well-known.yml` | Negative result — no `/.well-known/` documents published |
| `llms/knoetic-llms.txt` | Generated agent-facing summary (not published by Knoetic) |

> Re-run caution: `app.knoetic.com` is a SPA with a catch-all route that returns HTTP 200 for every
> path, including `/.well-known/*` and `/llms.txt`. Those are soft 404s, not real documents.
