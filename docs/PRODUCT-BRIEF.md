# AP3 Silent Possible — Product Brief

**Audience:** Product managers, design partners, and GTM stakeholders at Silence Laboratories  
**Status:** Living document — update when scope, priorities, or shipped experience change  
**Last updated:** June 2026

---

## Executive summary

**AP3 Silent Possible** is a static, framework-free web experience that helps people *imagine* how autonomous agents can collaborate without leaking private data. It is **not** a cryptographic implementation of AP3. It is a **conversation and alignment tool** published on **Vercel** (by Silence Laboratories) to generate interest in AP3, personal-agent builders (Hermes, OpenClaw), and the path to production privacy compute via **Silent Compute** (linked outbound).

The site complements—not replaces—the official [AP3 Playground](https://playground.ap3-protocol.org/), which runs real PSI and exposes protocol inspectors.

---

## What problem we are solving

### Market context

1. **Agents are proliferating**, especially “long-tail” personal agents (scheduling, family, finance, health admin, local services) built on frameworks like **Hermes** and **OpenClaw**.
2. **Collaboration today defaults to oversharing**: agents copy full lists, calendars, preferences, or files into shared context to coordinate.
3. **AP3** (Agent Privacy-Preserving Protocol) defines a standard way for two agents to run an **approved private operation** (today: primarily **PSI**) and return a **minimal result** plus an **evidence bundle**—without exposing raw inputs.
4. **Silent Compute** (Silence Laboratories) provides MPC/PET infrastructure for purpose-bound, auditable computation at scale—what enterprises need after the story clicks.

### The gap this project fills

| Resource | What it does well | What it does not do |
|----------|-------------------|---------------------|
| [ap3-protocol.org](https://ap3-protocol.org/) | Spec, SDK, roles, roadmap | Product narratives for personal agents |
| [AP3 Playground](https://playground.ap3-protocol.org/) | Live PSI, wire traces, compatibility lab | Family/creator/enterprise *stories* |
| **Silent Possible (this repo)** | Scenario atlas, simulated journey, pilot thinking | Real crypto, payments, or agent runtime |

**Our job:** Turn protocol concepts into *believable product surfaces* so PMs, builders, influencers, and enterprise buyers can say: “I see how *my* agent would use this.”

---

## Purpose and success criteria

### Primary purpose

Stimulate **thought and conversation** about AP3—especially multi-agent collaboration where each party keeps privacy over its data.

### Secondary purposes

1. **Silence Labs GTM:** Funnel from imagination → [AP3 docs / Playground](https://ap3-protocol.org/) → [Silent Compute](https://silencelaboratories.com/silent-compute) conversation.
2. **Builder activation:** Motivate Hermes/OpenClaw developers and influencers to ship **AP3-backed skills** and demos.
3. **Internal alignment:** Give product and sales a shared vocabulary (directives, evidence, operations, roles) before building real integrations.

**Hosting (current):** Public URL on **Vercel** only — not embedded on silencelaboratories.com. Outbound links to Silent Compute and AP3 docs remain.

### How we measure success (qualitative → quantitative)

| Signal | What “good” looks like |
|--------|------------------------|
| Conversation | Workshops, partner calls, and community threads reference specific use cases by name (e.g. Quiet Quorum) |
| Builder action | GitHub issues/skills that cite AP3; demos tagged Hermes/OpenClaw + AP3 |
| Funnel | Playground clicks, Silent Compute “book a call,” AP3 repo stars/issues attributed to this page |
| Content reuse | Sales uses cards/screenshots; influencers share `?case=` links |

We are **not** optimizing for time-on-site alone; we optimize for *clarity and shareability*.

---

## Relationship to Silence Laboratories and AP3

- **AP3** is an open protocol (research preview), contributed by Silence Laboratories under [LF Decentralized Trust Labs](https://lf-decentralized-trust-labs.github.io/labs/approved/ap3-protocol.html).
- **Silent Compute** is the commercial MPC/PET platform for regulated, cross-institution collaboration.
- **This wireframe** sits in the **imagination layer** of the stack:

```
┌─────────────────────────────────────────┐
│  Hermes / OpenClaw / Enterprise agents │  ← local memory, skills, policy
├─────────────────────────────────────────┤
│  AP3 on A2A (directives, roles, ops)   │  ← protocol surface (open)
├─────────────────────────────────────────┤
│  Silent Compute (MPC / PET execution)   │  ← production compute (Silence)
└─────────────────────────────────────────┘
```

Always be explicit in copy: **wireframe ≠ production security**. Point technical validators to the Playground.

---

## What exists today (shipped in repo)

### Deliverable

Single page: `index.html` (~1.7k lines: HTML, CSS, vanilla JS). Deployed as static site (e.g. Vercel). No backend.

### Core sections

| Section | Role |
|---------|------|
| Hero + status pill | Sets expectation: simulated, not real AP3 |
| Session simulator | Pick use case → staged flow → JSON “envelope” |
| Without / With AP3 | Contrast narrative |
| Use-case atlas (8 cases) | Filterable cards with load-into-simulator |
| OpenClaw / Hermes implementation view | Timeline + tabs (directive, manifest, evidence, settlement) |
| Evidence bundle wireframe | Trust surface vocabulary |
| Pilot brief form | LocalStorage + JSON download (no server) |

### Use cases (current catalog)

| Rank | ID | Title | Track |
|------|-----|-------|-------|
| #1 | quiet-quorum | Quiet Quorum | Personal |
| #2 | couplet | Couplet | Personal |
| #3 | eldercare | Eldercare decision and cost split | Personal |
| #4 | personal-admin | Personal admin proxy | Personal |
| #5 | diligence | Confidential diligence | Enterprise |
| P1 | fraud-psi | Privacy-preserving fraud consortium | Enterprise |
| B1–B5 | hermes-skill, calendar-match, … | Builder track (5 cases) | Builder |
| Future | community | Neighborhood mutual aid | Future |
| E2 | sanctions-pep | Sanctions / PEP screen | Enterprise |
| E3 | open-finance-consent | Open finance consent match | Enterprise |
| E4 | cross-border-compliance | Cross-border compliance screen | Enterprise |

### Simulator flow (AP3-aligned, v1.1)

Discovery → Compatibility → `init` → `msg0` / `msg1` → `msg2` → PrivacyResultDirective  

Envelopes include `roles`, `supported_operations`, `wire_phase`, and a final-step `psi_note` (only initiator learns PSI output). Compare to [AP3 Playground](https://playground.ap3-protocol.org/) for live crypto.

### Phase 1 UX (shipped)

- Hero reframed for **long-tail agents** and Hermes/OpenClaw
- **Stack strip**: agents → AP3 → Silent Compute
- CTAs: Playground, GitHub, Silent Compute
- **Wireframe vs Playground** callout
- **What AP3 ships today** section (`#ap3-today`)
- **Operation badges** on use-case cards (PSI / PSI+roadmap / Roadmap)
- **Path picker**: Explore / Builder / Enterprise (persisted in `sessionStorage`)
- **`?case=<id>`** URL loads a scenario into the simulator
- Footer: Silence Laboratories + LFDT attribution

### Phase 2 builder track (shipped)

- `#builders` section with Hermes SKILL.md and OpenClaw AgentCard stubs (copy buttons)
- **Builder platform** filter; Hermes silent-compute skill at rank **B1**
- **Four new use cases:** calendar-match, skill-overlap, introducer-dedup, chore-quorum
- **Copy link** per card; **discussion prompts** on builder-oriented cases
- Builder brief: framework, repo URL, ship target; **Markdown export**

### Phase 3 enterprise (shipped)

- Use cases: **sanctions-pep**, **open-finance-consent**, **cross-border-compliance**; **fraud consortium** upgraded
- **`#silent-compute`**: AP3 operation → Silent Compute mapping table + CTAs
- **`#discovery`**: long-tail AgentCard filtering narrative + network graphic
- Enterprise cards: Silent Compute link; sanctions links to Playground

### Phase 4 partial (shipped)

- **Debate mode** on simulator (Without / With AP3); per-case copy on key enterprise scenarios
- **[FACILITATION-GUIDE.md](./FACILITATION-GUIDE.md)** — 20-minute workshop script

### Phase 4 GTM (shipped)

- OG/Twitter meta + `/assets/og/default.svg`; per-case title/description via JS
- **Copy share text** on atlas cards
- **dataLayer** analytics (`docs/ANALYTICS.md`)
- **#challenge** — 30-day builder challenge
- `?embed=1` for iframe embeds

### Hosting (Vercel)

- Production deploy via [DEPLOYMENT.md](./DEPLOYMENT.md) — no corporate website embed for now
- `sitemap.xml` / `robots.txt` use `ap3-silent-possible.vercel.app` as default base (update after deploy if needed)
- Skip link, focus-visible, cache headers in `vercel.json`

---

## Design principles and considerations

These guide what we build and what we refuse to build.

### 1. Imagination over implementation

- **Do:** Show initiator/receiver, minimal output, evidence story, realistic JSON envelopes marked `ap3_wireframe: true`.
- **Don’t:** Imply live PSI, TEE attestation, or proof-of-computation before they exist in SDK—label roadmap items clearly.

### 2. Complement the Playground, don’t compete

- Playground = **protocol truth** (live crypto, inspector, tamper demos).
- Silent Possible = **product truth** (who benefits, what stays local, what gets revealed).
- Every enhanced version should link prominently to the Playground for “see it for real.”

### 3. Audience-aware paths

We serve three journeys on one page (path picker planned):

| Journey | Primary question | Tone |
|---------|------------------|------|
| **Builder** (Hermes/OpenClaw) | “What skill do I ship first?” | Concrete, copy-paste friendly |
| **Enterprise** | “How does this map to compliance and Silent Compute?” | Risk, audit, consortium |
| **Curious PM** | “What’s the user story?” | Scenario-first, low jargon |

### 4. Privacy story = minimal disclosure

Every use case should answer:

- **What never leaves the device?**
- **What crosses the wire?** (directives, commitments—not raw lists)
- **What is revealed?** (minimal result only)
- **What proves it happened?** (evidence bundle)

### 5. Framework-neutral, Hermes/OpenClaw-forward

OpenClaw and Hermes are called out because of **market momentum** and influencer reach—not because AP3 requires them. AP3 is transport-agnostic; A2A is the reference fabric today.

### 6. Static and maintainable

- No build chain unless maintenance cost forces it (keeps PMs and designers able to edit copy in one file or small docs).
- Prefer data-driven `useCases` array over duplicated HTML when adding scenarios.

### 7. Honest research preview

Mirror [AP3 roadmap](https://ap3-protocol.org/roadmap/) honesty:

- Today: PSI, signed commitments/intents/results.
- Roadmap: more operations, proof-of-computation, receiver-signed receipts, custom operation DSL.

Mark simulated operations (threshold, private score, dot product) as **manifest placeholders**.

### 8. Vercel deployment

- Static root deploy; no build step.
- Clear CTAs: Playground, AP3 GitHub, Silent Compute (outbound to silencelaboratories.com).
- Analytics via `dataLayer` — wire GTM on Vercel if needed.
- Corporate site embed deferred ([SITE-INTEGRATION.md](./SITE-INTEGRATION.md)).

---

## Motivations and priorities

### Why Silence Labs invests in this

1. **AP3 awareness** ahead of ecosystem maturity.
2. **Silent Compute pipeline** for enterprises who need MPC after they understand agent-layer privacy.
3. **Differentiation** in the agent privacy narrative vs “just use RAG and hope.”

### Priority order (agreed direction)

1. **Positioning clarity** — Silence → AP3 → Silent Compute; Playground handoff.
2. **Builder / influencer track** — Hermes skill story, skill stubs, shareable cases.
3. **Credibility** — Simulator aligned to PSI wire + roles; roadmap honesty.
4. **New personal-agent scenarios** — calendar soft-match, skill overlap, introducer dedup.
5. **Enterprise bridge** — anti-fraud consortium, open finance, sanctions link to Playground.
6. **Long-tail network story** — discovery, compatibility, many small agents.
7. **Facilitation assets** — workshop script, OG images, optional email capture.

### Explicit non-goals (for now)

- Running real AP3 SDK in the browser.
- User accounts, billing, or agent hosting.
- Replacing AP3 documentation or SDK tutorials.
- Legal/compliance sign-off language (frame as product exploration, not legal advice).

---

## Key vocabulary (for alignment)

| Term | Plain meaning |
|------|----------------|
| **AgentCard** | Public advertisement of roles, supported operations, commitments |
| **ap3_initiator / ap3_receiver** | PSI role pair; initiator learns result, receiver holds dataset |
| **Commitment** | Signed claim about dataset shape (not proof of possession yet—roadmap) |
| **PrivacyIntentDirective** | Signed permission slip: purpose, participants, expiry, allowed output |
| **Private operation** | e.g. PSI—computation over hidden inputs |
| **PrivacyResultDirective** | Signed minimal result for audit |
| **Evidence bundle** | Intents, compatibility checks, transcript hashes, policy log |
| **Silent Compute** | Silence MPC platform backing production compute |

---

## How to improve this project (PM playbook)

### When adding a use case

Use this checklist:

- [ ] One-sentence **user pain** (not technology-first).
- [ ] **Private inputs** vs **visible output** vs **evidence** (three bullets minimum).
- [ ] **Operation today**: PSI only, or labeled roadmap placeholder.
- [ ] **Framework hook**: Hermes skill, OpenClaw gateway, or enterprise agent.
- [ ] **Discussion prompt** for workshops/social.
- [ ] **Silent Compute mapping** (Secure Match, Statistics, etc.) if enterprise-relevant.
- [ ] Add to `useCases` in `index.html` + filter category + simulator envelope fields.

### When changing copy

- Preserve the **status pill** (“static click-through”) unless we ship real AP3 integration.
- Avoid claiming cryptographic guarantees the SDK does not yet provide.
- Prefer “minimal result” over “encrypted result” unless speaking about Silent Compute layer.

### When reviewing with engineering

Ask: “Does this story match [AP3 roles](https://ap3-protocol.org/roles/) and [PSI semantics](https://ap3-protocol.org/functions/psi/)?” If not, fix narrative or label as future operation.

### When reviewing with GTM

Ask: “Does this scenario earn a Playground visit or a Silent Compute conversation?” If neither, deprioritize.

---

## Open questions (for PM discussion)

| # | Question | Owner hint |
|---|----------|------------|
| 1 | ~~Corporate site URL~~ | **Resolved:** Vercel only — see [DEPLOYMENT.md](./DEPLOYMENT.md) |
| 2 | Capture builder emails on-site vs GitHub-only? | Growth + privacy |
| 3 | Influencer challenge/bounty budget and timeline? | Marketing |
| 4 | First “real” integration demo: Hermes skill repo vs OpenClaw plugin? | DevRel |
| 5 | Localize for APAC enterprise (cross-border card) now or Phase 3? | Regional GTM |

---

## Related documents

| Document | Purpose |
|----------|---------|
| [IMPLEMENTATION-PLAN.md](./IMPLEMENTATION-PLAN.md) | Phased delivery plan, task checklist, owners |
| [FACILITATION-GUIDE.md](./FACILITATION-GUIDE.md) | 20-minute workshop script |
| [ANALYTICS.md](./ANALYTICS.md) | Event catalog and UTM guidance |
| [DEPLOYMENT.md](./DEPLOYMENT.md) | Vercel hosting (primary) |
| [SITE-INTEGRATION.md](./SITE-INTEGRATION.md) | Corporate embed — deferred |
| [../README.md](../README.md) | Developer quick start and deploy |
| [ap3-protocol.org](https://ap3-protocol.org/) | Protocol source of truth |
| [AP3 Playground](https://playground.ap3-protocol.org/) | Live PSI |

---

## Document maintenance

Update this brief when:

- A phase ships (move items from plan to “What exists today”).
- Priorities change (re-order priority section).
- A new audience is added (e.g. ADK-only builders).
- AP3 SDK reaches a milestone that changes honesty boundaries (e.g. proof-of-computation ships).

**Changelog**

| Date | Change |
|------|--------|
| Jun 2026 | Initial brief + alignment with Silence site / Hermes–OpenClaw strategy |
