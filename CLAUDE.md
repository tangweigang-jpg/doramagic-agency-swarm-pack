# CLAUDE.md — Claude Code

Use the instructions in `AGENTS.md`. This file adds Claude Code specifics.

## Claude Code Reminders

- Claude Code supports `.md` files in the project root. `AGENTS.md` is readable as repository instructions.
- Keep tool calls explicit. Claude Code will ask before using browser, network, filesystem, or credentials.
- Run `06_EVALS/smoke_check.md` before claiming the pack works in your session.
- If blocked, write the failure into `TEST_LOG.md` or report it directly.

## Multi-Agent Context in Claude Code

When Claude Code works with agency-swarm:
- Initialize the agency hierarchy before delegating to sub-agents.
- Pass thread context explicitly between agent handoffs; do not assume implicit continuity.
- Verify each agent's role is correctly declared in the agency chart before tool use.

## Pre-Flight Checks

1. Read `00_QUICK_START.md`.
2. Run `06_EVALS/smoke_check.md` conceptually (describe expected behavior) before running commands.
3. If a command is needed, ask the user for approval first.
4. If blocked by a known pitfall, check `03_PITFALL_LOG.md` for recovery steps.

## Failure Reporting Format

When something fails, report:
- Eval or step that failed
- Expected behavior
- Actual behavior
- Suspected cause
- Recovery step from `03_PITFALL_LOG.md`
