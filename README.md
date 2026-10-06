# AI SEO Skills & Agent Workflows

A collection of reusable SEO skills and agent instructions for Codex and Gemini, designed for practical, evidence-driven workflows with AI.

## Downloadable bundles

- [Codex skills bundle (ZIP)](https://raw.githubusercontent.com/khajee/ahhhellnah/main/downloads/SEO-Suite-Codex-Optimized.zip)
- [Gemini skills bundle (ZIP)](https://raw.githubusercontent.com/khajee/ahhhellnah/main/downloads/SEO-Suite-Gemini-Optimized.zip)

Both public bundles exclude the proprietary keyword scraper and its standalone skill. The repository keeps the reusable skills and the private keyword engine separate.

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

The broader workflow also uses a proprietary keyword discovery and autocomplete expansion engine for recursive topic research and JSON/CSV exports. Its implementation is kept in a separate private repository. This public repository contains reusable SEO workflows for Codex and Gemini, but excludes the engine's source code and standalone Gemini instructions for using it.

## Design principles

- Modular skills with clear responsibilities
- Evidence-driven recommendations instead of unsupported SEO claims
- Search intent and topic-cluster thinking
- Localized language and regional considerations
- Outputs that are practical for both human teams and AI agents

## Repository structure

```text
codex/
├── agents/                 # Shared Codex agent instructions
└── skills/                 # Reusable Codex skills

gemini/
├── agents/                 # Optional Gemini SEO Director agent
├── skills/                 # Reusable Gemini skills
├── README.md               # Gemini package scope and contents
└── INSTALL.md              # Gemini installation steps
```

## Using the skills

Each skill directory contains a `SKILL.md` with its scope, workflow, constraints, and expected deliverables. See `codex/README.md` and `gemini/README.md` for package details; installation steps are in `gemini/INSTALL.md`.

## Scope note

These are workflow instructions and reusable agent configurations. They are designed to support thoughtful SEO analysis and content planning, not to present keyword suggestions or relative scores as search volume, traffic forecasts, or keyword difficulty without independent validation.
