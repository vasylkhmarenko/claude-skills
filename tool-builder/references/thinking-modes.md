# Thinking Mode Reference

Anthropic maps specific phrases to extended thinking budgets. Use these strategically.

## Thinking Levels

| Trigger | Budget | Use For |
|---------|--------|---------|
| `"think"` | Basic | Simple analysis, routine decisions |
| `"think hard"` | Medium | Architecture decisions, risk assessment |
| `"think harder"` | High | Complex tradeoffs, security review |
| `"ultrathink"` | Maximum | Critical decisions, novel problems |

## Recommended Usage by Phase

### Phase 1: Discovery & Analysis
- **Default**: Standard (no trigger needed)
- Use `"think"` when analyzing complex problem statements

### Phase 2: Requirements & Clarification
- **Default**: `"think"`
- Ensures completeness of requirements
- Helps identify missing edge cases

### Phase 3: Architecture & Planning
- **Default**: `"think hard"`
- Evaluates alternatives thoroughly
- Identifies architectural risks
- Use `"ultrathink"` for critical system design

### Phase 4: Development
- **Coding**: Standard (no trigger)
- **Self-review**: `"think"`
- **Security review**: `"think hard"`

### Phase 5: Documentation & Release
- **Default**: Standard
- Use `"think"` for API documentation accuracy

### Phase 6: Deployment & Testing
- **Default**: `"think"`
- Risk assessment for deployment
- Rollback planning

### Phase 7: Observability & Security
- **Default**: `"think hard"`
- Security audit requires thorough analysis
- Use `"ultrathink"` for critical security decisions

## Example Prompts

```
# Architecture decision
"Think hard about the tradeoffs between using a SQL database vs. NoSQL for this use case."

# Security review
"Think harder about potential security vulnerabilities in this authentication flow."

# Critical decision
"Ultrathink about the implications of this data migration strategy."
```

## When NOT to Use Extended Thinking

- Simple file edits
- Running commands
- Writing boilerplate code
- Straightforward bug fixes

Extended thinking has overhead. Reserve it for decisions that matter.
