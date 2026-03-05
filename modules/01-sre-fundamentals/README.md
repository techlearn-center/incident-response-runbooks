# Module 01: SRE Fundamentals and Culture

| | |
|---|---|
| **Time** | 3 hours |
| **Difficulty** | Beginner |

---

## Learning Objectives

- Understand Site Reliability Engineering principles
- Know the difference between SRE and traditional Ops
- Understand the SRE role in an organization

---

## Key Concepts

### What is SRE?

SRE is what happens when you ask a software engineer to design an operations team. Created at Google in 2003 by Ben Treynor.

**Core principles:**
1. **Embrace risk** — 100% reliability is wrong target
2. **SLOs, not SLAs** — Internal targets before customer contracts
3. **Eliminate toil** — Automate repetitive operational work
4. **Monitor meaningfully** — SLIs tied to user experience
5. **Release engineering** — Make deployments boring
6. **Simplicity** — Complexity is the enemy of reliability

### SRE vs DevOps

| SRE | DevOps |
|---|---|
| Specific role with specific practices | Cultural movement |
| Error budgets, SLOs, on-call | CI/CD, collaboration, automation |
| Prescriptive (how) | Descriptive (what) |
| SRE implements DevOps principles | DevOps is the philosophy |

---

## Hands-On Lab

### Exercise 1: Define Your Team Charter

Write an SRE charter for a fictional e-commerce platform:
- What services does the SRE team own?
- What is the on-call rotation?
- What is the error budget policy?
- When does the SRE team engage vs the dev team?

### Exercise 2: Identify Toil

List 10 manual operational tasks and classify:
- Is it manual? Repetitive? Automatable? No lasting value?
- If yes to all → It is **toil** and should be automated

**Next: [Module 02 →](../02-sli-slo-sla/)**
