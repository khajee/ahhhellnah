# AI SEO Skills & Agent Workflows

A collection of reusable Codex skills and agent instructions for building practical, evidence-driven SEO workflows with AI.

## What this repository contains

This repository packages a modular SEO toolkit. Each skill is self-contained and can be used independently or orchestrated through the SEO manager and director agents.

### SEO strategy and analysis

- **Competitor Analyzer** — identifies ranking patterns, intent mismatches, content gaps, and information-gain opportunities.
- **Technical Auditor** — reviews crawlability, indexing, site architecture, Core Web Vitals, and technical SEO risks.
- **Local Strategist** — develops localized search strategies for physical businesses, Google Maps, and regional visibility.
- **E-E-A-T Builder** — improves signals of experience, expertise, authoritativeness, and trustworthiness.
- **Content Pruner** — evaluates older content for updating, merging, redirecting, or removal to reduce cannibalization.

### Content and on-page optimization

- **Content Writer** — produces SEO-focused articles and service content around clustered search intent.
- **On-Page Optimizer** — creates titles, metadata, URLs, headings, image alt text, and resilient semantic targeting.
- **Internal Linker** — designs topic-cluster linking systems with natural, penalty-safe anchor text.
- **Schema Generator** — creates localized JSON-LD markup for articles, products, FAQs, and other entities.
- **Proposal Builder** — turns website analysis into client-facing SEO proposals and workload estimates.
- **Off-Page PR** — develops digital PR hooks and ethical outreach strategies for authority building.

### Orchestration

- **SEO Manager Agent** — coordinates specialized SEO skills into a structured workflow.
- **SEO Director Agent** — provides end-to-end orchestration across research, strategy, content, technical SEO, and promotion.
- **Local Model Orchestrator** — supports delegation to available local language models for research, coding, review, and testing.

## Private keyword discovery engine

The broader workflow also uses a proprietary keyword discovery and autocomplete expansion engine for recursive topic research and JSON/CSV exports. Its implementation is intentionally kept in a separate private repository; this public repository contains only the surrounding, reusable SEO workflows.

## Design principles

- Modular skills with clear responsibilities
- Evidence-driven recommendations instead of unsupported SEO claims
- Search intent and topic-cluster thinking
- Localized language and regional considerations
- Outputs that are practical for both human teams and AI agents

## Repository structure

```text
codex/
├── agents/                 # Shared agent instructions
└── skills/                 # Reusable Codex skills
    ├── seo-*/
    └── local-model-orchestrator/
```

## Using the skills

Each skill directory contains a `SKILL.md` with its scope, workflow, constraints, and expected deliverables. Copy the desired skill into your Codex skills directory, or use the manager/director agents to coordinate a larger SEO task.

## Scope note

These are workflow instructions and reusable agent configurations. They are designed to support thoughtful SEO analysis and content planning, not to present keyword suggestions or relative scores as search volume, traffic forecasts, or keyword difficulty without independent validation.
