# IntentBid Teaming

Opportunity-scoped teaming intelligence for government contractors.

IntentBid Teaming helps users find and activate the right partner for a specific bid so they can:

- satisfy compliance and eligibility requirements
- fill capability and geography gaps
- strengthen proposal competitiveness with verifiable partner evidence

## Why this exists

Most GovCon tools either:

- provide a broad relationship network without opportunity-specific fit scoring, or
- automate proposal drafting without deeply integrating external teaming into bid strategy.

IntentBid Teaming is designed to close that gap by combining:

- **IntentBid Intelligence** (matching, readiness, agency context, opportunity parsing)
- **IntentBid Proposal Engineering** (L1/L2/L3 intent-driven generation)
- **Teaming-specific gap closure logic** (who fills what, why, and how that improves winability)

## Product thesis

Do not build a heavy marketplace first.

Build an **Opportunity-Scoped Teaming Copilot** that answers:

1. What gaps block this bid for my company?
2. Which partners close those exact gaps?
3. How does this change my compliance posture and win strategy?
4. How do we turn this into proposal-ready teaming language?

## Core principles

- **Simplicity first**: recommendation > intro > activation, no noisy social feed.
- **Proof over hype**: every recommendation includes explicit gap-coverage rationale.
- **Deterministic first, AI second**: transparent scoring baseline, LLM explanations layered after.
- **Opportunity-native**: teaming starts inside each opportunity and pre-flight workflow.
- **Intent-consistent**: all partner strategy flows through L1/L2/L3 model.

## How it fits IntentBid architecture

### L1 - Company Truth

Add verified teaming profile fields per organization:

- offered capabilities, certifications, vehicles, clearance, geography
- desired partner roles (prime/sub/JV), preferred teaming patterns
- evidence artifacts usable for partner validation

### L2 - Proposal Intent

Add a teaming strategy block to proposal intent:

- requirement/compliance gaps to close
- selected partner(s) and scoped responsibilities
- win-theme contribution and risk mitigation rationale

### L3 - Generated Content

Generate partner-aware artifacts:

- teaming plan summary
- compliance matrix augmentation
- partner-contributed section stubs tied to evidence

## Team Builder path (aligned with existing intelligence roadmap)

### Phase A: Data foundation

- ingest and normalize candidate partner data (SBA profile signals + platform profiles)
- build teaming relationship graph from available subcontract/relationship signals
- map capability and eligibility attributes to opportunity requirement schema

### Phase B: Recommendation engine

- detect opportunity-specific gaps from current match profile + opportunity requirements
- rank partner candidates by weighted deterministic score:
  - gap coverage quality
  - certification / set-aside eligibility fit
  - vehicle and clearance fit
  - geography fit
  - relationship recency / teaming history
- return top candidates with explicit explanation and risk flags

### Phase C: Activation workflow

- one-click intro request with redacted opportunity summary
- role selection (prime/sub/JV/SME)
- lightweight status flow: requested, accepted, declined

### Phase D: Proposal integration

- inject teaming strategy into bid/no-bid and pre-flight readiness
- auto-draft teaming narrative and role matrix for proposal sections
- preserve claim traceability to L1 evidence and partner profile signals

### Phase E: Feedback loop

- capture outcomes (contacted, accepted, submitted, won/lost)
- calibrate weights and explanations from real performance data

## Initial scope

In scope:

- partner recommendation for a specific opportunity
- transparent fit scoring and explanation
- lightweight intro + tracking workflow
- proposal intent integration

Out of scope (initially):

- generalized social networking feed
- payments, revenue sharing, or escrow
- full legal contract lifecycle management

## Differentiation

IntentBid Teaming is differentiated by being:

- **proposal-native** instead of directory-native
- **gap-closure-first** instead of contact-first
- **explainable and auditable** instead of opaque ranking
- **integrated with compliance and intent workflows** instead of siloed matchmaking

## Repositories and responsibilities

- **intentwin**: application UX, organization profile capture, opportunity workflow, proposal integration
- **intentbid-intelligence**: requirement parsing, deterministic teaming scoring, recommendations API, analytics signals
- **intentbid-teaming** (this repo): product definition, roadmap, docs, and launch artifacts for Teaming capability

## Near-term build sequence

1. Define canonical teaming profile schema and scoring contract.
2. Ship intelligence endpoint for opportunity-scoped teaming recommendations.
3. Add "Find partner for this gap" UI in opportunity + pre-flight flows.
4. Add intro workflow and status tracking.
5. Add L2/L3 proposal integration and feedback calibration.

## GitHub landing page

The project landing page content is in `docs/index.md`.

To publish it with GitHub Pages:

1. Open repository settings.
2. Set **Pages Source** to `main` branch, `/docs` folder.
3. Save and use the generated Pages URL.
