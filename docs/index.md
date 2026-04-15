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

## Pathway

### Phase 1 - Foundation

- define teaming profile schema
- unify profile and opportunity requirement taxonomy
- finalize deterministic scoring contract

### Phase 2 - Team Builder recommendations

- build opportunity-scoped recommendation endpoint
- ship "fills your gap" reasoning output
- return top candidate partners with risk notes

### Phase 3 - Activation flow

- add intro requests and role selection
- add acceptance state tracking
- support secure, scoped collaboration artifacts

### Phase 4 - Proposal integration

- integrate with pre-flight readiness
- generate teaming plan and role matrix drafts
- support partner-aware compliance and win-theme content

### Phase 5 - Learning loop

- measure contacted -> accepted -> submitted -> won
- calibrate ranking weights from outcomes
- improve recommendation quality over time

## Execution roadmap

| Milestone | Outcome | Primary Repo |
| --- | --- | --- |
| M1 Schema + scoring contract | Teaming profile and fit factors locked | intentbid-teaming + intentbid-intelligence |
| M2 Recommendation API | Opportunity-specific partner recommendations live | intentbid-intelligence |
| M3 In-app Teaming panel | "Find partner for this gap" UX live | intentwin |
| M4 Intro + status workflow | Lightweight partner activation in product | intentwin |
| M5 Proposal integration | Teaming strategy appears in intent + generated content | intentwin |
| M6 Feedback calibration | Closed-loop ranking improvement | intentbid-intelligence |

## Strategic result

IntentBid Teaming gives customers a practical way to pursue more bids, raise compliance readiness, and increase winability - without adding operational complexity.
