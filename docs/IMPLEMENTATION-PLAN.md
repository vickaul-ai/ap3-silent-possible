# AP3 Silent Possible — Implementation Plan

**Purpose:** Phased plan to evolve the wireframe for Silence Laboratories hosting, AP3 awareness, and Hermes/OpenClaw builder activation.  
**Companion:** [PRODUCT-BRIEF.md](./PRODUCT-BRIEF.md) (why and for whom)  
**Tracking:** Master checklist in [TODO.md](./TODO.md)

---

## Overview

| Phase | Theme | Outcome | Est. effort |
|-------|--------|---------|-------------|
| **0** | Foundation & docs | PM/engineering aligned; README points to docs | ✅ Done (docs) |
| **1** | Positioning & trust | Clear funnel; AP3-accurate simulator; Silence CTAs | ✅ Done (Jun 2026) |
| **2** | Builder track | Hermes/OpenClaw kits, new personal cases, share links | ✅ Done (Jun 2026) |
| **3** | Enterprise & Silent Compute | Consortium/finance cards, stack diagram, analytics | ✅ Done (Jun 2026) |
| **4** | Conversation & GTM | Debate mode, facilitation, OG/social, optional capture | ✅ Done (Jun 2026) |
| **5** | Vercel hosting | Deploy static site; SEO files | Vercel only — corporate embed cancelled |

Phases can overlap; **1 and 2** are highest ROI before sharing the Vercel URL externally.

---

## Phase 0 — Foundation (complete)

**Goal:** Shared understanding before large `index.html` edits.

| ID | Task | Status |
|----|------|--------|
| 0.1 | Create [PRODUCT-BRIEF.md](./PRODUCT-BRIEF.md) | Done |
| 0.2 | Create [IMPLEMENTATION-PLAN.md](./IMPLEMENTATION-PLAN.md) | Done |
| 0.3 | Create [TODO.md](./TODO.md) master checklist | Done |
| 0.4 | Link docs from [README.md](../README.md) | Done |
| 1.x | Phase 1 positioning, simulator, path picker | Done (Jun 2026) |

---

## Phase 1 — Positioning, trust, and funnel

**Goal:** Visitors immediately understand *what this is*, *what it isn’t*, and *where to go next*.

### 1.1 Hero and three-lane positioning

| ID | Task | Acceptance criteria |
|----|------|---------------------|
| 1.1.1 | Rewrite hero subcopy: long-tail agents + AP3 substrate | Mentions multi-framework agents; links AP3 overview |
| 1.1.2 | Add **stack strip**: Hermes/OpenClaw → AP3 → Silent Compute | Three labeled layers with one-line each |
| 1.1.3 | Add primary CTAs: **Try live PSI** (Playground), **AP3 GitHub**, **Silent Compute** | Visible above fold; `rel=noopener` |
| 1.1.4 | Add **“Wireframe vs Playground”** callout box | Two bullets: this site = stories; playground = real crypto |

### 1.2 Research-preview honesty

| ID | Task | Acceptance criteria |
|----|------|---------------------|
| 1.2.1 | New section or sidebar: **What AP3 ships today** | PSI, signed directives, commitments; link roadmap |
| 1.2.2 | Tag non-PSI operations on cards as **Roadmap / modeled** | Badge on threshold, private score, dot product cases |
| 1.2.3 | Footer: Silence Laboratories + LFDT AP3 attribution | One line + links |

### 1.3 Simulator credibility (AP3-aligned)

| ID | Task | Acceptance criteria |
|----|------|---------------------|
| 1.3.1 | Rename stages to: Discovery, Compatibility, `init`, `msg0`/`msg1`, `msg2`, Result | Labels match ap3-protocol.org PSI doc |
| 1.3.2 | Envelope JSON: `roles`, `supported_operations`, `session_id` placeholder | `ap3_initiator` / `ap3_receiver` present |
| 1.3.3 | Result step note: **only initiator learns intersection** | One line in stage copy for PSI cases |
| 1.3.4 | Link “Compare to live run” under code panel | Deep link to Playground |

### 1.4 Path picker (lightweight)

| ID | Task | Acceptance criteria |
|----|------|---------------------|
| 1.4.1 | Add journey chips: **Builder** / **Enterprise** / **Explore** | Scrolls to anchor sections; sets default filter |
| 1.4.2 | `sessionStorage` remembers last path | Persists per tab |

**Phase 1 exit criteria:** PM can demo in 10 minutes: story → simulator → Playground → Silent Compute CTA without overclaiming crypto.

---

## Phase 2 — Builder track (Hermes / OpenClaw)

**Goal:** Influencers and developers have a **first skill to ship** and **shareable scenarios**.

### 2.1 Builder section (new)

| ID | Task | Acceptance criteria |
|----|------|---------------------|
| 2.1.1 | New `#builders` section after use-case atlas | Headline: “Build your first AP3-backed agent skill” |
| 2.1.2 | **Hermes panel**: SKILL.md stub (download/copy) | Includes operation id, evidence fields, disclaimer |
| 2.1.3 | **OpenClaw panel**: AgentCard JSON snippet | `params.roles`, `supported_operations`, commitments example |
| 2.1.4 | Link to `pip install ap3` + GitHub + Playground | Research preview disclaimer |

### 2.2 Promote Hermes silent-compute skill

| ID | Task | Acceptance criteria |
|----|------|---------------------|
| 2.2.1 | New filter: **Builder platform** | Shows hermes-skill + skill-overlap (2.3) |
| 2.2.2 | Move hermes-skill to rank **B1** in builder filter | Card copy: reusable session orchestration skill |
| 2.2.3 | Expand hermes-skill bullets: manifest registry, gateway, audit | Matches platform narrative |

### 2.3 New use cases (personal / viral)

Add to `useCases` array in `index.html` with full card + simulator support.

| ID | Use case | ID slug | Operation | Why |
|----|----------|---------|-----------|-----|
| 2.3.1 | **Calendar soft-match** | `calendar-match` | PSI (modeled filter) | Universal personal-agent pain |
| 2.3.2 | **Skill overlap check** | `skill-overlap` | PSI on skill IDs | Hermes/agentskills.io angle |
| 2.3.3 | **Introducer dedup** | `introducer-dedup` | PSI | Creator/solopreneur agents |
| 2.3.4 | **Roommate chore quorum** | `chore-quorum` | PSI / quorum | Lighter viral variant of Quiet Quorum |

Each must include: `privateInputs`, `output`, `evidence`, `discussionPrompt`, `frameworkTags: ["hermes","openclaw"]`.

### 2.4 Shareability

| ID | Task | Acceptance criteria |
|----|------|---------------------|
| 2.4.1 | URL param `?case=<id>` loads simulator + scrolls | Works on refresh/share |
| 2.4.2 | **Copy link** button on each use-case card | Copies canonical URL |
| 2.4.3 | Discussion prompt visible on each card | One italic line under summary |

### 2.5 Builder brief (replace/extend pilot form)

| ID | Task | Acceptance criteria |
|----|------|---------------------|
| 2.5.1 | Fields: framework, repo URL, target case, ship timeline | Optional email field (off by default) |
| 2.5.2 | Export **Markdown** brief in addition to JSON | `ap3-builder-brief.md` download |
| 2.5.3 | Pre-fill from `?case=` and “Use in brief” | Existing behavior preserved |

**Phase 2 exit criteria:** DevRel can tweet one `?case=skill-overlap` link + Hermes SKILL stub; three new cards appear in atlas.

---

## Phase 3 — Enterprise bridge & Silent Compute

**Goal:** Enterprise visitors see a path from story → consortium → Silent Compute.

### 3.1 Enterprise use cases

| ID | Task | Acceptance criteria |
|----|------|---------------------|
| 3.1.1 | New card: **Open finance consent match** | Maps to Silent Compute Open Finance |
| 3.1.2 | New card: **Sanctions / PEP screen** | Links Playground bank scenario |
| 3.1.3 | Upgrade **fraud-psi** card | Consortium diagram copy; link anti-fraud use case page |
| 3.1.4 | Optional: **Cross-border compliance** (roadmap-labeled) | Ties AP3 Phase 2 + Silent Compute cross-border |

### 3.2 Silent Compute mapping table

| ID | Task | Acceptance criteria |
|----|------|---------------------|
| 3.2.1 | Section: **Operation → Silent Compute capability** | Table: PSI → Secure Match; stats → Secure Statistics; etc. |
| 3.2.2 | CTA per enterprise card: **Discuss Silent Compute** | Links silencelaboratories.com book-a-call |

### 3.3 Long-tail discovery story

| ID | Task | Acceptance criteria |
|----|------|---------------------|
| 3.3.1 | New section: **Agent marketplace discovery** | Narrative: 1000 AgentCards → compatibility → 3 receivers |
| 3.3.2 | Optional mesh graphic: 5–7 nodes, one session highlighted | CSS-only animation OK |

**Phase 3 exit criteria:** Enterprise PM can walk fraud + diligence + open finance with Silent Compute mapping in one pass.

---

## Phase 4 — Conversation, facilitation, and measurement

**Goal:** The site facilitates workshops and measurable outbound interest.

### 4.1 Debate mode

| ID | Task | Acceptance criteria |
|----|------|---------------------|
| 4.1.1 | Toggle on simulator: **Without AP3 / With AP3** | Side-by-side transcript mock vs minimal result |
| 4.1.2 | Pre-baked leak examples per active use case | e.g. full preference list vs overlap only |

### 4.2 Compatibility failures

| ID | Task | Acceptance criteria |
|----|------|---------------------|
| 4.2.1 | Card or tab: **When agents don’t match** | PIR vs PSI mismatch story (from Playground) |
| 4.2.2 | Simulator optional “failed compatibility” path | Shows error envelope, no compute |

### 4.3 Facilitation kit

| ID | Task | Acceptance criteria |
|----|------|---------------------|
| 4.3.1 | `docs/FACILITATION-GUIDE.md` | 20-min workshop script: Quiet Quorum → Playground → Q&A |
| 4.3.2 | Printable PDF or linked Notion (optional) | Sales enablement |

### 4.4 Social / OG

| ID | Task | Acceptance criteria |
|----|------|---------------------|
| 4.4.1 | `og:image`, `twitter:card` per default + optional per `?case=` | Static images in `/assets/og/` |
| 4.4.2 | One-sentence share text copy button | For LinkedIn/X |

### 4.5 Analytics (hosting on Silence site)

| ID | Task | Acceptance criteria |
|----|------|---------------------|
| 4.5.1 | Event spec doc: `run_session`, `playground_click`, `book_call_click`, `case_share` | Implemented via GTM or Plausible—web team |
| 4.5.2 | UTM guidance for influencer links | Documented in FACILITATION-GUIDE |

### 4.6 Builder challenge (optional)

| ID | Task | Acceptance criteria |
|----|------|---------------------|
| 4.6.1 | Landing blurb: “Ship one AP3 skill in 30 days” | Links GitHub discussions |
| 4.6.2 | Hashtag + showcase gallery (manual Curation) | Marketing-owned |

**Phase 4 exit criteria:** Sales runs facilitation guide twice; analytics dashboard shows funnel steps.

---

## Phase 5 — Vercel hosting (corporate embed out of scope)

**Goal:** Production deploy on Vercel. See [DEPLOYMENT.md](./DEPLOYMENT.md).

| ID | Task | Status | Acceptance criteria |
|----|------|--------|---------------------|
| 5.0 | Hosting decision: Vercel only | Done | Documented |
| 5.3 | SEO meta + sitemap + robots | Done | Update base URL after first deploy |
| 5.5 | Accessibility | Done | Skip link, focus, aria |
| 5.6 | Performance | Done | preconnect, asset cache in vercel.json |
| 5.1–5.2, 5.4 | Corporate site embed | **Cancelled** | [SITE-INTEGRATION.md](./SITE-INTEGRATION.md) if revived |

**Phase 5 exit criteria:** `vercel --prod` (or Git integration) serves the studio at a stable public URL.

---

## Technical approach (cross-phase)

### File structure (recommended evolution)

```
ap3-silent-possible/
├── index.html              # shell + sections
├── assets/og/              # Phase 4
├── data/use-cases.json     # optional Phase 2 refactor
├── docs/
│   ├── PRODUCT-BRIEF.md
│   ├── IMPLEMENTATION-PLAN.md
│   ├── TODO.md
│   ├── FACILITATION-GUIDE.md
│   ├── DEPLOYMENT.md
│   └── ANALYTICS.md
└── README.md
```

Refactor `useCases` to JSON **only when** card count > 12 or non-engineers edit copy frequently.

### Quality gates (every PR)

- [ ] Status pill still visible
- [ ] No claim of live crypto unless integrated
- [ ] New cases have simulator + filter + `?case=` slug
- [ ] External links open in new tab with `rel=noopener`
- [ ] Mobile: simulator usable at 375px width
- [ ] PRODUCT-BRIEF “What exists today” updated if catalog changes

---

## Dependencies and risks

| Risk | Mitigation |
|------|------------|
| AP3 SDK changes wire shape | Link to versioned docs; envelope labeled `wireframe_version` |
| Playground makes wireframe feel redundant | Sharpen positioning; never duplicate inspector |
| Hermes/OpenClaw hype fades | Keep framework section swappable; add “your agent” generic copy |
| Legal overclaim on health/finance cases | “Illustrative scenario” disclaimer on enterprise/personal cards |
| Single-file maintenance pain | Phase 2+ extract `useCases` to JSON module |

---

## Suggested staffing (RACI-lite)

| Workstream | Responsible | Accountable | Consulted | Informed |
|------------|-------------|-------------|-----------|----------|
| Copy & scenarios | PM | PM lead | AP3 eng, DevRel | Sales |
| UI/UX | Design | PM | — | Marketing |
| `index.html` implementation | Eng / DevRel | PM | AP3 eng | — |
| Silent Compute CTAs | PM + GTM | GTM lead | Sales | — |
| Vercel deploy | Eng | PM | — | Marketing |
| Analytics | Marketing | PM | Web | — |

---

## Milestone timeline (indicative)

```
Jun 2026   Phase 0 docs ████████████████████ complete
           Phase 1 start ──► positioning + simulator
Jul 2026   Phase 2 ──► builder track + 4 new cases
           Phase 3 ──► enterprise bridge
Aug 2026   Phase 4 ──► facilitation + OG + analytics
           Phase 5 ──► Vercel production URL
```

Adjust dates with marketing (e.g. influencer push tied to Phase 2 completion).

---

## Definition of done (program level)

The program is **successful for v1** when:

1. Page is live on **Vercel** with Silence → AP3 → Silent Compute story (outbound links to Silence products).
2. **≥4 new or materially upgraded** use cases ship with share links and discussion prompts.
3. **Builder section** ships with Hermes SKILL + OpenClaw AgentCard stubs.
4. **Playground** is the mandatory technical next step (measured click-through).
5. **PRODUCT-BRIEF** and **TODO** are updated to reflect shipped state.

---

## Changelog

| Date | Change |
|------|--------|
| Jun 2026 | Initial plan (Phases 0–5) |
| Jun 2026 | Phase 5 scoped to Vercel only; corporate embed cancelled |
