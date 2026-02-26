# Phase 6: Deployment & Testing

**AI Role**: Deployment Agent
**Human Role**: Usability Tester (QA, Product, Real Users)
**Thinking Mode**: `"think"` - risk assessment

---

## Entry Point
- From Phase 5 with accepted documentation

## Actions

### 1. Prepare Deployment
Document deployment steps:
```markdown
## Deployment Steps

### Prerequisites
- [Required dependencies]
- [Environment setup]

### Installation
1. [Step 1]
2. [Step 2]

### Configuration
- [Config option 1]: [Description]
- [Config option 2]: [Description]

### Verification
- [How to verify deployment succeeded]
```

### 2. Deploy to Pre-Production/Staging
Execute deployment:
- Run deployment commands
- Verify deployment succeeded
- Check logs for errors

### 3. Provide Testing Support
Prepare for usability testing:
- Test scenarios to cover
- Expected behaviors
- Known limitations

### 4. Document Rollback Procedure
```markdown
## Rollback Steps

If issues are found:
1. [Rollback step 1]
2. [Rollback step 2]

### Verification
- [How to verify rollback succeeded]
```

---

## Deliverable
Validated deployment:
- Deployment successful
- Manual testing passed
- Rollback procedure documented

---

## Verification Checkpoint

Present to user:
```
## Deployment Complete

### Deployment Status
- Environment: [Staging/Production]
- Status: SUCCESS/FAILED
- URL: [If applicable]

### Testing Checklist
- [ ] Core functionality works
- [ ] Edge cases handled
- [ ] Error messages helpful
- [ ] Performance acceptable

### Rollback Ready
Rollback procedure documented and tested.

Please validate the deployment. Any issues found?
```

**Gate**: User must validate before production/completion.

---

## Decision Paths
- **Passed** → Deploy to production (if staging) → Proceed to Phase 7
- **Prompt Adjustments Needed** → Return to Phase 2 (Requirements)
- **Bug Found** → Return to Phase 4 (Development)

---

## Usability Testing Focus
- Does it solve the original problem?
- Is it intuitive to use?
- Are error messages helpful?
- Is performance acceptable?
