# AgentGate Installer

Public Claude Code and Codex installer metadata for AgentGate.

AgentGate itself is distributed from npm as `@idevelopers/agentgate`. The free
tier is local single-slice validation; the source repository remains private.
Polar handles paid licenses and issues license keys.

AgentGate helps AI coding agents prove work is done: define a slice, run real
validation gates, and keep completion blocked until checks pass.

Landing/demo page draft: [`landing.html`](landing.html)

## Claude Code Plugin Install

```text
/plugin marketplace add https://github.com/manish-1988/agentgate-installer
/plugin install agentgate@agentgate-marketplace
```

## Direct MCP Install

```sh
claude mcp add agentgate -- npx -y @idevelopers/agentgate
```

## Buy Pro Or Team

```text
https://buy.polar.sh/polar_cl_VxlhG8lCO6IUcLcveJ51YOXYXMHWdUNorKr0U1bhyqm
```

After purchase, activate the issued Polar license key with
`agentgate_activate_license`.

Pro unlocks multi-slice plan execution, bounded retries, typecheck/build/custom
gates, token-budget stops, and analytics export.
