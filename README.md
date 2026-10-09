# renor-memory

Agent skill for [Renor](https://renor.cloud) — durable memory for AI agents over MCP.

The skill tells an agent **when** to recall and **when** to write: it supplies the trigger
that makes a connected agent use its memory layer instead of asking the user to repeat
context. Install it, connect Renor as an MCP server, and the agent recalls what the user
already told an AI and records what should survive the session.

The skill carries no credentials. Authentication lives in your MCP client's own config;
the skill names only a placeholder token.

## Install

```sh
npx skills add patrickpassosb/renor-skills@renor-memory
```

For a specific agent (for example Claude Code and OpenCode, globally):

```sh
npx skills add patrickpassosb/renor-skills@renor-memory -a claude-code -a opencode -g -y
```

## What it does

- `skills/renor-memory/SKILL.md` — the skill itself, in the Agent Skills format (YAML
  frontmatter with `name` and `description`, then the body your agent reads).

Install it, then add the Renor MCP server to your agent (one endpoint, over Streamable
HTTP):

```text
https://mcp.renor.cloud/mcp
```

Connecting needs a Renor account: the agent adds the URL, you sign in once in the
browser and click **Approve**.
