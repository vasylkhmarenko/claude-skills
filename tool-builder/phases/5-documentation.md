# Phase 5: Documentation & Release Sign-off

**AI Role**: Docs Agent
**Human Roles**: PM (accepts), QA (validates accuracy)
**Thinking Mode**: Standard (use `"think"` for API docs)

---

## Entry Point
- From Phase 4 with approved code

## Context Management
> After Phase 4 (Development), consider starting Phase 5 in fresh context to avoid context bloat.

## Actions

### 1. Update Documentation
Based on changes made, update:

**README** (if applicable):
- New features section
- Updated usage examples
- Changed configuration options

**API Documentation** (if applicable):
- New endpoints
- Changed parameters
- Updated responses

**Code Comments**:
- Document non-obvious logic
- Explain "why" not "what"
- Update outdated comments

### 2. Create Changelog Entry
```markdown
## [Version] - YYYY-MM-DD

### Added
- [New feature description]

### Changed
- [Changed behavior]

### Fixed
- [Bug fixes]
```

### 3. Prepare Release Notes
User-facing summary of changes:
- What's new
- How to use it
- Breaking changes (if any)

### 4. Verify Documentation Accuracy
Cross-check:
- [ ] Code matches documentation
- [ ] Examples are runnable
- [ ] No outdated references

---

## Deliverable
Complete documentation package:
- Updated README/docs
- Changelog entry
- Release notes
- Accurate code comments

---

## Verification Checkpoint

Present to user:
```
## Documentation Update

### Files Updated
- [File 1]: [Changes]
- [File 2]: [Changes]

### Changelog Entry
[Changelog content]

### Release Notes
[Release notes content]

Please review documentation for accuracy. Ready to deploy?
```

**Gate**: User must accept docs before deployment.

---

## Decision Paths
- **Accepted** → Proceed to Phase 6 (Deployment)
- **Revisions Needed** → Update docs → Re-verify
