<p align="center">
  <h1 align="center">AON — Claude Code Skill</h1>
  <p align="center">
    Search the <a href="https://agentoffernetwork.com">Agent Offer Network</a> for product and service recommendations directly from Claude Code.
  </p>
</p>

<p align="center">
  <a href="https://opensource.org/licenses/MIT"><img src="https://img.shields.io/badge/license-MIT-blue.svg" alt="License" /></a>
  <a href="https://www.npmjs.com/package/@agentoffernetwork/skill"><img src="https://img.shields.io/npm/v/@agentoffernetwork/skill.svg" alt="npm version" /></a>
  <a href="https://github.com/aon-skills/aon/issues"><img src="https://img.shields.io/github/issues/aon-skills/aon.svg" alt="Issues" /></a>
</p>

---

## Install

```bash
npx skills add aon-skills/aon
```

Then install the MCP server:

```bash
npx @agentoffernetwork/skill --install
```

Restart Claude Code. You're ready to go.

## Usage

```
/aon noise-cancelling headphones under $300
/aon best project management tool for small teams
/aon online courses to learn Python
/aon luxury hotel in Tokyo for next week
/aon credit card with travel rewards and no annual fee
```

## How It Works

```
User: /aon <query>
  │
  ├─ 1. Parse intent (category, budget, features)
  │
  ├─ 2. Clarify if needed (via category schema)
  │
  ├─ 3. Search AON offers (real-time API)
  │
  └─ 4. Return ranked recommendations
         with pricing, links, and comparison
```

The skill connects to the [AgentOffer Network](https://agentoffernetwork.com) — an open marketplace where AI agents discover and recommend real products and services across 6 industry categories.

## Categories

| Category | Examples |
|----------|----------|
| Electronics | Headphones, laptops, wearables |
| Software & SaaS | Project management, CRM, dev tools |
| Education | Online courses, certifications |
| Travel & Hospitality | Hotels, flights, vacation packages |
| Financial Services | Credit cards, insurance, loans |
| Entertainment | Games, streaming, media subscriptions |

## MCP Tools

| Tool | Purpose |
|------|---------|
| `aon_search_offers` | Search offers by keywords, category, preferences, and budget |
| `aon_get_category_schema` | Get decision factors for a category (helps narrow down search) |

## Requirements

- [Claude Code](https://claude.ai/claude-code) with Skills support
- Node.js >= 18

## Links

- [npm: @agentoffernetwork/skill](https://www.npmjs.com/package/@agentoffernetwork/skill)
- [npm: @agentoffernetwork/sdk](https://www.npmjs.com/package/@agentoffernetwork/sdk)
- [AgentOffer Protocol](https://agentoffernetwork.org)
- [Agent Offer Network](https://agentoffernetwork.com)

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

## License

This project is licensed under the [MIT License](LICENSE).
