<div align="center">

# CoreMind Systems

**Compliance Software & Digital Solutions**

We build secure, multi-tenant systems that turn audit and compliance workflows into streamlined, automated processes — with rigorous quality standards baked into every step of development.

![Platform](https://img.shields.io/badge/platform-Helix-0366d6?style=for-the-badge)
![Tests](https://img.shields.io/badge/tests-220%2B%20passing-success?style=for-the-badge)
![Coverage](https://img.shields.io/badge/coverage-80%25%2B-brightgreen?style=for-the-badge)
![Auto--merge](https://img.shields.io/badge/auto--merge-enabled-purple?style=for-the-badge)

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

## How We Build Software

At CoreMind, quality isn't optional — it's enforced at every stage. Our development process is built around automated validation, strict quality gates, and a principle-driven approach that ensures every change meets our standards before it reaches production.

```
Specification → Validation → Implementation → Testing → Quality Gates → Review → Deploy
```

<table>
<tr><td>

| Practice | What it ensures |
|----------|----------------|
| **Constitutional Validation** | Every change checked against 6 core principles |
| **Precision Scoring** | Tasks are atomic, measurable, and unambiguous |
| **Automated Testing** | 220+ tests run on every pull request |
| **Coverage Enforcement** | Minimum 80% coverage — merge blocked otherwise |
| **Integration Sequencing** | Multi-component deployments in correct order |
| **Knowledge Base** | Fast internal search across docs & code patterns |
| **Auto-merge** | PRs that pass all gates merge automatically |

</td></tr>
</table>

### Self-Validating Pull Requests

Every change passes through automated gates before it can reach production:

> **220+ tests** &nbsp;·&nbsp; **80% coverage enforced** &nbsp;·&nbsp; **Principle compliance** &nbsp;·&nbsp; **E2E smoke tests** &nbsp;·&nbsp; **Auto-merge on success**

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

*Secure compliance software, built with discipline.*

</div>
