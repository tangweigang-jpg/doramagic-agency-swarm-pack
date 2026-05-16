# agency-swarm Doramagic Pack

Pack version: `v1.0.0` · Last updated: `2026-05-15`

[![Pack v1.0.0](https://img.shields.io/badge/pack-v1.0.0-blue)](./CHANGELOG.md)
[![License](https://img.shields.io/github/license/tangweigang-jpg/doramagic-agency-swarm-pack)](./LICENSE)
[![Issues](https://img.shields.io/github/issues/tangweigang-jpg/doramagic-agency-swarm-pack)](https://github.com/tangweigang-jpg/doramagic-agency-swarm-pack/issues)

Languages: English | [中文](./README.zh-CN.md)

Multi-agent orchestration breaks at agent handoffs, message routing, and shared state boundaries.

This independent capability pack gives AI coding hosts verifiable agency-swarm workflows with coordination rules, boundary checks, and recovery steps for real failures.

> Not affiliated with or endorsed by VRSEN/agency-swarm.

## Copy / Run / Verify

1. copy `AGENTS.md` into your AI coding host.
2. Run the first prompt in `01_PROMPT_PREVIEW.md`.
3. Verify with `06_EVALS/smoke_check.md`; recover from `03_PITFALL_LOG.md` if it fails.

Quick links:
[Start](./AGENTS.md) · [Prompt](./01_PROMPT_PREVIEW.md) · [Evals](./06_EVALS/) · [Pitfalls](./03_PITFALL_LOG.md) · [Manual](./05_HUMAN_MANUAL.md)

## When This Helps

Use this pack when you want an AI agent to work with agency-swarm's multi-agent coordination without guessing at failure modes or pretending the upstream tool is installed and verified.

## What You Get

- Host instructions for AI coding agents.
- Copyable prompt preview.
- Acceptance checks.
- Real pitfall log with recovery steps.
- Boundary and risk card.
- Source attribution.

## AGENTS.md for Claude Code and AI Coding Agents

See [AGENTS.md](./AGENTS.md) for host instructions. Claude Code reads `.md` files in the project root as agent instructions.

## Pitfalls and Recovery

Real failure modes and recovery paths are documented in [03_PITFALL_LOG.md](./03_PITFALL_LOG.md). Eval failure signals and recovery paths are in [06_EVALS/](06_EVALS/).

## Source Attribution

Assembled by [Doramagic](https://doramagic.ai) for portable AI capability.

- Upstream: https://github.com/VRSEN/agency-swarm
- License: MIT
- Pack contents: prompts, host instructions, checks, guardrails, validation notes

If this pack helps your agent work from evidence, star the repo or open an issue for bugs, usage questions, or new pitfall reports.
