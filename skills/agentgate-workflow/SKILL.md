---
name: agentgate-workflow
description: Use when implementing code under AgentGate validation gates, slice scopes, token budgets, or Pro multi-slice plans.
version: 0.1.1
---

# AgentGate Workflow

Use this skill when implementing work under AgentGate guardrails.

1. Load `agentgate.config.json` and identify the slice to run.
2. If the slice is created during the session, call `agentgate_define_slice` with its `id`, `description`, `fileScope`, `acceptance`, and `gates`.
3. Implement only inside the slice's `fileScope`.
4. Call `agentgate_run_gate` with the slice id after implementation.
5. Treat any failed, errored, or timed-out gate as blocking. Read the returned tails, fix the issue, and rerun the gate.
6. Do not mark a slice complete until all returned gates pass.
7. Between slices, call `agentgate_budget_status` and stop if the state is `stopped`.
8. For Pro multi-slice work, call `agentgate_run_plan` to execute slices in dependency order with bounded retries.
