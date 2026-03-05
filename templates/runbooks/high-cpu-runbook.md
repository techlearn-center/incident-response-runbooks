# Runbook: High CPU Usage

## Alert
**Name:** HighCPUUsage
**Severity:** Warning (>80%), Critical (>95%)
**Service:** Any

## Symptoms
- Slow response times
- Increased error rates
- Load balancer health check failures

## Investigation Steps

### Step 1: Identify the affected host
```bash
# Check which hosts have high CPU
kubectl top nodes
kubectl top pods --sort-by=cpu -A | head -20
```

### Step 2: Identify the process
```bash
# SSH to the affected node
top -bn1 | head -20
ps aux --sort=-%cpu | head -10
```

### Step 3: Check recent changes
```bash
# Recent deployments
kubectl get events --sort-by='.lastTimestamp' -A | tail -20

# Recent config changes
git log --oneline -10
```

## Resolution

### If caused by a deployment:
1. Rollback: `kubectl rollout undo deployment/<name>`
2. Verify CPU returns to normal
3. Investigate the code change

### If caused by traffic spike:
1. Scale up: `kubectl scale deployment/<name> --replicas=<N>`
2. Verify HPA is configured
3. Consider rate limiting

### If caused by a bug (memory leak, infinite loop):
1. Restart the pod: `kubectl delete pod <name>`
2. If persistent, rollback the deployment
3. File a bug ticket

## Escalation
- **After 15 min:** Escalate to on-call senior engineer
- **After 30 min:** Escalate to team lead
- **After 60 min:** Escalate to VP Engineering
