---
name: vault-driven-building
description: Anchors development in a Vault of structured research across all project pillars (users, market, competitors, tech, legal, ops, risks) before any PRD or code. Every learning updates the Vault first, then the plan, then code. Use when planning and building a new product, feature, or complex system.
---

STARTER_CHARACTER = 🏛️

Build [THING] using the Vault-first methodology: research before plan, plan before code, Vault before everything.

## Step 1: Build the Vault

Identify every pillar this project depends on:
- Users, market, competitors
- Business model, design language
- Tech constraints and integrations
- Legal/regulatory, ops, economics, risks

Write a pillar list with priorities. This is the Vault's foundation.

## Step 2: Research Each Pillar in Parallel

For each pillar, create a folder containing:
- Sources and links
- Raw notes and extracts
- What each source supports

Run research concurrently across all pillars.

## Step 3: Synthesize

For each pillar, distill into:
- What matters
- What's uncertain
- Decisions and assumptions
- Risks
- Minimum facts needed to build correctly

Then do one cross-synthesis: resolve conflicts across pillars into a single strategy.

## Step 4: Write the PRD

Only after synthesis is complete, write:
- PRD
- UX flows
- Acceptance criteria
- Architecture plan
- Backlog

Everything must be strictly constrained by what's in the Vault. No PRD item without Vault backing.

## Step 5: Build Iteratively

Build the product. Every time you learn something new:
1. Update the Vault first
2. Update the PRD/backlog second
3. Update the code last

Don't stop until the solution is finished and deployed.

## Anti-patterns

- Writing PRD or code before the Vault is populated
- Skipping synthesis between research and PRD
- Updating code without first updating the Vault
- Treating the Vault as write-once rather than living documentation
