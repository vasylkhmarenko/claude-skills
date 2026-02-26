# Phase 2: Requirements & Clarification

**AI Role**: Clarification Agent
**Human Roles**: PM (answers), Designer (UI context), QA (validates completeness)
**Thinking Mode**: `"think"` - ensure completeness

---

## Entry Points
- From Phase 1 (Discovery) - new feature
- From Phase 6 (Deployment) - prompt adjustments needed

## Actions

### 1. Detailed Clarification Cycle
Ask focused questions until requirements are complete:
- What MUST the feature do? (functional)
- How well must it perform? (non-functional)
- What are the constraints?
- What's out of scope?

### 2. Document Requirements
Structure requirements as:
```markdown
## Functional Requirements
- FR1: [Description]
- FR2: [Description]

## Non-Functional Requirements
- NFR1: Performance - [Criteria]
- NFR2: Security - [Criteria]

## Constraints
- [Technology constraints]
- [Time constraints]
- [Resource constraints]

## Out of Scope
- [Explicitly excluded items]

## Assumptions
- [List assumptions made]
```

### 3. Identify Edge Cases
Think about:
- Empty/null inputs
- Boundary conditions
- Concurrent access
- Error scenarios
- Network failures

### 4. Add Designer Context (if UI involved)
- User flow
- Wireframe references
- Accessibility requirements

### 5. Prepare Feature Prompt
Create a comprehensive prompt that contains ALL context needed so AI won't need to guess.

---

## Deliverable
Complete requirements document including:
- All functional requirements
- Non-functional requirements
- Edge cases
- Assumptions

---

## Verification Checkpoint

Present to user:
```
## Requirements Summary

**Functional Requirements**: [Count] items
**Non-Functional Requirements**: [Count] items
**Edge Cases Identified**: [Count]
**Assumptions**: [Count]

[Full requirements list]

Does this capture everything? Ready to proceed to Architecture?
```

**Gate**: User must approve requirements before architecture begins.

---

## Feedback Loop
Clarifications cycle → Requirements refined → User validates → Repeat until complete
