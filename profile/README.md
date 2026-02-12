# CoreMind Systems

**Compliance Platform & Digital Agency**

CoreMind Systems develops software solutions for compliance and audit workflows. Our main product is **Helix**, a multi-tenant SaaS platform for audit control management.

---

## Helix Platform

![Coverage](https://img.shields.io/badge/test%20coverage-80%25-brightgreen) ![Tests](https://img.shields.io/badge/tests-220%20passing-success) ![Auto-merge](https://img.shields.io/badge/auto--merge-enabled-purple)

**Helix** is a multi-tenant SaaS platform for managing audit control workflows.

### Technical Approach

- **Development Practices** — Comprehensive testing (220 tests), 80% coverage requirement, automated quality gates
- **Security Model** — Multi-tenant isolation at PostgreSQL level using Row-Level Security (RLS)
- **Architecture** — Database-first design with constitutional principles (multi-tenant, RLS, configuration over hardcoding)
- **Knowledge Management** — PostgreSQL-based documentation and code pattern search
- **Automation** — Automated PR validation and merge when quality gates pass

### Platform Stats

| Metric | Value | Status |
|--------|-------|--------|
| **Test Suite** | 220 tests | ✅ 100% pass |
| **Coverage Enforcement** | 80% minimum | ✅ Blocking |
| **Framework Modules** | 7 (280K lines) | ✅ Production ready |
| **Knowledge Search** | <10ms | ✅ PostgreSQL FTS |
| **Auto-merge PRs** | Enabled | ✅ On success |
| **Platform Status** | Multi-tenant SaaS | ✅ Production |

---

## Development Framework

The platform includes a development framework with 7 modules:

**1. Constitutional** — Specification validation against core principles  
**2. Precision** — Task atomicity scoring and ambiguity detection  
**3. Task Management** — Task generation and execution support  
**4. Integration** — Deployment sequencing with rollback capability  
**5. Knowledge Base** — PostgreSQL-based documentation search  
**6. Learning** — Time tracking and estimation improvement  
**7. Governance** — Automated code review and validation  

### Skill System

Knowledge management system for development patterns:

- **4 Production-Ready Skills** — Database, API design, UI patterns, testing strategies
- **<1ms Discovery** — 500x faster than baseline, keyword-based search
- **Linking System** — Skills reference each other, forming knowledge networks
- **Schema v2.0 Compliance** — 100% validated, consistent structure
- **63/63 Tests Passing** — 25 LinkIndex + 38 SkillSynthesizer tests

**Performance:**
- Skill synthesis: 30-50ms (4-7x faster than target)
- Index build: 0.26ms (38x faster than target)
- Keyword search: 0.002ms (500x faster than target)

---

## Tech Stack

**Frontend:** React 18 + Vite (PWA with responsive design)  
**API Gateway:** PostgREST (auto-generated REST from PostgreSQL schema)  
**Auth Service:** FastAPI (JWT signing + tenant extraction)  
**Database:** PostgreSQL 14+ (multi-tenant with RLS policies)  
**Reverse Proxy:** nginx (static files + API routing)  
**CDN/Tunnel:** Cloudflare (HTTPS + DDoS protection)  
**Deployment:** Docker Compose (local + production parity)  
**Testing:** Playwright (E2E tests on production URL)  

---

## Technical Details

### Multi-Tenant Security

Security enforced at PostgreSQL level, not application code:
- Every table has `tenant_id` column
- RLS policies enforce isolation automatically
- Zero-trust: Even if application has bugs, database blocks cross-tenant access

### Automated Testing and Validation

Every PR automatically runs:
- ✅ 220+ tests (unit + integration + E2E)
- ✅ Constitutional checks (0 violations required)
- ✅ Coverage enforcement (≥ 80%)
- ✅ Security scanning
- ✅ Smoke tests

PRs are automatically merged when all automated checks pass.

### Knowledge Base

10ms queries across 535 documentation sections + 9 code sections:
- ✅ Instant pattern lookup (<10ms)
- ✅ Auto-updated on code changes
- ✅ Exact line numbers for code sections
- ✅ Relevance scoring (0.75+ = valid match)

---

## Links

- **Production Platform:** [helix.coremindx.com](https://helix.coremindx.com)
- **Documentation:** See our repositories for technical documentation
- **Organization:** [CoreMind Systems on GitHub](https://github.com/CoreMind-Systems)
