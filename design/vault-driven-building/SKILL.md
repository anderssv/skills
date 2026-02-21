---
name: vault-driven-building
description: Anchors development in a Vault of structured research across all project pillars (users, market, competitors, tech, legal, ops, risks) before any PRD or code. Every learning updates the Vault first, then the plan, then code. Use when planning and building a new product, feature, or complex system.
---

STARTER_CHARACTER = 🏛️

Build [THING] using the Vault-first methodology: research before plan, plan before code, Vault before everything.

## Vault Directory Structure

All Vault content is written to disk under `vault/[project-slug]/`:

```
vault/[project-slug]/
  summary.md              ← cross-synthesis and strategy (written after all pillars)
  prd.md                  ← PRD, UX flows, acceptance criteria (written after summary)
  backlog.md              ← prioritized task list (written after PRD)
  pillars/
    [pillar-name].md      ← one file per pillar (written after research)
```

Use a kebab-case slug (e.g., `user-auth`, `payment-flow`, `new-product`).

## Step 1: Build the Vault Structure

Identify every pillar this project depends on:
- Users, market, competitors
- Business model, design language
- Tech constraints and integrations
- Legal/regulatory, ops, economics, risks

Write a pillar list with priorities. Create the vault directory. This is the Vault's foundation.

## Step 2: Research Each Pillar in Parallel

For each pillar, gather:
- Sources and links
- Raw notes and extracts
- What each source supports or contradicts

Run research concurrently across all pillars.

## Step 3: Write Each Pillar to Disk

After research, write one file per pillar to `vault/[project-slug]/pillars/[pillar-name].md`.

Each pillar file must contain:

```markdown
# Pillar: [Name]

## What matters
[Key facts and signals — bullets only]

## What's uncertain
[Gaps, conflicting sources, unknowns]

## Decisions and assumptions
[What this pillar forces us to decide or assume]

## Risks
[What could go wrong based on this pillar]

## Sources
[URLs or references with brief labels]
```

Write all pillar files before proceeding to synthesis.

## Step 4: Synthesize to summary.md

Do one cross-synthesis pass across all pillar files. Write `vault/[project-slug]/summary.md`:

```markdown
# [Project] — Vault Summary

_Researched: [date]_

## Strategic Conclusion
[One paragraph — the essential conclusion that constrains the PRD]

## Key Findings Per Pillar
[Per pillar, bullets only, no padding]

## Cross-Cutting Insights
[What emerged from connecting the pillars — numbered list]

## Open Questions
[Uncertainties that must be resolved before or during build]

## Pillar Files
[Links to each pillar file]
```

## Step 5: Write the PRD

Only after `summary.md` is complete, write `vault/[project-slug]/prd.md`:
- Problem statement and goal
- UX flows
- Acceptance criteria
- Architecture plan

Every PRD item must be traceable to a Vault pillar. No PRD item without Vault backing.

## Step 6: Write the Backlog

Write `vault/[project-slug]/backlog.md` — a prioritized task list derived strictly from the PRD.

## Step 7: Build Iteratively

Build the product. Every time you learn something new:
1. Update the relevant pillar file in the Vault first
2. Update `summary.md` if strategy changes
3. Update `prd.md` and `backlog.md` second
4. Update the code last

Don't stop until the solution is finished and deployed.

## Anti-patterns

- Writing PRD or code before the Vault is populated
- Skipping synthesis between research and PRD
- Updating code without first updating the Vault
- Treating the Vault as write-once rather than living documentation
- Leaving Vault content only in chat — always write to disk
