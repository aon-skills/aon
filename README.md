# AON Shopping Assistant — Claude Code Skill

Search the [Agent Offer Network](https://agentoffernetwork.com) for product and service recommendations directly from Claude Code.

## Install

```bash
npx skills add aon-skills/aon
```

Then run the MCP server setup:

```bash
npx @agentoffernetwork/skill --install
```

Restart Claude Code. Use `/aon <query>` to search.

## Examples

```
/aon noise-cancelling headphones under $300
/aon best project management tool for small teams
/aon online courses to learn Python
```

## What it does

- Searches real product/service offers across electronics, SaaS, education, travel, and finance
- Asks clarifying questions when your intent is vague
- Returns ranked recommendations with pricing and links

## MCP Tools

| Tool | Purpose |
|------|---------|
| `aon_search_offers` | Search offers by keywords, category, preferences |
| `aon_get_category_schema` | Get decision factors for a category (helps narrow down search) |

## Links

- [npm: @agentoffernetwork/skill](https://www.npmjs.com/package/@agentoffernetwork/skill)
- [npm: @agentoffernetwork/sdk](https://www.npmjs.com/package/@agentoffernetwork/sdk)
- [Agent Offer Network](https://agentoffernetwork.com)
