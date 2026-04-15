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

## Federal teaming compliance callout (LOS)

For federal opportunities, Teaming Copilot must use contract-aware limitations on subcontracting (LOS) checks.

- do not use a universal "49% partner max" rule
- apply LOS rules when FAR 52.219-14 / set-aside context is present
- enforce by contract type (services/supplies/construction variants) and similarly situated logic
- in the POC, require estimated partner work-share input and show LOS compliance status in readiness delta
- flag potential "unusual reliance / ostensible subcontractor" risk when partner scope appears primary/vital

## Operating guardrails

- treat teaming outputs as **informational compliance support, not legal advice**
- separate outputs into:
  - coverage fit
  - compliance / eligibility flags
  - structure risk
- use confidence labels when data is incomplete or unverified
- require fresh, sourced partner data for high-risk claims where possible
- keep teaming decisions connected to proposal strategy, not as a standalone sidebar

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

### Phase 1 (POC): Readiness model + manual partner onboarding

- define the readiness delta model before building UI:
  - what moves an opportunity from weak to stronger
  - what is coverage-only vs compliance-sensitive
  - what requires contracts/legal review
- let users manually add teaming partners from opportunity context
- capture lightweight partner profile fields:
  - identity: company, website, contact, preferred role (prime/sub/JV/SME)
  - fit signals: NAICS, certifications, set-asides, vehicles, clearance, coverage states
  - proof: capability tags + past-performance blurbs
  - bid mapping: which gap the partner closes (compliance/capability/geography/vehicle)
- show a deterministic "readiness delta":
  - before partner: current gaps and blockers
  - after partner: gaps closed and score uplift
- capture estimated work-share by partner and show LOS pass/warn/fail status
- add confidence labels: no issue detected / potential risk / insufficient data / counsel review recommended

### Phase 2: Compliance and structure guardrails

- build LOS and structure-risk logic as a standalone, versioned rule module
- evaluate LOS applicability, contract type, similarly situated handling, and role structure
- flag ostensible subcontractor / unusual reliance risk separately from simple percentage checks

### Phase 3: Data foundation and schema

- define canonical teaming profile schema and evidence freshness fields
- ingest and normalize candidate partner data (SBA profile signals + platform profiles)
- build teaming relationship graph from available subcontract/relationship signals
- map capability and eligibility attributes to opportunity requirement schema

### Phase 4: Recommendation engine
- detect opportunity-specific gaps from current match profile + opportunity requirements
- rank partner candidates by weighted deterministic score:
  - gap coverage quality
  - certification / set-aside eligibility fit
  - vehicle and clearance fit
  - geography fit
  - relationship recency / teaming history
- return top candidates with explicit explanation, risk flags, and confidence labels

### Phase 5: Activation workflow

- one-click intro request with redacted opportunity summary
- role selection (prime/sub/JV/SME)
- lightweight status flow: requested, accepted, declined

### Phase 6: Proposal integration

- inject teaming strategy into bid/no-bid and pre-flight readiness
- auto-draft teaming narrative and role matrix for proposal sections
- preserve claim traceability to L1 evidence and partner profile signals
- update L2 teaming strategy and keep warnings visible during L3 generation

### Phase 7: Feedback loop

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

1. Lock the readiness delta model and output taxonomy.
2. Ship manual partner onboarding flow in opportunity context (POC).
3. Add readiness delta view with confidence labels.
4. Build LOS + structure-risk checks as a standalone advisory rule module.
5. Define canonical teaming profile schema, freshness fields, and scoring contract.
6. Ship intelligence endpoint for opportunity-scoped teaming recommendations.
7. Add "Find partner for this gap" UI in opportunity + pre-flight flows.
8. Add intro workflow and status tracking.
9. Make proposal integration explicit in L2/L3 flow.
10. Add feedback calibration after real usage data exists.

## GitHub landing page

The project landing page content is in `docs/index.md`.

To publish it with GitHub Pages:

1. Open repository settings.
2. Set **Pages Source** to `main` branch, `/docs` folder.
3. Save and use the generated Pages URL.
