---
layout: default
title: IntentBid Teaming
---

# IntentBid Teaming - GitHub Landing Page

## Opportunity

Government contractors regularly miss bids they could win because they lack one or two critical elements:

- a required certification or set-aside qualification
- a specific technical capability
- a contract vehicle, clearance, or geographic footprint

IntentBid Teaming turns this into a solvable workflow by finding partners that close those gaps for a specific opportunity.

## What we are building

An **Opportunity-Scoped Teaming Copilot** integrated with IntentBid Intelligence and proposal generation:

1. detect bid-specific gaps
2. recommend best-fit partners on-platform
3. explain why each partner improves compliance and competitiveness
4. convert chosen partner strategy into proposal-ready content

## Why now

Current market options split across two patterns:

- network tools that help with introductions but are weak on bid-specific fit intelligence
- proposal AI tools that help draft content but are weak on structured external teaming

IntentBid can unify both in a single, simple workflow.

## Differentiation

### 1) Gap-closure intelligence, not just networking

Recommendations are built around exact requirement gaps for each bid, not generic directory browsing.

### 2) Deterministic + explainable scoring baseline

Partner ranking starts with transparent weighted factors (eligibility, capability, vehicles, clearance, geography, teaming history), then adds AI-generated rationale.

### 3) Native to IDD proposal system

Teaming flows directly into L1/L2/L3:

- L1 verified organization truth
- L2 proposal intent and teaming strategy
- L3 generated sections with claim traceability

### 4) Workflow simplicity

Start with recommendation + intro + activation. Avoid a heavy marketplace until demand proves it.

## Compliance callout for federal teaming

For federal opportunities, Teaming Copilot must apply contract-aware limitations on subcontracting (LOS):

- do not hard-code a universal 49% partner rule
- enforce LOS only where applicable (for example, FAR 52.219-14 context)
- evaluate limits by contract type and similarly situated entity handling
- flag potential unusual reliance / ostensible subcontractor risk as an explicit warning

## Pathway

### Phase 1 - Pilot POC: Manual partner onboarding

- allow users to manually add teaming partners per opportunity
- collect key partner details:
  - identity and contact
  - role preference (prime/sub/JV/SME)
  - NAICS, certifications, set-asides, vehicles, clearance, geography
  - capability proof snippets and past performance notes
  - mapped gap this partner closes
- show a simple readiness delta:
  - before partner: blockers and gaps
  - after partner: gaps closed and bid readiness lift
- capture estimated partner work-share and show LOS compliance status (pass/warn/fail)

### Phase 2 - Foundation

- define teaming profile schema
- unify profile and opportunity requirement taxonomy
- finalize deterministic scoring contract

### Phase 3 - Team Builder recommendations

- build opportunity-scoped recommendation endpoint
- ship "fills your gap" reasoning output
- return top candidate partners with risk notes

### Phase 4 - Activation flow

- add intro requests and role selection
- add acceptance state tracking
- support secure, scoped collaboration artifacts

### Phase 5 - Proposal integration

- integrate with pre-flight readiness
- generate teaming plan and role matrix drafts
- support partner-aware compliance and win-theme content

### Phase 6 - Learning loop

- measure contacted -> accepted -> submitted -> won
- calibrate ranking weights from outcomes
- improve recommendation quality over time

## Execution roadmap

| Milestone | Outcome | Primary Repo |
| --- | --- | --- |
| M1 Manual partner POC | Users add partners manually and map gaps per bid | intentwin |
| M2 Readiness delta view | Before/after partner impact is visible and explainable | intentwin + intentbid-intelligence |
| M3 LOS guardrail check | Contract-aware subcontracting limit warnings and checks | intentwin + intentbid-intelligence |
| M4 Schema + scoring contract | Teaming profile and fit factors locked | intentbid-teaming + intentbid-intelligence |
| M5 Recommendation API | Opportunity-specific partner recommendations live | intentbid-intelligence |
| M6 In-app Teaming panel | "Find partner for this gap" UX live | intentwin |
| M7 Intro + status workflow | Lightweight partner activation in product | intentwin |
| M8 Proposal integration | Teaming strategy appears in intent + generated content | intentwin |
| M9 Feedback calibration | Closed-loop ranking improvement | intentbid-intelligence |

## Strategic result

IntentBid Teaming gives customers a practical way to pursue more bids, raise compliance readiness, and increase winability - without adding operational complexity.
