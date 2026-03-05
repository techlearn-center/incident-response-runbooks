# Postmortem: [Incident Title]

**Date:** YYYY-MM-DD
**Duration:** X hours Y minutes
**Severity:** P1/P2/P3
**Author:** [Name]

## Summary
One paragraph describing what happened, impact, and resolution.

## Impact
- **Users affected:** X
- **Revenue impact:** $Y
- **Duration:** Z minutes

## Timeline (all times UTC)
| Time | Event |
|---|---|
| 14:00 | Alert fired: HighErrorRate |
| 14:05 | On-call engineer acknowledged |
| 14:15 | Root cause identified |
| 14:25 | Fix deployed |
| 14:30 | Verified recovery |

## Root Cause
Detailed technical explanation of what went wrong.

## Resolution
What was done to fix the immediate issue.

## Lessons Learned
### What went well
- Alert fired within 2 minutes
- Runbook was helpful

### What went wrong
- Took 15 min to identify root cause
- Missing monitoring for X

## Action Items
| Action | Owner | Priority | Due Date |
|---|---|---|---|
| Add monitoring for X | @engineer | P1 | YYYY-MM-DD |
| Update runbook for Y | @sre | P2 | YYYY-MM-DD |
| Add automated test for Z | @team | P2 | YYYY-MM-DD |
