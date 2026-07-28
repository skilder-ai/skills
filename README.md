# Skilder Skills

Agent Skills published by [Skilder](https://skilder.ai), the skills infrastructure platform for AI agents. Every skill in this repo uses the open [Agent Skills](https://agentskills.io) format: a directory with a `SKILL.md` and optional reference files, portable across any compliant agent.

## Install

```bash
npx skills add skilder-ai/skills
```

## Skills

| Skill | What it does |
|---|---|
| [`connect-to-skilder`](skills/connect-to-skilder) | One-shot instruction that makes an agent connect itself to Skilder over MCP (OAuth, zero config). Paste it into any agent chat once. |

## What connecting gets you

Skilder gives your team's skills and MCP tool connections a production lifecycle: versioning, publishing with rollback, per-skill usage measurement, and distribution to every connected agent from one governed endpoint:

```bash
claude mcp add --transport http skilder https://app.skilder.ai/mcp
```

Skills use the open Agent Skills format, so existing skill folders import as-is and everything stays portable.

Docs: [docs.skilder.ai](https://docs.skilder.ai) · Support: contact@skilder.ai

## License

MIT
