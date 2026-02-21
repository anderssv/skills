---
name: vault-driven-research
description: "Vault-structured research methodology: identifies all relevant pillars, researches each in parallel, writes each pillar to disk, then synthesizes into a final summary document. Use when researching a topic, technology, market, or system before making decisions."
---

STARTER_CHARACTER = 🔬

Research [TOPIC] using the Vault methodology: structure first, research in parallel, write each pillar to disk, then synthesize into a final document.

## Vault Directory Structure

All output is written to disk under `vault/[topic-slug]/`:

```
vault/[topic-slug]/
  summary.md              ← final synthesis (written last)
  pillars/
    [pillar-name].md      ← one file per pillar (written after research)
```

Use a kebab-case slug for the topic (e.g., `balder-forsikring`, `react-query`, `norwegian-insurance-market`).

## Step 1: Identify Pillars

Determine every dimension of the topic that matters. Adapt to the subject — common pillars include:
- Users and stakeholders
- Market and competitors
- Technology and constraints
- Risks and unknowns
- Economics and trade-offs
- Legal/regulatory (if relevant)

Write a prioritized pillar list. Drop pillars that don't apply.

## Step 2: Research Each Pillar in Parallel

For each pillar, gather:
- Sources and links
- Raw notes and extracts
- What each source supports or contradicts

Run across all pillars concurrently, not sequentially.

## Step 3: Write Each Pillar to Disk

After research, write one file per pillar to `vault/[topic-slug]/pillars/[pillar-name].md`.

Each pillar file must contain:

```markdown
# Pillar: [Name]

## What matters
[Key facts and signals — bullets only]

## What's uncertain
[Gaps, conflicting sources, unknowns]

## Sources
[URLs with brief labels]
```

Write all pillar files before proceeding to synthesis.

## Step 4: Cross-Synthesize

Do one pass across all pillar files:
- Resolve conflicts between pillars
- Identify cross-cutting themes
- Surface the open questions that most affect the decision

## Step 5: Write the Summary to Disk

Write `vault/[topic-slug]/summary.md`. Target: 2 pages. Hard limit: 5 pages.

Structure:
```markdown
# [Topic] — Research Summary

_Researched: [date]_

## Executive Summary
[One paragraph — the essential conclusion]

## Key Findings
[Per pillar, bullets only, no padding]

## Cross-Cutting Insights
[What emerged from connecting the pillars — numbered list]

## Open Questions
[Uncertainties that still matter — bullets]

## Conclusion
[What to do or decide, grounded in the findings]

## Pillar Files
[Links to each pillar file]
```

## Anti-patterns

- Writing the summary before finishing synthesis
- Exceeding 5 pages (more text is not more insight — cut ruthlessly)
- Listing per-pillar findings without the cross-synthesis step
- Treating source volume as a proxy for confidence
- Leaving output only in the chat — always write to disk
