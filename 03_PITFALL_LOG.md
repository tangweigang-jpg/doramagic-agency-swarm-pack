# Pitfall Log

Real agency-swarm failures from upstream issues and community reports.

## Agent Handoff Failures

### Pitfall: Handoff fails when thread context is lost

- Symptom: Next agent in agency hierarchy does not receive prior agent's context.
- Likely cause: Thread context not passed through agency hierarchy during handoff.
- How to verify: Check that agency hierarchy is initialized before handoff. Confirm thread_id is consistent across agents.
- Recovery step: Re-initialize thread context before handoff. Use explicit thread_id in agency constructor.
- Source: upstream behavior

### Pitfall: Duplicate call_ids cause openai.BadRequestError

- Symptom: API rejects request with BadRequestError when agent calls a tool multiple times.
- Likely cause: Duplicate call_ids submitted in message routing.
- How to verify: Check message history for duplicate call_id values before sending.
- Recovery step: Generate unique call_id per tool call. Do not reuse call_ids across agent handoffs.
- Source: https://github.com/VRSEN/agency-swarm/issues/151

## Message Routing Failures

### Pitfall: Commas break agent tags in terminal demo

- Symptom: Agent tags corrupted when message contains commas; routing fails silently.
- Likely cause: Tag parser splits on comma without escaping.
- How to verify: Send a message with comma in agent instructions; check tag parsing.
- Recovery step: Avoid commas in agent tags; escape commas if required.
- Source: https://github.com/VRSEN/agency-swarm/issues/410

### Pitfall: MCP server logs appear in terminal demo output

- Symptom: Server-side logs leak into agent output stream; user sees unexpected log lines.
- Likely cause: Output routing does not separate server logs from agent messages.
- How to verify: Enable verbose logging and check output stream for non-agent content.
- Recovery step: Configure output filter to separate agent messages from server logs.
- Source: https://github.com/VRSEN/agency-swarm/issues/409

### Pitfall: context_override mutated during streaming

- Symptom: Context values change unexpectedly during streaming; agent behavior becomes inconsistent.
- Likely cause: State management bug where context_override is modified in-place.
- How to verify: Log context values before and during streaming; check for unexpected mutations.
- Recovery step: Freeze context before streaming; clone context_override rather than mutating.
- Source: https://github.com/VRSEN/agency-swarm/issues/445

## State Management Failures

### Pitfall: Cross-client module leakage

- Symptom: Module state from one client bleeds into another client's session.
- Likely cause: Shared module imports not isolated per-client.
- How to verify: Run two clients concurrently; check if client B sees client A's module state.
- Recovery step: Isolate module imports per client process; do not share module state across clients.
- Source: https://github.com/VRSEN/agency-swarm/issues/447

### Pitfall: Shared state initialization failures

- Symptom: Agents start with inconsistent shared state; tools behave differently across agents.
- Likely cause: Shared state not initialized atomically; race condition during init.
- How to verify: Check init logs; look for partial init before all agents report ready.
- Recovery step: Re-initialize shared state; ensure all agents confirm state ready before proceeding.
- Source: https://github.com/VRSEN/agency-swarm/issues/165

### Pitfall: Hosted tool writes to wrong thread during agent-to-agent runs

- Symptom: Tool output goes to caller thread instead of agent thread; callerAgent shows None.
- Likely cause: ThreadLocal context not propagated through agent handoff.
- How to verify: Run agent-to-agent tool call; check callerAgent in output.
- Recovery step: Ensure ThreadLocal is propagated; set callerAgent explicitly in agency hierarchy.
- Source: https://github.com/VRSEN/agency-swarm/issues/390

### Pitfall: LoopAffineAsyncProxy async context manager missing hooks

- Symptom: MCP runs crash when using async context managers in agent loops.
- Likely cause: Async context manager not properly entered/exited in proxy.
- How to verify: Run async agent loop; check for RuntimeError or task group errors.
- Recovery step: Update to latest agency-swarm; avoid nested async context in agent loops.
- Source: https://github.com/VRSEN/agency-swarm/issues/405

## Integration / Compatibility Failures

### Pitfall: litellm models visualization breaks

- Symptom: Visualization works with OpenAI models but not litellm models.
- Likely cause: Provider-specific response format not handled in visualization layer.
- How to verify: Test visualization with litellm provider; compare output format to OpenAI.
- Recovery step: Use OpenAI-compatible provider for visualization, or disable visualization for litellm.
- Source: https://github.com/VRSEN/agency-swarm/issues/408

### Pitfall: openai-agents-python version mismatch

- Symptom: Import errors or missing methods after dependency update.
- Likely cause: agency-swarm pins openai-agents-python; breaking changes in newer versions.
- How to verify: Check installed version vs. required version in pyproject.toml.
- Recovery step: Pin openai-agents-python to version specified in requirements; do not auto-update.
- Source: https://github.com/VRSEN/agency-swarm/issues/367

## Generic Recovery Protocol

1. Identify failure type (handoff, routing, state, integration).
2. Check if a known pitfall above matches symptoms.
3. If match found, apply recovery step from that pitfall.
4. If no match, re-initialize agency hierarchy and retry.
5. If still failing, open issue in this repo with failure details.
