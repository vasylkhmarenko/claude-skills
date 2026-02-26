# Phase 1: Discovery & Analysis

**AI Role**: Analysis Agent
**Human Role**: Product Manager (sets intent)
**Thinking Mode**: Standard (use `"think"` for complex problems)

---

## Entry Point
- New feature request from user

## Actions

### 1. Analyze Request
- Parse the feature request
- Identify the core problem being solved
- Assess complexity (Simple / Medium / Complex)

### 2. Check for Conflicts
- Review existing codebase patterns
- Identify potential conflicts with existing features
- Note dependencies

### 3. Estimate Scope
- List major components needed
- Identify unknowns
- Flag areas requiring clarification

### 4. Interview (for complex features)
Use this prompt for complex features:
```
"I want to build [brief description]. Interview me using AskUserQuestion.

Ask about:
- Technical implementation details
- UI/UX requirements (if applicable)
- Edge cases and error handling
- Security considerations
- Performance requirements
- Integration points

Keep interviewing until we've covered everything."
```

### 5. Generate Clarifying Questions
Create focused questions covering:
- Functional requirements
- Non-functional requirements
- Constraints
- Success criteria

---

## Deliverable
Feature ticket / clear problem statement including:
- Problem description
- Proposed solution (high-level)
- Open questions

---

## Verification Checkpoint

Present to user:
```
## Discovery Summary

**Problem**: [Clear problem statement]
**Proposed Solution**: [High-level approach]
**Complexity**: Simple / Medium / Complex
**Key Questions Answered**: [List]

Does this capture your requirements? Ready to proceed to Requirements & Clarification?
```

**Gate**: User must confirm before proceeding.

---

## Feedback Loop
User provides clarifications → Agent refines understanding → Repeat until clear
