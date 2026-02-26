# Phase 7: Observability & Security

**AI Roles**: Logging Agent, Security Agent, Rollback Agent
**Human Role**: Escalation on-demand (any stage)
**Thinking Mode**: `"think hard"` - thorough security analysis

---

## Entry Point
- From Phase 6 with validated deployment

## Actions

### 1. Logging & Audit Setup
Implement/verify:
```markdown
## Logging Checklist
- [ ] Key operations are logged
- [ ] Log levels are appropriate (debug, info, warn, error)
- [ ] Sensitive data is NOT logged
- [ ] Log format is parseable
- [ ] Logs include correlation IDs (if applicable)
```

### 2. Feature-Level Observability
Track:
- Feature usage metrics
- Error rates
- Performance metrics
- User interactions (if applicable)

### 3. Security Audit (Subagent)
```
Use the security-reviewer subagent to perform a final security audit:
- OWASP Top 10 review
- Secrets scan
- Dependency vulnerability check
- Access control validation
```

### 4. Health Check (if applicable)
```markdown
## Health Check Endpoint
- URL: [Health check URL]
- Expected response: 200 OK
- What it checks: [List]
```

### 5. Monitoring & Alerts (if applicable)
```markdown
## Monitoring Setup
- [ ] Uptime monitoring configured
- [ ] Error rate alerts set
- [ ] Performance thresholds defined
- [ ] On-call rotation notified
```

### 6. Auto-Rollback Criteria
Define when to auto-rollback:
```markdown
## Auto-Rollback Triggers
- Error rate > [X]%
- Response time > [Y]ms
- Health check fails [Z] consecutive times
```

---

## High-Severity Issue Detection

```
     ┌─────────────────────┐
     │ High-severity issue │
     │     detected?       │
     └─────────────────────┘
              │
       ┌──────┴──────┐
       │             │
      YES           NO
       │             │
       ▼             ▼
  ┌─────────┐   ┌─────────┐
  │ Auto    │   │Continue │
  │Rollback │   │Monitoring│
  └─────────┘   └─────────┘
```

---

## Deliverable
Stable, monitored feature:
- Logging implemented
- Security audited
- Monitoring configured
- Rollback ready

---

## Verification Checkpoint

Present to user:
```
## Observability Complete

### Logging
- Key operations logged: YES/NO
- Log levels correct: YES/NO

### Security Audit
[Summary from security-reviewer subagent]

### Monitoring
- Health check: [Status]
- Alerts configured: YES/NO

### Rollback
- Procedure documented: YES/NO
- Auto-rollback criteria: [Defined/Not applicable]

Feature is production-ready and monitored.
```

---

## Human Escalation

User can intervene at ANY time:
- Request additional security review
- Pause deployment
- Trigger manual rollback
- Ask questions

**Escalation triggers**:
- Security alerts
- High error rates
- User-reported issues
- Performance degradation

---

## Completion

Once Phase 7 is verified:
```
## SDLC Complete

Feature: [Name]
Status: Shipped & Monitored

Phases Completed:
1. Discovery & Analysis ✓
2. Requirements & Clarification ✓
3. Architecture & Planning ✓
4. Development ✓
5. Documentation & Release ✓
6. Deployment & Testing ✓
7. Observability & Security ✓

The feature is now in production with monitoring enabled.
```
