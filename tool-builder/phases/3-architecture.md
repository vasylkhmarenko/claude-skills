# Phase 3: Architecture & Planning

**AI Role**: Architecture Agent + Self-Review
**Human Role**: Architect (reviews and approves)
**Thinking Mode**: `"think hard"` - evaluate alternatives thoroughly

---

## Entry Point
- From Phase 2 with approved requirements

## Actions

### 1. Solution Planning
Design architecture covering:
- Component structure
- Data flow
- Technology choices
- API contracts (if applicable)

### 2. Self-Review (IMPORTANT)
Before presenting, challenge your own solution:
- Is this the simplest solution that works?
- What are the alternatives?
- What could go wrong?

### 3. Use Architecture Challenger Subagent
```
Use the architecture-challenger subagent to review this proposed architecture.
Focus on: scalability, failure modes, complexity, and alternatives.
```

### 4. Document Architecture
```markdown
## Architecture Overview

### Components
- [Component 1]: [Purpose]
- [Component 2]: [Purpose]

### Data Flow
[Description or diagram]

### Technology Choices
| Decision | Choice | Rationale |
|----------|--------|-----------|
| [Area] | [Tech] | [Why] |

### Alternatives Considered
| Alternative | Pros | Cons | Why Not |
|-------------|------|------|---------|
| [Option] | [+] | [-] | [Reason] |

### Risks
- [Risk 1]: [Mitigation]
- [Risk 2]: [Mitigation]
```

### 5. Security Review
```
Use the security-reviewer subagent to identify security concerns in this architecture.
```

---

## Deliverable
Approved architecture plan including:
- Component diagram/description
- Technology decisions with rationale
- Alternatives considered
- Risk assessment

---

## Verification Checkpoint

Present to user:
```
## Architecture Proposal

[Architecture overview]

### Key Decisions
1. [Decision]: [Choice] because [rationale]

### Alternatives Considered
- [Alternative 1]: Not chosen because [reason]

### Risks Identified
- [Risk]: [Mitigation]

### Challenger Review Summary
[Key points from architecture-challenger subagent]

Do you approve this architecture? Ready to proceed to Development?
```

**Gate**: User must explicitly approve architecture.

---

## Decision Paths
- **Approved** → Proceed to Phase 4 (Development)
- **Changes Requested** → Revise architecture → Re-review

---

## Parallel Opportunities
Can run in parallel:
- Architecture design (main)
- Risk analysis (subagent)
- Security review (subagent)
