---
name: local-model-orchestrator
description: Orchestrate available local language models for coding, review, research, and testing while a primary Codex agent owns integration and verification. Use when the user asks to use, manage, delegate to, or prioritize local or Ollama models. Do not activate merely because a local model is installed.
---

# Local Model Orchestrator

Use local models as explicit specialists without weakening project ownership, safety, or validation.

## Establish the local pool

- Use only model IDs that the current environment exposes or the user explicitly provides. Never invent a local model name.
- Prefer explicit model selection per delegated task instead of relying on a runtime default.
- Briefly tell the user which local models will handle which roles. Do not claim that the full Codex session, orchestration layer, or all data flows are local unless the environment proves that.
- If no local model is callable, report that fact and continue with the primary agent only unless the user made local execution a hard requirement.

## Minimize primary-model usage

- Keep the currently selected primary model as the root orchestrator responsible for scope, decisions, integration, verification, and the final response.
- Use callable local models first for bounded analysis, code drafting, test design, edge-case enumeration, documentation summaries, and first-pass review. Give them only the files and context needed for that subtask.
- When local models cannot reliably cover a bounded task, prefer the lowest-consumption available OpenAI model that can do it: choose the currently exposed Luna-tier model first, then Terra-tier. Use a higher-capability model only when correctness, ambiguity, or integration risk justifies it.
- When creating agents, pass minimal history (`fork_turns="none"` or a small recent-turn window) whenever sufficient, explicitly assign a local/Luna/Terra model for bounded work, and leave the selected primary model in charge of the overall task.
- Avoid redundant parallel reviews, repeated full-repository reads, and sending unchanged large files to multiple models. Reuse verified findings and concise structured outputs.
- Report local and fallback model contributions separately. Do not claim an exact Codex token saving unless a reliable per-task meter exists; label estimates as estimates.

## Delegate by bounded responsibility

Keep the primary agent responsible for scope, repository state, integration, and the final answer. Delegate only work that has a clear input, output, and completion test, such as:

- proposing a data model or implementation approach;
- implementing an isolated file or module when concurrent editing is permitted;
- reviewing a specified diff or API boundary;
- drafting targeted tests or checking edge cases.

Match tasks to model strengths when evidence exists. Otherwise start with one small representative task before expanding a model's role. Avoid multiple agents editing the same files. Follow any active project or artifact skill's stricter delegation rules; when those rules reserve editing for the owner, local agents return recommendations only.

## Prompt and recover deliberately

Give each local agent the minimum relevant context, exact deliverable, constraints, file ownership, and instruction not to broaden scope. Prefer concise English task prompts for smaller local models while preserving the user's required language and locale in the deliverable.

If a model misreads non-Latin text, returns unrelated output, or fails to follow the task, retry once with a shorter English prompt and explicit acceptance criteria. After a second failure, switch to another available model or complete the task with the primary agent. Do not loop indefinitely.

## Verify before integration

Treat local-model output as an untrusted draft. The primary agent must:

1. inspect proposed changes or recommendations;
2. check them against the user's scope and repository instructions;
3. run proportionate builds, tests, or focused checks;
4. repair or reject output that is incorrect, unsafe, or needlessly complex.

Prefer a small verified contribution over broad parallel generation. In the final response, summarize material local-model contributions and any part the primary agent replaced or corrected; omit routine orchestration details.
