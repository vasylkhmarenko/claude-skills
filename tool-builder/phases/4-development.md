# Phase 4: Development

**AI Role**: Coding Agent + Self-Review
**Human Role**: Code Reviewer (reviews PR)
**Thinking Mode**: Standard for coding, `"think"` for self-review

---

## Entry Point
- From Phase 3 with approved architecture

## Actions

### 1. Write Code
Follow these principles:
- Match approved architecture
- Follow existing codebase patterns
- Keep it simple ("dumbest possible thing that will work")
- Prefer functions over classes
- Use descriptive names

### 2. Write Tests
- Unit tests for core functionality
- Test edge cases from Phase 2
- Test error scenarios

### 3. Self-Review
Before presenting, review your own code:
```
Think about potential issues in this code:
- Are there any bugs?
- Is error handling complete?
- Are there any security issues?
- Does it match the architecture?
```

### 4. Run Verification
```bash
# Run all applicable checks
npm run typecheck  # or equivalent
npm test
npm run lint
```

### 5. Security Review (Subagent)
```
Use the security-reviewer subagent to review this implementation for:
- OWASP Top 10 vulnerabilities
- Secrets in code
- Input validation
- Access control
```

### 6. Create Pull Request
Present code for human review with:
- Summary of changes
- Files modified
- Test coverage
- Security review results

---

## Deliverable
Working code with:
- All tests passing
- Linter clean
- Security reviewed
- Ready for human review

---

## Verification Checkpoint

Present to user:
```
## Development Complete

### Changes Made
- [File 1]: [Summary]
- [File 2]: [Summary]

### Test Results
- Tests: [X] passing, [Y] failing
- Coverage: [Z]%

### Verification
- [ ] Typecheck: PASS/FAIL
- [ ] Tests: PASS/FAIL
- [ ] Lint: PASS/FAIL
- [ ] Security Review: [Summary]

### Code for Review
[Key code sections or PR link]

Please review. Any changes needed?
```

**Gate**: User must approve code before documentation.

---

## Decision Paths
- **Approved** → Proceed to Phase 5 (Documentation)
- **Changes Requested** → Revise code → Re-verify → Re-review

---

## Writer/Reviewer Pattern (Optional)
For critical code, use fresh context for review:

**Session A (Writer)**: Implement and test
**Session B (Reviewer)**: Review with fresh eyes
**Session A**: Address feedback

---

## Parallel Opportunities
Can run in parallel:
- Code implementation (main)
- Test writing (subagent)
- Security review (subagent)
