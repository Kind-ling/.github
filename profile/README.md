<div align="center">

<svg width="160" height="32" viewBox="0 0 320 64" fill="none" xmlns="http://www.w3.org/2000/svg">
  <rect x="0" y="38" width="10" height="26" rx="2" fill="#E8652A"/>
  <rect x="14" y="24" width="10" height="40" rx="2" fill="#E8652A"/>
  <rect x="28" y="10" width="10" height="54" rx="2" fill="#E8652A"/>
</svg>

# kindling

**Open infrastructure for the agent economy.**

*Transparent discovery, reputation, and settlement rails for AI agent services.*

---

[![Docs](https://img.shields.io/badge/docs-kind--ling%2Fdocs-E8652A?style=flat-square)](https://github.com/Kind-ling/docs)
[![License](https://img.shields.io/badge/license-MIT-5EBB6E?style=flat-square)](https://github.com/Kind-ling/igniter/blob/main/LICENSE)
[![Built by PUC](https://img.shields.io/badge/built%20by-Permanent%20Upper%20Class-9898AC?style=flat-square)](https://permanentupperclass.com)

</div>

---

## What is Kindling?

Agent adoption is a **configuration and selection decision**, not a marketing funnel.

Five mechanisms determine how AI agents discover, evaluate, adopt, and propagate information about services: MCP tool descriptions, A2A Agent Cards, x402 settlement, context window content, and on-chain transaction history.

The connective infrastructure layer — reputation scoring, quality benchmarking, developer tooling, task routing — is unoccupied. Kindling occupies it with open-source modules that each provide standalone value and, when composed, create reinforcing loops across all five mechanisms.

---

## Modules

| Module | Phase | Status | What it does |
|--------|-------|--------|-------------|
| [**Kindling Igniter**](https://github.com/Kind-ling/igniter) | 1 | 🟠 Building | x402 + MCP + A2A scaffolding. `npx @kindling/igniter init` |
| **Kindling Verifier** | 1 | 🔵 Planned | Multidimensional reputation: Demand · Reliability · Outcome |
| **Kindling Documenter** | 2 | 🔵 Planned | Benchmark engine. Methodology first, results second. |
| **Kindling Scout** | 3 | 🔵 Planned | Agent task routing with on-chain referral economics |

Phase N+1 ships only when Phase N exit criteria are met. No schedule-driven shipping.

---

## Quick Start

```bash
# Add x402 payment + A2A + MCP to any Express service
npm install @kindling/igniter
```

```typescript
import { kindlingPayment } from '@kindling/igniter';

app.get('/api/forecast', kindlingPayment({
  payTo: '0xYourWallet',
  amount: '50000', // $0.05 USDC
}), handler);
```

Every 402 response discloses referral economics before payment. All splits are on-chain and auditable.

---

## Principles

**Open-source, self-hostable, bypassable.** Every module runs standalone. No lock-in.

**Methodology before scores.** Verifier scoring methodology is published and versioned before any score is emitted. Anyone can reproduce a score from on-chain data.

**First-party disclosed everywhere.** [Permanent Upper Class](https://permanentupperclass.com) operates services that participate in Kindling. They are labeled `is_first_party: true` throughout and receive no scoring advantages.

**Referral economics are not routing economics.** Split size has zero effect on ranking or routing position. Hard rule, enforced in code.

---

## Governance

PUC operates both the infrastructure and first-party services. This conflict is real and managed structurally — not through promises.

→ [Read the full governance policy](https://github.com/Kind-ling/docs/blob/main/governance.md)  
→ [Economics & referral mechanics](https://github.com/Kind-ling/docs/blob/main/economics.md)  
→ [Verifier scoring methodology](https://github.com/Kind-ling/docs/blob/main/methodology.md)  
→ [What Kindling is not](https://github.com/Kind-ling/docs/blob/main/what-kindling-is-not.md)

---

## Repositories

| Repo | Description |
|------|-------------|
| [**igniter**](https://github.com/Kind-ling/igniter) | x402 + MCP + A2A scaffolding for any agent service |
| [**docs**](https://github.com/Kind-ling/docs) | Governance, economics, methodology, architecture |
| [**brand**](https://github.com/Kind-ling/brand) | Design tokens, logo system, typography |

---

<div align="center">

*Built by [Permanent Upper Class](https://permanentupperclass.com) · [@zozDOTeth](https://twitter.com/zozDOTeth) · March 2026*

</div>
