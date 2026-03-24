# Kindling

> Kindling is the SEO platform for the agent economy. We help agent services get discovered, selected, and chosen by the autonomous systems that are now the buyers.

---

## Products

| Product | What it does | Status |
|---------|-------------|--------|
| [**Twig**](https://github.com/Kind-ling/twig) | Audit and optimize MCP descriptions + A2A Agent Cards for agent discovery. Continuous monitoring. Free audit. Paid monitoring. | 🟢 Live |
| [**Flint**](https://github.com/Kind-ling/flint) | Growth engine for agent social platforms (Moltbook). Analyze, optimize, schedule, track. | 🟠 Private beta |
| [**Igniter**](https://github.com/Kind-ling/igniter) | x402 + MCP + A2A scaffolding for any agent service. Compatible with MCPay. | 🟡 Ecosystem tool |
| [**Docs**](https://github.com/Kind-ling/docs) | Governance, economics, methodology | 🟢 Live |
| [**Brand**](https://github.com/Kind-ling/brand) | Design tokens, logos, typography | 🟢 Live |

---

## Agent SEO — the full suite

- **Twig** audits and optimizes how agents *see* your service — descriptions, Agent Cards, registry presence
- **Flint** builds your visibility on agent social platforms — Moltbook growth, content optimization, scheduling
- **Igniter** scaffolds the infrastructure your service runs on — x402, MCP, A2A in one package

Kindling doesn't rebuild payments ([MCPay](https://mcpay.tech)), identity ([ERC-8004](https://eips.ethereum.org/EIPS/eip-8004)), or discovery indexes ([x402-discovery](https://x402-discovery.rplryan.workers.dev/services)). We're the optimization layer on top.

Everyone else helps you *exist*. Kindling helps you get *chosen*.

---

## The Problem

Every MCP tool has a description. That description is what an LLM reads when deciding whether to call your service. It's the only signal between **selected** and **skipped**.

```
exa/answer       →  "AI-powered answer"            ← F (28/100)
wordspace/invoke →  "Run wordspace AI agent loop"  ← F (31/100)
jupiter/portfolio → "Wallet portfolio positions"   ← D (42/100)
```

These tools are useful. Their descriptions are not.

```bash
npx @kindling/twig analyze https://myservice.com/.well-known/agent.json
```

---

## Principles

- Measure everything on-chain. Revenue claims are verifiable.
- No composite scores that hide dimension trade-offs.
- Referral splits can't influence rankings — enforced in code.
- Methodology changes require 7-day public notice.
- Free audit, always. Pay only for monitoring and intelligence.

→ [Governance and methodology](https://github.com/Kind-ling/docs)

---

*Permanent Upper Class · [permanentupperclass.com](https://permanentupperclass.com)*
