# Claude Instructions

This is the **Health Shield Content System (HSCS)**, a skill-based system for content creation across UX writing, content design, content strategy, technical documentation, developer content, marketing, editorial, AI/MCP agents, and research synthesis.

## What This Repo Is

HCS is a library of **skills**—structured packages for specific content tasks. Each skill defines exactly how to produce a type of content: what inputs you need, what workflow to follow, what format to use, and how to validate quality.

## Repo Structure

```
/shared/              → Global content standards (apply to ALL outputs)
/governance/          → Repo rules, skill catalog, glossary, eval spec
/evals/               → Test cases for skill outputs
/{category}/{skill}/  → Individual skill packages
```

## Skill Categories

| Category | Content Types |
|----------|---------------|
| `ux-writing` | Error messages, empty states, dialogs, notifications, forms, onboarding |
| `content-design` | UI copy systems, patterns, audits, naming, cognitive load |
| `content-strategy` | Voice/tone, taxonomy, messaging hierarchy, roadmaps |
| `content-context` | Feature context packs, vocabulary, state maps, user journeys |
| `technical-documentation` | How-to guides, API docs, reference docs, release notes |
| `developer-content` | CLI help, SDK docs, code comments, configuration guides |
| `mcp-and-agents` | Agent instructions, system prompts, tool descriptions, evals |
| `marketing` | Landing pages, product messaging, campaigns, app store listings |
| `editorial-and-blog` | Blog posts, case studies, thought leadership, tutorials |
| `research-and-insights` | User research synthesis, feedback analysis, audit reports |

## Trigger Index

Quick-match triggers to skills. See `governance/skill-catalog.md` for full details.

**ux-writing:** `writing-error-messages` (error, error message, failure) · `writing-empty-states` (empty state, no results, blank state) · `writing-confirmation-dialogs` (confirmation, dialog, modal, delete confirm) · `writing-onboarding-steps` (onboarding, welcome, getting started) · `writing-settings-and-preferences` (settings, preferences, options) · `writing-status-and-progress` (status, progress, loading) · `writing-form-labels-and-helptext` (form, label, placeholder, help text) · `writing-permission-and-access-messages` (permission, access, allow, deny) · `writing-loading-and-latency-messaging` (loading, wait, processing) · `writing-notifications-and-toasts` (notification, toast, alert, snackbar) · `writing-accessible-ui-copy` (accessible copy, screen reader, a11y)

**content-context:** `creating-context-packs-for-ai` (context pack, AI context) · `defining-feature-vocabulary` (vocabulary, terminology) · `diffing-and-versioning-context-packs` (context diff, version comparison) · `generating-feature-content-context` (feature context, content context) · `generating-state-maps` (state map, UI states) · `mapping-content-to-user-journeys` (journey mapping, user flow) · `updating-feature-context-from-feedback` (context update, feedback integration) · `validating-context-completeness` (context validation, completeness check)

**content-design:** `auditing-ui-copy` (copy audit, UI review) · `designing-content-governance-flows` (governance, approval flow) · `designing-content-pattern-libraries` (pattern library, content patterns) · `designing-microcopy-systems` (microcopy, UI text system) · `designing-progressive-disclosure` (progressive disclosure, layered content) · `mapping-user-intents-to-copy` (intent mapping, user goals) · `naming-features-and-settings` (feature naming, setting names, naming) · `reducing-cognitive-load` (cognitive load, simplification) · `structuring-ui-content` (content structure, UI organization)

**content-strategy:** `aligning-content-with-brand` (brand alignment, brand voice) · `building-taxonomy-and-ia` (taxonomy, IA, information architecture) · `creating-content-briefs` (content brief, project brief) · `creating-content-principles` (content principles, guiding principles) · `creating-messaging-hierarchy` (messaging hierarchy, message priority) · `defining-voice-and-tone` (voice, tone, personality) · `designing-content-experiments` (content testing, A/B test) · `measuring-content-performance` (content metrics, measurement) · `planning-content-roadmaps` (content roadmap, planning)

**developer-content:** `designing-developer-onboarding` (developer onboarding, quickstart) · `documenting-tooling-workflows` (tooling docs, workflow documentation) · `writing-cli-errors-and-exit-codes` (CLI error, exit code) · `writing-cli-help-and-usage` (CLI help, usage, --help) · `writing-code-comments-and-docstrings` (code comments, docstrings) · `writing-command-tutorial-flows` (CLI tutorial, walkthrough) · `writing-configuration-guides` (config guide, configuration) · `writing-sdk-docs-and-samples` (SDK docs, code samples)

**technical-documentation:** `writing-how-to-guides` (how-to, step-by-step, procedure) · `writing-reference-docs` (reference, API reference) · `writing-troubleshooting-guides` (troubleshooting, debug, fix) · `writing-api-documentation` (API docs, endpoint docs) · `writing-release-notes` (release notes, changelog, what's new) · `maintaining-docs-as-code` (docs as code, doc automation) · `structuring-doc-information-architecture` (doc IA, doc navigation) · `documenting-breaking-changes` (breaking change, migration guide) · `designing-documentation-navigation` (doc navigation, sidebar, TOC)

**editorial-and-blog:** `designing-headline-variants` (headline, title variants) · `editing-and-style-enforcement` (editing, style enforcement) · `improving-readability-and-flow` (readability, flow, clarity) · `structuring-long-form-content` (long-form structure, article structure) · `writing-blog-posts` (blog post, blog, article) · `writing-case-studies` (case study, customer story) · `writing-thought-leadership` (thought leadership, opinion) · `writing-tutorial-articles` (tutorial, how-to article)

**marketing:** `creating-message-maps` (message map, messaging matrix) · `designing-conversion-copy` (conversion copy, CTA) · `writing-app-store-listings` (app store, Play Store) · `writing-email-campaigns` (email campaign, newsletter) · `writing-landing-pages` (landing page, LP, product page) · `writing-product-announcements` (announcement, launch) · `writing-product-messaging` (product messaging, positioning, value prop) · `writing-sales-enablement-content` (sales enablement, battle cards) · `writing-social-media-content` (social media, social post)

**mcp-and-agents:** `auditing-agent-behavior` (agent audit, behavior review) · `defining-guardrails-and-constraints` (guardrails, constraints) · `designing-agent-instructions` (agent instructions, agent prompt) · `designing-agent-workflows` (agent workflow, orchestration) · `designing-context-injection-patterns` (context injection, RAG) · `designing-evaluations-for-agents` (agent evals, testing agents) · `structuring-system-prompts` (system prompt, base prompt) · `writing-mcp-tool-descriptions` (MCP, tool description)

**research-and-insights:** `synthesizing-user-research` (user research, research synthesis) · `extracting-insights-from-feedback` (feedback analysis, user feedback) · `structuring-content-audit-reports` (audit report, content audit findings) · `writing-research-summaries` (research summary, findings) · `mapping-qualitative-to-quantitative` (qual to quant, mixed methods) · `designing-interview-guides` (interview guide, user interview) · `analyzing-survey-results` (survey analysis, survey data) · `creating-content-opportunity-maps` (opportunity map, content gaps)

## Skill Package Structure

Every skill folder contains:

| File | What It Does | How You Use It |
|------|--------------|----------------|
| `SKILL.md` | Defines triggers, required inputs, workflow, degrees of freedom | Read first. Tells you what the skill does and what you need to execute it. |
| `TEMPLATES.md` | Provides output structures and formats | Use as your output scaffold. Follow this structure unless user overrides. |
| `RUBRIC.md` | Lists pass/fail criteria for output quality | Validate output against every criterion before delivering. |
| `EXAMPLES.md` | Shows input/output pairs of correct execution | Reference when handling edge cases or unfamiliar scenarios. |

Optional files:
- `CHECKLIST.md` – Quick validation checklist
- `reference/` – Domain-specific reference docs
- `scripts/` – Validation scripts

## How to Execute a Skill

### Step 1: Find the Right Skill
Look up `governance/skill-catalog.md`. Match the user's request to a skill using triggers.

**Example:** User asks "write an error message for a failed upload" → triggers match `writing-error-messages` skill.

### Step 2: Read SKILL.md
Open the skill's `SKILL.md`. Identify:
- **Required inputs** – Must have before you proceed
- **Optional inputs** – Have defaults if not provided
- **Workflow** – Steps to follow in order
- **Degrees of freedom** – Where you can use judgment

### Step 3: Gather Missing Inputs
If the user hasn't provided required inputs, ask for them. Be specific about what you need and why.

### Step 4: Apply Shared Standards
Load and apply all files from `/shared`:

| File | Governs |
|------|---------|
| `shared/style.md` | Capitalization, punctuation, formatting |
| `shared/voice.md` | Voice attributes, tone for context |
| `shared/accessibility.md` | Inclusive language, reading level |
| `shared/localization.md` | Translation-ready patterns |
| `shared/legal-safety.md` | Prohibited claims, disclosures |

### Step 5: Generate Using TEMPLATES.md
Use the structure from `TEMPLATES.md` as your output format. This ensures consistency.

### Step 6: Validate with RUBRIC.md
Before delivering, check your output against every criterion in `RUBRIC.md`. All criteria must pass.

### Step 7: Check EXAMPLES.md for Edge Cases
If you're unsure how to handle something, look for a similar scenario in `EXAMPLES.md`.

## Terminology

Use canonical terms from `governance/glossary.json`. Never use prohibited synonyms listed there.

## What You Must Not Do

- Invent rules not documented in this repo
- Skip a skill when one exists for the request
- Deliver output that fails any RUBRIC.md criterion
- Override or ignore `/shared` standards
- Assume file contents—always read them

## Quick Start with Prompts

If the user wants a fast start, point them to `PROMPTS.md`. It contains ready-to-use prompts for every skill category—they just fill in the brackets and go.

## When No Skill Matches

1. Tell the user no matching skill exists.
2. Apply `/shared` standards only.
3. Offer to help scope a new skill if the task is recurring.

## Output Format

1. Lead with the content output.
2. State which skill you applied (or that none matched).
3. Flag any rubric items that may need user judgment.
4. Keep explanations brief unless asked for rationale.
