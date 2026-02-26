# Verification Checklist by Phase

> "If you can't verify it, don't ship it." - Anthropic Best Practices

## Phase 1: Discovery & Analysis

- [ ] Problem statement is clear and specific
- [ ] User confirmed intent
- [ ] Scope is defined (what's included AND excluded)
- [ ] Success criteria documented

**Verification**: User explicitly approves problem statement

---

## Phase 2: Requirements & Clarification

- [ ] All functional requirements listed
- [ ] Non-functional requirements defined (performance, security, etc.)
- [ ] Edge cases identified
- [ ] Assumptions documented
- [ ] Dependencies listed

**Verification**: User reviews and approves requirements checklist

---

## Phase 3: Architecture & Planning

- [ ] Component diagram/description provided
- [ ] Data flow documented
- [ ] Technology choices justified
- [ ] Alternatives considered and documented
- [ ] Security reviewed (use security-reviewer subagent)
- [ ] Architecture challenged (use architecture-challenger subagent)

**Verification**: User approves architecture before coding begins

---

## Phase 4: Development

- [ ] Code compiles/runs without errors
- [ ] All tests pass
- [ ] Linter passes (if applicable)
- [ ] Self-review completed
- [ ] Security review completed (subagent)
- [ ] Code matches approved architecture

**Verification**:
```bash
# Run these commands and confirm all pass:
npm run typecheck  # or equivalent
npm test
npm run lint
```

---

## Phase 5: Documentation & Release

- [ ] README updated (if applicable)
- [ ] API documentation matches implementation
- [ ] Changelog entry added
- [ ] Code comments are accurate
- [ ] Usage examples provided

**Verification**: User reviews documentation for accuracy

---

## Phase 6: Deployment & Testing

- [ ] Deployment steps documented
- [ ] Deployment successful
- [ ] Manual testing completed
- [ ] Integration points verified
- [ ] Rollback procedure documented

**Verification**:
- Deployment script/commands run successfully
- Manual smoke test passes
- User validates functionality

---

## Phase 7: Observability & Security

- [ ] Logging implemented
- [ ] Health check endpoint (if applicable)
- [ ] Error handling verified
- [ ] Security audit completed (subagent)
- [ ] Monitoring alerts configured (if applicable)

**Verification**:
- Health check returns 200
- Logs are being written
- No security issues flagged

---

## Quick Reference: Verification Commands

```bash
# TypeScript/JavaScript
npm run typecheck && npm test && npm run lint

# Python
python -m pytest && python -m mypy . && python -m flake8

# Go
go build ./... && go test ./... && go vet ./...

# Rust
cargo build && cargo test && cargo clippy
```
