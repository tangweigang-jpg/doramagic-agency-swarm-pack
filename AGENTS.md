## Goal

Use this pack to help an AI coding agent work with VRSEN/agency-swarm safely and verifiably.

## When To Use

- The user wants a verifiable agency-swarm workflow with multi-agent coordination rules, boundary checks, and recovery steps for agent communication failures.
- The user accepts that this is an independent Doramagic pack.
- The agent can run the acceptance checks before claiming success.

## Inputs Expected From User

- Target host or coding environment.
- Task goal.
- Safety boundary.
- Whether external tools, browser, network, filesystem, or credentials are allowed.

## Allowed Actions

- Read files in this pack.
- Ask clarifying questions.
- Produce a plan.
- Run only user-approved verification commands.
- Record failures in the pitfall log format.

## Disallowed Actions

- Do not claim official endorsement.
- Do not access secrets by default.
- Do not send messages, publish, purchase, delete, or modify external systems without explicit user approval.
- Do not claim the upstream tool works until an acceptance check passes.

## Agent Communication Boundaries

agency-swarm agents communicate through a hierarchy with explicit handoff protocols:

- **Agency**: top-level container managing agent roles and delegation.
- **Agent**: individual agent with defined instructions and tools.
- **Message routing**: agents send messages through the agency hierarchy; misrouted messages cause failures.
- **Thread context**: messages carry thread context; losing context breaks continuity.

Boundary rules:
- Never assume message delivery without verifying thread context.
- Never modify shared state without explicit agent role authorization.
- Never skip the agency hierarchy in inter-agent communication.

## Coordination Failure Recovery

When coordination fails, check `03_PITFALL_LOG.md` for the specific failure mode:

1. **Handoff failure**: agent cannot pass control to next agent.
   - Check: thread context intact? agent roles defined? agency hierarchy initialized?
   - Recovery: re-initialize thread context or re-declare agency hierarchy.

2. **Message routing failure**: message delivered to wrong agent or lost.
   - Check: correct recipient agent in agency chart? message format valid?
   - Recovery: re-send with correct routing or rebuild message.

3. **Shared state corruption**: agent writes conflict with other agent writes.
   - Check: #165, #390 in pitfall log for known state issues.
   - Recovery: isolate per-agent state or re-initialize shared state.

## Verification Steps

1. Read `00_QUICK_START.md`.
2. Run at least one eval in `06_EVALS/`.
3. Check `03_PITFALL_LOG.md` before escalating.
4. Check `04_BOUNDARY_RISK_CARD.md` before using external tools.

## Failure Recovery

If verification fails, stop and report:

- Which eval failed.
- Expected result.
- Actual result.
- Suspected cause.
- Recovery step from `03_PITFALL_LOG.md`.

## Source / Risk Reminder

This is an independent Doramagic pack. Use `SOURCE_MAP.md` for evidence and source links.
