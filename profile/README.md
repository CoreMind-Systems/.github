<div align="center">

# CoreMind Systems

**Building Autonomous, AI-Powered Compliance Infrastructure**

We build software that turns audit and compliance workflows into self-operating, secure, multi-tenant systems — powered by AI agents that handle everything from specification to production deployment.

![Platform](https://img.shields.io/badge/platform-Helix-0366d6?style=for-the-badge)
![Autonomous](https://img.shields.io/badge/autonomous-90%25-blue?style=for-the-badge)
![Tests](https://img.shields.io/badge/tests-220%2B%20passing-success?style=for-the-badge)
![Coverage](https://img.shields.io/badge/coverage-80%25%2B-brightgreen?style=for-the-badge)

[**helix.coremindx.com**](https://helix.coremindx.com) &nbsp;&bull;&nbsp; [**coremindx.com**](https://coremindx.com)

</div>

---

## Helix — Audit Compliance Platform

**Helix** is our production multi-tenant SaaS platform where organisations execute compliance inspections, document findings, and manage audit deviations — all within a zero-trust security model.

<table>
<tr>
<td width="50%">

### What it does

- **Compliance Inspections** — Execute and track audit control workflows
- **Finding Management** — Document, assign and resolve deviations
- **Multi-Org Isolation** — Each tenant's data is cryptographically separated at the database level
- **Mobile-Ready** — Full PWA, works on any device down to 375px

</td>
<td width="50%">

### How it's built

| Layer | Technology |
|-------|-----------|
| **Frontend** | React 18 + Vite (PWA) |
| **API** | PostgREST — auto-generated REST from schema |
| **Auth** | FastAPI Edge — JWT (HS256) |
| **Database** | PostgreSQL 14+ with RLS |
| **Infra** | Docker Compose + Cloudflare Tunnel |

</td>
</tr>
</table>

---

## Autonomous AI Framework

What makes CoreMind different: an **in-house AI development framework** that handles 90% of the development lifecycle autonomously — from specification to deployed, tested code.

```
User Request → Constitutional Validation → Task Generation → Parallel Execution → Validation Gates → PR → Auto-merge
```

<table>
<tr><td>

| Module | Purpose | Status |
|--------|---------|--------|
| **Constitutional** | Enforce 6 core principles on every change | ✅ 95% |
| **Precision** | Score task atomicity, detect ambiguity | ✅ 95% |
| **Autonomous** | Generate tasks, execute with retry & rollback | ✅ 90% |
| **Integration** | Multi-component deployment sequencing | ✅ 90% |
| **Knowledge Base** | PostgreSQL RAG — <10ms semantic search | ✅ 100% |
| **Learning** | Track metrics, improve future estimates | ✅ 90% |
| **Governance** | Constitutional PR review + auto-merge | ✅ 85% |

</td></tr>
</table>

### Self-Validating Pull Requests

Every change passes through automated gates before it can reach production:

> **220+ tests** &nbsp;·&nbsp; **80% coverage enforced** &nbsp;·&nbsp; **Constitutional compliance** &nbsp;·&nbsp; **E2E smoke tests** &nbsp;·&nbsp; **Auto-merge on success**

No code reaches production without passing every gate. No exceptions.

---

## Security Model

We enforce **database-first, zero-trust** multi-tenant isolation:

- Every table has a `tenant_id` column with Row-Level Security policies
- Isolation is enforced by PostgreSQL — not by application code
- Even if the application has bugs, the database blocks cross-tenant access
- JWT tokens carry tenant context, set at session level via `current_setting('app.tenant_id')`

```sql
-- Every query is automatically scoped
CREATE POLICY tenant_isolation ON control_points
  FOR ALL USING (tenant_id = current_setting('app.tenant_id')::uuid);
```

---

## Constitutional Principles

Six principles are automatically validated on every commit, PR, and deployment:

| # | Principle | Enforced By |
|---|-----------|-------------|
| 1 | **Multi-Tenant Isolation** — All tables have `tenant_id`, RLS enabled | Migration validator |
| 2 | **No Hardcoded Values** — Colors via CSS vars, types in DB | Code validator |
| 3 | **Configuration Over Code** — Settings in DB/env, never hardcoded | Code validator |
| 4 | **Role-Based UI** — Interface adapts dynamically to user role | Code validator |
| 5 | **Evidence-Based Claims** — All assertions have verification commands | Spec validator |
| 6 | **Responsive Design** — Works at 375px mobile to 1440px desktop | E2E tests |

---

<div align="center">

### Connect with us

[**Platform**](https://helix.coremindx.com) &nbsp;&bull;&nbsp; [**Website**](https://coremindx.com) &nbsp;&bull;&nbsp; [**GitHub**](https://github.com/CoreMind-Systems)

*Building the future of autonomous compliance software.*

</div>
