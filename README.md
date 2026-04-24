<p align="center">
  <h1 align="center">AON — MCP Skill</h1>
  <p align="center">
    Search the <a href="https://agentoffernetwork.com">Agent Offer Network</a> for product and service recommendations from any MCP-compatible AI host.
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
npx @agentoffernetwork/skill --install --global
```

Restart your MCP host (Claude Code, Claude Desktop, Cursor, etc.). You're ready to go.

Alternative install via the official AON CLI:

```bash
npm install -g @agentoffernetwork/cli
aon skill install @agentoffernetwork/skill --global
```

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

The skill connects to the [AgentOffer Network](https://agentoffernetwork.com) and follows the canonical AON taxonomy defined here:

- <https://github.com/agentoffernetwork/protocol/blob/main/specs/category-taxonomy.md>

Current public categories:

- `software_saas`
- `travel_hospitality`
- `education`
- `financial_service`
- `electronics`
- `entertainment`
- `health_beauty`
- `fashion`
- `food_grocery`
- `home_garden`
- `automotive`

## Categories

| Category | Examples |
|----------|----------|
| Software & SaaS | Project management, CRM, dev tools |
| Travel & Hospitality | Hotels, flights, vacation packages |
| Education | Online courses, certifications |
| Financial Services | Credit cards, insurance, loans |
| Electronics | Headphones, laptops, wearables |
| Entertainment | Games, streaming, AI companions, music, live content |
| Health & Beauty | Skincare, supplements, cosmetics, wellness |
| Fashion | Clothing, shoes, accessories, jewelry |
| Food & Grocery | Meal kits, grocery delivery, snacks, beverages |
| Home & Garden | Furniture, appliances, decor, smart home |
| Automotive | Cars, lease, insurance, parts, EV charging |

## MCP Tools

| Tool | Purpose |
|------|---------|
| `aon_search_offers` | Search offers by keywords, category, preferences, and budget |
| `aon_get_category_schema` | Get decision factors for a category (helps narrow down search) |

`aon_get_category_schema` currently ships built-in decision schemas for all 11 current canonical categories: `software_saas`, `travel_hospitality`, `education`, `financial_service`, `electronics`, `entertainment`, `health_beauty`, `fashion`, `food_grocery`, `home_garden`, and `automotive`.

## Requirements

- Any MCP-compatible host (Claude Code, Claude Desktop, Cursor, Windsurf, etc.)
- Node.js >= 18

## Links

- [npm: @agentoffernetwork/skill](https://www.npmjs.com/package/@agentoffernetwork/skill)
- [npm: @agentoffernetwork/cli](https://www.npmjs.com/package/@agentoffernetwork/cli)
- [npm: @agentoffernetwork/sdk](https://www.npmjs.com/package/@agentoffernetwork/sdk)
- [AgentOffer Protocol](https://agentoffernetwork.org)
- [Agent Offer Network](https://agentoffernetwork.com)

## Source of Truth

This repository mirrors the public MCP skill definition and wrapper documentation. The packaged MCP server implementation is published from `@agentoffernetwork/skill` and maintained in the main AON monorepo:

- [AON monorepo](https://gitlab.com/jolibox-dev-team/aon/aon-main)

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

## License

This project is licensed under the [MIT License](LICENSE).
