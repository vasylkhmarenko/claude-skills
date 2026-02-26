---
name: tool-builder
description: Build tools using Hybrid Intelligence SDLC. Use when creating any tool, app, script, CLI, API, or software. Triggers on "build," "create," "develop," "make a tool."
---

# Hybrid Intelligence SDLC

Human strategy + AI execution. 7 phases, never skip, always verify.

## Pipeline

```
Feature Request → [1] Discovery → [2] Requirements → [3] Architecture → [4] Development → [5] Documentation → [6] Deployment → [7] Observability → Shipped
```

## Phases (details in @phases/)

| # | Phase | AI Role | Human Gate | Thinking |
|---|-------|---------|------------|----------|
| 1 | Discovery | Analysis Agent | Confirms intent | standard |
| 2 | Requirements | Clarification Agent | Approves requirements | "think" |
| 3 | Architecture | Architecture Agent | Approves design | "think hard" |
| 4 | Development | Coding Agent | Reviews PR | standard |
| 5 | Documentation | Docs Agent | Accepts docs | standard |
| 6 | Deployment | Deployment Agent | Validates | "think" |
| 7 | Observability | Security Agent | Escalation | "think hard" |

## Core Rules

1. **NEVER skip phases** - Discovery → Requirements → Architecture → Development
2. **NEVER proceed without verification** - Each phase has a checkpoint
3. **NEVER code without approved architecture** - Phase 3 must be approved first
4. **Use TodoWrite** - Track progress through all phases
5. **Use subagents** - Delegate security review and architecture challenge

## Subagents (@agents/)

- **security-reviewer**: OWASP Top 10, secrets scan, input validation
- **architecture-challenger**: Challenge designs, suggest alternatives

## Quick Start

1. Create todos for all 7 phases
2. Start Phase 1: Analyze request, ask clarifying questions
3. Present checkpoint, wait for approval
4. Proceed to next phase
5. Repeat until Phase 7 complete

## References

- @phases/1-discovery.md through @phases/7-observability.md
- @references/verification-checklist.md
- @references/thinking-modes.md

## Context Management

- Use `/clear` between major phases if context > 50%
- Delegate research to subagents (separate context)
- After Phase 4, consider fresh context for Phase 5
