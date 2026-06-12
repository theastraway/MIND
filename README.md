# MIND — Persistent Memory for AI Agents

[MIND](https://m-i-n-d.ai) is the persistent memory and knowledge-graph layer
for AI agents — identity, memories, decisions, tasks, contacts, and emotional
context that survive across every session, every tool, and every agent.

This is the public MIND integration hub: everything you need to connect any
agent to a MIND, three ways.

| Door | For | Start here |
|---|---|---|
| **MCP** | Claude Desktop, claude.ai, Cursor, Windsurf — any MCP client | [m-i-n-d.ai/mcp](https://m-i-n-d.ai/mcp) |
| **CLI** | Claude Code, VPSs, CI, terminals | [m-i-n-d.ai/cli](https://m-i-n-d.ai/cli) |
| **Skills** | Claude Code, Cursor, and skills-aware agents | [m-i-n-d.ai/skills](https://m-i-n-d.ai/skills) |

Every door opens onto the same brain: **24 tools, 147 actions** covering
memory, the knowledge graph, LIFE board, calendar, CRM, tasks, emotional
intelligence, autonomous insights, deep research, self-training, social,
automations, and the Agent Command Center.

## MCP

```bash
npm install -g @astramindapp/mcp-server
```

Get a key at [m-i-n-d.ai](https://m-i-n-d.ai) → Settings → Developer → API
Keys (prefix `mind_`), then connect:

**Claude Code**

```bash
claude mcp add mind -- env MIND_API_KEY=mind_xxx mind-mcp
```

**Claude Desktop / Cursor** — add to your MCP config:

```json
{
  "mcpServers": {
    "mind": {
      "command": "mind-mcp",
      "env": { "MIND_API_KEY": "mind_your_key_here" }
    }
  }
}
```

## CLI

The same package ships two binaries:

```bash
mind-mcp-setup                      # guided onboarding — wires your MCP clients
MIND_API_KEY=mind_xxx mind-mcp      # run the server directly, anywhere
```

## Skills

```bash
npx skills add theastraway/MIND
```

Pulls the [`mind`](./skills/mind/SKILL.md) skill — the MIND operating
discipline: session protocol (context → query → remember), privacy rules,
and the full tool map — into your agent.

## REST

Everything above maps 1:1 to the REST API:

```
https://m-i-n-d.ai/developer/v1     header: X-API-Key: mind_xxx
```

Use it from n8n, scripts, backends, or any runtime without MCP support.

## OpenClaw

OpenClaw agents skip the MCP server and install the native plugin:

```bash
openclaw plugins install @astramindapp/openclaw-mind
```

## Links

- App: [m-i-n-d.ai](https://m-i-n-d.ai)
- MCP server on npm: [`@astramindapp/mcp-server`](https://www.npmjs.com/package/@astramindapp/mcp-server)
- Connect pages: [/mcp](https://m-i-n-d.ai/mcp) · [/cli](https://m-i-n-d.ai/cli) · [/skills](https://m-i-n-d.ai/skills)

---

MIND is built by [Astra AI](https://m-i-n-d.ai). Patents pending.
