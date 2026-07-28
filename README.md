# Skilder Skills

Agent Skills published by [Skilder](https://skilder.ai), the skills infrastructure platform for AI agents. Every skill in this repo uses the open [Agent Skills](https://agentskills.io) format: a directory with a `SKILL.md` and optional reference files, portable across any compliant agent.

## Install

```bash
npx skills add skilder-ai/skills
```

Or install a single skill:

```bash
npx skills add skilder-ai/skills --skill connect-to-skilder
```

## Skills

| Skill | What it does |
|---|---|
| [`connect-to-skilder`](skills/connect-to-skilder) | One-shot instruction that makes an agent connect itself to Skilder over MCP (OAuth, zero config). Paste it into any agent chat once. |
| [`product-and-service-catalog`](skills/product-and-service-catalog) | Answer "what do we sell / what does it cost / who owns it" from a structured catalog template. |
| [`customer-directory`](skills/customer-directory) | Customer lookups (contacts, account managers, status) with a built-in access policy the agent enforces. |
| [`supplier-directory`](skills/supplier-directory) | Supplier and vendor lookups: contracts, lead times, payment terms, expiring-contract flags. |
| [`team-weekly-planning`](skills/team-weekly-planning) | "Who's working on what this week / who's on PTO" from a weekly planning template. |

The four business skills ship with placeholder reference documents. Fill them with your real data and the agent answers from your numbers, your contacts, your planning.

## Run these skills as production software

These same skills are built into [Skilder](https://app.skilder.ai), where they get versioning, publishing with rollback, per-skill usage measurement, and distribution to every connected agent from one governed MCP endpoint:

```bash
claude mcp add --transport http skilder https://app.skilder.ai/mcp
```

Docs: [docs.skilder.ai](https://docs.skilder.ai) · Support: contact@skilder.ai

## License

MIT
