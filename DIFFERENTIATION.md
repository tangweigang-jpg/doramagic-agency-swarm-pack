# Differentiation

## What Already Exists

The VRSEN/agency-swarm GitHub repo provides:
- `README.md` — installation and basic usage instructions
- `agency_swarm/` source code — the agency hierarchy and communication primitives
- `examples/` — sample agency configurations
- GitHub Issues — community Q&A and bug reports
- No AGENTS.md or CLAUDE.md for AI coding hosts
- No eval suites or smoke/boundary/failure checks
- No pitfall recovery documentation

## Why This Doramagic Pack Is Different

Agency-swarm ships source code and examples. This pack ships a production-ready capability pack with:

- **Failure-first framing**: starts with pitfalls, boundaries, and verification before any command runs
- **Eval-backed assurance**: smoke, boundary, and failure checks validated against real agency-swarm behavior
- **Host portability**: AGENTS.md and CLAUDE.md work with Claude Code and other AI coding hosts
- **Pitfall recovery**: structured recovery paths for agency-swarm-specific failure modes (thread context loss, shared state corruption, cross-client module leakage)
- **Source traceability**: SOURCE_MAP.md documents Doramagic additions vs upstream

## What This Pack Adds

| Asset | Purpose |
|-------|---------|
| `AGENTS.md` | Human-readable instructions for AI coding agents operating agency-swarm |
| `CLAUDE.md` | Claude Code specifics: multi-agent context, pre-flight checks, failure format |
| `00_QUICK_START.md` | Step-by-step onboarding with Copy/Run/Verify |
| `03_PITFALL_LOG.md` | Structured pitfalls: symptom, cause, verification, recovery |
| `04_BOUNDARY_RISK_CARD.md` | Permissions, stop conditions, and runtime risk boundaries |
| `06_EVALS/smoke_check.md` | Automated smoke test for agency-swarm initialization |
| `06_EVALS/boundary_check.md` | Boundary test for agent handoff and context limits |
| `06_EVALS/failure_check.md` | Failure injection and recovery validation |
| `SOURCE_MAP.md` | Doramagic source additions vs upstream attribution |

## What This Pack Does NOT Do

- Not an official VRSEN/agency-swarm product or endorsed distribution
- Not a generic starter template that works without reading the upstream docs
- Not an awesome list aggregating third-party tutorials or videos
- Not an SEO backlink repository or marketing landing page
- Not a hosted service; this pack runs locally in the user's own environment
