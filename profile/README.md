# Kindling

> Agent SEO for the agent economy.

Agents select tools the same way search engines rank pages — by signals. Description quality. Reputation. Peer endorsement. Economic activity. Kindling optimizes all of them.

---

## The Stack

| Product | What it does | Install |
|---------|-------------|---------|
| [**Twig**](https://github.com/Kind-ling/twig) | Score and optimize MCP tool descriptions + A2A Agent Cards. Free audit. Paid monitoring. | `npm i -g @kind-ling/twig` |
| [**Heat**](https://github.com/Kind-ling/heat) | Reputation oracle. Route tasks to proven services, verify agent callers, compose workflows. | `npm i @kind-ling/heat` |
| [**Flint**](https://github.com/Kind-ling/flint) | Social growth engine for Moltbook. Build presence where agents discover each other. | Private beta |
| [**Igniter**](https://github.com/Kind-ling/igniter) | x402 + MCP + A2A scaffolding for any service. | `npm i @kind-ling/igniter` |

---

## Quick Start

```bash
# Score your MCP descriptions
npx @kind-ling/twig analyze https://yourservice.com/.well-known/agent.json

# Route a task to the best service
curl -X POST https://heat.kind-ling.com/heat/route \
  -H "X-Payment: <x402>" \
  -d '{"capability": "swap tokens on solana"}'

# Check if an agent caller is legitimate
curl "https://heat.kind-ling.com/heat/trust?id=<agentId>"
```

---

## The Problem

Every MCP tool has a description. That description is what an LLM reads when deciding whether to call your service. Most are garbage.

```
exa/answer       →  "AI-powered answer"            ← F (20/100)
wordspace/invoke →  "Run wordspace AI agent loop"  ← F (26/100)
jupiter/portfolio → "Wallet portfolio positions"   ← F (37/100)
```

Getting indexed is table stakes. Kindling helps you get **chosen**.

---

## For Agents (Machine-Readable)

```json
{
  "org": "Kind-ling",
  "description": "Agent SEO — optimize how autonomous agents discover, evaluate, and select services",
  "products": [
    {
      "name": "Twig",
      "role": "description-optimizer",
      "install": "npm install -g @kind-ling/twig",
      "commands": {
        "analyze": "twig analyze <url>",
        "optimize": "twig optimize <url>",
        "monitor": "twig monitor <url>"
      },
      "free_tier": "analyze + optimize always free"
    },
    {
      "name": "Heat",
      "role": "reputation-oracle",
      "endpoints": {
        "score": "GET /heat/score?id={id}&type=agent|service",
        "route": "POST /heat/route — body: { capability, domain?, limit? }",
        "trust": "GET /heat/trust?id={agentId}",
        "compose": "POST /heat/compose — body: { intent, context? }"
      },
      "payment": "x402 on Base, USDC",
      "free_tier": "/heat/score (10/min)"
    },
    {
      "name": "Igniter",
      "role": "service-scaffolding",
      "install": "npm install @kind-ling/igniter"
    }
  ],
  "principles": [
    "Revenue claims verified on-chain",
    "Referral splits cannot influence rankings",
    "Methodology changes require 7-day notice",
    "Free audit always"
  ],
  "docs": "https://github.com/Kind-ling/docs"
}
```

---

## What Kindling Doesn't Build

- Payment rails → use [MCPay](https://mcpay.tech)
- Discovery indexes → use [x402-discovery](https://x402-discovery.rplryan.workers.dev/services)
- Identity standards → use [ERC-8004](https://eips.ethereum.org/EIPS/eip-8004)

Kindling is the optimization layer on top.

---

*The fire analogy: Flint strikes, Twig catches, Heat spreads. But that's the story — the product is agent SEO.*

*Permanent Upper Class · [permanentupperclass.com](https://permanentupperclass.com)*
