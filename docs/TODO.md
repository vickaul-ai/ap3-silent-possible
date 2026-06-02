# AP3 Silent Possible — Master TODO

**How to use:** Check boxes as work completes. Link PRs in the Notes column.  
**Plan detail:** [IMPLEMENTATION-PLAN.md](./IMPLEMENTATION-PLAN.md)  
**PM context:** [PRODUCT-BRIEF.md](./PRODUCT-BRIEF.md)

**Legend:** `[ ]` todo · `[~]` in progress · `[x]` done

---

## Phase 0 — Foundation

| Status | ID | Task | Notes |
|--------|-----|------|-------|
| [x] | 0.1 | PRODUCT-BRIEF.md | |
| [x] | 0.2 | IMPLEMENTATION-PLAN.md | |
| [x] | 0.3 | TODO.md (this file) | |
| [x] | 0.4 | README links to docs/ | |

---

## Phase 1 — Positioning, trust, funnel

### Hero & positioning

| Status | ID | Task | Notes |
|--------|-----|------|-------|
| [x] | 1.1.1 | Rewrite hero for long-tail agents + AP3 | Jun 2026 |
| [x] | 1.1.2 | Stack strip: agents → AP3 → Silent Compute | |
| [x] | 1.1.3 | CTAs: Playground, GitHub, Silent Compute | |
| [x] | 1.1.4 | Wireframe vs Playground callout | |

### Honesty & attribution

| Status | ID | Task | Notes |
|--------|-----|------|-------|
| [x] | 1.2.1 | “What AP3 ships today” section | `#ap3-today` |
| [x] | 1.2.2 | Roadmap badges on non-PSI operations | `operationBadge` on cards |
| [x] | 1.2.3 | Footer Silence + LFDT attribution | |

### Simulator (AP3-aligned)

| Status | ID | Task | Notes |
|--------|-----|------|-------|
| [x] | 1.3.1 | PSI wire stage labels (init/msg0/…) | 6-step flow |
| [x] | 1.3.2 | Envelope: roles + supported_operations | `wireframe_version` 1.1 |
| [x] | 1.3.3 | Copy: only initiator learns result | `psi_note` on final step |
| [x] | 1.3.4 | Link to Playground under code panel | |

### Path picker

| Status | ID | Task | Notes |
|--------|-----|------|-------|
| [x] | 1.4.1 | Builder / Enterprise / Explore chips | |
| [x] | 1.4.2 | sessionStorage path persistence | |
| [x] | — | `?case=` deep link (early) | Shipped with Phase 1 |

**Phase 1 complete when:** all 1.x rows checked. ✅ Jun 2026

---

## Phase 2 — Builder track (Hermes / OpenClaw)

### Builder section

| Status | ID | Task | Notes |
|--------|-----|------|-------|
| [x] | 2.1.1 | `#builders` section | |
| [x] | 2.1.2 | Hermes SKILL.md stub (copy/download) | |
| [x] | 2.1.3 | OpenClaw AgentCard JSON snippet | |
| [x] | 2.1.4 | SDK install + GitHub links | |

### Hermes skill promotion

| Status | ID | Task | Notes |
|--------|-----|------|-------|
| [x] | 2.2.1 | Filter: Builder platform | |
| [x] | 2.2.2 | hermes-skill rank B1 in builder filter | |
| [x] | 2.2.3 | Expand hermes-skill card copy | |

### New use cases

| Status | ID | Task | Notes |
|--------|-----|------|-------|
| [x] | 2.3.1 | calendar-match | |
| [x] | 2.3.2 | skill-overlap | |
| [x] | 2.3.3 | introducer-dedup | |
| [x] | 2.3.4 | chore-quorum | |

### Shareability & brief

| Status | ID | Task | Notes |
|--------|-----|------|-------|
| [x] | 2.4.1 | `?case=` deep links | Shipped in Phase 1 |
| [x] | 2.4.2 | Copy link per card | |
| [x] | 2.4.3 | Discussion prompt per card | New cases; add more to legacy cards later |
| [x] | 2.5.1 | Builder brief form fields | |
| [x] | 2.5.2 | Markdown brief export | |
| [x] | 2.5.3 | Pre-fill from case + Use in brief | |

**Phase 2 complete when:** all 2.x rows checked. ✅ Jun 2026

---

## Phase 3 — Enterprise & Silent Compute

| Status | ID | Task | Notes |
|--------|-----|------|-------|
| [x] | 3.1.1 | open-finance-consent card | |
| [x] | 3.1.2 | sanctions-pep card + Playground link | |
| [x] | 3.1.3 | Upgrade fraud-psi / consortium copy | |
| [x] | 3.1.4 | cross-border compliance card (optional) | |
| [x] | 3.2.1 | Operation → Silent Compute table | `#silent-compute` |
| [x] | 3.2.2 | Book-a-call CTA on enterprise cards | |
| [x] | 3.3.1 | Agent marketplace discovery section | `#discovery` |
| [x] | 3.3.2 | Multi-node mesh graphic (optional) | CSS network |

**Phase 3 complete when:** all 3.x rows checked. ✅ Jun 2026

---

## Phase 4 — Conversation & GTM

| Status | ID | Task | Notes |
|--------|-----|------|-------|
| [x] | 4.1.1 | Debate mode toggle on simulator | |
| [x] | 4.1.2 | Per-case leak vs minimal examples | enterprise + default |
| [x] | 4.2.1 | Compatibility failure card/tab | in `#discovery` |
| [x] | 4.2.2 | Failed compatibility simulator path | Preview failure envelope button |
| [x] | 4.3.1 | FACILITATION-GUIDE.md | |
| [ ] | 4.3.2 | Sales PDF/Notion (optional) | |
| [x] | 4.4.1 | OG images + meta per case | `assets/og/default.svg` + dynamic meta |
| [x] | 4.4.2 | Share text copy button | |
| [x] | 4.5.1 | Analytics event spec + implementation | `docs/ANALYTICS.md` + dataLayer |
| [x] | 4.5.2 | UTM guidance for influencers | in ANALYTICS.md |
| [x] | 4.6.1 | Builder challenge blurb (optional) | `#challenge` |
| [ ] | 4.6.2 | Showcase gallery (optional) | deferred |

**Phase 4 complete when:** all required 4.x rows checked (4.3.2, 4.6.2 optional). ✅ Jun 2026

---

## Phase 5 — Hosting (Vercel only)

| Status | ID | Task | Notes |
|--------|-----|------|-------|
| [x] | 5.0 | Decision: Vercel only, not corporate site | Jun 2026 |
| [x] | 5.3 | SEO + sitemap | sitemap.xml, robots — update URL after deploy |
| [x] | 5.5 | Accessibility | skip link, focus, aria-pressed |
| [x] | 5.6 | Performance | preconnect, vercel.json cache |
| [x] | — | DEPLOYMENT.md | Primary hosting doc |
| [-] | 5.1–5.2, 5.4 | Corporate site embed | **Cancelled** — see SITE-INTEGRATION.md |

**Phase 5 complete when:** production deploy on Vercel is live. ✅ https://ap3-silent-possible.vercel.app

---

## Ongoing maintenance

| Status | Task | Trigger |
|--------|------|---------|
| [ ] | Update PRODUCT-BRIEF “What exists today” | Any catalog change |
| [ ] | Sync roadmap honesty with ap3-protocol.org | AP3 release notes |
| [ ] | Review Hermes/OpenClaw links | Quarterly or major release |

---

## Decisions log

Record outcomes here so PMs do not re-debate.

| Date | Decision | Rationale |
|------|----------|-----------|
| Jun 2026 | Phased plan 0–5; Phase 1+2 before site embed | Max ROI for builder + positioning |
| Jun 2026 | Keep static single-page until >12 use cases | Low maintenance |
| Jun 2026 | **Vercel only** — no silencelaboratories.com embed | User decision; DEPLOYMENT.md is source of truth |
| | Email capture on builder brief | *TBD — privacy/GTM* |

---

## Changelog

| Date | Change |
|------|--------|
| Jun 2026 | Initial master TODO from implementation plan |
